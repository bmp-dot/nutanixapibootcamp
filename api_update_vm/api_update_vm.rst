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

Takeaways
+++++++++
