# Project Constraints

This project is implemented within an AWS sandbox environment with the following constraints:

- IAM access is read-only
- All services run using a preconfigured LabRole
- Infrastructure provisioning (IAM, networking) is not permitted

## Design Decisions

Due to these constraints:
- Amazon S3 is used as the primary storage layer
- AWS Glue is used for batch data transformations
- Amazon Athena is used as the analytical query engine on top of Parquet datasets
- The pipeline is executed manually rather than orchestrated