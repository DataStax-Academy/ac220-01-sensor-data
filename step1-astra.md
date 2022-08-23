<!-- TOP -->
<div class="top">
  <img src="https://datastax-academy.github.io/katapod-shared-assets/images/ds-academy-logo.svg" />
  <span class="scenario-title">Sensor Data Modeling</span>
  <span class="scenario-subtitle">ℹ️ For technical support, please contact us via <a href="mailto:aleksandr.volochnev@datastax.com">email</a> or <a href="https://dtsx.io/aleks">LinkedIn</a>.</span> 
</div>

<!-- NAVIGATION -->
<div id="navigation-top" class="navigation-top">
 <a href='command:katapod.loadPage?[{"step":"intro"}]' 
   class="btn btn-dark navigation-top-left">⬅️ Back
 </a>
<span class="step-count"> Step 1 of 7</span>
 <a href='command:katapod.loadPage?[{"step":"step2"}]' 
    class="btn btn-dark navigation-top-right">Next ➡️
  </a>
</div>

<!-- CONTENT -->

<div class="step-title">Connect to Astra DB and create a database</div>

✅ Create an application token to access Astra. Skip this step is you already have a token.

<ol>
  <li>Sign in (or sign up) to your Astra account at <a href="https://astra.datastax.com" target="_blank">astra.datastax.com</a></li>
  <li>Create an application token by following <a href="https://awesome-astra.github.io/docs/pages/astra/create-token/" target="_blank">these instructions</a></li>
</ol>

You can reuse the same token in our other scenarios, too.

✅ Setup Astra CLI by providing your application token:
```
astra setup
```




- **✅ Step 1d: List your databases**

```
astra db list
```

- **✅ Step 1e: Create a database `ac201` with the keyspace `sensor_data`**

```
astra db create ac201 -k sensor_data --if-not-exist
```

- **✅ Step 1f: Wait for the DB be becomes active**

If you list again the databases you should see the one you just created.

```
astra db list
```

You can get the details with 

```
astra db get ac201
```

Wait until the Status is `ACTIVE`

```
astra db get ac201 | grep Status
```

- **✅ Step 1g: Start CqlSh against keyspace `sensor_data`**

```
clear
astra db cqlsh ac201 -k sensor_data
```

> If the command above fails that mean the database is not ready yet. Wait a few seconds and retry. A new database will take about 1 min to start, it is a 3 nodes cluster.

<!-- NAVIGATION -->
<div id="navigation-bottom" class="navigation-bottom">
 <a href='command:katapod.loadPage?[{"step":"intro"}]'
   class="btn btn-dark navigation-bottom-left">⬅️ Back
 </a>
 <a href='command:katapod.loadPage?[{"step":"step2"}]'
    class="btn btn-dark navigation-bottom-right">Next ➡️
  </a>
</div>

