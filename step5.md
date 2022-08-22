<!-- TOP -->
<div class="top">
  <img src="https://datastax-academy.github.io/katapod-shared-assets/images/ds-academy-logo.svg" />
  <span class="scenario-title">Sensor Data Modeling</span>
  <span class="scenario-subtitle">ℹ️ For technical support, please contact us via <a href="mailto:aleksandr.volochnev@datastax.com">email</a> or <a href="https://dtsx.io/aleks">LinkedIn</a>.</span> 
</div>

<!-- NAVIGATION -->
<div id="navigation-top" class="navigation-top">
 <a href='command:katapod.loadPage?[{"step":"step4"}]'
   class="btn btn-dark navigation-top-left">⬅️ Step 4
 </a>
<span class="step-count"> Step 5 of 7</span>
 <a href='command:katapod.loadPage?[{"step":"step6"}]'
    class="btn btn-dark navigation-top-right">Step 6 ➡️
  </a>
</div>

<!-- CONTENT -->

# Exercise

- **✅ Step 5a: Build a Cql query that matches those requirements**

> Q2: Find hourly average temperatures for every sensor in network `forest-net` and date range [`2020-07-05`,`2020-07-06`] within the week of `2020-07-05`; order by date (desc) and hour (desc):

<details>
  <summary><b style="color:#003882">Show me the Solution for Q2</b></summary>

```
SELECT date_hour, avg_temperature, 
       latitude, longitude, sensor 
FROM temperatures_by_network
WHERE network    = 'forest-net'
  AND week       = '2020-07-05'
  AND date_hour >= '2020-07-05'
  AND date_hour  < '2020-07-07';
```
</details>

<br/>

- **✅ Step 5b: Build a Cql query that matches those requirements**

> Q3: Find hourly average temperatures for every sensor in network `forest-net` and date range [`2020-07-04`,`2020-07-06`] within the weeks of `2020-06-28` and `2020-07-05`; order by date (desc) and hour (desc):

<details>
  <summary><b style="color:#003882">Show me first solution for Q3</b></summary>

```
SELECT date_hour, avg_temperature, 
       latitude, longitude, sensor 
FROM temperatures_by_network
WHERE network    = 'forest-net'
  AND week       = '2020-07-05'
  AND date_hour >= '2020-07-04'
  AND date_hour  < '2020-07-07';
  
SELECT date_hour, avg_temperature, 
       latitude, longitude, sensor 
FROM temperatures_by_network
WHERE network    = 'forest-net'
  AND week       = '2020-06-28'
  AND date_hour >= '2020-07-04'
  AND date_hour  < '2020-07-07';  
```

</details>

<br/>Often there are multiple solutions working like here where we can find another way.

<details>
  <summary><b style="color:#003882">Show me another solution for Q3</b></summary>

```
SELECT date_hour, avg_temperature, 
       latitude, longitude, sensor 
FROM temperatures_by_network
WHERE network    = 'forest-net'
  AND week      IN ('2020-07-05','2020-06-28')
  AND date_hour >= '2020-07-04'
  AND date_hour  < '2020-07-07';  
```

</details>

<!-- NAVIGATION -->
<div id="navigation-bottom" class="navigation-bottom">
 <a href='command:katapod.loadPage?[{"step":"step6"}]' 
    class="btn btn-primary btn-astra navigation-bottom-right">CONTINUE ➡️
  </a>
</div>
