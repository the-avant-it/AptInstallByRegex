# Common.AptInstallByRegex

Role for performing apt install with package version specified as regex. Very usefull for packages that often get deleted (like postgresql)

# Changelog

## 1.2.1

- Add apt retries
- IMPORTANT: Change defaut value for apt_extra_args

## 1.1.0

- Add support for apt_extra_args
- Fix critical bug when role installs all versions if multiple matched (newes will be installed)

## 1.0.0

- Initial

# Documentation for 1.2.1

## Requirements

## Variables

### Non-secret

```yaml
apt_install_by_regex:
  # Required. Package name
  package_name: postgresql-14
  # Required. Package version regexp evaluated via grep
  package_version_regex: "14.+"
  # Optional. -oP by default
  grep_flags: -oP
  # Optional. Which handlers to notify
  notify: []
  
  # Optional. Apt retry configuration
  apt_retries: 10
  apt_retry_delay: 12
  apt_retry_on_stderr_containing: "Could not get lock"

  # Optional. Default value is shown below:
  apt_extra_args: --yes --force-yes -o Dpkg::Options::="--force-confdef" -o Dpkg::Options::="--force-confold"

```  

### Secret

```yaml

```