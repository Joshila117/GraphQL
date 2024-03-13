**GraphQL Library Management System**

**Overview**
This is a simple GraphQL-based Library Management System built using Express.js and GraphQL. It provides a GraphQL API to manage books and authors.

**Features**
Retrieve a single book by ID
Retrieve a list of all books
Retrieve a single author by ID
Retrieve a list of all authors

**Technologies Used**
Node.js
Express.js
GraphQL
express-graphql

**Working** 
Server Setup: The application uses Node.js and Express.js to set up a server that listens for incoming HTTP requests.

GraphQL Schema Definition: It defines the schema using the GraphQLSchema class from the graphql package. The schema includes:

BookType: Describes the structure of a book, including its ID, name, and the ID of its author. It also defines a field to resolve the author of the book.

AuthorType: Describes the structure of an author, including their ID, name, and a list of their books. It also defines a field to resolve the books written by the author.

RootQueryType: Defines the root queries that can be performed, such as fetching a single book by ID, fetching a list of all books, fetching a single author by ID, and fetching a list of all authors.

Data Mocking: Mock data for books and authors is defined statically within the application. This data includes information such as book titles, author names, and IDs.

Resolvers: Resolvers are functions responsible for fetching the actual data for each field in the schema. Resolvers are defined for fields like author in BookType and books in AuthorType to fetch related data based on the provided IDs.

GraphQL Middleware: The Express.js server uses the express-graphql middleware to handle GraphQL requests. This middleware is mounted at the /graphql endpoint and takes in a configuration object containing the GraphQL schema and other options.

GraphiQL Interface: When the server is running, developers can navigate to http://localhost:9000/graphql in their browser to access the GraphiQL interface. GraphiQL is an interactive graphical interface that allows users to explore and interact with the GraphQL API. It provides features like auto-completion and documentation.

Executing Queries: Developers can write and execute GraphQL queries within the GraphiQL interface. For example, they can query for a list of all books, a single book by its ID, a list of all authors, or a single author by their ID.

Query Execution: When a GraphQL query is executed, the server resolves the query by invoking the appropriate resolvers. Resolvers fetch data from the mock data sources based on the query parameters and return the requested data to the client in the format specified by the GraphQL query.


Overall, the GraphQL Library Management System provides a flexible and efficient way to query and manipulate data related to books and authors using GraphQL. Developers can easily extend the functionality by adding more types, fields, and resolvers to the schema as needed.
