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

<ul>
  <li>Sign in (or sign up) to your Astra account at <a href="https://astra.datastax.com" target="_blank">astra.datastax.com</a></li>
  <li>Create an application token by following <a href="https://awesome-astra.github.io/docs/pages/astra/create-token/" target="_blank">these instructions</a></li>
</ul>

You can reuse the same token in our other scenarios, too.

✅ Setup Astra CLI by providing your application token:
```
astra setup
```

✅ List your existing Astra DB databases:
```
astra db list
```

✅ Create database `data-modeling` and keyspace `sensor_data` if they do not exist:
```
astra db create data-modeling -k sensor_data --if-not-exist
```

✅ Check the status of database `data-modeling`:
```
astra db get data-modeling
```

✅ If database `data-modeling` exists and has status `HIBERNATED`, resume the database:
```
astra db resume data-modeling
```

✅ If database `data-modeling` has status `RESUMING` or `PENDING`, **wait until the status becomes `ACTIVE`**:
```
astra db get data-modeling
```

✅ Start the CQL shell and connect to database `data-modeling` and keyspace `sensor_data`:

```
clear
astra db cqlsh data-modeling -k sensor_data
```

If the command fails, please revisit the previous steps to make sure that the database exists and is `ACTIVE`, and retry connecting to the database again.

<!-- NAVIGATION -->
<div id="navigation-bottom" class="navigation-bottom">
 <a href='command:katapod.loadPage?[{"step":"intro"}]'
   class="btn btn-dark navigation-bottom-left">⬅️ Back
 </a>
 <a href='command:katapod.loadPage?[{"step":"step2"}]'
    class="btn btn-dark navigation-bottom-right">Next ➡️
  </a>
</div>

