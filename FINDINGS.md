## Finding: imported index.css without use

- Location:main.tsx
- Status: fixed
- Evidence: 
- Impact: not breaking but eslint error
- Priority:small
- Proposed solution: Import the css in the base entry index.html
- Verification:
- Implementation notes:

## Finding: compare task status with string

- Location: Multple frontend file
- Status: deffered
- Evidence:in the taskitem
- Impact: can cause type mismatch
- Priority: moderate
- Proposed solution:  use enum for proper type comparison for avoide future mismatch during developmenent and easy to maintain
- Verification:
- Implementation notes:

## Finding: most of the parameter lack type

- Location:
- Status: deffered
- Evidence:
- Impact:type mismatch
- Priority:
- Proposed solution: Proper typing with interface or type for help catching compile time error
- Verification:
- Implementation notes:

## Finding: the project toggle button is not loading the actually task from the backend

- Location:Taskboard.tsx
- Status:  fixed
- Evidence:
- Impact: fail to update the Ui after the update of the task per project
- Priority:high
- Proposed solution: add a dependency tracker for the useEffect to automatically retriger the fetching of the data
- Verification:
- Implementation notes: add the needed dependency to update the fetching of the task

## Finding: UI not responding to changes when item is mark as complete

- Location:Taskboard
- Status: fixed
- Evidence:
- Impact: UI not reacting in real time for user feedback 
- Priority:High
- Proposed solution: create a new array and filter to update the changed task, instead of modifying the exisiting one
- Verification: 
- Implementation notes: filter the through to update the need task instead of modifying in-place array.


## Finding: Empty tasks not be communicated to the user when the select a project with no task

- Location:Taskboard
- Status: fixed
- Evidence: not information informing the user
- Impact: could confuse the user, as to the wherether the app is working on not
- Priority: moderate
- Proposed solution: add a notification for empty state to help communicate to the user that the project has no tasks
- Verification:
- Implementation notes: now shows a message that says "No task for the selected project"

