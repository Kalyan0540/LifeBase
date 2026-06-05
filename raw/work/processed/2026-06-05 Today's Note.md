# Today's Note

Date: 2026-06-05

## Open Tasks

### Cross Tabs

- [ ] Update filter journeys for the confirmation dialogue. `P2` `TASK-2026-05-18-002`
- [x] Design changes to Saved crosstab page views. `TASK-2026-06-04-001`

### Design System

- [ ] Design system colour tokens. `P1` `TASK-2026-05-18-004`
  - [ ] Map and test with few components to check the structure and mapping hierarchy.
  - [ ] Create styles and tokens in Figma.
  - [ ] Create dev handoff for the latest tokens.

### AI Summarisation

- [ ] Summarisation backend flag turn on/off for member side. `P2` `TASK-2026-05-18-005`

### AI

- [ ] Claude skills quick demo recording. `P3` `TASK-2026-05-18-006`

## Blocked / On Hold

### Cross Tabs

- [ ] Update variable creation flows in UI per new scope decisions ([[Variable Creation Scope]]); cover edge cases when switching output type after setup. `P0` `TASK-2026-05-20-003` *(On Hold: Need confirmation on the number output type from Kristina based on the crosstabs weekly call.)*
  - [ ] Table output flows designs.
- [ ] Crosstab prototype demo recording. `P2` `TASK-2026-05-18-003` *(On Hold)*


# Meeting Notes
## Weekly PM Sync Call
 We have decided to only use a one set output type, that is going to be a string output type, so I should update all the designs using only one as an output type. So this is one of the decisions which we have made and this is confirmed by Kristina and the team members. - Crosstab

Reason: we are not using number and string output types anywhere in the table directly. They are more or less used as column or row labels. Because of this, having number and text as separate output types does not add value, so we will just have one output type.
