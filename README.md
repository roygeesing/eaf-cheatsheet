# JPA

```java
@Entity(name = "EntityName")
@Table(name = "TableName")
public class Employee {
  @Id
  @GeneratedValue(strategy = GenerationType.IDENTIY)
  Long id;

  @Column(name = "ColumnName", nullable = false)
  String name;
}
```

## JPQL

```
SELECT c.name, c.address.city FROM Customer c
```

# AOP

## Annotations

* `@Before`
* `@AfterReturning`
* `@AfterThrowing`
* `@After`
* `@Around`

## Pointcut Expressions

|   |   |
|---|---|
| excution | method execution join points |
| within | join points within matching types |
| args | join points with matching arguments |
| @target | within classes with the given annotation |
| @args | joints points where arguments have given annotations |

```
execution(
  modifiers-pattern? ret-type-pattern declaring-type-pattern?name-pattern(param-pattern)
  throws-pattern?
)
```

# Transactions

## Propagation

|   |   |
|---|---|
| Required | Transatkion wird gestartet, falls noch nicht vorhanden |
| RequiresNew | Transaktion wird gestartet |
| Mandatory | Transaktion muss vorhanden sein |
| Supports | Transaktion wird verwendet, falls vorhanden |
| NotSupported | Transaktion wird nicht verwendet |
| Never | Transaktion darf nicht vorhanden sein |
| Nested | Transaktion muss vorhanden sein, neue wird gestartet |
