# Saga

- LLT (Long Lived Transactions)
- Limitations of database transactions (long locks)
- Microservice (One Service - One Database)
- Saga - Manange failure when one microservice fail in chain

# Saga Failure Modes

- Backward Recovery - Revert Faliure, Cleanup, Rollback
- Forward Recovery - Start from where failed
- Saga only accunts for businuss failure & not technical fauiluer such as HTTP-500
- Diffrent from ACID Rollback
- Compensating Transaction
- Sometime Reoredering workflow helps
- Mix & Match Backward & forward approches

# Saga Implemeatation

## Orchestrated Saga
- Centralized (Command & Control)
- Easy to manage
- Works well when single team owns the saga

## Choriographed Saga
- Distributed (Trust but Verify)
- Lots of events
- Works well when multiple teams own the saga

- -------------------------------------\\


<dependencies>
    <dependency>
        <groupId>jakarta.xml.bind</groupId>
        <artifactId>jakarta.xml.bind-api</artifactId>
        <version>4.0.0</version> <!-- Use the latest version -->
    </dependency>
    <dependency>
        <groupId>org.glassfish.jaxb</groupId>
        <artifactId>jaxb-runtime</artifactId>
        <version>4.0.0</version> <!-- Use the latest version -->
    </dependency>
</dependencies>

-------------------------

Download the JAXB Standalone Distribution:

Download the standalone JAXB implementation from the Maven repository or GitHub: JAXB GitHub Releases.
Run the XJC Tool: After downloading, you can use the xjc tool to generate Java classes from an XSD (XML Schema Definition) file.

Example command:

bash
Copy
Edit
xjc -d <output_directory> -p <package_name> <schema_file>.xsd
-d: Specifies the output directory for the generated files.
-p: Specifies the package name for the generated classes.
<schema_file>.xsd: The XML schema file.
Add the Generated Classes to Your Project: Copy the generated classes into your project directory and ensure they are included in your build.


