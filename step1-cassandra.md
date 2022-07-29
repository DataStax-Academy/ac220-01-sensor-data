<div class="top">
  <img src="https://datastax-academy.github.io/katapod-shared-assets/images/ds-academy-logo.svg" />
  <span style="position:absolute;top:20px;left:350px;font-size:30px"><b>[AC220][01] - Sensor Data Modeling</b></span>
  <span style="position:absolute;top:80px;left:350px;font-size:12px">ℹ️ You run this scenario using DataStax Katapod platform, which is beta at the moment.</span> 
  <span style="position:absolute;top:100px;left:350px;font-size:12px">For any kind of questions, issue reports or anything other please contact our team using <a href="mailto:aleksandr.volochnev@datastax.com">email</a> or <a href="https://dtsx.io/aleks">LinkedIn</a></span>
</div>

<a href="command:katapod.loadPage?%5B%7B%22step%22%3A%22intro%22%7D%5D" class="btn btn-primary btn-astra" class="btn btn-primary" style="background-color:#111111;border:0px;position:absolute;top:150px;left:20px">
      ⬅️ Previous
  </a>
  Step 1 of 7 
  <a href="command:katapod.loadPage?%5B%7B%22step%22%3A%22step2%22%7D%5D" class="btn btn-primary btn-astra" class="btn btn-primary" style="background-color:#111111;border:0px;position:absolute;top:150px;left:100px">
       Next ➡️
  </a>

### [◂](command:katapod.loadPage?intro){.steps} Step 1 of 7 [▸](command:katapod.loadPage?step2){.steps}

# Start Cassandra 

- Cassandra is Starting, wait for the message `Ready`

```
echo -n 'Waiting for Cassandra to start...'; timeout 60 bash -c 'until cqlsh -e "describe cluster" >/dev/null 2>&1; do sleep 2; echo -n "."; done'; echo ' Ready!'
```

- Start the CQL shell:

```
cqlsh
```

- Create the `sensor_data` keyspace:

```
CREATE KEYSPACE sensor_data
WITH replication = {
  'class': 'NetworkTopologyStrategy', 
  'DC-Houston': 1 };
```

- Set the current working keyspace:

```
USE sensor_data;
```

[continue](command:katapod.loadPage?step2){.orange_bar}
