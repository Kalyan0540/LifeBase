	# Tasks

Current global task dashboard across products.

Only explicit tasks appear here. A note becomes a task only if the raw note uses a checkbox, says it is a task/todo/action item, or you explicitly ask me to create a task.

---

## Open

### [[Cross Tabs - Index|Cross Tabs]]

- [ ] Update filter journeys for the confirmation dialogue. `P0` `TASK-2026-05-18-002`
  - [ ] Recheck the filter reset and filter details patterns.
- [ ] Update Run Button functionality in final UJ's page in Figma. `P1` `TASK-2026-06-12-001`
- [ ] Work on the crosstabs new comments by Pradnya. `P1` `TASK-2026-06-12-002`
  - [ ] Display the variable code in Figma designs everywhere, including column/row/nesting sections and table name brackets, and share images for ED-1098.
  - [ ] Explore footer interaction and scroll-pattern best practices for crosstabs; check with Nima.
  - [ ] Create sections in Figma for the crosstabs design QA testing file.
- [ ] Update variable creation flows in UI per string-only output decision ([[String-Only Custom Variable Output]]). `P0` `TASK-2026-05-20-003`
  - [x] Update all designs to use only one string output type. `completed 2026-06-15`
  - [ ] Table output flows designs. *(Review against string-only scope.)*
  - [x] Update delete & Edit custom variable. `completed 2026-06-01`
  - [x] Confirm on the functionality similar to filters for editing and others. `completed 2026-06-02`
  - [x] Confirm if a custom variable can be further bucketed. `completed 2026-06-02`
  - [x] Added view mode for custom variable. `completed 2026-06-02`
- [ ] Design QA: Crosstabs table layouts testing without data (ED-860 Dev Ticket). `P2` `TASK-2026-06-09-001`

### [[Design System - Index|Design System]]

- [ ] Design system colour tokens. `P2` `TASK-2026-05-18-004`
  - [x] Research on the best practises for color system.
  - [x] Analyse and setup framework for migrating to new scalable system.
  - [x] Create color primitives and map existing colors to the color scale. `completed 2026-06-03`
  - [x] Derive semantics tokens from created primitives. `completed 2026-06-04`
  - [ ] Review the draft & work on the feedback.
  - [ ] Map and test with few components to check the structure and mapping hierarchy.
  - [ ] Create styles and tokens in Figma.
  - [ ] Create dev handoff for the latest tokens.

### [[AI Summarisation - Index|AI Summarisation]]

- [ ] Summarisation backend flag turn on/off for member side. `P2` `TASK-2026-05-18-005`
- [ ] Experiment on UX improvements for AI summaries. `P3` `TASK-2026-06-16-001`
  - [ ] Loading indication and generated indication at tab level.
  - [ ] Collapsible or see-more option for header metadata.
  - [ ] Clarify the difference between response size at summary level and header level in discussion/conversation.
  - [ ] Index-like option to navigate within tab between each value output.
  - [ ] Scroll indication after a response is generated.
  - [ ] Show generated summary progressively like a typewriter instead of populating it all at once.
  - [ ] Explore moving away from dialog view to page view.

### [[AI - Index|AI]]

- [ ] Claude skills quick demo recording. `P3` `TASK-2026-05-18-006`
- [/] Persona Bot's UX/UI design. `TASK-2026-06-09-004`
  - [/] Research & Documentation
  - [ ] Ideation
    - [ ] Create two substantively different first-page/core app mock-up options.
  - [ ] First Draft + Review
  - [ ] Final Draft + Review
  - [ ] Dev Handoff
  - [ ] Check with Tish on prioritization so Persona Bots can move in parallel with Enlyta work.
  - [ ] Coordinate with Suveer to create a UX board ticket for Persona Bots tracking.

### Standalone

- [ ] Research the design brief and provide templates and best practises to add it to the Jira board. `P1` `TASK-2026-06-08-001`
- [/] User Groups Enhancement - Historical Change Visibility & Activity Indicators. `P1` `TASK-2026-06-12-003`

---

## Blocked

### [[Cross Tabs - Index|Cross Tabs]]

- [ ] Crosstab prototype demo recording. `P2` `TASK-2026-05-18-003` *(On Hold)*

---

## Superseded

### [[Cross Tabs - Index|Cross Tabs]]

