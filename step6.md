<!-- TOP -->
<div class="top">
  <img src="https://datastax-academy.github.io/katapod-shared-assets/images/ds-academy-logo.svg" />
  <span class="scenario-title">Sensor Data Modeling</span>
  <span class="scenario-subtitle">ℹ️ For technical support, please contact us via <a href="mailto:aleksandr.volochnev@datastax.com">email</a> or <a href="https://dtsx.io/aleks">LinkedIn</a>.</span> 
</div>

<!-- NAVIGATION -->
<div id="navigation-top" style="width:100%;text-align:center;margin-top:10px;margin-bottom:30px">
 <a href="command:katapod.loadPage?%5B%7B%22step%22%3A%22step5%22%7D%5D" 
   class="btn btn-dark" 
   style="float:left">⬅️ Step 5
 </a>
<span style="font-size:20px;"> Step 6 of 7</span>
 <a href="command:katapod.loadPage?%5B%7B%22step%22%3A%22step7%22%7D%5D" 
    class="btn btn-dark" 
    style="float:right">Step 7 ➡️
  </a>
</div>

# Exercise

- **✅ Step 6a: Build a Cql query that matches those requirements**

> Q4: Find information about all sensors in network `forest-net`:

<details>
  <summary><b style="color:#003882">Show me first solution for Q4</b></summary>

```
SELECT * 
FROM sensors_by_network
WHERE network = 'forest-net';
```
</details>

<!-- NAVIGATION -->
<div id="navigation-bottom" style="width:100%;text-align:center;">
 <a href="command:katapod.loadPage?%5B%7B%22step%22%3A%22step7%22%7D%5D" 
    class="btn btn-primary btn-astra" 
    style="float:right">CONTINUE ➡️
  </a>
</div>
