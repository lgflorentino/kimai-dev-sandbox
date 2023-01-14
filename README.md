# kimai-dev-sandbox
A space to save Kimai dev tooling and debugging helpers 

### Usage

Inspect the `ctrlr` script for more help

```sh
    ./ctrlr <mysql|pgsql> <unit|integration|db>
```

### Environment file

The `.env` file in this directory is used to configure the db backend by setting environment variables inside the docker container running the `php` interpreter.
These get set by `$1` option. 
The `php` environment will select the variables in the environment over the ones defined in `kimai2/.env`


### Notes

    * Database connections for `Doctrine` are configured in `kimai2/config/packages/doctrine.*.yaml`
    * The `kimai2/tests/bootstrap.php` kicks off another php interpreter to reset the test DB before running any test code.



