=========================
Choosing server hardware
=========================

Consider the following factors when selecting compute (server) hardware:

* Server density
   A measure of how many servers can fit into a given measure of
   physical space, such as a rack unit [U].

* Resource capacity
   The number of CPU cores, how much RAM, or how much storage a given
   server delivers.

* Expandability
   The number of additional resources you can add to a server before it
   reaches capacity.

* Cost
   The relative cost of the hardware weighed against the level of
   design effort needed to build the system.


Compute (server) hardware selection
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Weigh these considerations against each other to determine the best
design for the desired purpose. For example, increasing server density
means sacrificing resource capacity or expandability. Increasing resource
capacity and expandability can increase cost but decrease server density.
Decreasing cost often means decreasing supportability, server density,
resource capacity, and expandability.

Compute capacity (CPU cores and RAM capacity) is a secondary
consideration for selecting server hardware. The required
server hardware must supply adequate CPU sockets, additional CPU cores,
and more RAM. Network connectivity and storage capacity are not as
critical. Your hardware will need to provide enough network connectivity and
storage capacity to meet the user requirements.

For a compute-focused cloud, emphasis should be on server
hardware that can offer more CPU sockets, more CPU cores, and more RAM.
Network connectivity and storage capacity are less critical.

When designing a OpenStack cloud architecture, you must
consider whether you intend to scale up or scale out. Selecting a
smaller number of larger hosts, or a larger number of smaller hosts,
depends on a combination of factors: cost, power, cooling, physical rack
and floor space, support-warranty, and manageability.

Consider the following in selecting server hardware form factor suited for
your OpenStack design architecture:

* Most blade servers can support dual-socket multi-core CPUs. To avoid
  this CPU limit, select ``full width`` or ``full height`` blades. Be
  aware, however, that this also decreases server density. For example,
  high density blade servers such as HP BladeSystem or Dell PowerEdge
  M1000e support up to 16 servers in only ten rack units. Using
  half-height blades is twice as dense as using full-height blades,
  which results in only eight servers per ten rack units.

* 1U rack-mounted servers have the ability to offer greater server density
  than a blade server solution, but are often limited to dual-socket,
  multi-core CPU configurations. It is possible to place forty 1U servers
  in a rack, providing space for the top of rack (ToR) switches, compared
  to 32 full width blade servers.

  To obtain greater than dual-socket support in a 1U rack-mount form
  factor, customers need to buy their systems from Original Design
  Manufacturers (ODMs) or second-tier manufacturers.

  .. warning::

     This may cause issues for organizations that have preferred
     vendor policies or concerns with support and hardware warranties
     of non-tier 1 vendors.

* 2U rack-mounted servers provide quad-socket, multi-core CPU support,
  but with a corresponding decrease in server density (half the density
  that 1U rack-mounted servers offer).

* Larger rack-mounted servers, such as 4U servers, often provide even
  greater CPU capacity, commonly supporting four or even eight CPU
  sockets. These servers have greater expandability, but such servers
  have much lower server density and are often more expensive.

* ``Sled servers`` are rack-mounted servers that support multiple
  independent servers in a single 2U or 3U enclosure. These deliver
  higher density as compared to typical 1U or 2U rack-mounted servers.
  For example, many sled servers offer four independent dual-socket
  nodes in 2U for a total of eight CPU sockets in 2U.

Other factors that influence server hardware selection for an OpenStack
design architecture include:

Instance density
 More hosts are required to support the anticipated scale
 if the design architecture uses dual-socket hardware designs.

 For a general purpose OpenStack cloud, sizing is an important consideration.
 The expected or anticipated number of instances that each hypervisor can
 host is a common meter used in sizing the deployment. The selected server
 hardware needs to support the expected or anticipated instance density.

Host density
 Another option to address the higher host count is to use a
 quad-socket platform. Taking this approach decreases host density
 which also increases rack count. This configuration affects the
 number of power connections and also impacts network and cooling
 requirements.

 Physical data centers have limited physical space, power, and
 cooling. The number of hosts (or hypervisors) that can be fitted
 into a given metric (rack, rack unit, or floor tile) is another
 important method of sizing. Floor weight is an often overlooked
 consideration. The data center floor must be able to support the
 weight of the proposed number of hosts within a rack or set of
 racks. These factors need to be applied as part of the host density
 calculation and server hardware selection.

Power and cooling density
 The power and cooling density requirements might be lower than with
 blade, sled, or 1U server designs due to lower host density (by
 using 2U, 3U or even 4U server designs). For data centers with older
 infrastructure, this might be a desirable feature.

 Data centers have a specified amount of power fed to a given rack or
 set of racks. Older data centers may have a power density as power
 as low as 20 AMPs per rack, while more recent data centers can be
 architected to support power densities as high as 120 AMP per rack.
 The selected server hardware must take power density into account.

Specific hardware concepts
~~~~~~~~~~~~~~~~~~~~~~~~~~

Consider the following in selecting server hardware form factor suited for
your OpenStack design architecture:

* Most blade servers can support dual-socket multi-core CPUs. To avoid
  this CPU limit, select ``full width`` or ``full height`` blades. Be
  aware, however, that this also decreases server density. For example,
  high density blade servers such as HP BladeSystem or Dell PowerEdge
  M1000e support up to 16 servers in only ten rack units. Using
  half-height blades is twice as dense as using full-height blades,
  which results in only eight servers per ten rack units.

* 1U rack-mounted servers have the ability to offer greater server density
  than a blade server solution, but are often limited to dual-socket,
  multi-core CPU configurations. It is possible to place forty 1U servers
  in a rack, providing space for the top of rack (ToR) switches, compared
  to 32 full width blade servers.

  To obtain greater than dual-socket support in a 1U rack-mount form
  factor, customers need to buy their systems from Original Design
  Manufacturers (ODMs) or second-tier manufacturers.

  .. warning::

     This may cause issues for organizations that have preferred
     vendor policies or concerns with support and hardware warranties
     of non-tier 1 vendors.

* 2U rack-mounted servers provide quad-socket, multi-core CPU support,
  but with a corresponding decrease in server density (half the density
  that 1U rack-mounted servers offer).

* Larger rack-mounted servers, such as 4U servers, often provide even
  greater CPU capacity, commonly supporting four or even eight CPU
  sockets. These servers have greater expandability, but such servers
  have much lower server density and are often more expensive.

* ``Sled servers`` are rack-mounted servers that support multiple
  independent servers in a single 2U or 3U enclosure. These deliver
  higher density as compared to typical 1U or 2U rack-mounted servers.
  For example, many sled servers offer four independent dual-socket
  nodes in 2U for a total of eight CPU sockets in 2U.
