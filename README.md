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
This database dump is provided as sample data to help you test and develop your MariaDB applications. It contains a pre-populated dataset that you can use to experiment, prototype, or demonstrate features.

> [!IMPORTANT]  
> This repository does not include the necessary Docker configuration files or instructions on how to set up MariaDB. You'll need to have a local MariaDB instance running on your machine in order to import this database dump.

If you don't already have a working MariaDB installation, you can use this pre-built Docker image:

* [MariaDB Sample Database Image](https://hub.docker.com/r/agentlans/mariadb-sample)

This container is preloaded with the sample database data, making it easy to get started quickly. Simply pull and run the image to access the sample dataset for testing and development purposes.

## Licence
Like the original database, this work is licensed under the Creative Commons Attribution-Share Alike 3.0 Unported License.
