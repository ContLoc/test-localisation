.. \_backup\_monitoring:

Backup Monitoring
==================

To display the list of backups, configure:ref: ` connection to the backup system <backup>`.

You can view the list of backups for a tenant, workspace, or specific instance. You can access  'Backup monitoring ' in different ways:

	#. In the left panel menu, select 'Modules' -> 'Backup Monitoring'. In this case, a list of tenant backups will be opened.

		.. thumbnail:: ../_static/backup/go_to_backup_monit_1.png

	#. On the workspaces page, click on  'Failed backups '. In this case, backups on the page will be sorted by working space and  'Failed ' status.

		.. thumbnail:: ../_static/backup/go_to_backup_monit_2.png

	#. In the instance menu, select  'Backup Monitoring '. In this case, a list of instance backups will be opened.

		.. thumbnail:: ../_static/backup/go_to_backup_monit_3.png

On  'Backup Monitoring ' page there is a list of backups, information on them, and controls:

.. thumbnail:: ../\_static/backup/backup\_monit\_info.png

\#. Search field to search for backups by FQDN. #. Update page button. #. Backups can be sorted by workspaces, instances, and statuses. #. Gear icon: 

	.. thumbnail:: ../_static/backup/backup_monit_setting.png
		:width: 300
		:align: center

	1. Using this button, you can change the position of columns in the table.
	2. Click the button icon to freeze the column in the table.
	3. Check the columns that need to be displayed in the table.

\#. List of backups with information on them:

	FQDN/IP - FQDN or IP address of the database instance;
	Working space - the name of the working space for which a backup is created;
	* Number of full backups - the number of full backups;
	* Number of increment. backups - the number of incremental backups;
	* Date of the latest backup- date and time of creating backup;
	* Size of the latest backup;
	* Status of the latest backup - in progress, complete, failed, or scheduled.