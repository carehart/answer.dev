---
---

# Command-line

:::tip

Answer binary support some command-line options

:::

## Usage
`answer command [command or global options] [arguments...]`

```shell
To run answer, use:
        - 'answer init' to initialize the required environment.
        - 'answer run' to launch application.

Usage:
  answer [command]

Available Commands:
  check       checking the required environment
  dump        back up data
  help        Help about any command
  init        init answer application
  run         Run the application

Flags:
  -h, --help      help for answer
  -v, --version   version for answer

Use "answer [command] --help" for more information about a command.
```

## Global options
All global options can be placed at the command level.
- `--help`, `-h`: Show help text and exit. Optional.
- `--version`, `-v`: Show version and exit. Optional.
- `--config` path, `-c` path: configuration file path. Optional. (default: data/conf/config.yaml)
- `--data-path` path, `-C` path: data saved path. Optional. (default: /data/)

## Commands
### init
> init command will initialize the application required environment, contains: default config-file, data directory, initialize database etc.

- Options
  - `--data-path` path, `-C` path: data saved path. Optional. (default: /data/)
- Examples
  - `answer init -C ./data/`
- Notes
  - if answer already initialized, this command will not be executed. For example, if config file is already exist so it will not be created or overwritten.
  - if answer initialized failed, run command can not be executed.

### check
> check command will check the application whether it can run or not. check the config file if exist. check the database if connection can be established etc.

- Examples
  - `answer check -c ./data/conf/config.yaml`

### run
> run command will run the application.

- Examples
  - `answer run -c ./data/conf/config.yaml`

### dump
> dump command will dump the database data to sql file.

- Options
  - `--path` path, `-p` path: dump data path. Optional. (default: ./)
- Examples
  - `answer dump -p /tmp/`