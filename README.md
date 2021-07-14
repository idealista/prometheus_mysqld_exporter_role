![Logo](https://raw.githubusercontent.com/idealista/prometheus_mysqld_exporter_role/master/logo.gif)

# Prometheus MySQL Exporter Ansible role
[![Build Status](https://travis-ci.org/idealista/prometheus_mysqld_exporter_role.svg?branch=master)](https://travis-ci.org/idealista/prometheus_mysqld_exporter_role)

This ansible role installs a Prometheus MySQL Exporter in a debian environment.

- [Getting Started](#getting-started)
	- [Prerequisities](#prerequisities)
	- [Installing](#installing)
- [Usage](#usage)
- [Testing](#testing)
- [Built With](#built-with)
- [Versioning](#versioning)
- [Authors](#authors)
- [License](#license)
- [Contributing](#contributing)

## Getting Started

These instructions will get you a copy of the role for your ansible playbook. Once launched, it will install a [Prometheus MySQL Exporter](https://github.com/prometheus/mysqld_exporter) server in a Debian system.

*Note:* Beginning with the 3.0 version, the default behaviour is the service sending logs to systemd's journal instead to a log file. You can change it modifying the necessary ansible vars (see defaults/main.yml)
### Prerequisities

Ansible >= 2.9.0 version installed.
Inventory destination should be a Debian environment.

For testing purposes, [Molecule](https://molecule.readthedocs.io/) with Docker as driver and [Goss](http://goss.rocks) as verifier

### Installing

Create or add to your roles dependency file (e.g requirements.yml) from GitHub:

```
- src: http://github.com/idealista/prometheus_mysqld_exporter_role.git
  scm: git
  version: 3.2.0
  name: prometheus_mysqld_exporter
```

or using [Ansible Galaxy](https://galaxy.ansible.com/idealista/prometheus_mysqld_exporter_role/) as origin if you prefer:

```
- src: idealista.prometheus_mysqld_exporter_role
```

Install the role with ansible-galaxy command:

```
ansible-galaxy install -p roles -r requirements.yml -f
```

Use in a playbook:

```
- hosts: someserver
  roles:
    - { role: prometheus_mysqld_exporter }
```

## Usage

Look to the [defaults](defaults/main.yml) properties file to see the possible configuration properties.

## Testing

### Installing dependencies

```sh
$ pipenv sync
$ pipenv run molecule test
```

For more information read the [pipenv docs](https://docs.pipenv.org/).

### Running test

```
$ pipenv run molecule test
```

See molecule/molecule.yml to check possible testing platforms.

## Built With

![Ansible](https://img.shields.io/badge/ansible-4.0.0-green.svg)
![Molecule](https://img.shields.io/badge/molecule-3.3.2-green.svg)
![Goss](https://img.shields.io/badge/goss-0.3.16-green.svg)

## Versioning

For the versions available, see the [tags on this repository](https://github.com/idealista/prometheus_mysqld_exporter_role/tags).

Additionaly you can see what change in each version in the [CHANGELOG.md](CHANGELOG.md) file.

## Authors

* **Idealista** - *Work with* - [idealista](https://github.com/idealista)

See also the list of [contributors](https://github.com/idealista/prometheus_mysqld_exporter_role/contributors) who participated in this project.

## License

![Apache 2.0 Licence](https://img.shields.io/hexpm/l/plug.svg)

This project is licensed under the [Apache 2.0](https://www.apache.org/licenses/LICENSE-2.0) license - see the [LICENSE](LICENSE) file for details.

## Contributing

Please read [CONTRIBUTING.md](.github/CONTRIBUTING.md) for details on our code of conduct, and the process for submitting pull requests to us.
