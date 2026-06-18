**The question is:**
In crosstabs Filters when there is no selected filter is available should we have "Clear filter" or "Clear date Range" or "Filter details" visible? Currently we are disabling the actions instead of completely hiding when not available.


![[Pasted image 20260618170959.png|297]]![[Pasted image 20260618171224.png|296]]

https://www.smashingmagazine.com/2024/05/hidden-vs-disabled-ux/

> Show important, persistent workflow actions in disabled state when users will be able to use them later. Hide actions only when they are irrelevant, unavailable to that user, or tied to an object that does not exist.


So the reasoning is not “disabled is always better.” It is:
- If the user can use the action later, and the action helps them understand the workflow, show it disabled.
- If the user will never be able to use the action, or it is irrelevant because the object does not exist, hide it.
- If disabled state is used, the reason should be obvious or explainable.

![[Pasted image 20260618171628.png]]
![[Pasted image 20260618171645.png]]



## Filter View Mode vs Edit Mode

**The question is:**
In saved filters, should delete and drag controls be hidden in view mode and shown only in edit mode?

Also, only filter creators can edit filters. Non-creators cannot edit the original filter and only get the option to modify and use.

![[Filter View Non Creator 2026-06-18.png]]

![[Filter View Creator 2026-06-18.png]]

![[Filter Edit Creator 2026-06-18.png]]

**Decision / recommendation:**
Yes, it is the right choice to hide drag and row-delete controls in view mode and show them only in edit mode.

For non-creators, hide edit/delete controls because they do not have permission to edit the original filter. Show the valid path instead: "Modify & Use".

**Reasoning:**
Drag and row-delete are edit-mode controls, not persistent workflow actions.

In view mode, the user is reading, reviewing, or applying the saved filter. Showing disabled drag/delete icons there would add noise and may create the wrong expectation that the filter can be manipulated inline.

For non-creators, edit and delete are not temporarily unavailable. They are permission-restricted. So disabled controls would communicate the wrong thing. The user should see what they can do, not owner-only actions that they cannot access.

**Suggested behavior:**
- Non-creator view: show "Modify & Use"; hide "Edit Filter", row drag, row delete, and owner delete actions.
- Creator view mode: show high-level owner actions like "Edit Filter" and filter-level "Delete"; hide row drag/delete because row editing is not active.
- Creator edit mode: show row drag/delete, "Discard", "Save", visibility toggle, and other editing controls.

**Guiding principle:**
> Keep persistent workflow actions visible when they are temporarily unavailable; hide mode-specific or permission-restricted actions until the user enters the mode or has the permission to use them.

