# Explanation the database selection and justification

## Lab 1 26W_CST8917 Serverless Applications

### Student: Olga Durham
### St#: 040687883

---

## Database Choice for Text Analyzer Results

### My Choice
**Azure Cosmos DB (Core / SQL API – Serverless)**

### Justification
Azure Cosmos DB is the best choice for this use case because it natively stores JSON documents, which matches the structure of the Text Analyzer output. Its schema-less design allows analysis results to be stored without additional data modeling or schema management. The serverless tier aligns well with a serverless Azure Functions architecture by automatically scaling and handling capacity. In addition, Cosmos DB integrates well with Azure Functions and provides strong Python SDK support.

### Alternatives Considered
Azure Table Storage was considered but rejected due to its limited query capabilities and difficulty handling complex or nested JSON data. Azure SQL Database was not selected because it requires predefined schemas and relational modeling, which adds unnecessary complexity for storing document-based analysis results. Azure Blob Storage was also evaluated, but it lacks indexing and querying features, making it unsuitable for efficiently retrieving historical analysis data.

### Cost Considerations
Azure Cosmos DB offers a free tier that includes a limited amount of throughput and storage, making it suitable for student projects. The serverless pricing model further reduces cost by charging only for the database operations performed, with no charges when the database is idle. This pay-per-request model makes Cosmos DB cost-effective for low-traffic and experimental serverless applications.

[<< Back to README.md](/README.md)
