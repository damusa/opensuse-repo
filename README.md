# openSUSE Workstation Fleet Repository

Cryptographically signed, domain-agnostic Zypper meta-package repository (`damusa-os-update`, `damusa-user-flatpak-store`, `damusa-workstation`, `damusa-laptop`, `damusa-xps9310`) for **openSUSE Tumbleweed & Slowroll (`x86_64`)** and **openSUSE Tumbleweed (`aarch64`)**.

- **GitHub Pages Zypper URL**: `https://damusa.github.io/opensuse-repo/`
- **Zero binaries in Git**: Signed `.rpm` packages and `repodata/` are published as versioned [GitHub Releases](../../releases) and deployed directly via `actions/deploy-pages`.

## Quick Setup on openSUSE

```bash
sudo rpm --import https://damusa.github.io/opensuse-repo/RPM-GPG-KEY-damusa-repo
sudo zypper addrepo --refresh https://damusa.github.io/opensuse-repo/opensuse-repo.repo
sudo zypper refresh
# Full managed family workstation:
sudo zypper install damusa-workstation
# Or standalone building blocks (no sudoers/LDAP changes):
sudo zypper install damusa-os-update damusa-user-flatpak-store
```
