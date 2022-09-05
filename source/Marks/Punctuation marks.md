## Common punctuation marks

The most common punctuation marks in technical documents are: period, comma, comma, semicolon, colon, quotation mark, parenthesis, title mark, hyphen, dash, ellipsis, exclamation mark, slash and backslash. The specifications for their use are described below.

### period

The full stop is in the form of ".", which indicates the declarative tone and is used to pause at the end of a sentence.

The full stop indicates that the meaning of a sentence is complete. The full stop should be used in technical documents to segment the semantics to help users clarify the logic.

- [Error example] The reason is that the DM needs to save the synchronized binlog position information, but the MySQL binlog position official definition uses uint32 storage, so the offset value of the binlog position that exceeds the 4G part will overflow, and an incorrect binlog position will be stored. After restarting the task or dm-worker, you need to use the binlog position to parse the binlog/relay log again, and the above error occurs.
- [Correct example] Since the DM needs to save the synchronized binlog position information, and the MySQL binlog position official definition uses uint32 storage, the offset value of the binlog position exceeding 4G will overflow. This will result in an incorrect binlog position being stored. After restarting the task or dm-worker, you need to use the binlog position to reparse the binlog/relay log, and the above error occurs.

### comma

A comma of the form "," indicates a general pause inside a sentence.

Commas are most commonly used, but should not be abused. **Do not make the mistake of "one 'amuse' to the end" in technical documents, that is, commas are used for all pauses in the entire paragraph except the end of the paragraph. **

- [Error example] First judge whether the error occurred in relay log writing or binlog replication/syncer unit synchronization (you can judge by the component information in the log error message), if the error occurred in the relay log module, the binlog replication/syncer unit saved If the breakpoints are correct, you can stop the task first, stop the DM-worker, manually adjust the binlog-position of the relay meta to 4, restart the DM-worker, and re-pull the relay log. After the relay log is written normally, the task will be automatically started from Breakpoints continue to sync.

- [Correct example] First, use the component information in the log error message to determine whether the error occurred during the relay log writing phase or the binlog replication/syncer unit synchronization phase. If the error occurs in the relay log module and the breakpoints saved by the binlog replication/syncer unit are correct, you can stop the task and DM-worker first, manually adjust the binlog-position of the relay meta to 4, and then restart the DM-worker to pull it again. relay log. After the relay log is written normally, the startup task will automatically resume synchronization from the breakpoint.

### comma

The comma is in the form of ",", which means a short pause between two or more juxtaposed elements within a Chinese sentence. The juxtaposed elements here usually refer to **similar words, words or phrases**.

There is no comma in English, and commas are often used to indicate the pause of co-ordinated words. Therefore, for English-Chinese technical translators, more attention should be paid to the usage scenarios of commas.

