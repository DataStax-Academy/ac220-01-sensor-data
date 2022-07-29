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
<span style="font-size:20px;"> Step 2 of 7</span>
 <a href="command:katapod.loadPage?%5B%7B%22step%22%3A%22step3%22%7D%5D" 
    class="btn btn-dark" 
    style="float:right">Step 3 ➡️
  </a>
</div>

<!-- CONTENT -->

## Create schema for keyspace `sensor_data`

- **✅ Step 2a: Create table `networks`**

```
CREATE TABLE IF NOT EXISTS networks (
  bucket TEXT,
  name TEXT,
  description TEXT,
  region TEXT,
  num_sensors INT,
  PRIMARY KEY ((bucket),name)
);
```

- **✅ Step 2b: Create table `temperatures_by_network`**

```
CREATE TABLE IF NOT EXISTS temperatures_by_network (
  network TEXT,
  week DATE,
  date_hour TIMESTAMP,
  sensor TEXT,
  avg_temperature FLOAT,
  latitude DECIMAL,
  longitude DECIMAL,
  PRIMARY KEY ((network,week),date_hour,sensor)
) WITH CLUSTERING ORDER BY (date_hour DESC, sensor ASC);
```

- **✅ Step 2c: Create table `sensors_by_network`**

```
CREATE TABLE IF NOT EXISTS  sensors_by_network (
  network TEXT,
  sensor TEXT,
  latitude DECIMAL,
  longitude DECIMAL,
  characteristics MAP<TEXT,TEXT>,
  PRIMARY KEY ((network),sensor)
);
```

- **✅ Step 2d: Create table `temperatures_by_sensor`**

```
CREATE TABLE IF NOT EXISTS  temperatures_by_sensor (
  sensor TEXT,
  date DATE,
  timestamp TIMESTAMP,
  value FLOAT,
  PRIMARY KEY ((sensor,date),timestamp)
) WITH CLUSTERING ORDER BY (timestamp DESC);
```

- **✅ Step 2e: Check that the 4 tables are created**

```
describe tables;
```

<!-- NAVIGATION -->
<div id="navigation-bottom" style="width:100%;text-align:center;">
 <a href="command:katapod.loadPage?%5B%7B%22step%22%3A%22step3%22%7D%5D" 
    class="btn btn-primary btn-astra" 
    style="float:right">CONTINUE ➡️
  </a>
</div>
