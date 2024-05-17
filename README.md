# CSharp-Tooling-HeadBook

## Logging
### Libraries
- [Serilog](https://github.com/serilog/serilog-aspnetcore]): Leads the pack and is the go-to library for logging in .Net applications
- NLog
- Log4Net

### Sinks
- SQL and NoSQL database
- Data Streaming Platforms like Kafka

### Logging Services
- Splunk
- Datadog
- Loggly

### Structure Logging Tools & Platforms
- [Seq](https://datalust.co/seq)
  The self-hosted search, analysis, and alerting server built for structured logs and traces.

## Clean Architecture

### CQRS
- MediatR: Simplifies the implementation of CQRS pattern


### API Endpoints
- Carter: Routing and handling of HTTP requests, easier to define API endpoints with clean concise code.

### Object Mapping
- Mapster: It is a fast, configurable object mapper that simplifies the task of mapping and transforming objects.

### Validation
- Fluent Validation: For building strongly-typed validation rules ensure inputs are correct before processed.

## Databases

### Document Stores
- PostgreSQL + Marten: Marten turns PostgreSQL into a .NET transactional document store using its JSON columns features. Combines the flexibility of document database with the reliability of relational PostgreSQL database. It allows us to store and query our data as JSON documents.
- Mongodb.NET

## Project Folder Structure
### Vertical Slice Architecture
```
- Catalog.API
  + Data
    - CatalogIntitialData.cs
  + Exceptions
    - ProductNotFoundException.cs
  + Models
    - Product.cs
  + Products
    + CreateProduct
      - CreateProductEndpoint.cs
      - CreateProductHandler.cs
    + DeleteProduct
    + GetProductByCategory
    + GetProductById
    + GetProducts
    + UpdateProduct
  - app.settings.json
  - Dockerfile
  - Program.cs
```
 - The project is organized in **Model**, **Features**, **Data** and **Abstractions**.
 - **Features** like **CreateProduct** and **GetProduct** have dedicated handlers and endpoint definitions.
 - The feature folder will be **Products**.
 - Data folder and Context objects manages database interaction
