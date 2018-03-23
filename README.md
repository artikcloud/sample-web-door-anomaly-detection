# ARTIK Cloud Door Anomaly Detection Sample

This is an interactive web sample to detect lock anomaly using the ARTIK Cloud [Machine Learning API for Anomaly Detection](https://developer.artik.cloud/documentation/api-reference/rest-api.html#machine-learning).    The sample will assist in prepopulating training data to the device and walk through setup anomaly detection in the Rule Engine.

##### **Prerequisites**

* You should already be familar ARTIK Cloud platform like [Creating Device Types](https://developer.artik.cloud/documentation/getting-started/devices.html#create-a-device-type) , adding devices into your account, retrieving the device ID and device Token, and using the Rule Engine.
* We will use python to run the build-in web container and run the sample locally on `http://localhost:8000`.   

### Setup / Installation

  1. [Create a new device type](https://developer.artik.cloud/documentation/getting-started/devices.html#create-a-device-type) for this sample.   To facilitate setting up the manifest, upload the `virtual-lock-manifest.json` file after creating.
  2. Add a device (of above Device Type) into your account and retrieve the **device ID** and **device token**.   Click "GENERATE DEVICE TOKEN…" to get one.

### 1. Run Sample 

We will use the built-in web server in python.   

The following command will start startup a local server running on port 8000.

```
%> python -m SimpleHTTPServer 8000
Serving HTTP on 0.0.0.0 port 8000 ...
```

Then browser to the following link http://localhost:8000 using your favorite web browser.   

The tutorial is self contained and you can follow the remaining instructions.  For convenience, we'll provide outline of some steps below.

### 2. Setup Lock Device  

The remaining sections here refer to the sample web application.

Go to the "Setup a lock device" section and enter the device ID and device Token and click **Save**.

### 3. Feed Training Data  

Click on the "Generate data" button.   This will feed 1 month of past data with locked and unlocked events to the device.  

### 4. Setup Anomaly Detection Rule
Go to the [Rule Engine](my.artik.cloud) dashboard to setup an anomaly rule.   Detailed instructions are also provided in the web application if you need help here.

Here we are creating a Rule if an anomaly is detected.

### 5. Simulate sending a new Lock or Unlock event 

In the <u>send regular data section</u> of the web application, click on the Lock or Unlock button to simulate sending new event.   If the rule detects an anomaly based on the trained past data, it will trigger the Rule you created in the previous step (Anomaly Detection Rule).



More about ARTIK Cloud
---------------

If you are not familiar with ARTIK Cloud, we have extensive documentation at https://developer.artik.cloud/documentation

The full ARTIK Cloud API specification can be found at https://developer.artik.cloud/documentation/api-reference/

Peek into advanced sample applications at https://developer.artik.cloud/documentation/samples/

To create and manage your services and devices on ARTIK Cloud, visit the Developer Dashboard at https://developer.artik.cloud

License and Copyright
---------------------

Licensed under the Apache License. See [LICENSE](LICENSE).

Copyright (c) 2016 Samsung Electronics Co., Ltd.
