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


