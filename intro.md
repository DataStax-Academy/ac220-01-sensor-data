<div class="top">
  <img src="https://datastax-academy.github.io/katapod-shared-assets/images/ds-academy-logo.svg" />
  <span style="position:absolute;top:20px;left:350px;font-size:30px"><b>Sensor Data Modeling</b></span>
  <span style="position:absolute;top:90px;left:350px;font-size:20px"><u>Difficulty:</u> <b>Beginner</b></span>
  <span style="position:absolute;top:60px;left:350px;font-size:20px"><u>Time :</u> <b>10min </b></span>
</div>

<main>
    <div class="container px-4 py-5">
    <h2 class="pb-2 border-bottom blue_900">Overview</h2>
   Explore how IoT sensor data can be stored and queried in Cassandra NoSQL database
     <div class="row g-4 py-5 row-cols-1 row-cols-lg-3">
          <div class="feature col div-choice">
            <b>In this scenario, you will:</b>
<li>Create tables for a sensor data use case 
<li>Populate tables with sample sensor data
<li>Design and execute CQL queries over sensor data
     </div>
    </div>
    <div class="container px-4 py-5" id="featured-2" >
        <h2 class="pb-2 border-bottom blue_900">🏁 Before Starting</h2>
        <p><br/>You can run the hands-on using either a local environment or a cloud service. Pick the one you like:</p>
        <div class="row g-4 py-5 row-cols-1 row-cols-lg-3">
          <div class="feature col div-choice">
            <div style="height:50px;">
              <img src="https://datastax-academy.github.io/katapod-shared-assets/images/logo-astradb.svg" height="30px"/>
            </div>
            <h2>Free Cloud DBaas Datastax Astra</h2>
            <p>Save installation time and reuse databases and data across scenarios. You need to sign up and create an account and generate a token. It is totally free and we will guide you.</p>
            <a href="command:katapod.loadPage?%5B%7B%22step%22%3A%22start-astra%22%7D%5D" class="btn btn-primary btn-astra">
              Run with ASTRA
            </a>
          </div>
          <div class="feature col div-choice">
            <div style="height:80px;margin-top:-30px">
                <img src="https://datastax-academy.github.io/katapod-shared-assets/images/logo-docker.png" height="80px"/>
            </div>
            <h2>Run Locally as a Docker container</h2>
            <p>Docker is already installed. After pulling the image and starting the container (~40s) you will have a full running Cassandra node locally.</p>
            <a href="command:katapod.loadPage?%5B%7B%22step%22%3A%22start-cassandra%22%7D%5D" class="btn btn-primary btn-astra" class="btn btn-primary" style="background-color:#024BA2;border:0px;float:right">
              Run with DOCKER
            </a>
            </center>
          </div>
        </div>
      </div>
      </main>







<div class="top">

# Sensor Data Modeling
## Explore how IoT sensor data can be stored and queried in Cassandra NoSQL database
</div>

<div><b>Difficulty</b>: Beginner</div>
<div><b>Time</b>: 15 minutes</div>
<div><b>Prerequisite</b>: <a href="https://www.datastax.com/learn/data-modeling-by-example/sensor-data-model" target="_blank">how to create a data model for temperature monitoring sensor networks</a></div>

**In this scenario, you will:**

* Create tables for a sensor data use case 
* Populate tables with sample sensor data
* Design and execute CQL queries over sensor data

_This scenario is also available on our [datastax.com/dev](https://www.datastax.com/dev) site, where you can find many more resources to help you succeed with Apache Cassandra™._

[start scenario](command:katapod.loadPage?step1){.orange_bar}
