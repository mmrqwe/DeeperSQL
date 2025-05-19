# DeeperSQL Software Detailed Tutorial

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

# DeeperSQL 软件详细教程

## 教程目录
* 1. 软件简介
* 2. 安装与启动
* 3. 主要功能
* 4. 操作步骤演示
* 5. 常见问题
* 6. 联系与支持

## 1. 软件简介
DeeperSQL 是一款集成Excel智能交互、知识图谱构建、AI问答、数据可视化等多功能于一体的工具软件，适用于数据编辑与分析、知识管理、智能问答等多种场景。
* 导入Excel文件后，可通过自然语言处理并导出。
* 内置图表组件，可对数据进行可视化分析
* 可以通过大语言模型构建知识图谱，并进行智能问答
* 跨平台支持（Windows/macOS）

## 2. 安装与启动
### 2.1 环境要求
* 操作系统：Windows 10/11 或 macOS
* 依赖：.NET 8.0 及以上
### 2.2 安装步骤
1. 下载最新安装包。
2. 确保.NET组件支持，同时具备在线/离线大模型和嵌入式模型支持。
3. 运行 `DeeperSQL` 主程序。
### 2.3 启动软件
1. 双击可执行文件。
2. 首次启动请配置好大语言模型相关设置，以保证软件正确运行。

## 3. 主要功能
### 3.1 Excel智能交互
导入Excel文件后，可将其保存至数据库中，可通过自然语言进行智能处理、分析并导出。
### 3.2 知识图谱
支持知识图谱的节点、关系、社区的自动生成、查看、查询，软件通过大语言模型自动生成知识图谱。
### 3.3 AI问答
AI问答模块支持多种大语言模型的接入，用户可通过自然语言进行智能问答，可选择已生成的知识图谱进行问答。
### 3.4 数据分析
导入的Excel文件入库后可进行数据分析、可视化。
### 3.5 API服务
对SQL智能交互提供API服务。

## 4. 操作步骤演示
### 4.1 设置
1. 主界面点击设置，选择设置属性。
2. 弹出设置界面后，点击大模型tab，选择常用模型提供商，再填入api地址，如果有api key则填入，再选择对应模型。
3. 填入合适的每分钟调用次数限制和token限制，一般在线api限制较低，10-30，token限制要大于等于4096，一般小于10240（根据实际情况调整）。
4. 再填入嵌入模型的api地址和api key，选择对应模型。如果本地模型填入localhost无反应则可尝试127.0.0.1
5. 如果模型加载有问题会弹窗，请务必保障模型正确加载。
6. 如果勾选SQL请求使用示例数据,会将数据库表中第一行数据作为示例数据,如果涉及隐私或保密安全,请使用本地LLM或不勾选
7. 如果勾选使用原文索引,会增加Token使用量,但同时检索更准确
### 4.2 创建知识图谱
1. 主界面点击知识库，选择子项知识库。
2. 在知识库界面左边树形控件中选择节点，并点击右键。
3. 弹出选择框后点击添加组，并填入该组名称，并点击确认。
4. 添加完成后，在属性控件中点击该组，并在上方菜单栏中点击添加，并选择需要添加的文件。
5. 耐心等待生成知识图谱完成，如果没有报错，则创建成功。
6. 在知识库界面左边树形控件中选择节点，并点击右键，弹出选择框后点击导入组、导出组按键可以。
### 4.3 管理知识图谱
1. 主界面点击知识库，选择子项知识库。
2. 在知识库界面左边树形控件中选择节点，并点击右键。
3. 弹出选择框后点击删除组、导入组、导出组可以实现知识组删除、导入、导出功能。
4. 选择默认节点，点击菜单栏"模板"可以导出点赞库，点击"导入"可导入点赞库。点击编辑、删除可以编辑和删除具体的点赞内容。
### 4.4 查看知识图谱
1. 知识图谱管理界面，选择知识库后，点击"知识图谱"按键。
2. 进入知识图谱查看界面后，点击相应的节点、边后点击查看按钮，可以查看对应数据。
3. 填入搜索内容，按下回车，显示相应搜索内容。
### 4.5 添加Excel文件
1. 选择"文件"菜单，点击"打开"，选择Excel文件
2. 导入成功后，点击数据库，填入数据库名后，点击保存。（注意：Excel表的第一行自动识别为数据库表的字段名）
3. 点击刚才保存的数据库，再点击加载，可将数据库加载到当前表格中。
### 4.6 编辑数据库表
1. 打开Excel文件或加载数据库后，可以在"编辑"菜单中选择"复制、粘贴、撤销、恢复、添加列、添加行"相应功能。
2. 点击表格，右键可以选择相应功能。
3. 菜单栏中点击表项（例如sheet1）可以新建、删除、重命名数据库表项。
### 4.7 统计分析
1. 加载数据库后，主界面点击"统计分析"按钮，进入"统计分析"页面。
2. 选择想要分析的数据库和表。
3. 选择要分析的字段后点击分析按钮，查看分析结果。点击导出可以导出分析结果
### 4.8 Excel智能交互
1. 添加Excel文件并保存数据库后，加载此数据库。
2. 主界面右下方填入自然语言问题，点击"生成"按钮。
3. LLM处理后，自动弹出对话框，确认生成的sql可行后，点击执行按钮，生成结果。（支持产生多个结果，例如：按月份生成十二个结果）
4. 点击导出，选择文件夹可以导出结果Excel表。点击"点赞"按钮可以将结果反馈给本地数据库（不会上传数据），帮助软件生成更准确结果。
### 4.9 AI对话
1. 选择"知识库"菜单，点击"对话"
2. 不点击左边知识库树，在输入框中输入问题，点击开始对话按钮，等待结果生成。
3. 点击左边知识库树，会加载相应知识库，在输入框中输入问题，点击开始对话按钮，等待结果生成。结果生成后，点击引用、历史可以查看相关内容。
### 4.10 API服务
* /api/SQL/List 获取数据库列表
* /api/SQL/Tables 获取制定数据库的表列表 参数:dbname
* /api/SQL/TableInfo 获取表结构和行数 参数:dbname,tablename
* /api/SQL/Get 分页获取表数据 参数:dbname,tablenam,start,num
* /api/SQL/Chat SQL智能问答 参数:dbname,content
* /api/SQL/Do 执行SQL语句 参数:dbname,content
* /api/status 服务状态

## 5. 常见问题
### Q1: 启动时报错怎么办？
**A1:** 请检查 .NET 环境是否安装，或查看日志文件获取详细错误信息。
### Q2: Excel文件导入错误或者数据库创建错误怎么办？
**A2:** 请确保Excel文件第一行为数据库字段名，确保Excel数据格式正确，如数据库表的日期字段格式为"2025-12-30"。
### Q3: 模型加载报错怎么办？
**A3:** 首先确认模型地址是否正确，如果需要填入api key，是否填入了正确的api key。地址的http、https前缀等是否正确，网络是否正常等等。更换地址后可重启软件再进行测试。
### Q4: AI对话错误怎么办？
**A4:**
1. 确保模型地址、api key等是否正确。
2. 确保网络正常。
3. 如果是本地模型，确保模型服务正常。
4. 如果是在线模型，确保api key是否正确。
5. 确保token限制、每分钟调用次数限制等是否正确，不能太高也不能太低。

## 6. 联系与支持
如有问题或建议，请联系开发团队：
* 邮箱：deepersql@hotmail.com
