# Zeus21: An analytic code for 21-cm at cosmic dawn

Zeus21 encodes the effective model for the 21-cm power spectrum and global signal from [Muñoz 2023](https://arXiv:XXXX). The goal is to capture all the nonlocal and nonlinear physics of cosmic dawn in a light and fully Pythonic code. Zeus21 takes advantage of the approximate log-normality of the star-formation rate density (SFRD) during cosmic dawn to compute the 21-cm power spectrum analytically. It agrees with more expensive semi-numerical simulations to better than 10% precision, but has comparably negligible computational cost (~ s) and memory requirements.

Zeus21 (Zippy Early-Universe Solver for 21-cm) pairs well with data from [HERA](https://reionization.org/), but can be used for any 21-cm inference or prediction. Current capabilities include finding the 21-cm power spectrum (at a broad range of k and z), the global signal, IGM temperatures (Tk, Ts, Tcolor), neutral fraction xHI, Lyman-alpha fluxes, and the evolution of the SFRD; all across cosmic dawn z=5-35. Zeus21 can use three different astrophysical models, one of which emulates 21cmFAST, and can vary the cosmology through CLASS.

For a tutorial see `docs/`. Full documentation to appear soon. Here is an example power spectrum (at k=0.3/Mpc) and global signal as a function of redshift, for two cases of X-ray luminosity. You can run it yourself with the tutorial included!

<p align="center">
<img src="docs/PspecandGlobal_Zeus21.png" width=50% height=50%>
</p>

## Installation

You can download and install this package by doing:

```
git clone https://github.com/julianbmunoz/zeus21.git zeus21
cd zeus21/
pip install .
```

that should take care of all dependencies (remember to work in your favorite conda env). If you have issues with cache'd versions of packages you can add `--no-cache-dir` at the end of `pip install .`. 

**NOTE:** You may run into problems when pip-installing `classy` (the Python wrapper of `CLASS`). If so, their installation guide is [here](https://github.com/lesgourg/class_public/wiki/Installation), but in a gist the steps are:

```
git clone https://github.com/lesgourg/class_public.git class
cd class/
make
cd python/
python setup.py install --user
```

(modifying the Makefile to your `gcc` as needed)

## Citation

If you find this code useful please cite:
XXXXX
and include a link to [this Github](https://github.com/JulianBMunoz/Zeus21).
