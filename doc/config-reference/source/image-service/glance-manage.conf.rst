==================
glance-manage.conf
==================

The Image service's custom logging options are found in the
``glance-manage.conf`` file.

.. note::

    Options set in ``glance-manage.conf`` will override options of the same
    section and name set in ``glance-registry.conf`` and ``glance-api.conf``.
    Similarly, options in ``glance-api.conf`` will override options set in
    ``glance-registry.conf``.

.. remote-code-block:: ini

   https://git.openstack.org/cgit/openstack/glance/plain/etc/glance-manage.conf?h=stable/mitaka
