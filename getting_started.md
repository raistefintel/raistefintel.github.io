# Get Started with the Intel® Distribution for Python\*
The Intel® Distribution for Python\* is a cluster of packages including NumPy, SciPy, scikit-learn, XGBoost and Data Parallel Extensions for Python*. It contains packages that are optimized via the Intel® oneAPI Math Kernel Library (oneMKL) and the Intel® oneAPI Data Analytics Library (oneDAL) to make Python\* application more efficient.

## Supported Installation Options

### Install via Anaconda
1. Follow [Conda Installation Guide](https://docs.conda.io/projects/conda/en/latest/user-guide/install/) to install Conda in your environment. If you already have conda installed in your system, please update your conda:
   ```
   conda update conda
   ```
2. Add Intel channel. <br>
  Tell conda to choose Intel packages over default packages, when available.
    ```
    conda config --add channels intel
    ```
3. Install Intel Distribution for Python\* via conda. We recommend that you create a new environment while installing. To install the core python3 environment, run:
   ```
   conda create -n idp intelpython3_core python=3.x
   ```
   **Please note that “x” in “python=3.x” should signify which version of Python\* you would like to install.** For example, for Python\* version 3.9: conda create -n idp intelpython3_core python=3.9.
4. Activate the conda environment:
   ```
   conda activate idp
   ```
## Sanity Check
After the activation of the environment, type `python` in the command line to find the Python\* distribution info.
- Linux\* & Windows\*: `python` <br>
  The distribution info should include `Intel Corporation`:
    * Linux:
      ```
      Python 3.7.10 (default, Jun 4 2021, 06:52:02)
      [GCC 9.3.0] :: Intel Corporation on linux
      Type "help", "copyright", "credits" or "license" for more information.
      Intel(R) Distribution for Python is brought to you by Intel® Corporation.
      Please check out: https://software.intel.com/en-us/python-distribution
      ```
    * Windows:
      ```
      Python 3.9.10 (main, Mar 21 2022, 08:44:00) [MSC v.1916 64 bit (AMD64)] :: Intel Corporation on win32
      Type "help", "copyright", "credits" or "license" for more information.
      Intel(R) Distribution for Python is brought to you by Intel Corporation.
      Please check out: https://software.intel.com/en-us/python-distribution
      ```
  These methods can be used as a sanity check that Intel Distribution for Python is properly installed.

## Sample Code
Run this numpy sample code in a stock Python\* environment and in an IntelPython environment. You will see benefits from IntelPython.
```
import numpy as np
import time
  
start = time.time()
  
rd = np.random.RandomState(88)
a = rd.randint(1,1000,(1000,1000))
y = rd.randint(1,1000,(1000))
res = np.linalg.solve(a,y)
  
end = time.time()
  
print(res)
print('Time consumed:',end-start)
```

## Build Your Own Project
No special modifications to your existing Python* projects are required to start using them with this toolkit. Check out the [Reference Section](#references) for Github samples.

## References
- [Intel Distribution for Python Landing Page](https://huiyan2021.github.io/intelpython.github.io/2023.1.1/getting_started.html)
- [Intel AI Tools Landing Page](https://www.intel.com/content/www/us/en/developer/tools/oneapi/ai-analytics-toolkit.html)
- [Code Samples](https://github.com/oneapi-src/oneAPI-samples/tree/master/AI-and-Analytics/Getting-Started-Samples)

## Support
If you have further questions or need support on your workload optimization, please submit your queries to the Intel® Distribution for Python\* Forum or [IntelPython](https://github.com/IntelPython) GitHub, on the Issues or Discussions pages depending on the type of support required.

## Notices and Disclaimers
Performance varies by use, configuration and other factors. Learn more at www.Intel.com/PerformanceIndex. <br>
<br>
Performance results are based on testing as of dates shown in configurations and may not reflect all publicly available updates. See backup for configuration details. No product or component can be absolutely secure. <br>
<br>
Your costs and results may vary.<br>
<br>
Intel technologies may require enabled hardware, software or service activation.<br>
<br>
© Intel Corporation. Intel, the Intel logo, and other Intel marks are trademarks of Intel Corporation or its subsidiaries. Other names and brands may be claimed as the property of others.
  

      
    
