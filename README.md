# mariadb-test_db

A single-file database dump of a MySQL sample [`employees`](https://github.com/datacharmer/test_db) database, created using MariaDB running inside a Debian Docker container.

## Overview
This repository contains a compressed SQL file (`all-dump.sql.zst`) that includes data from two separate SQL files: `employees.sql` and `test_employees_md5.sql`. The original scripts were spread across multiple files and scripts, making this single-file dump more convenient to use as sample data for testing MariaDB applications.

## Usage
1. Clone the repository.
2. Decompress the file using `unzstd all-dump.sql.zst` (this will create a 172 MB SQL file).
3. Import the database into your local MariaDB instance:
```bash
mariadb -u root < all-dump.sql
```
## Purpose
This database dump is intended to be used as sample data for testing and development purposes with MariaDB applications.

Note: This repository does not include any Dockerfile or instructions on how to set up the MariaDB container. You will need to have a local MariaDB instance running in order to import and use this database dump.

## Licence
Like the original database, this work is licensed under the Creative Commons Attribution-Share Alike 3.0 Unported License.

