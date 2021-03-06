## Release 2.2.0
### Summary
A release improving puppetlabs-apt compatibility and updating Docker repo.

#### Features and improvements
- apt::update copied and adapted from puppetlabs-apt
- apt::repo::docker replaces apt::repo::dockerproject. The public key is included
- unattended-upgrades fixed in wheezy

### Backward incompatible changes
- Class[apt::aptget\_update] and Exec[aptget\_update] are removed, use Class[apt::update] in notify instead
- Class[apt::repo::dockerproject] is removed, use Class[apt::repo::docker] instead

## Release 2.1.0
### Summary
A release targeting puppetlabs-apt compatibility.

#### Features
- apt::key copied and adapted from puppetlabs-apt
- apt::setting copied and adapted from puppetlabs-apt
- apt::source copied and adapted from puppetlabs-apt

### Deprecations
- apt::key parameters url, keyserver and fingerprint are deprecated and should be replaced by source, server and id.
- apt::key parameters environment and path are deprecated and ignored.
- apt::repository is deprecated, use apt::source instead

