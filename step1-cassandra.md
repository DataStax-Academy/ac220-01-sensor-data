<!-- TOP -->
<div class="top">
  <img src="https://datastax-academy.github.io/katapod-shared-assets/images/ds-academy-logo.svg" />
  <span style="position:absolute;top:20px;left:350px;font-size:30px"><b>Sensor Data Modeling</b></span>
  <span style="position:absolute;top:80px;left:350px;font-size:12px">ℹ️ You run this scenario using DataStax Katapod platform, which is beta at the moment.</span> 
  <span style="position:absolute;top:100px;left:350px;font-size:12px">For any kind of questions, issue reports or anything other please contact our team using <a href="mailto:aleksandr.volochnev@datastax.com">email</a> or <a href="https://dtsx.io/aleks">LinkedIn</a></span>
</div>

<!-- NAVIGATION -->
<div id="navigation-top" style="width:100%;text-align:center;margin-top:10px;margin-bottom:30px">
 <a href="command:katapod.loadPage?%5B%7B%22step%22%3A%22intro%22%7D%5D" 
   class="btn btn-dark" 
   style="float:left">⬅️  Introduction
 </a>
<span style="font-size:20px;"> Step 1 of 7</span>
 <a href="command:katapod.loadPage?%5B%7B%22step%22%3A%22step2%22%7D%5D" 
    class="btn btn-dark" 
    style="float:right">Step 2 ➡️
  </a>
</div>


<!-- CONTENT -->

## Start Cassandra

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
<div id="navigation-bottom" style="width:100%;text-align:center;">
 <a href="command:katapod.loadPage?%5B%7B%22step%22%3A%22step2%22%7D%5D" 
    class="btn btn-primary btn-astra" 
    style="float:right">CONTINUE ➡️
  </a>
</div>
