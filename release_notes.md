# Releases

For Intel® Distribution for Python* Release Notes prior to version 2024.0 release, please visit [this page.](https://www.intel.com/content/www/us/en/developer/articles/release-notes/distribution-for-python-release-notes.html)

## 2024.1
[Release Notes](https://www.intel.com/content/www/us/en/developer/articles/release-notes/distribution-for-python-release-notes.html)

**What's New:**

The following are new features for the release:

- Significant improvements for **Data Parallel Extensions for Python**
	- **Data Parallel Controls** - `dpctl`
		- The library is now **100% conformant with core Python Array API 2022.12 spec**
		- The following **new features** added:
			- Reduction Functions: `min`, `max`, `prod`, `logsumexp`, `reduce_hypot`
			- Statistical Functions: `mean`, `std`, `var`
			- Sorting Functions: `sort`, `argsort`
			- Set Functions: `unique_values`, `unique_counts`, `unique_inverse`, `unique_all`
			- Elementwise Functions: `clip`, `cbrt`, `rsqrt`, `exp2`, `copysign`, `reciprocal`
			- Linear Algebra Functions: `matmul`, `vecdot`, `tensordot`
			- In-Place Elementwise Operations: 
			- 	Dedicated support for in-place Python operators (+=, -=, *=, /=, ^=, &&=, ||=, ^^=, <<=, >>=, %=) on `usm_ndarray` Python type
		- **Performance enhancements** and **bug fixes**
			- The library now supports **NVidia* devices**. Follow [GitHub instructions](https://github.com/IntelPython/dpctl/discussions/1124) how to compile dpctl for CUDA devices.
	- **Data Parallel Extension for NumPy\*** -`dpnp`
		- **New features** added:
			- Linear Algebra Functions: `slogdet`, `solve`
			- Manipulation Functions: `broadcase_arrays`, `can_cast`, `column_stack`, `row_stack`, `dstack`, `vstack`, `tile`
			- Mathematical Functions: `clip`, `logaddexp`, `logsumexp`, `positive`, `reduce_hypot`
			- Statistical Functions: `nanargmax`, `nanargmin`, `nanmax`, `nanmin`, `nanmean`, nanstd, `nanvar`
			- Type Relating Functions: `finfo`, `iinfo`
		- **Extended support for keyword arguments:**
			- Array Creation Functions: `diag`, `diagflat`, `geomspace`, `linspace`, `logspace`, `identity`, `tril`, `vander`
			- Counting Functions: `count_nonzero`
			- Indexing Functions: `indices`, `put_along_axis`, `take_along_axis`
			- Linear Algebra Functions: `cholesky`, `det`, `dot`, `inv`, `matmul`, `qr`, `svd`
			- Manipulation Functions: `atleast_1d`, `atleast_2d`, `atleast_3d`, `astype`, `concatenate`, `stack`, `ravel`, `repeat`
			- Mathematical Functions: `absolute`, `abs`, `angle`, `reciprocal`, `cbrt`, `rsqrt`, `copysign`, `diff`, `exp`, `exp2`, `expm1`, `fmax`, `fmin`, `maximum`, `minimum`, `hypot`, `log10`, `log1p`, `log2`, `prod`, `nanprod`
			- Searching Functions: `argmax`, `argmin`
			- Sorting Functions: `argsort`, `sort`
			- Statistical Functions**: `average`, `max`, `min`, `amax`, `amin`, `mean`, `nansum`, `ptp`, `std`, `var`
		- **Bug fixes** and **performance improvements** (elementwise and linear algebra functions)
	- **Data Parallel Extension for Numba\*** - `numba-dpex`
		- **Added support for Numba 0.59**. Minimum required Numba version is 0.58
		- **New features in kernel API** that enable greater control of device execution:
			- **Atomic Fetch Operations**: `fetch_add`, `fetch_sub`, `fetch_min`, `fetch_max`, `fetch_and`, `fetch_or`, `fetch_xor`.
			- **Atomic Load, Store, Exchange Operations**: `atomic_load`, `atomic_store`, `atomic_exchange` 
			- **Atomic Compare-Exchange Operation**: `atomic_compare_exchange`.
			- **New indexing classes**, `Item` and `NdItem`, which allow to express different levels of parallelism. All indexing functions are supported with these new classes. 
				- NOTE: Old indexing functions have been deprecated!
			- Added **support for `group_barrier` functions**, fixing code generation issues in the existing barrier function.
		- **Performance** and **other enhancements:**
			- Significantly **improved kernel launch times.**
			- **Kernel** functions **can now be submitted asynchronously** to execution queues.
			- **Kernel** functions are now **callable from inside dpjit** functions.
		- Version updates of conda packages.

## 2024.0
[Release Notes](https://www.intel.com/content/www/us/en/developer/articles/release-notes/distribution-for-python-release-notes.html)

**What's New**:

The following are new features for the release:

- Installer is now based on Conda Constructor, which improves user installation experience by
	- Faster conda package installation and error-handling
	- Compatibility with .conda files
	- Customizable install paths
	- Command-line interface installation

Other changes in this release:
  - Performance improvements and other enhancements for Data Parallel Extensions for Python (dpctl, dpnp, numba-dpex)
  - macOS no longer supported for 2024.0
 

**OS Deprecation Notice**

The following OS support is now deprecated and will be discontinued with our 2025.0 release in Fall 2024.​​​​​​

CPU
  - SUSE Linux Enterprise Server (SLES) version 15 SP3
  - Ubuntu Linux version 20.04

GPU
  - Red Hat Enterprise Linux (RHEL) version 8.6
  - SUSE Linux Enterprise Server (SLES) version 15 SP3

### Highlights

The following are new features for the release:
 

### Known Issues

Please refer to the **Known Issues** in the **Resources** of the document that is available online:

https://www.intel.com/content/www/us/en/developer/articles/troubleshooting/python-known-issues.html

**Intel® Distribution for Python, version 2024.1** does not include the latest functional and security
updates. **Intel® Distribution for Python, Version 2024.2** is targeted to be released in **June 2024** and will
include additional functional and security updates. Customers should update to the latest version as it
becomes available.


### Deprecation Notices

#### Deprecation Notice for Python\* 3.8

Beginning with the Intel® Distribution for Python* 2024.0 release, Python version 3.8 will no longer be supported.

#### Deprecation of Intel® Distribution for Python* for macOS*

This is a forewarning: Intel® Distribution for Python for macOS is obsolete, use is discouraged, and it will be phased out starting with removal from our future product release in oneAPI 2024.0

Starting with the Intel® oneAPI 2024.0, Intel will no longer package or release Intel® Distribution for Python for macOS.

#### Deprecation of Intel® Extension for Scikit-Learn* for macOS*

Intel® Extension for Scikit-Learn* on macOS is now deprecated and will be discontinued in the 2024.0 release. Support for Linux*, Windows* and Windows Server* is available.
