<!-- TOP -->
<div class="top">
  <img src="https://datastax-academy.github.io/katapod-shared-assets/images/ds-academy-logo.svg" />
  <span class="scenario-title">Sensor Data Modeling</span>
  <span class="scenario-subtitle">ℹ️ For technical support, please contact us via <a href="mailto:aleksandr.volochnev@datastax.com">email</a> or <a href="https://dtsx.io/aleks">LinkedIn</a>.</span> 
</div>

<!-- NAVIGATION -->
<div id="navigation-top" style="width:100%;text-align:center;margin-top:10px;margin-bottom:30px">
 <a href="command:katapod.loadPage?%5B%7B%22step%22%3A%22step3%22%7D%5D" 
   class="btn btn-dark" 
   style="float:left">⬅️ Step 3
 </a>
<span style="font-size:20px;"> Step 4 of 7</span>
 <a href="command:katapod.loadPage?%5B%7B%22step%22%3A%22step5%22%7D%5D" 
    class="btn btn-dark" 
    style="float:right">Step 5 ➡️
  </a>
</div>

# Exercise

- **✅ Step 4a: Build a Cql query that matches those requirements**

> Q1: Find information about all networks; order by name (asc):

<details>
  <summary><b style="color:#003882">Show me the Solution for Q1</b></summary>

```
SELECT name, description,
       region, num_sensors
FROM networks
WHERE bucket = 'all';
```

</details>

<!-- NAVIGATION -->
<div id="navigation-bottom" style="width:100%;text-align:center;">
 <a href="command:katapod.loadPage?%5B%7B%22step%22%3A%22step5%22%7D%5D" 
    class="btn btn-primary btn-astra" 
    style="float:right">CONTINUE ➡️
  </a>
</div>
