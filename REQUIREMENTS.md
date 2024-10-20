# Requirements

We're going to build a Trello-like app (ex. https://trello.com/) that can manage tasks and their status. 

We need to build
1. An overall view of tasks and their status. Ideally this should be a board with columns or rows for each 'status'
2. A way for the user to perform operations on a task
   1. Create Task
   2. Update Task status
   3. Edit Task Title/Description
   4. Delete a Task
3. A way to search/filter tasks

You can use the sample model and JSON below to represent a task, but feel free to update the model/example as needed

```
export type TaskStatus = 'Not Started' | 'In Progress' | 'Completed';

export type Task = {
    id: number;
    title: string;
    description: string;
    status: TaskStatus;
    dueDate?: string;
    labels: string[];
};

const tasks: Task[] = [{
  id: 1,
  title: 'Sample Task',
  description: 'This is a sample task with a description...",
  status: 'Not Started',
  dueDate: null,
  labels: [],
 }];
```
