.. \_ldap:

External authentication
======================

.. contents:: :depth: 3 :local:

This page describes how to manage the integration of Platform and Active Directory/FreeIPA/ALD pro servers in a single LDAP profile.

To use the LDAP functionality, in the left panel, click 'Tenant Configuration' -> 'External Authentication'.

.. thumbnail:: ../\_static/image226.png :width: 400 :align: center

The LDAP tab of the 'External Authentication' page will open.

.. thumbnail:: ../\_static/image227.png
   
Connection to LDAP and profile setup
--------------------------------------

.. attention:: The client of the company is responsible for the secure configuration of LDAP and the setup of a secure connection.

Below are the options for connecting to the following directory services:

	* :ref:`Active Directory (AD) <active_directory>`,
	* :ref:`FreeIPA <freeipa>`,
	* :ref:`ALD Pro <ald_pro>`.

.. \_active\_directory:

Active Directory (AD) ~~~~~~~~~~~~~~~~~~~~~

To connect to LDAP and configure a profile, perform the following steps:

**Step 1.**

* Specify the domain name or IP address of the domain controller, for example, '10.128.0.189'.
* Specify port - 389 for unsecured connection or 636 for secureв one.
* If required, check 'Secured connection'.

.. thumbnail:: ../\_static/image228.png :width: 500 :align: center

**Step 2.**

* Specify the email address of the user under whose credentials the Platform will authenticate with LDAP, for example, 'serviceman@ad.tantorlabs.ru'.
* Enter the password for the user under whose credentials the Platform will authenticate with LDAP.

.. thumbnail:: ../\_static/image263.png :width: 500 :align: center

**Step 3.**

Set up searching for users and groups in LDAP.

	* the path to users, for example, 'cn=Users, dc=company,dc=com';
	* the path to groups, for example, 'cn=Users, dc=ad, dc=tantorlabs, dc=ru'.
	* search filter by groups, for example, '(&(objectClass=group)(cn=Tantor*))'.

.. thumbnail:: ../\_static/image264.png :width: 500 :align: center

**Step 4.**

Configure attribute comparison for user attributes in LDAP and the Tantor platform.

	* 'Login' of LDAP user parameter, for example, 'sAMAccountName';
	* 'Name' of LDAP user parameter, for example, 'givenName';
	* 'Last Name' of LDAP user parameter, for example, 'sn';
	* 'Email' of LDAP user parameter, for example, 'mail'.

.. thumbnail:: ../\_static/image265.png :width: 500 :align: center

.. important::

	The user will not be added if an empty/unfilled LDAP attribute is specified as the login.

After entering all parameters, a connection with the target server will be checked. Timeout to establish connection - 10 seconds. If the connection is successful, 'Confirm and Сomplete integration' button will be activated.

.. thumbnail:: ../\_static/image230.png :width: 500 :align: center

After clicking this button, users will be loaded.

.. thumbnail:: ../\_static/users\_loading.png :width: 500 :align: center

Upon successful integration with LDAP, additional users from AD/FreeIPA/ALD pro, who are not associated with internal users and groups, will appear in the list of groups and users.

.. \_freeipa:

FreeIPA ~~~~~~~

To connect to LDAP and configure a profile, perform the following steps:

**Step 1.**

* Specify the domain name or IP address of the domain controller, for example, 'freeipa.tantorlabs.ru'.
* Specify port - 389 for unsecured connection or 636 for secureв one.
* If required, check 'Secured connection'.

.. thumbnail:: ../\_static/freeipa1.png :width: 500 :align: center

**Step 2.**

* Specify the username under whose credentials the Platform will authenticate with LDAP.
* Enter the password for the user under whose credentials the Platform will authenticate with LDAP.

.. thumbnail:: ../\_static/freeipa2.png :width: 500 :align: center

**Step 3.**

Set up searching for users and groups in LDAP.

	* the path to users, for example, 'cn=users,cn=accounts,dc=freeipa,dc=tantorlabs,dc=ru';
	* the path to groups, for example, 'cn=groups,cn=accounts,dc=freeipa,dc=tantorlabs,dc=ru';
	* search filter by groups, for example, '<<(cn=*)>>'.

.. thumbnail:: ../\_static/freeipa3.png :width: 500 :align: center

**Step 4.**

