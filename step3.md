<!-- TOP -->
<div class="top">
  <img src="https://datastax-academy.github.io/katapod-shared-assets/images/ds-academy-logo.svg" />
  <span class="scenario-title">Sensor Data Modeling</span>
  <span class="scenario-subtitle">ℹ️ For technical support, please contact us via <a href="mailto:aleksandr.volochnev@datastax.com">email</a> or <a href="https://dtsx.io/aleks">LinkedIn</a>.</span> 
</div>

<!-- NAVIGATION -->
<div id="navigation-top" style="width:100%;text-align:center;margin-top:10px;margin-bottom:30px">
 <a href="command:katapod.loadPage?%5B%7B%22step%22%3A%22step2%22%7D%5D" 
   class="btn btn-dark" 
   style="float:left">⬅️ Step 2
 </a>
<span style="font-size:20px;"> Step 3 of 7</span>
 <a href="command:katapod.loadPage?%5B%7B%22step%22%3A%22step4%22%7D%5D" 
    class="btn btn-dark" 
    style="float:right">Step 4 ➡️
  </a>
</div>


# Import the DataSet

- **✅ Step 3a: Execute the CQL script to insert sample data**

```
SOURCE 'assets/sensor_data.cql'
```

- **✅ Step 3b: Retrieve all rows from table `networks`**

```
SELECT * FROM networks;        
```

- **✅ Step 3c: Retrieve all rows from table `temperatures_by_network`**

```
SELECT network, week, date_hour, 
       sensor, avg_temperature 
FROM temperatures_by_network;
```

- **✅ Step 3d: Retrieve all rows from table `sensors_by_network`**

```
SELECT * FROM sensors_by_network;                    
```

- **✅ Step 3e: Retrieve all rows from table `temperatures_by_sensor`**

```
SELECT * FROM temperatures_by_sensor; 
```

<!-- NAVIGATION -->
<div id="navigation-bottom" style="width:100%;text-align:center;">
 <a href="command:katapod.loadPage?%5B%7B%22step%22%3A%22step4%22%7D%5D" 
    class="btn btn-primary btn-astra" 
    style="float:right">CONTINUE ➡️
  </a>
</div>