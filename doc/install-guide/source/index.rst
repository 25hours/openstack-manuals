.. title:: OpenStack Installation Guide

.. Don't remove or change title tag manually, which is used by the build tool.

.. Be aware that index-debian and index need to have the same content
   so that translations work. Only the strings from the file
   index-debian gets send to our translation server.

.. only:: rdo

   =============================================================================
   OpenStack Installation Guide for Red Hat Enterprise Linux, CentOS, and Fedora
   =============================================================================

.. only:: obs

   ===================================================================
   OpenStack Installation Guide for openSUSE and SUSE Linux Enterprise
   ===================================================================

.. only:: ubuntu

   =======================================
   OpenStack Installation Guide for Ubuntu
   =======================================

.. only:: debian

   =======================================
   OpenStack Installation Guide for Debian
   =======================================


Abstract
~~~~~~~~

The OpenStack system consists of several key projects that you install
separately. These projects work together depending on your cloud
needs. These projects include Compute, Identity Service, Networking,
Image Service, Block Storage, Object Storage, Telemetry,
Orchestration, and Database. You can install any of these projects
separately and configure them stand-alone or as connected entities.

.. only:: rdo

   This guide shows you how to install OpenStack by using packages
   available through Fedora 22 as well as on Red Hat Enterprise Linux
   7 and its derivatives through the EPEL repository.

.. only:: ubuntu

   This guide walks through an installation by using packages
   available through Canonical's Ubuntu Cloud archive repository.

.. only:: obs

   This guide shows you how to install OpenStack by using packages on
   openSUSE 13.2 and SUSE Linux Enterprise Server 12 through the Open
   Build Service Cloud repository.

.. only:: debian

   This guide walks through an installation by using packages
   available through Debian 8 (code name: Jessie).

Explanations of configuration options and sample configuration files
are included.

This guide documents OpenStack Liberty release.

.. warning:: This guide is a work-in-progress and changing rapidly
   while we continue to test and enhance the guidance. Please note
   where there are open "to do" items and help where you are able.

Contents
~~~~~~~~

.. toctree::
   :maxdepth: 2

   common/conventions.rst
   overview.rst
   environment.rst
   keystone.rst
   glance.rst
   nova.rst
   neutron.rst
   horizon.rst
   cinder.rst
   swift.rst
   heat.rst
   ceilometer.rst
   launch-instance.rst
   app_reserved_uids.rst

   common/app_support.rst
   common/glossary.rst

Search in this guide
~~~~~~~~~~~~~~~~~~~~

* :ref:`search`
