# Communications

## CUD

| Name                       | Sync/Async | Producer    | Consumer                           | Data                                    |
| -------------------------- | ---------- | ----------- | ---------------------------------- | --------------------------------------- |
| Create/Update/Delete User  | Async      | Auth        | TaskTracker, Accounting, Analytics | User data                               |
| Create task                | Async      | TaskTracker | Accounting                         | Cost of task, task description, User id |
| Close task                 | Async      | TaskTracker | Accounting, Analytics              | Cost of task, task description, User id |
| Assign task                | Async      | TaskTracker | Accounting                         | Cost of task, task description, User id |
| Count bills at the day end | Async      | Accounting  | Accounting, Mail                   | User, amount of money                   |

## Business events

| Name                       | Sync/Async | Producer    | Consumer    |
| -------------------------- | ---------- | ----------- | ----------- |
| Create/Update/Delete User  | Sync       | Auth        | Auth        |
| Login in TaskTracker       | Sync       | TaskTracker | Auth        |
| Login in Accounting        | Sync       | Accounting  | Auth        |
| Login in Analytics         | Sync       | Analytics   | Auth        |
| Create Task                | Sync       | TaskTracker | TaskTracker |
| Close Task                 | Sync       | TaskTracker | TaskTracker |
| Assign Task                | Sync       | TaskTracker | TaskTracker |
| Count bills at the day end | Async      | Accounting  | Accounting  |
| List tasks                 | Sync       | TaskTracker | TaskTracker |
| List bill                  | Sync       | Accounting  | Accounting  |
