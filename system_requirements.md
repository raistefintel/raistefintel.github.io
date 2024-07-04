# Introduction
This document provides details about hardware, operating system, and software prerequisites for the [Intel® Distribution for Python*](https://www.intel.com/content/www/us/en/developer/tools/oneapi/distribution-for-python.html).

Release notes can be found in a [dedicated article.](https://github.com/raistefintel/raistefintel.github.io/blob/main/release_notes.md))


# Supported Host Operating Systems
These OS distributions are tested by Intel or known to work; other distributions may or may not work and are not recommended. If you have questions, access the [Intel Community Forums](https://community.intel.com/t5/Developer-Software-Forums/ct-p/developer-software-forums) when you need assistance.

If you have [Commercial Support](https://supporttickets.intel.com/s/?language=en_US), create a support ticket.

## Operating systems:

Note: These OS distributions are tested by Intel or known to work; other distributions may or may not work and are not recommended. If you have questions, access the [Intel Community Forums](https://community.intel.com/t5/Developer-Software-Forums/ct-p/developer-software-forums) when you need assistance.  If you have [Commercial Support](https://supporttickets.intel.com/s/?language=en_US), create a support ticket.

- Linux*
- Windows® 10
- Windows® 11
 
# Supported Target Hardware Platforms

## CPUs:
- Intel® Core™ processor family
- Intel® Xeon® processor family

## GPUs:
- Intel® UHD Graphics for 11th generation Intel processors or newer
- Intel® Iris® Xᵉ graphics
- Intel® Arc™ graphics
- Intel® Data Center GPU Flex Series
- Intel® Data Center GPU Max Series


# Software Requirements

### Language: 
- Python 3.9, Python 3.10

### Package management:
- conda*
- pip

### For Linux users
- The driver packages needed on Linux are described in the
  [Data Center GPU Series Driver Installation](https://dgpu-docs.intel.com/driver/installation.html) and
  [Client GPU Driver Installation](https://dgpu-docs.intel.com/driver/client/overview.html) pages.

### For Windows users
- For GPU development, the latest GPU drivers need to be installed. This can be
  downloaded from [Intel® Arc™ & Iris® Xe Graphics - Windows*](https://www.intel.com/content/www/us/en/download/785597/intel-arc-iris-xe-graphics-windows.html).
	- Note: see [Installation Guide for Intel® oneAPI Toolkits](https://www.intel.com/content/www/us/en/developer/articles/guide/installation-guide-for-oneapi-toolkits.html) on how to install the GPU drivers.




# Development Environment

**Compatible with**:
- Microsoft Visual Studio*
- PyCharm*

# Notices and Disclaimers
Intel technologies may require enabled hardware, software or service activation.

No product or component can be absolutely secure.

Your costs and results may vary.

© Intel Corporation. Intel, the Intel logo, and other Intel marks are trademarks of Intel Corporation or its subsidiaries. Other names and brands may be claimed as the property of others.

No license (express or implied, by estoppel or otherwise) to any intellectual property rights is granted by this document.

The products described may contain design defects or errors known as errata which may cause the product to deviate from published specifications. Current characterized errata are available on request.

Intel disclaims all express and implied warranties, including without limitation, the implied warranties of merchantability, fitness for a particular purpose, and non-infringement, as well as any warranty arising from course of performance, course of dealing, or usage in trade.
