<div class="top">

# Create a keyspace
### [◂](command:katapod.loadPage?intro){.steps} Step 1 of 7 [▸](command:katapod.loadPage?step2){.steps}
</div>

Create the `sensor_data` keyspace:
```sql
CREATE KEYSPACE sensor_data
WITH replication = {
  'class': 'NetworkTopologyStrategy', 
  'DC-Houston': 1 };
```

Set the current working keyspace:
```sql
USE sensor_data;
```

[start scenario](command:katapod.loadPage?step2){.orange_bar}