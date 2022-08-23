<!-- TOP -->
<div class="top">
  <img src="https://datastax-academy.github.io/katapod-shared-assets/images/ds-academy-logo.svg" />
  <span class="scenario-title">Sensor Data Modeling</span>
  <span class="scenario-subtitle">ℹ️ For technical support, please contact us via <a href="mailto:aleksandr.volochnev@datastax.com">email</a> or <a href="https://dtsx.io/aleks">LinkedIn</a>.</span> 
</div>

<!-- NAVIGATION -->
<div id="navigation-top" class="navigation-top">
 <a href='command:katapod.loadPage?[{"step":"intro"}]'
   class="btn btn-dark navigation-top-left">⬅️ Introduction
 </a>
<span class="step-count"> Step 1 of 7</span>
 <a href='command:katapod.loadPage?[{"step":"step2"}]' 
    class="btn btn-dark navigation-top-right">Step 2 ➡️
  </a>
</div>

<!-- CONTENT -->

<div class="step-title">Start Cassandra</div>

During this chapter we will validate that Apache Cassandra™ is running for you and will create the dedicated keyspace for our scenario.

- **✅ Step 1a: Validate that Cassandra is `Ready`**

```
chmod 700 ./wait-cassandra.sh
./wait-cassandra.sh
```

- **✅ Step 1b: Start the CQL shell**

```
cqlsh 2>/dev/null
```

- **✅ Step 1c: Create the `sensor_data` keyspace:**

Notice that we are working with a single node with datacenter name `DC-Houston`
```
CREATE KEYSPACE IF NOT EXISTS sensor_data
WITH replication = {
  'class': 'NetworkTopologyStrategy', 
  'DC-Houston': 1 };
```

- **✅ Step 1d: Set the current working keyspace:**

```
USE sensor_data;
```

<!-- NAVIGATION -->
<div id="navigation-bottom" class="navigation-bottom">
 <a href='command:katapod.loadPage?[{"step":"step2"}]' 
    class="btn btn-primary btn-astra navigation-bottom-right">CONTINUE ➡️
  </a>
</div>
