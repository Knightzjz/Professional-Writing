## list

Vertical lists are the clearest and most eye-catching way to show when there are 3 or more important pieces of information to display. But if the item is less than 3 and doesn't need special emphasis, it usually works better to put it directly in the sentence.

You can also create multi-level nested lists, start a new line below a level, and indent **four spaces** to start a lower-level list.

### Unordered and ordered lists

Lists in technical documents are divided into ordered lists and unordered lists. In general, use an unordered list when the order between list items is not important; use an ordered list when the order between items is important. **

[Example of no sequence table]

Currently, the TiDB database uses the following components:

- Prometheus Server: used to collect and store time series data.
- Client code base: used for the metrics required in the customizer.
- Alertmanager: used to implement the alert mechanism.

[Example of ordered list]

Solution:

1. Edit the data source file.
2. Manually create all tables.
3. Set the parameter to skip the check.

There are fewer usage scenarios for ordered lists. An ordered list should be used when the contents of the list items are as follows.

- Steps that must be performed in sequence (most common)
- Multiple items to rank
- Rules or other information that needs to be referenced below (e.g. "rule 3" when referring to item 3 of the list below)

**[Important Principle] Ordered lists are not recommended unless order is important. **

### List

The following guidelines are recommended for use of lists in technical documentation.

| Specifications for Using Lists | Wrong Cases | Right Cases |
| ------------------ | ------------------------- | --- ----------------------- |
| 1. Similar sentence structures are suggested in tied list items. | SQL Query Optimizer: <br> - Support eager aggregate <br> - More detailed explain information<br> - Union operator parallelization<br> - Subquery performance optimization<br> - Optimize CBO framework | SQL query optimization <br> - Support eager aggregate <br> - Support more detailed explain information<br> - Support union operator parallelization<br> - Optimize sub-query performance<br> - Optimize CBO framework |
| 2. The length of each item should be as close as possible. | New Issues submitted on GitHub fall into the following categories: <br> - If you find a bug to report<br> - Request to develop a new feature<br> - General issues<br> - To fix or improve performance Issues raised | New Issues submitted on GitHub are divided into the following categories: <br> - Bug Reports<br> - Feature Requests<br> - General Issues<br> - Performance Issues|
| 3. Avoid repeating the same words at the beginning of each item. | Differences between TiDB and MySQL security features: <br> - Does not support external authentication methods. <br> - Column level permission settings are not supported. <br> - Authentication using certificates is not supported. | Compared with MySQL security features, TiDB does not support the following functions: <br> - External authentication method <br> - Column level permission setting <br> - Certificate authentication method |
| 4. Use clear, descriptive sentences or phrases to introduce the list. | The state can be determined by the state_name of the store: <br> - Up: the store is in normal service<br> - Disconnected: the heartbeat of this store is not currently detected, it may be a failure or the network connection is interrupted<br> - Down: more than one There is no store heartbeat for hours, at this time PD will add a copy to the data on this store | You can determine its state through the state_name of the store: <br> - Up: This store is in normal service<br> - Disconnected: currently not detected The heartbeat of this store may be a failure or a network connection interruption<br> - Down: If the store heartbeat has not been received for more than an hour, the PD will add a copy to the data on this store |
| 5. Keep punctuation consistent across side-by-side list items. <br> If the list item is a sentence, it is recommended to end each item with a period; <br> If the list item is a phrase, it is not recommended to end with any punctuation; <br> If the list item contains both a phrase and a sentence, it is recommended Unity ends with a period. | [Example 1] TiDB Binlog supports the following functional scenarios: <br> - Data synchronization. <br> - Real-time backup and restore. <br> <br> 【例二】指定数据源的相关信息： <br> - 在 Name 处，为数据源指定一个名称。 <br> - At Type, select Prometheus. <br> - At URL, specify the IP address of Prometheus. <br> - 其他字段| 【例一】TiDB Binlog 支持以下功能场景： <br>  - 数据同步<br>  - 实时备份和恢复<br> <br> 【例二】指定数据源的相关信息： < br> - At Name, specify a name for the data source. <br> - At Type, select Prometheus. <br> - At URL, specify the IP address of Prometheus. <br> - Additional fields. |
| 6. Do not abuse unordered lists, otherwise they will lose their effect. | None | None |
| 7. Avoid nested lists, which are often verbose and complex. If you must express a multi-level list, it is recommended to have no more than 3 levels, and each level should use a different style of small dots. | None | None |
8. An ordered list is usually used to describe the steps of an operation task. For the convenience of users’ memory, it is recommended to strictly limit the list items to less than 7 and no more than 9 steps at most. | None | None |