Previous parent scope for `TASK-2026-05-20-003`: update variable creation flows in UI per new scope decisions; cover edge cases when switching output type after setup.
- [x] Create variable - Set output as number flow. `completed 2026-06-01` `superseded 2026-06-05`
- [x] Create variable - Set output as text flow. `completed 2026-06-01` `superseded 2026-06-05`
- [x] Handle edge cases - switch variable type, disabled state for the output text box if no variable type selected. `completed 2026-06-02` `superseded 2026-06-05`

---

## Completed

### [[Cross Tabs - Index|Cross Tabs]]

- [x] Mobile view for crosstabs. `P1` `TASK-2026-06-09-003` `completed 2026-06-12`
  - [x] Draft 1 & Review. `completed 2026-06-10`
  - [x] Finalise & Handover. `completed 2026-06-12`
- [x] Support tickets for crosstabs. `P0` `TASK-2026-06-10-001` `completed 2026-06-10`
- [x] Update the saved crosstabs view changes in the Final UJ's. `P0` `TASK-2026-06-09-002` `completed 2026-06-09`
- [x] Design changes to Saved crosstab page views. `TASK-2026-06-04-001` `completed 2026-06-05`
- [x] Review designs for crosstabs dev. `P0` `TASK-2026-05-29-001` `completed 2026-06-04`
- [x] Connected with Aniruddh on the crosstabs table views and functionality. `TASK-2026-06-04-003` `completed 2026-06-04`
- [x] For Run in Cross Tabs, add the recommendation flow and reasoning in the design along with the last discussed designs. `P0` `TASK-2026-05-26-001` `completed 2026-05-27`
- [x] Demo call for crosstab with new QA. `P0` `TASK-2026-06-03-001` `completed 2026-06-03`
- [x] Render Table designs. `P0` `TASK-2026-05-18-007` `completed 2026-05-19`
- [x] Complete the decision making on new variable creation: [[Custom Variable Creation - Text Output#Creating New Variable|text output]], [[Custom Variable Creation - Number Output#Creating New Variable|number output]], and [[Custom Variable Creation - Variable Output#Creating New Variable|variable output]]. `TASK-2026-05-18-001` `completed 2026-05-21`
- [x] User journey for Run-before-Save flow; add Save button tooltip. `P0` `TASK-2026-05-20-001` `completed 2026-05-21`
- [x] Design confirmation dialogue for when user clicks back/reload without running. `P0` `TASK-2026-05-20-002` `completed 2026-05-21`
- [x] Confirm with Pradnya on bucketing flow difference between Catalyst and Enlyta (Catalyst carries only bucketed data, not values data). `P0` `TASK-2026-05-20-007` `completed 2026-05-21`
- [x] Add validation that bucket names should not be the same. `P0` `TASK-2026-05-20-008` `completed 2026-05-21`
- [x] Update table designs: update all screenshots and check links in Jira. `P0` `TASK-2026-05-21-001` `completed 2026-05-25`

### [[AI Summarisation - Index|AI Summarisation]]

- [x] Update the Discussion, Conversation & OE Summary designs with latest design options in Catalyst. `P1` `TASK-2026-06-08-002` `completed 2026-06-16`
  - [x] Update OE Summarisation Flows. `completed 2026-06-10`
  - [x] Update Discussion Summarisation Flows. `completed 2026-06-16`
  - [x] Update Conversation Summarisation Flows. `completed 2026-06-16`
- [x] Update the OE Summary flows with - Show Confirmation for Modifiying Bucketing after Summary Generated. `P0` `TASK-2026-06-15-001` `completed 2026-06-15`
- [x] Provide Dominique the links to updated copy design, dialogue layout, and selection interaction in profile fields. `P0` `TASK-2026-05-20-006` `completed 2026-05-25`
- [x] Warning message for deleting bucketing if a summary is already generated. `P0` `TASK-2026-05-20-004` `completed 2026-05-21`
- [x] Update button text to "Reset to default" instead of "Reset". `P0` `TASK-2026-05-20-005` `completed 2026-05-21`
- [x] Confirm with Pradnya on bucketing flow difference between Catalyst and Enlyta (Catalyst carries only bucketed data, not values data). `P0` `TASK-2026-05-20-010` `completed 2026-05-21`
- [x] Add validation that bucket names should not be the same. `P0` `TASK-2026-05-20-011` `completed 2026-05-21`
- [x] Create loading state for N size in bucketing. `P0` `TASK-2026-05-20-012` `completed 2026-05-21`

### [[Activity Feed - Index|Activity Feed]]

- [x] Peer review new activity feed in Catalyst for both member side and facilitator side. `P0` `TASK-2026-05-26-002` `completed 2026-05-25`
