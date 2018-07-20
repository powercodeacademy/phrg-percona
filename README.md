# Percona

## What is Percona?

[Percona](https://www.percona.com/) is a database performance company that Power employs to help us maintain and optimize our MySql databases. Power keeps an open dialog running with Percona on Slack, and use Percona technology to analyze our migrations before they get run on production servers.

The percona technology we use is called [Percona Toolkit](https://www.percona.com/doc/percona-toolkit/LATEST/index.html). Specifically, we monitor migrations with a tool called [pt-online-schema-change](https://www.percona.com/doc/percona-toolkit/LATEST/pt-online-schema-change.html), which is included in this kit. If `nitro-web` is up and running on your laptop, it is likely you have this installed already.

## Percona and Migrations

The are various reasons Percona may prevent one of your migrations from running locally, or in production. One item to take note of is that we use a Ruby gem called [Departure](https://github.com/departurerb/departure) to wrap around the pt-online-schema-change validations. So if you encounter an error pointing towards a `Departure` library, it means there is an issue with percona tech and you migration/database.

If confused by a percona related error, it is best to best to take your questions to a senior developer at Power. Steps to recover from database issues vary, and change frequentl, as we continue to build Nitro.
