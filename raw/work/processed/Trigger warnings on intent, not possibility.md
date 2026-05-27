For catalyst AI summarisation it was a decision making and pattern, for enlyta crosstabs it is a pattern as the decision making is only done in catalyst product

![[raw/work/assets/Catalyst Summary Generated for the selected bucketing.png|517]]
![[raw/work/assets/Catalyst Summary Bucketing.png|518]]
So the image, one which you are seeing is the first page where user sees the list of all the variables which are created by him or created by anyone else, and clicking on custom variable shows the image too, where user can modify the custom variables which are created by user or variables that user wants to create as new custom variables.

 so the pattern which we have found out is, like, let's say, if user is editing a custom variable for which a summer is already generated, so we want to show a confirmation if user is doing any delete. Which will completely remove the summary.

so the pattern which we have figured out is, we were initially thinking of 2 approaches. One approach is showing a banner in the bucketing, just about the values and buckets text, as in information or warning messages that you have used this variable for summarisation -  please delete or modify with caution. the second approach is if user is clicking on delete of any of the buckets, for example, under 50K, we thought of showing a confirmation dialogue, indicating that user is trying, you are trying to delete a bucket which is already used in AI summarisation.

 show the pattern or decision that we have taken is showing a banner directly at the income range level might not be very useful because user might have other intents like just adding a new bucket or adding a new value to a bucket, which is not completely delayed, and it is not a destructive action.

So it is of giving warning when the user didn't have intent. And also it is adding information in the 1st place without a user action or progressively disclosing it. So our pattern is only show things progressively when there is a intent of the user.

If not, do not show it or just show it on the user's action.  so let's say, instead of like, let's say, we have a button called edit, over year, and doing any changes will affect, the other users, that might have make sense when, as soon as user clicks on edit, showing a banner would make sense because it is affecting all the users for all the places, for any modification.

But in this case, it is not that same way. So banner didn't make sense, but the banner usage can be different when the user has an intent, that is clicking on edit to do something. But over here, it's already in edit view where user can do anything and it's not impacting any of them.

I feel this is a pattern which we have decided to go with. 


#### The UX principle essentially is
**Below is the chatgpt reasoning**

You can frame it internally like this:

> Warnings should appear only when users perform actions with meaningful destructive consequences, not merely when they enter an editable state.

Or even shorter:

> Trigger warnings on intent, not possibility.


That’s the pattern your solution is following. It’s a strong and scalable decision.


The reason we avoided showing a warning banner directly inside the bucketing screen is because users can perform both destructive and non-destructive actions there.

For example:

Non-destructive actions:
- Adding a new bucket
- Renaming a bucket
- Adding values to an existing bucket

Destructive actions:
- Deleting a bucket already used in AI summarisation

Showing a warning upfront, before any user action, creates unnecessary cognitive noise because the user may not even intend to do something destructive. It also exposes warning information too early without progressive disclosure.

Instead, we decided that warnings should appear only when the user performs a destructive action with clear intent — such as deleting a bucket that is already used in summarisation.

This pattern feels more contextual because:
- Entering edit mode itself is not harmful
- Only specific delete actions have impact
- Warnings are tied to user intent instead of possibility

A banner would have made more sense if simply entering edit mode itself affected all users/system behaviour. But in this flow, the impact happens only during specific destructive actions.

Final pattern:
- No passive warning banner in the bucketing screen
- Show confirmation only for destructive actions affecting summaries

In short:
Trigger warnings on intent, not possibility.