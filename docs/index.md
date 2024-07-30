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
  
4.  Create a system user with a new home folder under which you wish
    to run paperless.

    ```shell-session
    adduser paperless --system --home /opt/paperless --group
    ```

5.  Get the release archive from
    <https://github.com/paperless-ngx/paperless-ngx/releases> for example with

    ```shell-session
    curl -O -L https://github.com/paperless-ngx/paperless-ngx/releases/download/v1.10.2/paperless-ngx-v1.10.2.tar.xz
    ```

    Extract the archive with

    ```shell-session
    tar -xf paperless-ngx-v1.10.2.tar.xz
    ```

    and copy the contents to the
    home folder of the user you created before (`/opt/paperless`).

#### Quellen

Paperless-ngx Dokumentation [https://docs.paperless-ngx.com/setup/#bare_metal](https://docs.paperless-ngx.com/setup/#bare_metal)  
Tutorial Paperless-ngx Discussion [https://github.com/paperless-ngx/paperless-ngx/discussions/5822](https://github.com/paperless-ngx/paperless-ngx/discussions/5822)  
Update Tutorial [https://nerdig.es/paperless-baremetal-update/](https://nerdig.es/paperless-baremetal-update/)  
