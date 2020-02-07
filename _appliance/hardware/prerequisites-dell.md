---
title: [Prerequisites]
summary: "Complete these prerequisites to deploy ThoughtSpot on your Dell appliance."
last_updated: 2/4/2020
sidebar: mydoc_sidebar
permalink: /:collection/:path.html
---
## Installation prerequisites
Ensure that you have the following items, information, and understanding of policies before you begin installing your Dell 6420 appliance.

<table>
<tr>
<td>&#10063;</td>
<td>10gbE switch with IPv6 broadcast and multicast enabled. You need one switch for each cluster, with one port for each node on the cluster.</td></tr>

<tr>
<td>&#10063;</td>
<td>Data center with proper environment controls, such as cooling.</td></tr>

<tr>
<td>&#10063;</td>
<td>AC power</td></tr>

<tr>
<td>&#10063;</td>
<td>10G connection: SFP+ for the switch side</td></tr>

<tr>
<td>&#10063;</td>
<td>10GbE network cables, either direct attach copper (DAC) or fiber. See <a href="cable-networking.html">Cable Reference</a> for more information to decide between the two types.</td></tr>

<tr>
<td>&#10063;</td>
<td>100Mbps or 1Gbps switch for connection to the iDRAC (Out of Band Management) port. You need one for each node in your cluster.</td></tr>

<tr>
<td>&#10063;</td>
<td>Cat5 network cables, for iDRAC/ management port use. You need one for each node.</td></tr>

<tr>
<td>&#10063;</td>
<td>Rack space of 2U or 3.5 inches for each appliance, and a power strip</td></tr>

<tr>
<td>&#10063;</td>
<td>VGA Monitor and USB keyboard</td></tr>

<tr>
<td>&#10063;</td>
<td>Networking information: IP addresses for data & management NICs, for up to 2 DNS servers, up to 4 NTP servers and for the default gateway. Ensure that you only configure two DNS servers. ThoughtSpot does not support configuration of three DNS servers. You also need to know the timezone for your cluster. Typically, your timezone is where most of the people who will use the product are. <a href="{{ site.baseurl }}/site-survey.pdf" download>Download</a> and fill out the ThoughtSpot site survey so that you have a quick reference. Contact your network administrator if you need help filling out the site survey. </td></tr></table>

## Review hardware requirements
Next, [review hardware requirements.]({{ site.baseurl }}/appliance/hardware/hardware-requirements-dell.html)