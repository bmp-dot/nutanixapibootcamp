.. _api_cluster_list:

----------------------
1) API: List of Clusters
----------------------

Overview
++++++++

In this exercise you will list the clusters connected to Prism Central.  Later exercises
will require the cluster uuid in the JSON body.

.. note::

  Estimated time to complete: **5 MINUTES**



Exercise: List the clusters
+++++++++++++++++++++++++++++++++++++++++++

#. Click + in the main window to create a new tab-window

#. Click the dropdown and select POST

    - v3 standardizes on POST for listing to offer server-side filtering, grouping, and sorting

#. Enter the URL to list images

    - https://{{prism_central_ip}}:9440/api/nutanix/v3/clusters/list

#. Configure basic authentication for this API call

    - Follow the same steps from the first exercise
    - v3 conforms to HTTP as a stateless protocol such that each API call is authenticated

#. Set the media type to application/json

    - Follow the same steps 5 from the first exercise

#. Fill out the body

    - Click the Body tab
    - Copy or type an empty dictionary in the json body as seen below

    .. code-block:: bash

      {}

    .. figure:: images/apimetajson.png

#. Click Send to submit the v3 API call

  - The intent response provides an array of cluster resources
  - Take note of the cluster UUID under the metadata

  .. figure:: images/clusteruuid.png





Takeaways
+++++++++