Common misuse scenarios for commas:
| Wrong Example | Correct Example | Explanation |
| ------------------- | :------------------ | ------------- --------- |
| This operation will close TiDB, Pump, TiKV, PD services, and clear the Pump, TiKV, PD data directories. | This operation will close TiDB, Pump, TiKV, and PD services, and clear the data directories of Pump, TiKV, and PD | TiDB, Pump, TiKV, and PD are parallel words. Use a comma for a short pause, no comma is required. |
| Observe and analyze things from multiple angles and sides, and report in an all-round and perspective. | Observe and analyze things from multiple angles and sides, and report in an all-round and perspective. Although commas can also represent juxtapositions, they pause for a long time. If commas are misused as commas between juxtaposed words, the sentences will be loose, making it inconvenient for semantic expression and reading. |
How to further enhance the government's crisis awareness, enhance the transparency of the government's response to emergencies, and improve the ability to respond to emergencies, so as to truly deal with changes without panic and deal with them in an orderly manner, it is necessary to improve the relevant systems. How to further enhance the government's crisis awareness, enhance the transparency of the government's response to emergencies, improve the ability to respond to emergencies, and truly achieve calm and orderly handling, it is necessary to improve the relevant systems. | "Enhance the government's awareness of crisis" and "enhance the government's transparency in responding to emergencies" are clauses. The pauses between clauses are long, and commas should not be used instead of commas. |
| When we study Mr. Mao Dun, we should insist on writing for the people, go deep into social practice, reflect the creative principles of social life, and keep pace with the times and the people. | When we study Mr. Mao Dun, we should insist on writing for the people, go deep into social practice, reflect the creative principles of social life, keep pace with the times, and be of the same mind with the people as he did. | Before and after the comma is not a coordinating word, but a clause, so the comma should be changed to a comma. |
| The hierarchical structure of resources (primary, secondary and tertiary resources) is out of proportion, the distribution of disciplines and regions is uneven, and the repetition rate is too high. | The hierarchical structure of resources (primary, secondary and tertiary resources) is out of proportion, the distribution of disciplines and regions is uneven, and the repetition rate is too high. | After the comma is used incorrectly here, "the distribution of disciplines and regions is uneven" and "the repetition rate is too high" become juxtaposed words, resulting in ambiguity of the sentence. Therefore, the comma after "balance" should be changed to a comma, so that the sentence becomes a complex sentence composed of two clauses. |
| In a situation where our modernization drive is facing the dual challenges of population, resources, and environmental endurance, and international competitiveness is becoming more intense, education should play a role in promoting sustainable social, environmental and economic development. | Under the situation that our modernization construction is facing the dual challenges of population, resources, and environment, and the international competitiveness is becoming more intense, education should play a role in promoting the sustainable development of society, environment and economy. The function of the comma is equivalent to conjunctions such as "and", "follow", "and" and "or". If the coordinating words are long, the last item can be connected with conjunctions such as "and", "with", "and" and "or", and a comma can be added before the conjunction. The comma at this time not only means a pause, but also for the purpose of sparse and clear language. However, a comma cannot be used before a conjunction. Because in coordinating words, the function of the conjunction is equivalent to the comma. If you use a comma before a conjunction, you are using two commas in a row. |
| Any difference in syllabus, teaching method, or assessment method can foster innovative thinking. | Any difference in syllabus, teaching method or assessment method can foster innovative thinking. | Same as above |
| Routine operation and maintenance work can be performed through the TiUP cluster component, including deployment, startup, shutdown, destruction, elastic scaling, upgrading TiDB cluster, and managing TiDB cluster parameters. | Through the TiUP cluster component, you can perform daily operation and maintenance work, including deployment, startup, shutdown, destruction, elastic scaling, upgrading TiDB cluster, and managing TiDB cluster parameters. | Some coordinating words contain coordinating words inside, forming multi-level coordinating words. If commas are used between multi-level co-ordinated words, the levels between co-ordinated words will be confused, which is not conducive to understanding. |
| In the 1960s and 1970s, accusations that multinational corporations charged developing countries exorbitant technology transfer fees and transferred a large number of unsuitable technologies to developing countries were endless. | In the 1960s and 1970s, there were accusations that multinational corporations charged developing countries exorbitant technology transfer fees and transferred a large number of unsuitable technologies to developing countries. | **Two adjacent numbers are used side by side to indicate approximate numbers, Chinese characters must be used, and two numbers used in a row must not be separated by a comma ','. ** (from "GB/T 15835-1995 "Regulations on the Use of Numbers in Publications") |
| Strengthen the close cooperation between the government, enterprises, scientific research institutions and academic groups to realize the organic integration of production, learning and research. | Strengthen the close cooperation between the government, enterprises, scientific research institutions and academic groups to realize the organic combination of production, education and research. | **Some of the short co-ordinated words are closely related without pauses, and have become an inseparable whole. There is no need for commas inside them, and it has been established by convention. ** Such as "Marxism-Leninism", "Primary and Middle School Students", "Words and Sentences", "Industry-University-Research", "Ups and Downs", etc. |
3. Administration according to law in the construction of administrative civilization will directly promote the realization of my country's strategy of governing the country by law. 3. Administration according to law in the construction of administrative civilization will directly promote the realization of my country's strategy of governing the country by law. | Arabic numerals are used as ordinal numbers. For example, use a period instead of a comma after "1"; use a comma after the Chinese character "一", and use a comma after "first". These are conventional usages. |
| - "Day" and "Month" form the word "Ming". <br />- Banners such as "Customer is God" and "Quality is Life" hang in the store. <br />- "A Dream of Red Mansions", "Romance of the Three Kingdoms", "Journey to the West" and "Water Margin" are the four famous novels of Chinese novels. <br />- Li Bai's "white hair three thousand feet" ("Qiu Pu Song") "morning like blue silk and evening turning into snow" ("will enter the wine") are all well-known poems. | **A comma is usually not used between coordinating elements marked with quotation marks and between coordinating elements marked with title numbers. **If there are other components inserted between parallel quotation marks or parallel book titles (for example, there are parentheses after quotations or title numbers), a comma should be used. | - "Day" and "Month" form the word "Ming". <br />- Banners such as "Customer is God" and "Quality is Life" hang in the store. <br />- "A Dream of Red Mansions", "Romance of the Three Kingdoms", "Journey to the West" and "Water Margin" are the four famous novels of Chinese novels. <br /> - Li Bai's "white hair three thousand feet" ("Qiupu Song"), "morning like blue silk and evening snow" ("will enter the wine") are all well-known poems. | **A comma is usually not used between coordinating elements marked with quotation marks and between coordinating elements marked with title numbers. **If there are other components inserted between parallel quotation marks or parallel book titles (for example, there are parentheses after quotations or title numbers), a comma should be used. |
| - After I'm gone, you have to keep improving, literate, and productive. <br /> - The story is beautiful and moving. | - After I leave, you have to keep improving, literacy, and production. <br /> - The story is beautifully told and moving. | ** For parallel predicates, use commas instead of commas between complements. ** |
### Semicolon

The semicolon is in the form of ";", indicating a pause between coordinating clauses within a complex sentence. **In general, when there are three or more sentences in a coordinating clause, it is recommended to use a semicolon to indicate a pause. **

[Example] Placement Driver (PD) is the management module of the entire cluster. It has three main tasks: one is to store the meta information of the cluster (which TiKV node a key is stored in); the other is to schedule and load balance the TiKV cluster (such as data migration, Raft group leader migration, etc.); the third is to allocate a globally unique and incremental transaction ID.

### colon

The colon has the form ":". It is often used after the words that need to be explained in technical documents, indicating that explanations and explanations are drawn.

Colons are often used in technical documents to introduce lists.

[Example] The hardware system of a von Neumann system computer is divided into five parts:

- Calculator
- Controller
- memory
- input device
- output device

It is recommended not to use colons consecutively within a sentence.

- [Error example] Counting system: Logical representation: 1, the counter is incremented by one; 0, the counter remains unchanged.
- [Correct example] Counting system: 1 means the counter is incremented by one, 0 means the counter remains unchanged.

### quotation marks

Quotation marks are divided into right angle quotation marks and curly quotation marks. Right-angle quotation marks are "", and curly quotation marks have two forms: double quotation marks and single quotation marks. Generally speaking, right-angle quotation marks or curly quotation marks can be used in technical documents, but **must ensure the unity of all documents and prohibit mixing**.

This section only discusses some specifications for the use of curly quotation marks, and "quotation marks" used in the following all mean "curly quotation marks".

- When using quotation marks within quotation marks, use double quotation marks for the outer layer and single quotation marks for the inner layer.
- Quotes are recommended when error messages, specific operations or names, abbreviations, special nouns, and excerpts from quoted documents appear in technical documents.

    - 【Correct example 1】What is the reason for the "Timeout when waiting for search string 200 OK" message when the cluster is activated or upgraded?
    - [Correct example 2] Sysbench imports data in the order of "Create Table -> Insert Data -> Create Index".
    - [Correct example 3] If `tidb-lightning` ever exits abnormally, the cluster may remain in "import mode", which is not suitable for working in a production environment. At this point you need to force a switch back to "normal mode".
    - [Correct example 4] As a NewSQL database, TiDB takes into account the excellent features of traditional relational databases, the scalability of NoSQL databases, and high availability in cross-data center (hereinafter referred to as "center") scenarios.
    - [Correct example 5] The following operations may form a "relationship ring".

- If the body of the technical document involves specific parameter names, field names, interface fields, etc., it is recommended to use quotation marks (or backticks) to wrap.

    - [Correct example 1] The relationship between the TMN interfaces and the physical components supporting these interfaces is specified in the parameter table, where "M" means mandatory and "O" means optional.
    - [Correct example 2] For specific commands, see "1.2.1 Installation Steps" in the Quidway S8016 Routing Switch Installation Manual.
    - [Correct example 3] Please set the following three parameters: "Card Number", "Password", "Discount Rate".

### Parentheses

Common forms of parentheses include round brackets "()", square brackets "[ ]", square brackets "[]", angle brackets "<>" (also known as single book title), and curly brackets "{}". Among them, parentheses, square brackets and angle brackets are commonly used in technical documents.

Annotative text immediately following a word or sentence in a Chinese document, annotated with parentheses. When annotating certain words in a sentence, parentheses are placed after the word being annotated; when annotating an entire sentence, parentheses are placed after the punctuation at the end of the sentence.

- [Correct example 1] TiDB uses GC (Garbage Collection) that runs periodically to clean up.
- [Correct example 2] The configuration file needs to be edited to adjust the value of the parameter. (This method is not recommended)

In general, square and angle brackets have the following specific uses in technical documentation.

- Square brackets "[ ]" indicate window name, menu name, etc., such as "pop up [New Task] window", "[Display/Appearance/Full Screen] Multi-level menu".
- Angle brackets "< >" indicate button names, key names, etc., such as "click the <Cancel> button", "`<Tab>` indicates the tab key".
### Book Title

The title of the book is in the form of """. Titles of books, newspapers and periodicals should be marked with the title number. The title of the English manual shall be indicated in Chinese double quotation marks or italics, and shall not be indicated by the title number.

- [Example 1] The book "The Little Prince" is available in many languages.
- [Example 2] For details, see the article "TiDB-Lightning Table Library Filtering".

It is recommended to use the full name of the document name in the title number, not the abbreviation.

- [Error example] For details, see Table Library Filtering.
- [Correct example] For details, see "TiDB Lightning Table Library Filtering".

### connection number

The connection number indicates the connection relationship of some related components. Common forms of hyphens include the one-line "—" (the width of one Chinese character), the dash "-" (the width of half a Chinese character), and the wavy line "～" (the width of one Chinese character).

The functions and usage examples of several connection numbers are shown in the following table.

| Symbols | Usage Examples |
| --- | ------------------------------------- |
| One-word line — | - indicates the start and end of time, the start and end of space or the direction, the start and end of ordinal numbers, etc., such as Lu Xun (1881-1936), 2016-2020, January-March, Beijing-Shanghai Express Train, Qinling-Huaihe Line, - Building 15, Articles 50-100<br> - Connect the serial number and the year number in the standard numbering, such as GB/T 15835-2011 "Numbers in Publications" |
| The dash - | - plays a connecting role in various compound nouns such as telephone numbers, house numbers, chart numbers, and Arabic numerals, such as Room 2-1-201, No. 15 Xueyuan Road, Figure 2-1, Table 3-4, 2020-09-30, Turpan-Hami Basin<br> - plays a connecting role in the internal components of exonyms, such as Jean-Jacob Rousseau, Anglo-Saxons<br> - Indicates the name of certain products and model, such as GC-50 model equipment |
| Wavy line ~ | Marked value range: 1 to 3 g, 2 to 4 meters, 3 to 7 years |

> Rough memory method: use a single line (-) to indicate the start and end, use a wavy line (~) to indicate a range, and use a dash (-) for compound nouns.

### Dash

The dash is in the form of "——", which occupies the width of two Chinese characters. Dashes are often used in technical documentation to introduce notes and explanations.

[Example] So a new database concept - NewSQL database came into being.

No spaces before or after the dash.

- [Error example] So a new database concept - NewSQL database came into being.
- [Correct example] So a new database concept - NewSQL database came into being.

### ellipsis

The Chinese ellipsis is in the form of "...", with six small dots, occupying the width of two Chinese characters. Generally speaking, English ellipses are prohibited in the Chinese context, that is, three small dots "..." (occupying the width of one Chinese character), and six small dots "..." must be used.

The ellipsis is mainly used in the following two scenarios.

- Omissions of citations are indicated with ellipses.

    [Example] The Chinese writing specification requires: "Periods are often used at the end of declarative sentences. They are often used at the end of simple sentences and compound sentences in product materials, indicating that the meaning of the sentence is complete..."

- The omission of enumeration is indicated by an ellipsis.

    [Example] Branch selection supports all types of partition tables, whether range partition or hash partition. For hash partitions, if no partition name is specified, `p0`, `p1`, `p2`, ..., or `pN-1` are automatically used as the partition name.

### Exclamation mark

The following guidelines are recommended for the use of exclamation marks in technical documents.

- Try to speak in a calm tone and avoid exclamation marks.
- Do not use multiple exclamation marks together, such as "!!", etc.

### Slashes and backslashes

The symbol for a slash (slash or forward slash) is "/", which means a delimiter. The backslash symbol is "\", which means the escape character. Backslashes generally only appear in code, so this section focuses on the use of slashes.

Slashes can be used in the following ways.

- Indicates division, such as 120/60 = 2
- Indicates units (variant of division) such as 60 km/h
- means "or" like he/she. Note: If you need to represent multiple parallel items, it is not recommended to use "/" connection, it is recommended to use comma to connect.
    - [Error example] High availability is another major feature of TiDB. The three components of TiDB/TiKV/PD can tolerate partial instance failure without affecting the availability of the entire cluster.
    - [Correct example] High availability is another major feature of TiDB. The three components of TiDB, TiKV, and PD can tolerate partial instance failure without affecting the availability of the entire cluster.

Spaces around slashes are not recommended.

- [Error example] do / ignore rule
- [Correct example] do/ignore rule

### Backticks

> Note: This section only discusses backticks that appear in Markdown documents.

The backtick symbol is "`", which is usually typed by the key above the Tab key in the upper left corner of the keyboard under the English input method.

Backticks can be used in the following two ways.

| Usage categories | Single backticks wrap single-line elements | Triple backticks wrap multi-line elements |
| ---- | ---- | ---- |
| Function| Emphasize the wrapped part and distinguish it from the text content| - It is convenient to display multiple lines of code<br> - Emphasize the wrapped part and distinguish it from the text content<br> - In Markdown syntax, if the code is specified after the preceding ``` Syntax in blocks to highlight code blocks |
| Example | ``` `time_zone` default value is `System` ``` | <three backticks> <br> create table t (ts timestamp, dt datetime); <br> SELECT * FROM t1; <br > <three backticks> |
| Applicability| The following elements need to be enclosed in single backticks: <br> - variable name<br> - variable value<br> - syntax name<br> - command or code<br> - configuration item name<br> - Field name<br> - Other names that need to be emphasized, such as file name, table name, column name, library name, data type name, etc. | The following elements need to be enclosed in three backticks: <br> - Multi-line code block (multiple line SQL statement, multi-line bash command, etc.) <br> - code execution result<br> - multi-line configuration in configuration file |
