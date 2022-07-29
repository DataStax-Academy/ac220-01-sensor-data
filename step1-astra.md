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

## Create Astra Database

- **✅ Step 1a: Create Astra Account (if needed)**

> If you already have your token go to step **1c**

<a href="https://astra.datastax.com" target="_blank"  class="btn btn-dark">
Open DataStax Astra
</a>

- Once you signed in there is no need to create a database from the user interface, simply create tken.

- **✅ Step 1b: Create Astra Token (if needed)**

> If you already have your token go to step **1c**

```
gp preview https://awesome-astra.github.io/docs/pages/astra/create-token/
```

- **✅ Step 1c: Setup your environment**

```
astra setup
```

- **✅ Step 1d: List your databases**

```
astra db list
```

- **✅ Step 1e: Create a database `ac201` with the keyspace `sensor_data`**

```
astra db create demo -k sensor_data --if-not-exist
```

- **✅ Step 1e: Wait for the DB be becomes active**

```
astra db get demo | grep Status
```

# Start Cqlsh

```
clear
astra db cqlsh -k demo
```

<!-- NAVIGATION -->
<div id="navigation-bottom" style="width:100%;text-align:center;">
 <a href="command:katapod.loadPage?%5B%7B%22step%22%3A%22step2%22%7D%5D" 
    class="btn btn-primary btn-astra" 
    style="float:right">CONTINUE ➡️
  </a>
</div>

