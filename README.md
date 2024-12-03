# Note Pad
#### Video Demo:  <https://youtu.be/E3QF3Yb73hU>
#### Description:
My final project for CS50 2024 is a note taking app with an extended feature of a task management app
This Notepad with To-Do List app represents a simple, yet functional project designed using Java and XML in Android Studio. This app serves as a multi-purpose tool for managing text notes and tasks, integrating both note-taking capabilities and a to-do list feature into a single, easy-to-use interface.

The purpose of this project is to demonstrate a practical application of coding principles learned throughout the course. The app incorporates a user-friendly design, efficient code architecture, and essential functionality for creating, managing, and saving notes and to-do lists. It is an example of how fundamental mobile development concepts can be combined to solve everyday problems, like organizing notes and tasks in one place.

App Features and Functionality
NOTE TAKING
The notes app enables users to take quick notes on the go, with local storage making the app lightweight. With a clean user interface, it allows users to write, view, and delete notes when required.

Activity_main.xml
This XML file defines the basic layout and UI of the note-taking page. It includes the edit title, edit content, save notes button, displaying saved notes, and the open to-do list button. It also allows scrolling in case notes are large enough to take the entire mobile screen space.

Main_activity.java
Written in Java, it defines the functionality of the note-taking page of the app. Libraries are imported, and SharedPreferences is used as local storage to store the notes. It contains a function to display the stored notes from SharedPreferences. It defines the open to-do list button that will take us to the task page. The saveNote function will save the notes written in the local storage. After clicking the save notes button, a function clears the input fields that were in the EditText box. A delete function allows users to delete notes by holding the click on the note to be deleted, displaying a dialog box that asks for confirmation. Then it removes those notes from SharedPreferences.

note_bg.xml
This XML file decorates the layout of the saved notes and gives them a background color.

edittext_bg.xml
This XML file decorates the editing box of the note-taking app.

note_item.xml
This XML file defines the layout of saved notes, with note_bg.xml extracted here.

TO-DO LIST
The app also includes a built-in to-do list feature, allowing users to manage tasks in addition to notes. This feature is integrated within the same app to provide an all-in-one solution for productivity. Users can add tasks, check them off once completed, and delete them when no longer needed. The simple task manager allows for an intuitive experience, ensuring that users can quickly switch between note-taking and task management without any hassle.

activity_to_do_list.xml
This XML file defines the layout of the to-do list page. It has a linear layout and includes an enter task box, a button to save the task, and a button to open the notes.

task_item.xml
This XML file defines and displays the saved task along with the checkbox that indicates whether a task is completed or not.

Task.java
This Java file defines functions such as getDescription, isCompleted and setCompleted that are imported later into other Java files.

TaskAdapter.java
In this file, one function inflates the layout for each task item in the RecyclerView, while another function binds task data (description and completed status) to the ViewHolder. It also handles task status changes and long-clicks for task deletion, and it returns the total number of tasks in the list.

ToDoListActivity.java
This file initializes the task list and sets up a RecyclerView with a TaskAdapter in the onCreate method, allowing for the dynamic display of tasks. The addTaskButton adds a new task to the list when clicked, updates the RecyclerView to reflect the changes, and clears the input field. Additionally, the openNotesButton starts the MainActivity when clicked, allowing navigation to another screen.

The Notepad with To-Do List app is a practical and straightforward tool that provides users with the ability to manage notes and tasks in one place. Its simplicity and functionality make it a valuable tool for personal organization, while its development demonstrates a solid understanding of Android development principles. This project highlights key skills in Java programming, XML-based UI design, and the integration of multiple functionalities into a cohesive user experience.

By combining the basic principles of note-taking with task management, this app fulfills a clear need for organization and productivity in everyday life, while showcasing the essential skills needed for mobile app development.
