**🧠 Store Module Documentation (store.js)**

The store.js file serves as the Data Access Layer for the Kanban application. It acts as the "Manager" of the browser's localStorage, ensuring that all task data is persistent, uniquely identified, and correctly formatted.

**FUNCTIONS EXPLAINATION:**

**1. getToday()**
    **Definition:** A utility function that standardizes the current system date.

    **The Logic:** It takes a new Date() object, converts it to an ISO string, and splits it at the "T" to extract       only the YYYY-MM-DD portion.

    **Why it's used:** To ensure the application always opens to a consistent "Current Day" view and to provide a        standardized date format for database filtering.


**2. getTasks(filterDate)**
**Definition:** The primary "Read" function for the database.

**The Logic:**

**Retrieval:** It fetches the raw JSON string from localStorage using the STORAGE_KEY.

**Parsing:** It converts that text back into a JavaScript Array using JSON.parse().

**Filtering:** It uses the .filter() method to extract only the tasks where the task.date matches the filterDate provided.

**Output:** Returns an array of task objects specifically for the selected day.


3. saveTasks(allTasks)
Definition: An internal helper function responsible for the final "Write" to memory.

The Logic: Since localStorage can only store strings, this function uses JSON.stringify(allTasks) to "vacuum-pack" the entire task array into a single text block.

The Action: It overwrites the existing data in the STORAGE_KEY drawer with the new, updated string.
