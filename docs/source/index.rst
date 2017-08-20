Usage
=====

.. toctree::
   :maxdepth: 2
   :caption: Contents:

.. code-block:: javascript

    const client = require('gsheetsdb');
    const sheetId = 'SHEET_KEY'

    // Create a service account to get a JSON key
    const credentials = {
      client_email: 'EMAIL',
      private_key: 'JSON_KEY'
    };

    client.connect(sheetId, credentials, (err, db)  => {
      if (err) return console.error(err);

      db.select('users').find({ name: 'Anshul' }).then(user => {
        console.log(user);
        // Do some nasty stuff with user
      });
    })


Indices and tables
==================

* :ref:`search`
