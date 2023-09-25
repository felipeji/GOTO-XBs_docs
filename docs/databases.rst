Databases Description
=====================

GOTO-XBs uses an SQLite database with two primary tables:


Source Table
~~~~~~~~~~~~

The `Source` table contains fundamental information about the X-ray binaries (XBs) being tracked. It is structured with the following columns:

- ``source_id``: a unique identifier for each source.
- ``name``: the name of the source.
- ``pretty_name``: a human-readable name for the source.
- ``ra``: Right Ascension (RA) coordinate of the source.
- ``dec``: Declination (Dec) coordinate of the source.

Photometry Table
~~~~~~~~~~~~~~~~

The `Photometry` table stores photometric data obtained from the GOTO database. It includes the following columns:

- ``source``: a unique identifier linking the data to a specific source. This field serves as a foreign key referencing the `source_id` in the `Source` table.
- ``date``: date of the observation.
- ``mjd``: Modified Julian Date (MJD) of the observation.
- ``mag``: magnitude.
- ``mag_err``: error associated with the magnitude.

