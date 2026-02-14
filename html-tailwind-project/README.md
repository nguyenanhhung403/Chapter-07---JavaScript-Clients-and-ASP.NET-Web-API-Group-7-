# ASP.NET Core Architecture - Chapter 07 Documentation

This project provides a comprehensive visual and code-based documentation for **Chapter 07: JavaScript Clients and ASP.NET Web API**.

## Project Structure (Splitted for Debugging)
To ensure better maintainability and debugging, the documentation is split into separate modules:

1.  **[index.html](./src/index.html)** - **Overview & Architecture**
    -   Visual Diagram of the Request Flow (Client -> Proxy -> Host -> App).
    -   Detailed explanation of each layer (Edge, Web Server, Middleware, App Logic).
2.  **[code-samples.html](./src/code-samples.html)** - **Code Implementation**
    -   JavaScript Fetch API examples.
    -   ASP.NET Core Controller implementation.
    -   CORS Configuration in `Program.cs`.
3.  **[advanced-diagrams.html](./src/advanced-diagrams.html)** - **Deep Dive Flows**
    -   Authentication Flow (Login -> JWT -> Authorized Request).
    -   CORS Preflight Mechanism (OPTIONS -> Access-Control -> Data).
4.  **[input.css](./src/input.css)** - **Custom Styles**
    -   Contains all custom animations and Tailwind directives.

## How to Run
Simply open `src/index.html` in your web browser. No server required for viewing static documentation (though running via Live Server is recommended).

## Architecture Overview
The system follows a standard ASP.NET Core Request Pipeline:
1.  **Request** starts from Client -> Nginx.
2.  **Kestrel** receives -> Middleware Pipeline.
3.  **Auth & Logic** processes the request.
4.  **Database** (SQL Server) is queried via EF Core.

> **Group 7 Presentation** - JavaScript Clients and ASP.NET Web API
