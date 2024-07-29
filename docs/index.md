### Bare Metal Route {#bare_metal}

Test, Test, Test

Paperless runs on linux only. The following procedure has been tested on
a minimal installation of Debian/Buster, which is the current stable
release at the time of writing. Windows is not and will never be
supported.

Paperless requires Python 3. At this time, 3.9 - 3.11 are tested versions.
Newer versions may work, but some dependencies may not fully support newer versions.
Support for older Python versions may be dropped as they reach end of life or as newer versions
are released, dependency support is confirmed, etc.

1.  Install dependencies. Paperless requires the following packages.

    - `python3`
    - `python3-pip`
    - `python3-dev`
    - `default-libmysqlclient-dev` for MariaDB
    - `pkg-config` for mysqlclient (python dependency)
    - `fonts-liberation` for generating thumbnails for plain text
      files
    - `imagemagick` >= 6 for PDF conversion
    - `gnupg` for handling encrypted documents
    - `libpq-dev` for PostgreSQL
    - `libmagic-dev` for mime type detection
    - `mariadb-client` for MariaDB compile time
    - `mime-support` for mime type detection
    - `libzbar0` for barcode detection
    - `poppler-utils` for barcode detection
    - `whatever`