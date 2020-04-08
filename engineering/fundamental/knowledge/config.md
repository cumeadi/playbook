## Config

> Store config in the environment

Apps sometimes store config as constants in the code. This is a violation of twelve-factor, which requires strict separation of config from code. Config varies substantially across deploys, code does not.

Your code must always be separated from the configuration (environment variables). We use a .env file to store all environment variables of the app, and this should be different among environments.

Example in Go, the binary file could be run in following options:

- With option to load config from .env files
- With option to load config from environment variables
- It also coule be run without any config file, loading default config.
