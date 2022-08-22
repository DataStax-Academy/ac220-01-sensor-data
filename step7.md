<!-- TOP -->
<div class="top">
  <img src="https://datastax-academy.github.io/katapod-shared-assets/images/ds-academy-logo.svg" />
  <span class="scenario-title">Sensor Data Modeling</span>
  <span class="scenario-subtitle">ℹ️ For technical support, please contact us via <a href="mailto:aleksandr.volochnev@datastax.com">email</a> or <a href="https://dtsx.io/aleks">LinkedIn</a>.</span> 
</div>

<!-- NAVIGATION -->
<div id="navigation-top" class="navigation-top">
 <a href='command:katapod.loadPage?[{"step":"step6"}]'
   class="btn btn-dark navigation-top-left">⬅️ Step 6
 </a>
<span class="step-count"> Step 7 of 7</span>
 <a href='command:katapod.loadPage?[{"step":"finish"}]'
    class="btn btn-dark navigation-top-right">Finish ➡️
  </a>
</div>

<!-- CONTENT -->

# Exercise

- **✅ Step 7a: Build a Cql query that matches those requirements**

> Q5: Find raw measurements for sensor `s1003` on `2020-07-06`; order by timestamp (desc):

<details>
  <summary><b style="color:#003882">Show me first solution for Q5</b></summary>

```
SELECT timestamp, value 
FROM temperatures_by_sensor
WHERE sensor = 's1003'
  AND date   = '2020-07-06';
```

</details>

<!-- NAVIGATION -->
<div id="navigation-bottom" class="navigation-bottom">
 <a href='command:katapod.loadPage?[{"step":"finish"}]'
    class="btn btn-primary btn-astra navigation-bottom-right">CONTINUE ➡️
  </a>
</div>
