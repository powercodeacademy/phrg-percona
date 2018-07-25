# Percona

## What is Percona?

[Percona](https://www.percona.com/) is a Database Administrator that Power employs to help us maintain and optimize our MySql databases. Power keeps an open dialog running with Percona on Slack, and use Percona technology to analyze our migrations before they get run on production servers.

Percona technology set is called [Percona Toolkit](https://www.percona.com/doc/percona-toolkit/LATEST/index.html). Power uses some of the tools from this set, but not all. One tool developers encounter is called [pt-online-schema-change](https://www.percona.com/doc/percona-toolkit/LATEST/pt-online-schema-change.html). If `nitro-web` is up and running on your laptop, it is likely you have this installed already.

## Percona and Migrations

There are various reasons Percona may prevent one a migration from running locally, or in production. One item to take note of is that Power uses a Ruby gem called [Departure](https://github.com/departurerb/departure) to wrap around pt-online-schema-change validations. By default, all of Power's migrations are executed through the `departure` gem. If you encounter an error pointing towards a `Departure` class, it means there is an issue with your migration/database and Percona.

If confused by a Percona related error, it is best to take your questions to a senior level developer at Power. Steps to recover from a database issue vary, and change frequently as we build Nitro.

## Resources

- [Percona](https://www.percona.com/)
- [pt-online-schema-change](https://www.percona.com/doc/percona-toolkit/LATEST/pt-online-schema-change.html)
- [Departure](https://github.com/departurerb/departure)
