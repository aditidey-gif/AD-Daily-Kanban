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

**2. createCardElement(task)**

   **Definition:** The "Builder" function that generates a single Kanban card.

   **Step-by-Step Logic:**

    **Element Generation:** It uses document.createElement('div') to create a new HTML node in the browser's memory.
    
    **Property Injection: * Draggability:** It sets .draggable = true, which is the "on-switch" for the browser's
    native drag-and-drop system.
    
    **Data Attributes:** It stores the task's id and priority inside dataset. This is crucial because it allows other
    files (like dragDrop.js) to read information from the card just by looking at the HTML.
    
    **Styling:** It applies a background color. If no color is assigned, it uses a CSS variable (var(--black)) as a
    fallback to ensure the UI never looks broken.
    
    **Content Rendering:** It uses a template string to wrap the task's text (content) in a <span> for easier styling
