**🎨 UI Module Documentation (ui.js)**

The ui.js file serves as the Presentation Layer of the Kanban application. It acts as the "Architect" of the user
interface, responsible for translating raw JavaScript data into a visual, interactive experience. By isolating the
visual logic here, the application ensures that how a task looks is completely separate from how it is stored.

**Core Responsibilities**

  **DOM Orchestration:** It manages the Document Object Model (DOM), handling the creation, removal, and updating of
  HTML elements dynamically.
  
  **State Visualization:** It takes the arrays provided by store.js and maps them to the correct physical columns on
  the screen.
  
  **User Feedback:** It ensures that user actions (like clicking "Add Task") result in immediate visual changes,
  providing a responsive feel


**FUNCTIONS EXPLANATION**

