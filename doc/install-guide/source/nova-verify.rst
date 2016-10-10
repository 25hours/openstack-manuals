Verify operation
~~~~~~~~~~~~~~~~

Verify operation of the Compute service.

.. note::

   Perform these commands on the controller node.

#. Source the ``admin`` credentials to gain access to
   admin-only CLI commands:

   .. code-block:: console

      $ . admin-openrc

#. List service components to verify successful launch and
   registration of each process:

   .. code-block:: console

      $ openstack compute service list
      +----+--------------------+------------+----------+---------+-------+----------------------------+
      | Id | Binary             | Host       | Zone     | Status  | State | Updated At                 |
      +----+--------------------+------------+----------+---------+-------+----------------------------+
      |  1 | nova-consoleauth   | controller | internal | enabled | up    | 2016-02-09T23:11:15.000000 |
      |  2 | nova-scheduler     | controller | internal | enabled | up    | 2016-02-09T23:11:15.000000 |
      |  3 | nova-conductor     | controller | internal | enabled | up    | 2016-02-09T23:11:16.000000 |
      |  4 | nova-compute       | compute1   | nova     | enabled | up    | 2016-02-09T23:11:20.000000 |
      +----+--------------------+------------+----------+---------+-------+----------------------------+

   .. note::

      This output should indicate three service components enabled on
      the controller node and one service component enabled on the
      compute node.

#. List API endpoints in the Identity service to verify connectivity
   with the Identity service:

   .. note::

      Below endpoints list may differ depending on the installation of OpenStack components.

   .. code-block:: console

      $ openstack catalog list
      +---------------+---------------+---------------------------------------------------------------------------------+
      | Name          | Type          | Endpoints                                                                       |
      +---------------+---------------+---------------------------------------------------------------------------------+
      | nova          | compute       | RegionOne                                                                       |
      |               |               |   publicURL: http://controller:8774/v2/ae7a98326b9c455588edd2656d723b9d         |
      |               |               |   internalURL: http://controller:8774/v2/ae7a98326b9c455588edd2656d723b9d       |
      |               |               |   adminURL: http://controller:8774/v2/ae7a98326b9c455588edd2656d723b9d          |
      |               |               |                                                                                 |
      | glance        | image         | RegionOne                                                                       |
      |               |               |   publicURL: http://controller:9292                                             |
      |               |               |   internalURL: http://controller:9292                                           |
      |               |               |   adminURL: http://controller:9292                                              |
      |               |               |                                                                                 |
      | keystone      | identity      | RegionOne                                                                       |
      |               |               |   publicURL: http://controller:5000/v2.0                                        |
      |               |               |   internalURL: http://controller:5000/v2.0                                      |
      |               |               |   adminURL: http://controller:35357/v2.0                                        |
      |               |               |                                                                                 |
      +---------------+---------------+---------------------------------------------------------------------------------+

   .. note::

      Ignore any warnings in this output.

#. List images in the Image service to verify connectivity with the Image
   service:

   .. code-block:: console

      $ openstack image list
      +--------------------------------------+-------------+-------------+
      | ID                                   | Name        | Status      |
      +--------------------------------------+-------------+-------------+
      | 9a76d9f9-9620-4f2e-8c69-6c5691fae163 | cirros      | active      |
      +--------------------------------------+-------------+-------------+
