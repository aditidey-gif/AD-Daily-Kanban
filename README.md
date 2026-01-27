# AD-Daily-Kanban

**🚀 AD-Daily-Kanban : Technical Overview**

This project is built with a modular architecture. Instead of one giant file, the logic is split into specialized modules that communicate with each other.

**📊 The Architecture (Flowchart Explanation)**
Based on my project flowchart, the app follows a hierarchical structure:

**1) Entry Point:** Index.html loads the skeleton.

**2) The Orchestrator:** Main.js acts as the brain, connecting the UI with the Data.

**3) The Workers:** Store.js (Data), Ui.js (Visuals), and dragDrop.js (Interactions) handle specific tasks.

<img width="863" height="489" alt="image" src="https://github.com/user-attachments/assets/b74a5cc3-cee7-48b0-8930-ecd64aa1d54b" />

**🔄 The Connection:** store.js --> dragDrop.js. 
In the flowchart, you’ll notice an arrow pointing from the Store to DragDrop. This represents Data Persistence.
When you physically move a card in the UI, dragDrop.js catches it.
dragDrop.js then calls a function in store.js to update that task's status in the database.
Result: If you move a task to "Done" and refresh the page, it stays in "Done."
