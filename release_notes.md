# Release Notes

This page provides the current Release Notes for the Intel® Distribution for Python\*. The notes are categorized by year, from newest to oldest, with individual releases listed within each year.

All files are in PDF format - [Adobe Reader\*](https://get.adobe.com/reader/) (or compatible) required.

For information on known issues, see [Intel® Distribution for Python\* Known Issues.](https://www.intel.com/content/www/us/en/developer/articles/troubleshooting/python-known-issues.html)
For questions or technical support, visit [Intel® Distribution for Python\* Support Forum.](https://community.intel.com/t5/Intel-Distribution-for-Python/bd-p/distribution-python)

## 2024 
### 2024.2
<details open> 
	 <summary><b>Expand</b></summary>
	
 [Release Notes](https://cdrdv2.intel.com/v1/dl/getContent/825850)
 

**What's New:**

The Intel® Distribution for Python, 2024.2 has been updated to include functional and security updates. Users should update to the latest version.

The Intel® Distribution for Python* added the following features:

- Integrated libmamba solver to conda for concurrent package resolution.
- Version updates of conda packages.
- The Data Parallel Control Library added the following features:
	- It offers improved productivity with new sorting and summing functions (`dpt.searchsorted`, `dpt.cumulative_sum`, `dpt.cumulatove_prod`, `dpt.cumulative_logsumexp`).
	- Added support for the out keyword argument.
	- Correspondence of tensor functions signatures to array API (keyword-only argument can’t be provided as positional argument).
	- Updated documentation and bug fixes.
- The Data Parallel Extension for NumPy added the following features:
	- Increased productivity with the addition of a new family of cumulative functions and closed functional gaps in the linalg routine.
	- DPNP is now 100% functional in npbench benchmarks.
	- Implemented a family of cumulative functions. Full list of mathematical functions supported is available at [Mathematical Functions — Data Parallel Extension for NumPy documentation.](https://intelpython.github.io/dpnp/reference/math.html)
</details>

### 2024.1
<details>
  <summary><b>Expand</b></summary>

[Release Notes](https://www.intel.com/content/www/us/en/content-details/818309/intel-distribution-for-python-2024-1-release-notes.html)

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
</details>

### 2024.0
<details>
  <summary><b>Expand</b></summary>
	
[Release Notes](https://cdrdv2.intel.com/v1/dl/getContent/792860)

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
 </details>
 
## Known Issues

Please refer to the **Known Issues** in the **Resources** of the document that is available online:

https://www.intel.com/content/www/us/en/developer/articles/troubleshooting/python-known-issues.html

**Intel® Distribution for Python, version 2024.1** does not include the latest functional and security
updates. **Intel® Distribution for Python, Version 2024.2** is targeted to be released in **June 2024** and will
include additional functional and security updates. Customers should update to the latest version as it
becomes available.


## Deprecation Notices

#### Deprecation Notice for Python\* 3.8

Beginning with the Intel® Distribution for Python* 2024.0 release, Python version 3.8 will no longer be supported.

#### Deprecation of Intel® Distribution for Python* for macOS*

This is a forewarning: Intel® Distribution for Python for macOS is obsolete, use is discouraged, and it will be phased out starting with removal from our future product release in oneAPI 2024.0

Starting with the Intel® oneAPI 2024.0, Intel will no longer package or release Intel® Distribution for Python for macOS.

#### Deprecation of Intel® Extension for Scikit-Learn* for macOS*

Intel® Extension for Scikit-Learn* on macOS is now deprecated and will be discontinued in the 2024.0 release. Support for Linux*, Windows* and Windows Server* is available.

## Previous Releases 

### 2023 
#### 2023.2
<details>
  <summary><b>Expand</b></summary>

[Release Notes](https://cdrdv2.intel.com/v1/dl/getContent/783108?explicitVersion=true)

**What's New:**

- Migrated to conda-forge dependencies for greater compatibility with rich conda-forge packages
- Excluded mpi4py from IDP to provide flexibility for customers who want to use other MPI vendors in their Python environment
- Increased glibc minimum deployment target to 2.28 for GPU components to utilize newer glib functionality
- Updated data-parallel extensions for Python packages (numba-dpex, dpctl, dpnp)

**Deprecation Notice:**  Beginning with the Intel® Distribution for Python\* 2024.0 release, Python version 3.8 will no longer be supported.

**Deprecation of Intel® Distribution for Python* for macOS\***

This is a forewarning: Intel® Distribution for Python for macOS is obsolete, use is discouraged, and it will be phased out starting with removal from our future product release in oneAPI 2024.0

Starting with the Intel® oneAPI 2024.0, Intel will no longer package or release Intel® Distribution for Python for macOS.

**Deprecation of Intel® Extension for Scikit-Learn* for macOS\***

Intel® Extension for Scikit-Learn\* on macOS is now deprecated and will be discontinued in the 2024.0 release. Support for Linux*, Windows* and Windows Server* is available.
</details> 

#### 2023.1
<details>
  <summary><b>Expand</b></summary>

[Release Notes](https://cdrdv2.intel.com/v1/dl/getContent/774139)

- Updated conda to 22.11.1
	- Downloads and extract packages in parallel, which greatly speeds up package downloads when latency is high (controlled by the new fetch_threads config parameter
	- Removed pyeditline from distribution
- Source of segmentation fault issues when using tab completion
	- Caused interpreter to hang in Python 3.10 during SSH sessions
	- Users can still run `conda install pyeditline -c intel --override-channels`
</details> 

#### 2023.0
<details>
  <summary><b>Expand</b></summary>

[Release Notes](https://cdrdv2.intel.com/v1/dl/getContent/763158)

- Python 3.10 packages are available in online Intel channel
- Updated versions of packages (e.g. numpy, scipy, etc.)
- Numba-dpex has the following new features
	- Supports newer Numba version (Numba0.56).
	- Supports the latest release of dpnp (0.11) and dpctl (0.14).
	- Adds customized exception classes for better exception handling.
- Improves code stability when calling take() for input array with non-integer values.
- Allows pairwise_distance.py to run on machine with no FP64 support in HW.
- DPC++ RT is ABI incompatible with earlier version of DPC++ RT.
	- Applications compiled with 2022 DPC++ compiler are incompatible with DPC++ RT 2023 Gold and must be recompiled, or used with DPC++ RT 2022
	- Applications compiled with 2023 DPC++ compiler are not compatible with earlier versions of DPC++ RT.
</details> 

### 2022 
#### Intel® oneAPI 2022.3.1
<details>
  <summary><b>Expand</b></summary>

[Release Notes](https://cdrdv2.intel.com/v1/dl/getContent/751943)

- Take advantage of new performance optimizations of element-wise operations and Windows OS support in the Dpnp package 
- Gain explicit control of device memory allocation and kernel execution with the Dpnp and numba-dppy packages  
- This release is immediately available through the Intel® Developer Zone. It will be available through repositories at a later date.
</details> 

#### Intel® oneAPI 2022.3
<details>
  <summary><b>Expand</b></summary>

[Release Notes](https://cdrdv2.intel.com/v1/dl/getContent/741452)

- Addressed critical CVE -2018-25032

Please note:

As announced previously, Windows driver support of integrated graphics processors included with 6th - 10th Gen Intel Core Processor and related Intel Atom®, Pentium®, and Celeron® processors is deprecated and has moved to maintenance mode. Only security and critical bug fixes will be updated.

oneAPI tools using existing integrated graphics processor functionality in the aforementioned processors may continue to work, but will no longer be supported. Note that CPU functionality for these processors remains fully supported and unaffected.

Intel® oneAPI 2022.3 is validated on Windows and Linux.
- Windows Intel® Graphics Driver, see this article for instructions to download and install.
- Linux General Purpose Intel GPUs (GPGPU) Driver, see this article. Click the one labeled 20220830 for instructions to download and install.​​​​
</details> 

#### Intel® oneAPI 2022.2
<details>
  <summary><b>Expand</b></summary>

[Release Notes](https://software.intel.com/content/dam/develop/external/us/en/documents/2022.2_Python_Release_Notes_Intel(R)_Distribution_for_Python.pdf)

- Updated packages to latest versions with CVE fixes
- dpnp updates
	- Implemented the "compute follows data" programming model for the dpnp library
	- dpnp package on Windows become available
	- performance improvement of element-wise functions in dpnp in case of input data with strides
- numba-dppy updates
	- Implemented the "compute follows data" programming model for the kernel API in numba-dppy
	- Device private memory support in numba-dppy
	- numba-dppy support for any array that supports the `__sycl_usm_array_interface__` protocol for the kernel API
	- Provided support for Numba 0.55 and new debugging features in numba-dppy
	- Enable DPNP support in numba-dppy on Windows
</details> 

#### Intel® oneAPI 2022.1 
<details>
  <summary><b>Expand</b></summary>

[Release Notes](https://software.intel.com/content/dam/develop/external/us/en/documents/2022_Python_Release_Notes_Intel(R)_Distribution_for_Python-Release1.pdf)

- Intel® Distribution for Python now supports Python version 3.9
- The dpctl package offers developers increased debugging capabilities with improved error handing and reporting
- Data Parallel Python technology now provides zero copy data exchange performance across packages

**New in 2022.1.2 Product Release for Windows\* only:**
- Fixes Intel® Distribution for Python installation issue
</details> 

### 2021
#### Intel® oneAPI 2021.4
<details>
  <summary><b>Expand</b></summary>

[Release Notes](https://software.intel.com/content/dam/develop/external/us/en/documents/2021_Python_Release_Notes_Intel(R)_Distribution_for_Python_Release4.pdf)

- Numba-dppy works as an extension to off-the-shelf Numba 0.54.0.
- Pandas.MultiIndex support added in SDC.
- Numba-dppy’s @dppy.kernel now support __sycl_usm_array_interface through dpctl’s usm_ndarray.
- Updated all LLVM packages to LLVM 11
- Enabled @vectorize for target dppy in Numba-dppy
- Dpctl now has the ability to get command status and get profiling information from events.
- Dpctl has added queue.submit_barrier method to provide advanced synchronization mechanism to users.
- Expanded the Python C-API for working with dpctl Python objects in native extensions written in C/C++, example added for Pybind11.
- Implemented multi-versioning of DPCTLSyclInterface library on Linux.
- Dpctl can now be built using Open Source LLVM Sycl compiler.
</details> 

#### Intel® oneAPI 2021.3
<details>
  <summary><b>Expand</b></summary>
	
[Release Notes](https://software.intel.com/content/dam/develop/external/us/en/documents/2021_Python_Release_Notes_Intel(R)_Distribution_for_Python-Release3.pdf)

- Providing initial DPC++ compiler conda packages
- SDC with extended Pandas API support and reduced compilation time
- Numba-dppy improvements to documentation, code quality, Python 3.8 support, profiling support
- dpctl improvements to API usability, filter selector support, explicit SYCL context and queue creation, and Level Zero program creation support for Windows
</details> 
 
#### Intel® oneAPI 2021.2
<details>
  <summary><b>Expand</b></summary>

[Release Notes](https://software.intel.com/content/dam/develop/external/us/en/documents/2021_Python_Release_Notes_Intel(R)_Distribution_for_Python-Release2.pdf)

- Support for Level Zero driver to Numba-dppy
- Support SYCL filter selector in queue manager
- Better support for __sycl_usm_array_interface__ in numba-dppy
- Improvements to GDB support in Numba-DPPY generated kernels
- numpy package is updated to v1.20.1
- Improved performance of the following Intel scikit-learn CPU algorithms: Random forest, PCA, SVM
- Introduced bit-to-bit results reproducibility for Scikit-learn patches on CPU
- First public XGBoost version with GPU support
- Bug-fixes, improvements to documentations, user guides and examples
</details> 

#### Intel® oneAPI 2021.1
<details>
  <summary><b>Expand</b></summary>

[Release Notes](https://software.intel.com/content/dam/develop/external/us/en/documents/2021_Python_Release_Notes_Intel(R)_Distribution_for_Python-Update_1.pdf)

- Machine Learning
	- New accelerated Scikit-learn functionality: Random Forest Classification/Regression, kNN Search/Classification/Regression, tSNE, SVC, LASSO, ElasticNet, train_test_split, assert_all_finite, sparse K-means.
	- Scikit-learn and daal4py additional optimizations for DBSCAN, SVM, ElasticNet/LASSO, K-Means, train_test_split, Support Vector Classification (SVC), Random Forest, Logistic Regression, F-contiguous inputs.
	- Conversion of trained XGBoost and LightGBM models into daal4py Gradient Boosted Trees model for fast prediction.
	- XGBoost 1.2 with additional CPU optimizations with ‘hist’-tree method.
- Initial GPU support
	- dpnp – GPU-enabled Data Parallel NumPy, a collection of many NumPy algorithms accelerated for GPUs
	- dpctl – new Python package for device, queue, and USM data management with initial support in dpnp, scikit-learn, daal4py, and numba 
	- daal4py optimizations for GPU: KNN Classification, batch and streaming Covariance, DBSCAN, GBT Regression, K-Means, Linear & Logistic Regression, batch and streaming Low Order Moments, PCA, and binary SVM Classification
	- GPU support in scikit-learn for DBSCAN, K-Means, Linear Regression and Logistic Regression algorithms
	- numba – initial support for automatic GPU offload and GPU kernel semantics
- Numerical computing and image processing
	- New mkl_sparse package for Intel® MKL-powered sparse matrix computations in NumPy.
	- New mkl_umath package for acceleration of NumPy universal functions.
- Releasing scikit-ipp 1.2.0 for Intel® IPP-accelerated image warping , image filtering, and morphological operations
- Intel® Scalable Dataframe Compiler (Intel® SDC) Beta – Numba extension for accelerating Pandas* 
</details> 

### 2020
#### Update 4
<details>
  <summary><b>Expand</b></summary>

[Release Notes](https://software.intel.com/content/dam/develop/external/us/en/documents/2020_Python_Release%20Notes%20Intel(R)%20Distribution%20for%20Python%20-%20Update%204.pdf)

- Releasing scikit-ipp 1.2.0 for image warping, image filtering and morphological operations with scikit-image like API. Support for multi-threading for transform functions and partial multi-threading for filters using OpenMP. 
- Releasing mkl_umath Python package for Intel® technologies-powered NumPy universal function.
- Added new features for accelerated KNeighborsClassifier, RandomForestClassifier and RandomForestRegressor estimators, Sparse input support for KMeans and SVC, Probabilities prediction for SVC, Support of ‘normalize’ parameter for Lasso and ElasticNet in scikit-learn.
- Optimizations of train_test_split and Support Vector Classification (SVC) fit and prediction in scikit-learn.
- Conversion of trained XGBoost* and LightGBM* models into daal4py Gradient Boosted Trees model for fast prediction.
- Added new features for Brute Force method for k-Nearest Neighbors classification, new parameters support for k-Nearest Neighbors and Decision Forest in daal4py.
- Optimizations of Support Vector Machine training and prediction, Decision Forest classification training in daal4py.
- Latest CVE patches have been applied.
</details> 

#### Update 2
<details>
  <summary><b>Expand</b></summary>

[Release Notes](https://software.intel.com/content/dam/develop/external/us/en/documents/2020_Python_Release%20Notes%20Intel(R)%20Distribution%20for%20Python%20-%20Update%202.pdf)

- Implemented Scikit-Learn compatible Gradient Boosted Tree classifier, Decision Tree Classifier and tree-based Adaboost classifier in daal4py.
- Implemented computation of prediction probabilities in Scikit-Learn compatible RandomForest and Gradient Boosted Trees classifiers in daal4py.
- numpy package is updated to v1.18.5
- Scikit-learn package is updated to v 0.23.1
- Support of thunder SVM method for IDP sklearn in daal4py
- Performance optimizations for SVC fit and prediction, Elastic Net and LASSO fit, K-Means fit and prediction, PCA fit and transform, train_test_split
</details> 

#### Update 1
<details>
  <summary><b>Expand</b></summary>

[Release Notes](https://software.intel.com/sites/default/files/managed/e6/93/2020_Python_Release%20Notes%20Intel%28R%29%20Distribution%20for%20Python%20-%20Update%201.pdf)

- DBSCAN is accelerated in sklearn.
- Performance improvement for F-contiguous inputs in daal4py.
- Patches updated for compatibility with sklearn 0.22.
</details> 

#### 2020 Gold
<details>
  <summary><b>Expand</b></summary>

[Release Notes](https://software.intel.com/sites/default/files/managed/19/ed/2020-python-release-notes-intel-distribution-for-python-gold.pdf)

- Update to conda 4.7.12.
- Added support for Brownboost, Logistboost as well as Stump regression and Stump classification algorithms to daal4py.
- Added support for Adaboost classification algorithm, including support for method="SAMME" or "SAMMER" for multi-class data in daal4py.
- "Variable Importance" feature has been added to Gradient Boosting Trees in daal4py.
- Ability to compute class prediction probabilities has been added to appropriate classifiers, including logistic regression, tree-based classifiers, etc., in daal4py.
</details> 

### 2019
#### Update 5
<details>
  <summary><b>Expand</b></summary>

[Release Notes](https://software.intel.com/sites/default/files/managed/69/73/2019_Python_Release%20Notes%20Intel%28R%29%20Distribution%20for%20Python%20-%20Update%205.pdf)

- Single node support for DBSCAN, LASSO, Coordinate Descent (CD) solver algorithms through daal4py package
- Distributed model support for SVD, QR, K-means init++ and parallel++ algorithms through daal4py package
- Additional Scikit-Learn algorithms optimized using Intel® DAAL: Linear, Ridge, Logistic, PCA, KMeans, pairwise_distances and SVC
</details> 

#### Update 4
<details>
  <summary><b>Expand</b></summary>

[Release Notes](https://software.intel.com/sites/default/files/managed/4e/ac/2019_Python_Release%20Notes%20Intel%28R%29%20Distribution%20for%20Python%20-%20Update%204.pdf)

- New distributed model support for "Moments of low order" and "Covariance" algorithms through daal4py package
- Updated python package versions and their supported platforms
</details> 

#### Update 3
<details>
  <summary><b>Expand</b></summary>

[Release Notes](https://software.intel.com/sites/default/files/managed/f6/12/2019_Python_Release%20Notes%20Intel%28R%29%20Distribution%20for%20Python%20-%20Update%203.pdf)
  
- Extended availability of Intel® DAAL algorithms through daal4py package.
- Daal4py distributed mode support for scale-out to clusters & support for streaming mode for efficient memory handling.
- Updated python packages and their supported platforms.
</details> 

#### Update 2
<details>
  <summary><b>Expand</b></summary>
	
[Release Notes](https://software.intel.com/sites/default/files/managed/8f/c9/2019_Python_Release%20Notes%20Intel%28R%29%20Distribution%20for%20Python%20-%20Update%202.pdf)

- Intel® Distribution for Python 2019 Update 2 includes functional and security updates. Users should update to the latest version.
</details> 

#### Update 1
<details>
  <summary><b>Expand</b></summary>

 [Release Notes](https://software.intel.com/sites/default/files/managed/3b/7c/2019_Python_Release%20Notes%20Intel%28R%29%20Distribution%20for%20Python%20-%20Update%201.pdf)

- Scikit-learn optimizations for Logistic Regression, Random Forest Regressor & Classifier.
- New machine learning package (daal4py) with an easy to use API and performance accelerated by Intel® DAAL.
- Introducing Numba* threading layer abstraction that allows to switch between Intel® TBB (default) and OpenMP* threading layer.
- Access to MKL runtime settings available through easy-to-use Python control package (mkl-service)
</details> 

#### Initial Release
<details>
  <summary><b>Expand</b></summary>
	
[Release Notes](https://software.intel.com/sites/default/files/managed/d9/bc/2019_Python_Release%20Notes%20Intel%28R%29%20Distribution%20for%20Python%20-%20Gold.pdf)

- Intel® Distribution for Python now integrated into Intel® Parallel Studio XE 2019 installer. Also available as easy command line standalone install.
- Faster Machine learning with Scikit-learn: Support Vector Machine (SVM) and K-means prediction, accelerated with Intel® DAAL.
- XGBoost package included in Intel® Distribution for Python (Linux only).
- Note: The deep learning packages and computer vision packages along with their dependencies will not be included in Intel Distribution for Python, henceforth. However, the packages continue to be available in anaconda/Intel conda channel. Click on the [What's Included in the Intel® Distribution for Python\*](https://www.intel.com/content/www/us/en/developer/articles/tool/whats-included-distribution-for-python.html) to learn more.
</details> 

#### Notices and Disclaimers
Intel technologies may require enabled hardware, software or service activation.

No product or component can be absolutely secure.

Your costs and results may vary.

© Intel Corporation. Intel, the Intel logo, and other Intel marks are trademarks of Intel Corporation or its subsidiaries. Other names and brands may be claimed as the property of others.

No license (express or implied, by estoppel or otherwise) to any intellectual property rights is granted by this document.

The products described may contain design defects or errors known as errata which may cause the product to deviate from published specifications. Current characterized errata are available on request.

Intel disclaims all express and implied warranties, including without limitation, the implied warranties of merchantability, fitness for a particular purpose, and non-infringement, as well as any warranty arising from course of performance, course of dealing, or usage in trade.
