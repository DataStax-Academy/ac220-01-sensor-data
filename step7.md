<!-- TOP -->
<div class="top">
  <img src="https://datastax-academy.github.io/katapod-shared-assets/images/ds-academy-logo.svg" />
  <span style="position:absolute;top:20px;left:350px;font-size:30px"><b>Sensor Data Modeling</b></span>
  <span style="position:absolute;top:80px;left:350px;font-size:12px">ℹ️ You run this scenario using DataStax Katapod platform, which is beta at the moment.</span> 
  <span style="position:absolute;top:100px;left:350px;font-size:12px">For any kind of questions, issue reports or anything other please contact our team using <a href="mailto:aleksandr.volochnev@datastax.com">email</a> or <a href="https://dtsx.io/aleks">LinkedIn</a></span>
</div>

<!-- NAVIGATION -->
<div id="navigation-top" style="width:100%;text-align:center;margin-top:10px;margin-bottom:30px">
 <a href="command:katapod.loadPage?%5B%7B%22step%22%3A%22step6%22%7D%5D" 
   class="btn btn-dark" 
   style="float:left">⬅️ Step 6
 </a>
<span style="font-size:20px;"> Step 7 of 7</span>
 <a href="command:katapod.loadPage?%5B%7B%22step%22%3A%22finish%22%7D%5D" 
    class="btn btn-dark" 
    style="float:right">Finish ➡️
  </a>
</div>

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
<div id="navigation-bottom" style="width:100%;text-align:center;">
 <a href="command:katapod.loadPage?%5B%7B%22step%22%3A%22finish%22%7D%5D" 
    class="btn btn-primary btn-astra" 
    style="float:right">CONTINUE ➡️
  </a>
</div>
