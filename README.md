# Common.AptInstallByRegex

Role for performing apt install with package version specified as regex. Very usefull for packages that often get deleted (like postgresql)

# Changelog

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