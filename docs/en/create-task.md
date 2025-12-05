# How to Prepare a Task for RS School

One of the features of the RS School course is its practical orientation. During the course, students complete a large number of tasks. And this is, indeed, a very effective and useful way to learn something new.
Let's consider how task preparation works.

## Task Content
You should try to make the task:
- interesting, as it is much more effective to learn something you take interest in
- nice-looking, so that you can add it to your portfolio
- educative, it is necessary to determine which important and relevant skills students acquire when they complete it, which relevant and modern technologies they master
- as realistic as possible, which will prepare students for solving professional problems
- quite complex and at the same time comprehensible for most students

Determining the optimal complexity of the proposed task is one of the most important points. A possible solution is to pre-complete the task by its author, in order to understand how much it is accomplishable by students, what problems they will face during its completion, how much time they will need.

## Task Description

The task description includes:
- a clear and detailed description of the appearance and functionality of the expected result. A layout in figma is welcomed. Even better, if the author provides a working application's prototype with minified code
- technical requirements: which browsers should the application be tested on, which technologies must be used, which are recommended, which are prohibited
- repository requirements: the repository to perform the task (private or public, school repository or student's personal repository), how to name the repository, development branch, project folder, [commit requirements](https://docs.rs.school/#/git-convention), [pull request requirements](https://docs.rs.school/#/pull-request-review-process?id=Pull-Request-Requirements), where to upload the demo version of the application (gh-pages are suitable for public repositories, netlify.com for private repositories)
- evaluation criteria, they will be mentioned below
- links to additional materials that will be useful for students when they complete the task
- link to the document with questions about the task: an editable Google spreadsheet created by the author of the task, where students can ask questions for the author to answer

You can find examples of task descriptions in the [school's repository](https://github.com/rolling-scopes-school/tasks)

## Task Evaluation Criteria

It is one of the most essential parts of the task description. If some requirements are indicated in the task description, but the number of points for them is not stated in the evaluation criteria, we can assume that these requirements do not exist.
Well-designed, clear and understandable evaluation criteria help students complete the task:
- break the task down into a list of subtasks that can be sequentially completed one after another
- allow reviewers to check the task more precisely and objectively
- make the process of assigning points for the task simpler and more justified

Now RS School uses three methods of task evaluation:
- [auto-checked tasks](https://docs.rs.school/#/rs-app-tasks)
- [tasks evaluated by the mentor](https://docs.rs.school/#/pull-request-review-process)
- [tasks evaluated by students](https://docs.rs.school/#/cross-check-flow?id=cross-check)

The most tolerant of possible inaccuracies in the description of requirements and evaluation criteria are the tasks that are checked by mentors. Mentors, thanks to their authority and experience, can clarify and adjust the requirements for the task, evaluate the result.

For a cross-check – tasks checked by students - evaluation criteria should be as clear, detailed, understandable and unambiguous as possible.

To work out evaluation criteria, the task is divided into small subtasks, with a certain number of points assigned for each of the subtasks, typically 10-20.
The basic, middle and extra levels are determined in a proportion of approximately 30% - 50% - 20% of the total number of points for the task.
The basic level - tasks that are completed by all students, the middle - comprehensible for most of the students, the extra level - tasks for well-performing students, so that the task for them is not too simple.

Penalty points are indicated if the goal is to draw students' attention to possible errors when completing the task. Penalty points allow you to reduce the number of errors, but you need to use them carefully, only where they are really needed.

The completed task is [added as a PR](https://docs.rs.school/#/fix-typo?id=How-to-add-changes-to-someone-elses-repository) to the [repository with school tasks](https://github.com/rolling-scopes-school/tasks)

## Task Assignment

When and what tasks will be assigned is specified in the course curriculum.

The deadline is set according to the estimated time needed to complete the task. It is desirable that it should not exceed 1-2 weeks.

For large and complex tasks the task author can hold an introductory FAQ webinar.
If the task is easy-to-understand, an announcement in the discord would be enough.

Simultaneously with the task assignment, a separate channel in the discord should be created for its discussion. During the discussion, students share links to useful materials, discuss problems, and try to find solutions together. It is a very good and helpful practice. It is desirable for the task author to view this channel in order to answer students' questions, especially those related to the task requirements.

Together with answering questions in Discord, the author of the task answers the questions in the FAQ document. The advantages of such a document are that students write questions addressed to the author personally, and only he answers these questions. This document becomes a "source of absolute truth" for students working on the task.

The answers of the author of the task in Discord and in the FAQ document should clarify and specify the requirements stated in the description of the task, but not contradict them. In case of divergence in interpretation, when the author implied one thing, and the students see it differently, the description of the task in the school repository is corrected. However, making changes when the task has already been assigned and is being worked on should only be done in extreme cases of necessity.

If the task is large, or it turns out that students have too many questions on the task, the author can conduct a webinar and explain the requirements and peculiarities of the task's completion.

## Results Analysis

After the deadline, the author of the task conducts a webinar to analyze the results of the task's completion. At the webinar he talks about the peculiarities of the task, shares best practices for completing separate elements of the task using his own code or student code as an example, dwells upon typical errors, analyzes several tasks of students, emphasizes their positive points. In the case of a cross-check, the author can show how to check and evaluate the task.

## Lyrical Digression

Why come up with tasks for the course, spend time to write their description, read students' comments about the task, not all of them being complimentary (but there are still more good ones), answer questions, and conduct webinars. Some consider this to be a way to improve karma, for some it is an opportunity to share knowledge; some regard it as their "civic duty". In fact, it is quite interesting and enjoyable. First, you come up with a task that you yourself like and which will be liked by others. Then you complete it and in the process imagine how this task will be done by another person who is just studying, and for whom completing the proposed task is another step towards their dream. While completing it, you describe the expected result, how it should work, share the materials that will be needed when completing the task. Then you read the comments and you are very surprised how different students can interpret what seemed crystal clear to you. You work on mistakes and learn to express your thoughts as accurately and clearly as possible. You read critical comments, with comments of those for whom the task seemed too simple and those who found it extremely difficult going one right after another. And then someone will write that completing the assignment you invented helped him to get a job, it was this task that was discussed during the interview. Someone else will remake the task and use it as a basis to make a greeting card for a loved one. And someone will come up with their own version of the solution for the task, and it will turn out to be much cooler and more interesting than the one you did. And that's great.

