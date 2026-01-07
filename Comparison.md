```mermaid
classDiagram
    class Architectural_Philosophy {
        +Dimension
        +Microsoft Fabric
        +Apache Ecosystem
    }

    class Design {
        +Fabric: Fully integrated, single SaaS platform
        +Apache: Loose federation of independent OSS projects
    }

    class Control_Plane {
        +Fabric: One unified control plane
        +Apache: No unified control plane; assemble your own
    }

    class Storage {
        +Fabric: OneLake (Delta-based)
        +Apache: HDFS, S3, Iceberg, Hudi, Delta
    }

    class Compute {
        +Fabric: Built-in Spark, SQL, pipelines, ML
        +Apache: Spark, Flink, Kafka, Hadoop, Airflow, etc.
    }

    class Ops_Model {
        +Fabric: Serverless, fully managed
        +Apache: You operate clusters, tuning, scaling, upgrades
    }

    Architectural_Philosophy --> Design
    Architectural_Philosophy --> Control_Plane
    Architectural_Philosophy --> Storage
    Architectural_Philosophy --> Compute
    Architectural_Philosophy --> Ops_Model
