# Inventory-Project

Simple Java inventory monitor that reports items at or below their reorder
threshold and rejects stock updates that would make inventory negative.

## Requirements

- JDK with `javac` and `java` available on `PATH`

## Build and run

From the repository root in PowerShell:

```powershell
javac -d out com/wipro/inventory/bean/InventoryItem.java com/wipro/inventory/util/NegativeStockException.java com/wipro/inventory/service/InventoryService.java com/wipro/inventory/service/InventoryMonitor.java
java -cp out com.wipro.inventory.service.InventoryMonitor
```

The monitor checks inventory every five seconds and exits after about fifteen
seconds. Its sample updates demonstrate a reorder alert and the negative-stock
exception.