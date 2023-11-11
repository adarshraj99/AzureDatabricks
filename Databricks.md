#### Intro: 
Databricks is Apache spark product hosted by MS Azure it provides clusters, Notebooks, Delta-lake storages .......to update.

#### Clusters: 
set of computation resources and configurations used to run data engineering, data science, and data analytics workloads. Types: Single node and MultiNode Clusters. 
Single node cluster is having only one Node and no worker nodes. Multi Node cluster will have 1 Node and multiple workers (for larger compute resources).

* Cluster config: Configs for creating Clusters are:
- Single user (only 1 user access)
- Shared user Clusters (Multi users have access with different environments)
- no isolation Shared cluster (It also allows to share cluster among different usersbut, not with different environments, it is less secure and hardwares are shared)

* auto termination: Auto terminate the databricks cluster when it is not in use after set x mins. Default time is 2hrs.

* auto scaling cluster: It can add or remove the cluster worker nodes depending on the needed work loads.
