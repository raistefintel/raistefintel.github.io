# Releases

For Intel® Distribution for Python* Release Notes prior to version 2023.2 release, please visit [this page.](https://www.intel.com/content/www/us/en/developer/articles/release-notes/distribution-for-python-release-notes.html)

## 2023.3

## 2023.2

### Highlights

The following are new features for the release:

- Migrated to conda-forge dependencies for greater compatibility with rich conda-forge
packages
- Excluded mpi4py from IDP to provide flexibility for customers who want to use other MPI
vendors in their Python environment
- Increased glibc minimum deployment target to 2.28 for GPU components to utilize newer glib
functionality
- Updated data-parallel extensions for Python packages (numba-dpex, dpctl, dpnp)

### Known Issues

There are no known issues in the 2023.2 release at this time.

### Deprecation Notices

#### Deprecation Notice for Python\* 3.8

Beginning with the Intel® Distribution for Python* 2024.0 release, Python version 3.8 will no longer be supported.

#### Deprecation of Intel® Distribution for Python* for macOS*

This is a forewarning: Intel® Distribution for Python for macOS is obsolete, use is discouraged, and it will be phased out starting with removal from our future product release in oneAPI 2024.0

Starting with the Intel® oneAPI 2024.0, Intel will no longer package or release Intel® Distribution for Python for macOS.

#### Deprecation of Intel® Extension for Scikit-Learn* for macOS*

Intel® Extension for Scikit-Learn* on macOS is now deprecated and will be discontinued in the 2024.0 release. Support for Linux*, Windows* and Windows Server* is available.
