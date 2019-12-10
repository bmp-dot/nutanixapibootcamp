.. _api_update_vm:

----------------------
API: Update VM
----------------------

Overview
++++++++

.. note::

  Estimated time to complete: **30 MINUTES**

Words there

Lab Setup
+++++++++
Exercise 4: Update your VM to mount an ISO and power on
++++++++++++++++++++
1. Click + in the main window to create a new tab-window
2. Click the dropdown and select PUT
 - v3 uses PUT to allow the declaration of a spec that describes the new desired final state
3. Enter the URL to update your VM
 - Copy the URL used in the second exercise: https://{{prism_central_ip}}:9440/api/nutanix/v3/vms/{{uuid}}
 - Replace {{prism_central_ip}} with the IP address mentioned in the lab handout

 .. figure:: images/updatevm.png

 4. Configure basic authentication for this API call
  - Follow the same steps from exercise 1
  - v3 conforms to HTTP as a stateless protocol such that each API call is authenticated
5. Set the media type to application/json
 - Follow the same step 5 from **exercise 1**
6. Fill out the body
 - Click on the tab for **exercise 2** where you retrieved the status of your VM
 - Copy the entire response
 - Click on the right-most tab for this exercise to update your VM
 - Paste the response from the GET as the body for the PUT
 - Only delete the status object from the body and keep the spec and metadata section.

  .. figure:: images/deletestatus.png

7. Adjust the body to mount an ISO and power on
 - Change the power_state attribute from OFF to ON
 - Add a comma, enter a newline, and then copy or type the following disk list into the spec

.. code-block:: bash

   "disk_list": [{
           "device_properties": {
               "disk_address": {
                   "device_index": 0,
                   "adapter_type": "IDE"
               },
               "device_type": "CDROM"
           },
           "data_source_reference": {
               "kind": "image",
               "uuid": "{{uuid}}"
           }
       }]

- Replace {{uuid}} with the uuid of the Ubuntu image from **exercise 3**



Takeaways
+++++++++
