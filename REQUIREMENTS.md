# Requirements 1

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


# Requirements 2
We're going to build an app that can keep track of books we want to read / have read / are currently reading, and information about that, including our rating.

We need to build
1. A way to view books on my list (in either a To Read / Currently Reading / Read 'status')
2. A way for the user to do simple CRUD to
  1. Add a new book to the list (in any status)
  2. Edit a book to rate it (between 1-10)
  3. Delete a book from the list
3. A way to search/filter books


You can use the sample model and JSON below to represent a book, but feel free to update the model/example as needed
```
export type BookStatus = 'To Read' | 'Reading' | 'Read';

export interface Book {
  id: number; // Unique identifier for each book
  title: string;
  author: string; 
  status: BookStatus;
  genre?: string;
  publicationYear?: number;
  notes?: string;
  rating?: number;
}

const books: Book[] = [{
  id: 1,
  title: 'Sample Book',
  author: 'John Smith",
  status: 'Read',
  genre: 'Historical Fiction',
  publicationYear: null,
  notes: 'I enjoyed reading this, but would only recommend if you are a big fan of historical fiction.',
  rating: 8.4,
 }];
```