Configure attribute comparison for user attributes in LDAP and the Tantor platform.

	 * 'Login' of LDAP user parameter, for example, 'krbPrincipalName';
	* 'Name' of LDAP user parameter, for example, 'givenName';
	* 'Last Name' of LDAP user parameter, for example, 'sn';
	* 'Email' of LDAP user parameter, for example, 'mail'.

.. thumbnail:: ../\_static/freeipa\_aldpro\_4.png :width: 500 :align: center

.. important::

	The user will not be added if an empty/unfilled LDAP attribute is specified as the login.

After entering all parameters, a connection with the target server will be checked. Timeout to establish connection - 10 seconds. If the connection is successful, 'Confirm and Сomplete integration' button will be activated.

.. thumbnail:: ../\_static/image230.png :width: 500 :align: center

After clicking this button, users will be loaded.

.. thumbnail:: ../\_static/users\_loading.png :width: 500 :align: center

Upon successful integration with LDAP, additional users from AD/FreeIPA/ALD pro, who are not associated with internal users and groups, will appear in the list of groups and users.

.. \_ald\_pro:

ALD Pro ~~~~~~~

To connect to LDAP and configure a profile, perform the following steps:

**Step 1.**

* Specify the domain name or IP address of the domain controller, for example, 'master-01.aldpro.tantorlabs.ru'.
* Specify port - 389 for unsecured connection or 636 for secureв one.
* If required, check 'Secured connection'.

.. thumbnail:: ../\_static/ald\_pro1.png :width: 500 :align: center

**Step 2.**

* Specify the username under whose credentials the Platform will authenticate with LDAP.
* Enter the password for the user under whose credentials the Platform will authenticate with LDAP.

.. thumbnail:: ../\_static/freeipa\_aldpro\_2.png :width: 500 :align: center

**Step 3.**

* Set up searching for users and groups in LDAP.

	* path to users, for example, 'cn=users,cn=accounts,dc=aldpro,dc=tantorlabs,dc=ru';
	* path to groups, for example, 'cn=groups,cn=accounts,dc=aldpro,dc=tantorlabs,dc=ru';
	* search filter for groups, for example, ''(cn=\*)''.

.. thumbnail:: ../\_static/ald\_pro3.png :width: 500 :align: center

**Step 4.**

* Configure attribute comparison for user attributes in LDAP and the Tantor platform.

	*  'Login' for LDAP user parameter, for example, 'krbPrincipalName';
	* 'Name' for LDAP user parameter, for example, 'givenName';
	* 'Surname' for LDAP user, for example, 'sn';
	*  'Email' for LDAP user parameter, for example, 'mail'.

.. thumbnail:: ../\_static/freeipa\_aldpro\_4.png :width: 500 :align: center

.. important::

	The user will not be added if an empty/unfilled LDAP attribute is specified as the login.

After entering all parameters, a connection with the target server will be checked. Timeout to establish connection - 10 seconds. If the connection is successful, 'Confirm and Сomplete integration' button will be activated.

.. thumbnail:: ../\_static/image230.png :width: 500 :align: center

After clicking this button, users will be loaded.

.. thumbnail:: ../\_static/users\_loading.png :width: 500 :align: center

Upon successful integration with LDAP, additional users from AD/FreeIPA/ALD pro, who are not associated with internal users and groups, will appear in the list of groups and users.

Changing connection or profile configuration
--------------------------------------

To change the connection or other profile parameters, click 'Change' in the top right corner.

.. thumbnail:: ../\_static/image231.png

LDAP integration removal
------------------------

To remove LDAP integration, click 'Remove' in the top right corner.

.. thumbnail:: ../\_static/delete\_ldap.png

Enter 'remove' in the text field and click 'Remove'.

.. thumbnail:: ../\_static/image232.png :width: 300 :align: center

LDAP users groups
-------------------------

To open the users groups page, click 'Tenant Configuration' in the left panel → 'Users and Groups' → 'Groups'.

.. thumbnail:: ../\_static/image233.png

On the users groups page, the 'Type' column shows which group users from identification catalogs are added to - 'External' group type, and which local users are added to - 'Local' group type.

.. thumbnail:: ../\_static/group\_type\_ldap.png

Click  group and go to 'Users' tab to open the list of group users.

.. thumbnail:: ../\_static/image239.png

.. attention:: On the 'Groups' page, you cannot edit the name and description of LDAP groups. Add and delete buttons for LDAP group on this page open the LDAP profile.