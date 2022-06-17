<div class="top">

# Design query Q1
### [◂](command:katapod.loadPage?step3){.steps} Step 1 of 7 [▸](command:katapod.loadPage?step5){.steps}
</div>

Find information about all networks; order by name (asc):

<details>
  <summary>Solution</summary>

```sql
SELECT name, description,
       region, num_sensors
FROM networks
WHERE bucket = 'all';
```{{execute}}

</details>

[continue](command:katapod.loadPage?step5){.orange_bar}