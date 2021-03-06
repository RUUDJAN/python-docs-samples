.. This file is automatically generated. Do not edit this file directly.

Google Cloud Spanner Python Samples
===============================================================================

.. image:: https://gstatic.com/cloudssh/images/open-btn.png
   :target: https://console.cloud.google.com/cloudshell/open?git_repo=https://github.com/GoogleCloudPlatform/python-docs-samples&page=editor&open_in_editor=spanner/cloud-client/README.rst


This directory contains samples for Google Cloud Spanner. `Google Cloud Spanner`_ is a highly scalable, transactional, managed, NewSQL database service. Cloud Spanner solves the need for a horizontally-scaling database with consistent global transactions and SQL semantics.




.. _Google Cloud Spanner: https://cloud.google.com/spanner/docs 

Setup
-------------------------------------------------------------------------------


Authentication
++++++++++++++

This sample requires you to have authentication setup. Refer to the
`Authentication Getting Started Guide`_ for instructions on setting up
credentials for applications.

.. _Authentication Getting Started Guide:
    https://cloud.google.com/docs/authentication/getting-started

Install Dependencies
++++++++++++++++++++

#. Install `pip`_ and `virtualenv`_ if you do not already have them. You may want to refer to the `Python Development Environment Setup Guide`_ for Google Cloud Platform for instructions.

 .. _Python Development Environment Setup Guide:
     https://cloud.google.com/python/setup

#. Create a virtualenv. Samples are compatible with Python 2.7 and 3.4+.

    .. code-block:: bash

        $ virtualenv env
        $ source env/bin/activate

#. Install the dependencies needed to run the samples.

    .. code-block:: bash

        $ pip install -r requirements.txt

.. _pip: https://pip.pypa.io/
.. _virtualenv: https://virtualenv.pypa.io/

Samples
-------------------------------------------------------------------------------

Snippets
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. image:: https://gstatic.com/cloudssh/images/open-btn.png
   :target: https://console.cloud.google.com/cloudshell/open?git_repo=https://github.com/GoogleCloudPlatform/python-docs-samples&page=editor&open_in_editor=spanner/cloud-client/snippets.py;spanner/cloud-client/README.rst




To run this sample:

.. code-block:: bash

    $ python snippets.py

    usage: snippets.py [-h] [--database-id DATABASE_ID]
                       instance_id
                       {create_database,insert_data,query_data,read_data,read_stale_data,add_column,update_data,query_data_with_new_column,read_write_transaction,read_only_transaction,add_index,query_data_with_index,read_data_with_index,add_storing_index,read_data_with_storing_index}
                       ...

    This application demonstrates how to do basic operations using Cloud
    Spanner.

    For more information, see the README.rst under /spanner.

    positional arguments:
      instance_id           Your Cloud Spanner instance ID.
      {create_database,insert_data,query_data,read_data,read_stale_data,add_column,update_data,query_data_with_new_column,read_write_transaction,read_only_transaction,add_index,query_data_with_index,read_data_with_index,add_storing_index,read_data_with_storing_index}
        create_database     Creates a database and tables for sample data.
        insert_data         Inserts sample data into the given database. The
                            database and table must already exist and can be
                            created using `create_database`.
        query_data          Queries sample data from the database using SQL.
        read_data           Reads sample data from the database.
        read_stale_data     Reads sample data from the database. The data is
                            exactly 15 seconds stale.
        add_column          Adds a new column to the Albums table in the example
                            database.
        update_data         Updates sample data in the database. This updates the
                            `MarketingBudget` column which must be created before
                            running this sample. You can add the column by running
                            the `add_column` sample or by running this DDL
                            statement against your database: ALTER TABLE Albums
                            ADD COLUMN MarketingBudget INT64
        query_data_with_new_column
                            Queries sample data from the database using SQL. This
                            sample uses the `MarketingBudget` column. You can add
                            the column by running the `add_column` sample or by
                            running this DDL statement against your database:
                            ALTER TABLE Albums ADD COLUMN MarketingBudget INT64
        read_write_transaction
                            Performs a read-write transaction to update two sample
                            records in the database. This will transfer 200,000
                            from the `MarketingBudget` field for the second Album
                            to the first Album. If the `MarketingBudget` is too
                            low, it will raise an exception. Before running this
                            sample, you will need to run the `update_data` sample
                            to populate the fields.
        read_only_transaction
                            Reads data inside of a read-only transaction. Within
                            the read-only transaction, or "snapshot", the
                            application sees consistent view of the database at a
                            particular timestamp.
        add_index           Adds a simple index to the example database.
        query_data_with_index
                            Queries sample data from the database using SQL and an
                            index. The index must exist before running this
                            sample. You can add the index by running the
                            `add_index` sample or by running this DDL statement
                            against your database: CREATE INDEX AlbumsByAlbumTitle
                            ON Albums(AlbumTitle) This sample also uses the
                            `MarketingBudget` column. You can add the column by
                            running the `add_column` sample or by running this DDL
                            statement against your database: ALTER TABLE Albums
                            ADD COLUMN MarketingBudget INT64
        read_data_with_index
                            Inserts sample data into the given database. The
                            database and table must already exist and can be
                            created using `create_database`.
        add_storing_index   Adds an storing index to the example database.
        read_data_with_storing_index
                            Inserts sample data into the given database. The
                            database and table must already exist and can be
                            created using `create_database`.

    optional arguments:
      -h, --help            show this help message and exit
      --database-id DATABASE_ID
                            Your Cloud Spanner database ID.





The client library
-------------------------------------------------------------------------------

This sample uses the `Google Cloud Client Library for Python`_.
You can read the documentation for more details on API usage and use GitHub
to `browse the source`_ and  `report issues`_.

.. _Google Cloud Client Library for Python:
    https://googlecloudplatform.github.io/google-cloud-python/
.. _browse the source:
    https://github.com/GoogleCloudPlatform/google-cloud-python
.. _report issues:
    https://github.com/GoogleCloudPlatform/google-cloud-python/issues


.. _Google Cloud SDK: https://cloud.google.com/sdk/