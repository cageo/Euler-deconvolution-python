# Reliable Euler deconvolution estimates throughout the vertical derivatives of the total-field anomaly

by
Felipe F. Melo and Valéria C.F. Barbosa

## About

This paper has been submitted for publication in the journal *Computers & Geosciences*.

This repository contains the source code to perform the first synthetic test presented. The codes `euler_python.py`, the synthetic data `synthetic_data.dat` of the first test presented in the paper and the codes `synthetic_test.py`, `estimates_statistics.py` and `plot_functions.py` to generate the results of the synthetic test related to our methodology.

The *euler_python* program is compatible with both Python 2.7 and Python 3.7 programming language.
 
## Abstract

We propose a novel methodology to select reliable Euler deconvolution estimates throughout the vertical derivatives of the total-field anomaly grounded on the capability of this quantity to locate anomalies due to its higher signal decay with distance. In applying Euler deconvolution to a small moving-data window, we compute the standard deviation of the vertical derivatives of the total-field anomaly for each data window. Then, we define the reliable source-location estimates as those estimates that are obtained by using the data windows with the largest standard deviations of the vertical derivatives of the total-field anomaly. For all tentative values of the structural index (SI), the reliable estimates with tight clustering define the correct SI and the mean of these estimates define the source position. Our methodology successfully works in two complex scenarios. In the first one, multiple sources with distinct SI generate a total-field anomaly which in turn is corrupted by an additive nonlinear background that simulates a regional field. This regional field strongly interfere the anomalies produced by the sources, changing their amplitudes and shapes. In the second scenario, nearby sources give rise to strongly interfering anomalies. In both scenarios, our methodology correctly defines the SIs, the horizontal positions and the depths of the causative sources. Application to real magnetic anomaly from southern Brazil allows inferring the presence of a plug intrusion.

## Content

- euler_python.py:
	General Python module containing the functions to compute de derivatives and 
	Euler deconvolution.
	
- synthetic_test.py:
	Python script to generate the synthetic results. The script loads the total-field
	anomaly of a synthetic model from the file "synthetic_data.dat" and computes the
	Euler deconvolution using the functions in "euler_python.py". The results are 
	generated using the functions "plot_functions.py" for the plots and 
	"estimates_statistics.py" to compute the statistics of the data.
	
- plot_functions.py:
	Python script to generate the figures 2d, 4 and 7 of the first synthetic test. 
	
- estimates_statistics.py:
	Python script to compute the mean of the northing, easting and depth estimates. 
	
Test data:

- synthetic_data.dat:
		Synthetic total-field anomaly data generated using the Python packaged
		"Fatiando a Terra": http://fatiando.org/. This data is an example used
		in the current publication and shown in figure 2d.

## Getting the code

You can download a copy of all the files in this repository by cloning the
[git](https://git-scm.com/) repository:

    git clone https://github.com/ffigura/Euler-deconvolution-python.git

or [download a zip archive](https://github.com/ffigura/Euler-deconvolution-python/archive/master.zip).


## Dependencies

The Python program for Euler deconvolution "euler_python.py" and the scripts "synthetic_test.py"
and "estimates_statistics.py" require the Python package "numpy", and the script "plot_functions.py"
requires the Python packages "numpy" and "matplotlib". 
The easier way to get Python and all libraries installed is through the Anaconda Python 
distribution (https://www.anaconda.com/distribution/). After installed Anaconda, install the libraries 
by running the following command in your terminal:

	conda install numpy matplotlib

The program for Euler deconvolution "euler_python.py" and the additional codes "synthetic_test.py",
"plot_functions.py" and "estimates_statistics.py" are compatible with both Python 2.7 and 3.7.

## Reproducing the results

The results and figures (2d, 4 and 7) for the synthetic test are reproducible from the folder `/test_4_sources`.
Running the code `synthetic_test.py` will allow the reprodution of the results of our methodology. For more information
read the file `README.MD` or `README.txt` in the folder `/code`.


## License

All source code is made available under a BSD 3-clause license. You can freely
use and modify the code, without warranty, so long as you provide attribution
to the authors. See `LICENSE.md` for the full license text.

The manuscript text is not open source. The authors reserve the rights to the
article content, which is currently submitted for publication in the
*Computers & Geosciences*.
