.. \_admin\_multitenants:

Management of tenants
====================

This section contains steps required to add a new :ref:`tenant <tenant>` and an overview of Platform tenant controls. The tenants page is the first screen you see when you login into the Platform.

Adding a new tenant
-------------------------

.. attention::

	Only System Owner can add a new tenant.

	You need to create a tenant to be able to add to it :ref:`new_workspace <new_workspace>` and PostgreSQL :ref:`instances <instance_adding`.

To add a new tenant:

\#. On the tenants page, click 'Add Tenant'.

	.. thumbnail:: ../_static/tenants/add_tenant.png

\#. In the opened modal window, select OperDB from the list, enter the name of the tenant in the 'Tenant Name' field, and click 'Create'.

	.. thumbnail:: ../_static/tenants/new_tenant.png
		:width: 300
		:align: center


After performing the specified steps, a new line with a tenant will appear on the page, within which you can create workspaces.

Tenant controls
-----------------------------

Let 's look through the controls in accordance with the numbering in the picture below:

.. thumbnail:: ../\_static/tenants/tenants\_panel.png

1. Search field to search for tenants by name.
2. Gear icon, using which you can fix, delete or change the positions of columns in the table.

	.. thumbnail:: ../\_static/tenants/tenants\_list\_setting.png :width: 300 :align: center

3. Information on the tenants:

	* 'Tenant name' - the name of the tenant.
	* 'Workspaces' - the number of workspaces within the tenant.
	* 'Clusters' - the number of clusters within the tenant.
	* 'Instances' - the number of instances within the tenant.
	* 'Alerts' - the number of alerts received for the tenant.
	* 'Failed tasks' - the number of tasks created on the tenant that failed.

4. Tenant menu with the following options:

	* 'Open tenant' - opens the page with workspaces of the tenant. On the 'instances' tab of this page, you can view all instances of the working spaces of the tenant.
	* 'Rename tenant' - opens a modal window for renaming the tenant. Enter the new name for the tenant in the text field and click 'Save'.

		.. thumbnail:: ../\_static/tenants/tenants\_rename.png :width: 300 :align: center


	* 'More information' - opens a page with expanded information on the tenant.
	* 'Delete tenant' - opens a modal window to delete a tenant. Enter 'delete' in the text field and click 'Delete'.

		.. thumbnail:: ../\_static/tenants/tenants\_delete.png :width: 300 :align: center

		.. note::

			Before deleting a tenant, delete all workspaces in it. You cannot delete a tenant containing working spaces.

			.. thumbnail:: ../_static/tenants/tenants_warning.png
				:width: 300
				:align: center

.. \_tenants\_info:

Page with more information on the tenant
-----------------------------------------

On the more information page you can manage user access rights for the tenant.

Let 's review the information on the page:

.. thumbnail:: ../\_static/tenants/info.png

1. Additional information on the tenant:

	* number of tenants owners;
	* number of local groups created within the tenant;
	* number of external groups synchronized with the tenant;
	* number of local users of the tenant;
	* number of external users of the tenant.

2. Search field to search for owners of tenants by name or email.
3. Button for adding Tenant Owner, which when clicked opens a modal window for adding Tenant Owner.

	.. thumbnail:: ../\_static/tenants/new\_owner.png :width: 350 :align: center

	To add a new owner, go through the following steps:

		* Fill in the username of the user who will be granted the Tenant Owner rights.
		* Fill in the user 's email.
		* Fill in the email again.
		* Click 'Add owner'.

4. List of tenants and information on them:

	* Tenant Owner name;
	* Tenant Owner email;
	* date and time of issuing Tennant Owner rights to the user.
	* email of the user who granted Owner rights for the Tenant.
	* date and time of the user 's last login to the tenant.

5. Owner 's menu has two options:

	* 'Revoke rights' to remove a user from the list of tenants ' owners. To do this, enter 'revoke' in the text field of the opened modal window and click 'Revoke rights'.

		.. thumbnail:: ../\_static/tenants/delete\_owner.png :width: 350 :align: center

		.. note::
	
			If you revoke the rights from the user, he will only be removed from the list of owners of the tenant, but will retain the user rights. He will be able to enter the tenant, but will only see the workspaces to which he has access.

			If you need to remove a user from the tenant, do the following:

				* select 'Revoke Rights' in the Owner menu;
				* go to the :ref:`list of users <users_common>` of the tenant and :ref:`deactivate  <users_deactivation>` the user;
				* :ref:`delete  <users_delete>` user.

	* 'Refresh password' to reset the old Owner password and automatically generate a new one or choose your own new password.

		* To automatically generate a password, click 'Reset'.

		.. thumbnail:: ../\_static/tenants/reset\_password\_1.png :width: 300 :align: center

		* To create a new password manually, uncheck 'Automatically generate password' box, enter a new password, and click 'Reset'.

		.. thumbnail:: ../\_static/tenants/reset\_password\_2.png :width: 300 :align: center