.. _api_image_list:

----------------------
API: List of Images
----------------------

Overview
++++++++

.. note::

  Estimated time to complete: **30 MINUTES**

Words there

Lab Setup
+++++++++

Exercise 3: List the images on the cluster
+++++++++++++++++++++++++++++++++++++++++++

#. Click + in the main window to create a new tab-window

#. Click the dropdown and select POST
 - v3 standardizes on POST for listing to offer server-side filtering, grouping, and sorting

#. Enter the URL to list images
 - https://{{prism_central_ip}}:9440/api/nutanix/v3/images/list

#. Configure basic authentication for this API call

 - Follow the same steps from the first exercise
 - v3 conforms to HTTP as a stateless protocol such that each API call is authenticated

#. Set the media type to application/json

 - Follow the same steps 5 from the first exercise

#. Fill out the body

 - Click the Body tab
 - Copy or type an empty dictionary in the json body

.. code-block:: bash

  {}

.. figure:: images/apimetajson.png

#. Click Send to submit the v3 API call

 - The intent response provides an array of image resources, similar to GET on one entity
 - Note the uuid of the Ubuntu 16.10 Desktop image in the metadata section

 .. figure:: images/imageuuid.png





Takeaways
+++++++++

- Nathan is Super cool
