Statistics Reporting
====================

In Allstar Linux you can enable reporting of Statistics of your installation to a remote source. By default this is disabled, and the example configuration sends the data to stats.allstarlink.org. However, this is not the only place you can send this information. You can configure Asterisk to send this to where ever you choose. For example, if you have a custom application that has an API endpoint for collecting these metrics, you can point Asterisk to that endpoint. From your API standpoint it will be a GET request. Generally the metrics you can collect are the Node Number, Total Transmissions, and Total Transmission Time. If you want to get deep in the weeds there are other metrics you can pull out from the body request that is sent over. For most users this is a deeper topic than needed to schieve their goal. 

Enabling Statistics Reporting
-----------------------------

1. SSH you your allstar Node
2. Using your favorite command line text editor (most folks use nano, I prefer vim), edit the rpt.conf file located at ``/etc/asterisk/rtp.conf``. 
3. Look for the following lines of code
   
.. code-block:: bash

    ; *** Status Reporting ***

    ; Uncomment either group following two statpost lines to report the status of your node to stats.allstarlink.org
    ; depending on whether you are running ACID, Debian or Limey Linux.
    ; The difference is simply where your wget is located.

    ; ** For ACID and Debian ***
    ;statpost_program = /usr/bin/wget,-q,--timeout=15,--tries=1,--output-document=/dev/null
    ;statpost_url = http://stats.allstarlink.org/uhandler.php ; Status updates

    ; ** For Limey Linux **
    ;statpost_program = /bin/wget,-q,--timeout=15,--tries=1,--output-document=/dev/null
    ;statpost_url = http://stats.allstarlink.org/uhandler.php ; Status updates

You want to uncomment the lines according to your system. For the ASL image you want to use the lines for Debian Linux. 


