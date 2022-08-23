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

<div class="step-title">Create Astra Database</div>

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

Configure the shell and initialize the cli with `astra-setup`

```
source /home/gitpod/.astra/cli/astra-init.sh
unset JAVA_TOOL_OPTIONS
astra setup
```

- Copy paste your Astra token as show below.

![](https://github.com/datastax/astra-sdk-java/blob/main/docs/img/astra-shell-config.png?raw=true")

Ok you are good the CLI should work now 

```
clear
astra --version
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
<br/>
