# Submitting Assignments in RS App

All assignments must be submitted in RS App **before the deadline**:

- Auto-checked tasks are submitted on the `Auto-Test` page. These include: tests, algorithmic assignments, codewars assignments.
- In case of Cross-Check assignment review, you need to submit the required link on the `Cross-check: Submit` page before the deadline. After submitting the link, you can continue working on the assignment until the deadline. The link can be submitted multiple times - the last one is saved. Everyone who didn't provide their work on time receives 0.

## Tests

- Tests for theoretical modules are in the `Auto-Test` tab in [RS App](https://app.rs.school/).
- Each test has a minimum passing score indicated in the description for each test (usually 70% of the maximum possible points).
- You can take the test the number of times indicated in the description. The last result counts.
- Also (if indicated), you can take the test more times, but the test score will be reduced by half.
- The test result will be displayed immediately. It will be added to `Score` after statistics update (at 04:00 GMT+3).

## Algorithmic Assignments

- [Example assignment](https://github.com/AlreadyBored/basic-js)
- Scores for these tasks are summed in the overall `Score`, as with all other assignments. The coefficient for each assignment is indicated in the `Weight` column in the schedule or in the detailed assignment description in `Score`.
- After finishing work on an assignment, go to [RS App](https://app.rs.school/), select `Auto-Test`, click `Open Task` in the desired assignment, click the `Start task` button, click the `Submit` button, then click `Refresh` or refresh the page. The verification result will be displayed in the `Score` column. If errors appear during verification, they will be described in the `Details` column.
- You can submit an assignment as many times as you want, each subsequent submission overwrites the previous one.
- Cheating on tasks ⇒ expulsion. Think carefully before submitting someone else's code just to get 10 points. We don't require solving all tasks.
- If during an interview you don't know how you solved the assignment you submitted ⇒ it was cheating ⇒ expulsion.
- If during an interview you know how you solved the assignment, but can't solve an obviously simpler task ⇒ it was cheating ⇒ expulsion.

#### Can I retake algorithmic assignments?

Yes, as many times as you want, but before the deadline.

#### How to find an error when solving algorithmic tasks?

- `console.log()` input parameters at the beginning of the solution
- you can run only one test to reduce the number of logs
  `mocha ./test/<TEST_NAME>.test.js`
  or
  `npm run test ./test/task-name.test.js`
- You can comment out everything except the failing test in the test itself
- You can [set up debugging in VSC](https://code.visualstudio.com/docs/nodejs/nodejs-debugging) and step through to see what's wrong.
- You can use [this service](http://pythontutor.com/javascript.html#mode=edit) to visually debug code.

## Codewars

Some assignments require solving several tasks on the [Codewars](https://www.codewars.com/) website

After finishing work on an assignment, go to [RS App](https://app.rs.school/), select `Auto-Test`, click `Open Task` in the desired assignment, click the `Start task` button, check that your Codewars username matches the displayed username\*, click the `Submit` button, then click `Refresh` or refresh the page. The verification result will be displayed in the `Score` column. If errors appear during verification, they will be described in the `Details` column.

You can submit an assignment as many times as you want, each subsequent submission overwrites the previous one.

_\*You can change your Codewars username via [this link](https://www.codewars.com/users/edit). Insert the specified username in the `Username` field and click the `Update` button at the very bottom of the page._

![edit username](../images/rs-app-tasks-1.jpg)

## Cross-check

Detailed description of the cross-check process [here](cross-check-flow.md)

### CodeJam

This is a task whose description is not known in advance, and limited time is allocated for completion (from 60 minutes to 48 hours).
For example, on Friday at 21:00 everyone receives a link with an assignment, for which 48 hours are allocated.

## FAQ

### What to do if I can't take a test or submit an assignment on time?

Skip it and try to complete the remaining assignments.

### Can I take task solutions from the internet?

In all possible sources, it's acceptable to take an idea, but not a solution.

### When can I submit a link in cross-check?

We recommend submitting the link as early as possible. You can complete a small part of the assignment, submit the link, and then continue working on the assignment until the deadline.

