# lab-4
# Hotel Management System

This project demonstrates a Windows Forms application written in C# for managing hotel room data. It includes features for adding rooms, checking for duplicate room numbers, viewing room details in a table format, and saving/loading data from files.

## Features
- **Room Addition:** Allows adding new rooms with specified number, price, and discount.
- **Duplicate Check:** Verifies if a room with the same number already exists.
- **Room Overview:** Displays existing rooms in a table format.
- **Data Save and Load:** Enables saving room data to a file and loading it back into the application.
- **Class Diagram:** Organized structure with separate classes for database connections, commands, UI forms, and data handling.

## Screenshots
### Room Overview
![Room Overview](screenshot_room_overview.png)

### Room Addition and Duplicate Check
![Room Addition and Duplicate Check](screenshot_room_addition.png)

### Data Save and Load
![Data Save and Load](screenshot_data_save_load.png)

### Class Diagram
![Class Diagram](class_diagram_part1.png)

## Class Overview
### MySqlConnection
Handles database connection operations.
- **Methods:**
  - `Open() : void`
  - `Close() : void`

### MySqlCommand
Executes SQL commands.
- **Methods:**
  - `ExecuteReader() : SqlDataReader`
  - `ExecuteNonQuery() : int`

### Form1
Manages room addition, duplicate checks, and data saving/loading.
- **Methods:**
  - `Check(int num, string name) : bool`
  - `button1_Click(sender: object, e: EventArgs) : void`
  - `SaveData(filePath: string) : void`
  - `LoadData(filePath: string) : void`

### Form2
Displays room overview in a table format.
- **Methods:**
  - `Form2_Load(sender: object, e: EventArgs) : void`
  - `button1_Click(sender: object, e: EventArgs) : void`

### Data Handling
#### DataGridView
Used to display data in a tabular format.
#### MySqlDataAdapter
Fills `DataTable` objects with data from the database.
#### File Operations
Handles saving and loading data to/from files.

## How to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/your-repo/hotel-management-system.git
   ```
2. Open the project in Visual Studio.
3. Build and run the project.

## Usage
1. **Add Room:**
   - Enter the room number, price, and discount.
   - Click the **Add** button.
   - If the room number already exists, a message box will notify the user.
2. **View Rooms:**
   - Open the second form to view the list of rooms in a table format.
3. **Save Data:**
   - Save current room data to a file for future use.
4. **Load Data:**
   - Load saved room data from a file into the application.

## License
This project is licensed under the MIT License.
