## grammar

This section lists several common grammatical errors in Chinese technical documents, which should be paid attention to by document engineers and reviewers.


### Missing ingredients

[Example 1] Session persistence: If the application does not provide the function of session persistence, HAProxy can provide this function.

[Recommendation] Session persistence: HAProxy can provide this function if the application does not provide the session persistence function.

### Mismatch

[Example 1] HAProxy was written in 2000 by Willy Tarreau, a core contributor to the Linux kernel, and is still responsible for the maintenance of the project, which provides free and version iterations in the open source community.

[Existing Issues] The subject of "and still in charge" is Willy Tarreau, not HAProxy.

[Suggestion] HAProxy was written in 2000 by Willy Tarreau, a core contributor to the Linux kernel, who still maintains the project and makes version iterations freely available in the open source community.

### misnomer

#### Multiple expression

It is recommended to follow the following specifications for expression multiples in technical documents.

- **The increase of the value must explicitly use "increased" or "increased to", not only "increased". "To" means increment, and "to" means quantification. **

    - [Error example] doubled
    - [Correct example 1] It has tripled—that is, it used to be one, and it is three now.
    - [Correct example 2] Increase to twice as much as in the past—that is, the past is one, and the present is two.

- **Value reduction must explicitly use "reduced" or "reduced to", not just "reduced". "To" means increment, and "to" means quantification. **

    - [Error example] 80% reduction
    - [Correct Example 1] Reduced by 80%—that is, it used to be one hundred, and now it is twenty.
    - [Correct Example 2] Reduced to 80% - that is, it was 100 before, and now it is 80.

- **Do not use the notation "N times less" or "N times less", use "decrease by a few percent" or "decrease by a few percent". **

### Excess ingredients

[Example 1] According to the official recommendation, the current stable version of HAProxy is the stable version [2.0 features](https://www.haproxy.com/blog/haproxy-2-0-and-beyond/).

[Explanation] The official currently recommends using the stable version 2.0 of HAProxy. For the features of 2.0, please refer to this link.

[Recommendation] It is currently recommended to use [HAProxy stable version 2.0](https://www.haproxy.com/blog/haproxy-2-0-and-beyond/).

### Sentence mix

[Example 1] When deploying multiple DM-master nodes, all DM-master nodes will use the embedded etcd to form a cluster and store metadata such as cluster node information and task configuration. At the same time, the leader node is elected through etcd to provide Various services related to cluster management and data migration task management. Therefore, if the number of available nodes of DM-master exceeds half of the deployed nodes, services can be provided normally.

【Explanation】Properly segment sentences, clarify the subject, and avoid mixed sentence patterns.

[Recommendation] When deploying multiple DM-master nodes, all DM-master nodes will use the embedded etcd to form a cluster. The DM-master cluster is used to store metadata such as cluster node information and task configuration, and to elect the leader node through etcd. The leader node is used to provide various services related to cluster management and data migration task management. Therefore, if the number of available DM-master nodes exceeds half of the deployed nodes, services can be provided normally.