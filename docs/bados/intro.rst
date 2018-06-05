.. _getting-started:

Getting Started
===============

Please follow the instructions provided by the instructor to start your
lab and access your jump host.

.. NOTE::
	 All work for this lab will be performed exclusively from the Linux Workstation
	 jumphost. No installation or interaction with your local system is
	 required.

Lab Topology
^^^^^^^^^^^^^
|image1|


Lab Components
^^^^^^^^^^^^^^^

The following table lists VLANS, IP Addresses and Credentials for all
components:

.. list-table::
    :widths: 20 40 40
    :header-rows: 1
    :stub-columns: 1

    * - **Component**
      - **VLAN/IP Address(es)**
      - **Credentials**
    * - bigip01 
      - - **Management:** 10.1.1.245
        - **Internal:** 10.1.20.245
        - **External:** 10.1.10.245
      - ``admin``/``admin``
    * - bigip02 
      - - **Management:** 10.1.1.246
        - **Internal:** 10.1.20.246
        - **External:** 10.1.10.246
      - ``admin``/``admin`` 
    * - Ubuntu Linux Workstation
      - - **eth0:** 10.1.1.51
        - **eth1:** 10.1.10.51
      - ``f5student``/``f5DEMOs4u``
    * - Kali Linux Workstation
      - - **eth0:** 10.1.10.60
      - ``root``/``f5DEMOs4u``

Accessing Lab Environment
^^^^^^^^^^^^^^^^^^^^^^^^^^^
Please follow the instructions below to access the lab environment used for this lab.

1. Open a browser and go to `http://training.f5agililty.com/<lab
       number>/X <http://training.f5agililty.com/%3clab%20number%3e/X>`__
       (where **X** is your student number)

    a. Look for the **xubuntu-jumpbox-vxx**. You will use the |xj| for all the labs. (see below)

        |image2|

    b. You can click on **RDP** to RDP to the |xj|, or you can select the **CONSOLE** link and access the jumpbox via your browser.  **The CONSOLE link requires you turn off pop-up blockers.**

        |image3|


F5 BIG-IP Base Configuration Steps
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Complete the following steps to get you F5 BIG-IP's configured and ready to complete remaining lab steps.

..TODO::should we just do this advance?

1. Open the Chrome browser and log into the |bip| GUI to verify the
   |bip| is up.

   a. Go to **https://10.1.1.245**

      i.  User: **admin**

      ii. Password: **admin**

2. Now you will perform an initial configuration via command line.

   a. Open a terminal window from the taskbar at the bottom.

      i.   Log in to the |bip| using the command: **ssh
           root@10.1.1.245**

      ii.  The password is **default.**

      iii. At the |bip| prompt, enter **tmsh**

           1. This will place you in the |bip| command line mode.

   b. In your browser, open then the **Lab Guides** link on the
      bookmarks bar in a new tab/window.

   c. Open the **AdvWAF Base Setup.txt** file and review the commands.

   d. Copy all the commands between **# BEGIN COPY - Lab prep** and **#
      END COPY - Lab prep**

   e. Paste the commands into the terminal window at the **tmsh**
      prompt.

   f. The BIG-IP will take several minutes to come back online.

3. Verify the |bip| virtual server and web site are up and running.

   a. Go to **Local Traffic >> Network Map**. There should be two
      virtual servers, and both should be available (green).

   b. Open up the Firefox browser. Go to http://hackazon.f5demo.com and
      https://hackazon.f5demo.com


.. |image1| image:: _images/image2.png
   :width: 6.59740in
   :height: 6.73203in
.. |image2| image:: _images/image3.png
   :width: 3.77500in
   :height: 2.87104in
.. |image3| image:: _images/image4.png
   :width: 3.36587in
   :height: 3.04167in


