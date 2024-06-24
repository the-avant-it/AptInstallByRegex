# Common.AptInstallByRegex

Role for performing apt install with package version specified as regex. Very usefull for packages that often get deleted (like postgresql)

# Changelog

## 1.2.0

- Add apt retries

## 1.1.0

- Add support for apt_extra_args
- Fix critical bug when role installs all versions if multiple matched (newes will be installed)

## 1.0.0

- Initial

# Documentation for 1.0.0

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
```  

### Secret

```yaml

```