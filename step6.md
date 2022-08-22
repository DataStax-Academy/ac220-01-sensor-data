<!-- TOP -->
<div class="top">
  <img src="https://datastax-academy.github.io/katapod-shared-assets/images/ds-academy-logo.svg" />
  <span class="scenario-title">Sensor Data Modeling</span>
  <span class="scenario-subtitle">ℹ️ For technical support, please contact us via <a href="mailto:aleksandr.volochnev@datastax.com">email</a> or <a href="https://dtsx.io/aleks">LinkedIn</a>.</span> 
</div>

<!-- NAVIGATION -->
<div id="navigation-top" class="navigation-top">
 <a href='command:katapod.loadPage?[{"step":"step5"}]'
   class="btn btn-dark navigation-top-left">⬅️ Step 5
 </a>
<span class="step-count"> Step 6 of 7</span>
 <a href='command:katapod.loadPage?[{"step":"step7"}]' 
    class="btn btn-dark navigation-top-right">Step 7 ➡️
  </a>
</div>

<!-- CONTENT -->

# Exercise

- **✅ Step 6a: Build a Cql query that matches those requirements**

> Q4: Find information about all sensors in network `forest-net`:

<details>
  <summary>Show me first solution for Q4</summary>

```
SELECT * 
FROM sensors_by_network
WHERE network = 'forest-net';
```
</details>

<!-- NAVIGATION -->
<div id="navigation-bottom" class="navigation-bottom">
 <a href='command:katapod.loadPage?[{"step":"step7"}]'
    class="btn btn-primary btn-astra navigation-bottom-right">CONTINUE ➡️
  </a>
</div>
