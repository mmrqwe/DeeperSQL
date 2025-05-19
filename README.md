# DeeperSQL Software Detailed Tutorial
## Language Change 
[简体中文](README.zh-CN.md)

## Tutorial Contents
* 1. Software Introduction
* 2. Installation & Launch
* 3. Main Features
* 4. Operation Steps
* 5. FAQ
* 6. Contact & Support

## 1. Software Introduction
DeeperSQL is a multi-functional tool that integrates Excel smart interaction, knowledge graph construction, AI Q&A, data visualization, and more. It's suitable for data editing and analysis, knowledge management, smart Q&A, and various other scenarios.
* After importing Excel files, you can process and export them using natural language.
* Built-in chart components for data visualization analysis
* Knowledge graphs can be constructed through large language models for intelligent Q&A
* Cross-platform support (Windows/macOS)

## 2. Installation & Launch
### 2.1 System Requirements
* Operating System: Windows 10/11 or macOS
* Dependencies: .NET 8.0 or higher
### 2.2 Installation Steps
1. Download the latest installation package.
2. Ensure .NET component support, with online/offline large model and embedded model support.
3. Run the `DeeperSQL` main program.
### 2.3 Launching the Software
1. Double-click the executable file.
2. For first-time launch, configure the large language model settings to ensure proper operation.

## 3. Main Features
### 3.1 Excel Smart Interaction
After importing Excel files, you can save them to a database and process, analyze, and export using natural language.
### 3.2 Knowledge Graph
Supports automatic generation, viewing, and querying of knowledge graph nodes, relationships, and communities. The software automatically generates knowledge graphs using large language models.
### 3.3 AI Q&A
The AI Q&A module supports integration with various large language models. Users can ask questions using natural language and select generated knowledge graphs for Q&A.
### 3.4 Data Analysis
Imported Excel files can be analyzed and visualized after being stored in the database.
### 3.5 API Service
Provides API services for SQL intelligent interaction.

## 4. Operation Steps
### 4.1 Settings
1. Click Settings on the main interface, then select "Setting".
2. After the settings interface appears, click the LLM tab, select a common model provider, enter the API address, input the API key if needed, and select the corresponding model.
3. Enter appropriate limits for API calls per minute and token limits. Online APIs typically have lower limits (10-30), and token limits should be at least 4096 but generally less than 10240 (adjust according to actual conditions).
4. Then enter the embedded model's API address and API key, and select the corresponding model. If localhost doesn't work for local models, try using 127.0.0.1.
5. If there are issues loading the model, a popup will appear. Ensure the model loads correctly.
6. If you check "Use sample data for SQL requests", the first row of data in the database table will be used as sample data. If privacy or confidentiality is a concern, use a local LLM or uncheck this option.
7. If you check "Use original text indexing", it will increase Token usage but improve retrieval accuracy.
### 4.2 Creating Knowledge Graphs
1. Click Knowledge Base on the main interface, then select the Knowledge Base sub-item.
2. In the knowledge base interface, select a node in the tree control on the left and right-click.
3. After the selection box appears, click Add Group, enter the group name, and click Confirm.
4. After adding, click the group in the property control and click Add in the top menu bar, then select the files to add.
5. Wait patiently for the knowledge graph generation to complete. If no errors occur, creation is successful.
6. In the knowledge base interface, select a node in the tree control on the left, right-click, and after the selection box appears, click Import Group or Export Group.
### 4.3 Managing Knowledge Graphs
1. Click Knowledge Base on the main interface, then select the Knowledge Base sub-item.
2. In the knowledge base interface, select a node in the tree control on the left and right-click.
3. After the selection box appears, click Delete Group, Import Group, or Export Group to perform these functions.
4. Select the default node, click "Template" in the menu bar to export the like database, or click "Import" to import it. Click Edit or Delete to modify or remove specific like content.
### 4.4 Viewing Knowledge Graphs
1. In the knowledge graph management interface, select a knowledge base and click the "Knowledge Graph" button.
2. After entering the knowledge graph viewing interface, click on the respective nodes or edges, then click the View button to see the corresponding data.
3. Enter search content, press Enter, and the corresponding search results will be displayed.
### 4.5 Adding Excel Files
1. Select the "Files" menu, click "Open", and select an Excel file.
2. After successful import, click Database, enter a database name, and click Save. (Note: The first row of the Excel sheet is automatically recognized as the database table field names)
3. Click the database you just saved, then click Load to load the database into the current table.
### 4.6 Editing Database Tables
1. After opening an Excel file or loading a database, you can select functions like "Copy, Paste, Undo, Redo, Add Column, Add Row" in the "Edit" menu.
2. Click on the table and right-click to select corresponding functions.
3. Click on table items (e.g., sheet1) in the menu bar to create, delete, or rename database table items.
### 4.7 Statistical Analysis
1. After loading a database, click the "Statistics" button on the main interface to enter the "Databse Statistics" page.
2. Select the database and table you want to analyze.
3. Select the fields to analyze, click the Analyze button, and view the analysis results. Click Export to export the analysis results.
### 4.8 Excel Smart Interaction
1. After adding an Excel file and saving the database, load this database.
2. Enter a natural language question in the bottom right of the main interface and click the "Generate" button.
3. After LLM processing, a dialog box automatically appears. Confirm the generated SQL is feasible, then click Execute to generate results. (Supports producing multiple results, e.g., generating twelve results by month)
4. Click Export and select a folder to export the results as an Excel table. Click the "Like" button to provide feedback to the local database (data is not uploaded), helping the software generate more accurate results.
### 4.9 AI Conversation
1. Select the "Knowledge Base" menu, then click "Chat".
2. Without clicking on the knowledge base tree on the left, enter a question in the input box, click the "Begin to Chat" button, and wait for results to be generated.
3. Click on the knowledge base tree on the left to load the corresponding knowledge base, enter a question in the input box, click the "Begin to Chat", and wait for results. After results are generated, click References or History to view related content.
### 4.10 API Service
* /api/SQL/List Get database list
* /api/SQL/Tables Get table list of the specified database Param: dbname
* /api/SQL/TableInfo Get table structure and row count Param: dbname, tablename
* /api/SQL/Get Get table data by page Param: dbname, tablename, start, num
* /api/SQL/Chat SQL intelligent Q&A Param: dbname, content
* /api/SQL/Do Execute SQL statement Param: dbname, content
* /api/status Service status

## 5. FAQ
### Q1: What should I do if there's an error during startup?
**A1:** Please check if the .NET environment is installed, or view the log file for detailed error information.
### Q2: What should I do if there's an error importing Excel files or creating a database?
**A2:** Please ensure the first row of the Excel file contains the database field names, and that the Excel data format is correct. For example, date fields in the database table should be in the format "2025-12-30".
### Q3: What should I do if there's an error loading the model?
**A3:** First, confirm if the model address is correct. If an API key is required, ensure you've entered the correct API key. Check if the http/https prefixes are correct, if the network is normal, etc. After changing the address, restart the software for testing.
### Q4: What should I do if there's an error with AI conversation?
**A4:**
1. Ensure the model address, API key, etc. are correct.
2. Ensure the network is normal.
3. For local models, ensure the model service is running properly.
4. For online models, ensure the API key is correct.
5. Ensure the token limits, API call limits per minute, etc. are correct—neither too high nor too low.

## 6. Contact & Support
For questions or suggestions, please contact the development team:
* Email: deepersql@hotmail.com

