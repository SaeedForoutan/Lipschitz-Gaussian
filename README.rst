.. Uniform Convergence of Lipschitz Functions with Dependent Gaussian Samples.

.. This project is under GNU v.3 license.

Uniform Convergence of Lipschitz Functions with Dependent Gaussian Samples
==========================================================================

|Latest Release| |Contributors| |Open Issues| |License|

This repository contains the research paper and code related to **Uniform Convergence of Lipschitz Functions with Dependent Gaussian Samples**. The work provides theoretical bounds for learning Lipschitz functions with dependent Gaussian data and includes experimental results.

Numerical experiments are in the `examples/` folder.

.. note::
    The ICASSP 2025 paper referenced here is currently not public. We will share further details and its publication status soon.


.. Examples

Examples
--------

The `examples/` folder contains **Jupyter notebooks** (`.ipynb` files) that reproduce the results presented in the paper. In version 0.1.1, we have included the notebooks with the exact results from the paper. As we develop future versions, the first version will be archived in the Releases section for later access. 

The following notebooks are provided as examples corresponding to the numerical results sections of the paper:

- `Simulation.ipynb`
- `TempPrediction_RealWorld.ipynb`
- `GeneExpression_RealWorld.ipynb`
- `SP500_RealWorld.ipynb`

To run an example:

.. code:: bash

   jupyter notebook examples/Simulation.ipynb

This will open the notebook and display outputs that match the theoretical results presented in the research paper.


.. Simple Example

Simple Example
--------------

A basic Python script to check data behavior and uniform convergence:

.. code:: python

   import numpy as np
   import matplotlib.pyplot as plt

   # Generate dependent Gaussian samples
   n = 100
   gamma = 0.5  # Dependency factor
   x = np.random.randn(n)
   for i in range(1, n):
       x[i] = gamma * x[i-1] + np.sqrt(1 - gamma**2) * np.random.randn()

   # Plot the dependent data
   plt.plot(x)
   plt.title("Generated Dependent Gaussian Data")
   plt.show()

.. Test

Testing
-------

After installation, you can run unit tests with:

.. code:: bash

   pytest tests/

We test against Python versions **3.8, 3.9, 3.10, 3.11**.

.. Versioning

Versioning and Releases
------------------------

We follow a versioning system to track changes and improvements in the project. Each version will include updates, bug fixes, or additional features.

- **Version 0.1.1**: Initial release with Jupyter notebooks reproducing the results in the paper. The exact outputs from the paper are included.
  
As the project progresses, older versions will be archived and made available in the **Releases** section for reference. You can always access previous versions there.



.. Contributions

Contributions
-------------

We welcome contributions!  
If you find a bug or want to suggest an improvement, please open an issue or submit a pull request.

To set up a development environment:

.. code:: bash

   git clone https://github.com/SaeedForoutan/Lipschitz-Gaussian.git
   cd Lipschitz-Gaussian
   pip install -e .

.. License

License
-------

This project is licensed under the terms of the **GNU General Public License v3.0**.

You can view the full license text here: https://www.gnu.org/licenses/gpl-3.0

By using this repository, you agree to comply with the terms and conditions of the GPL-3.0 license.


.. Citing

Citing
------

If you use this repository or the associated methods in your research, please cite the following paper:

**Mina Sadat Mahmoudi**, **Saeed Foroutan**, **Seyed Abolfazl Motahari**, **Babak Khalaj**.  
**Uniform Convergence of Lipschitz Functions with Dependent Gaussian Samples**.  
ICASSP 2025.

.. note::

   A BibTeX citation entry will be provided after publication notification.

.. Acknowledgments

Acknowledgments
---------------

This research was supported by the **Iran National Science Foundation (INSF)** under contract No. 99022756.

.. Badges

.. |Latest Release| image:: https://img.shields.io/github/v/release/SaeedForoutan/Lipschitz-Gaussian
   :target: https://github.com/SaeedForoutan/Lipschitz-Gaussian/releases

.. |Contributors| image:: https://img.shields.io/github/contributors/SaeedForoutan/Lipschitz-Gaussian
   :target: https://github.com/SaeedForoutan/Lipschitz-Gaussian/graphs/contributors

.. |Open Issues| image:: https://img.shields.io/github/issues/SaeedForoutan/Lipschitz-Gaussian
   :target: https://github.com/SaeedForoutan/Lipschitz-Gaussian/issues

.. |License| image:: https://img.shields.io/badge/License-GPLv3-blue.svg
   :target: https://www.gnu.org/licenses/gpl-3.0


