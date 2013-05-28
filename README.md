opends_cacti_graphs
===================

A LDAP Cacti Graphs created by Clément, located here: http://ltb-project.org/wiki/documentation#monitoring, adapted for OpenDS

Looking at the ltp-project-cacti-plugins download from the LTB Project, the files "cacti_graph_template_initiated_operations_opends.xml" and "opends_operations.pl" correspond to Clément's "cacti_graph_template_response_time" and "openldap_operations.pl", but are updated to work correctly with OpenDS.

The biggest difference lies in that OpenDS (at least under OpenDJ) keeps this information in its own set of "ds-mon-XXXXXX-operations-total-count" instead of the Initiated/Completed pair in OpenLDAP.  I actually chose to place the completed value in both Initiated and Completed in the graph so that I would have to do less as far as modifying the XML for now.

Probably it should be re-written, but my job was to get it working, so that's all I've really done ;)

Here is Clément's very straight-forward how-to for installing these scripts, and it works fine with my code:

http://ltb-project.org/wiki/documentation/cacti-plugins/openldap_operations

On a side note, Clément has also written another plugin for basic response time, which works equally well, unmodified, for OpenDS and OpenLDAP:

http://ltb-project.org/wiki/documentation/cacti-plugins/ldap_response_time

NOTE: These templates likely cannot be run side-by-side with the original code by Clément, as I did not change any of the UUIDs for the graphs and they would clash.

