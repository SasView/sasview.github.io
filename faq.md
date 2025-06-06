---
layout: page
title: FAQ
subtitle: Here are the answers to some common questions about SasView
---

[What is SasView?](#what-is-sasview)

[Is there a SasView Manual?](#is-there-a-sasview-manual)

[What platforms does SasView run on?](#what-platforms-does-sasview-run-on)

[Do I need to install Python or C or any compilers before I install SasView?](#do-i-need-to-install-python-or-c-or-any-compilers-before-i-install-sasview)

[What do xcrun errors mean?](#what-do-xcrun-errors-mean)

[Can SasView make use of my GPUs?](#can-sasview-make-use-of-my-gpus)

[Can I stop SasView trying to use my GPUs?](#can-i-stop-sasview-trying-to-use-my-gpus)

[Can I use SasView to analyse SANS or USANS data?](#can-i-use-sasview-to-analyse-sans-or-usans-data)

[Can I use SasView to analyse SAXS or USAXS data?](#can-i-use-sasview-to-analyse-saxs-or-usaxs-data)

[Can I use SasView to analyse SE(M)SANS data?](#can-i-use-sasview-to-analyse-sesans-data)

[Can SasView be used in a commercial environment?](#can-sasview-be-used-in-a-commercial-environment)

[What format should my data be in?](#what-format-should-my-data-be-in)

[What units should my data be in?](#what-units-should-my-data-be-in)

[Why is SasView no longer loading my data?](#why-is-sasview-no-longer-loading-my-data)

[Does SasView fit data in its I vs Q representation, or as Log I vs Log Q?](#does-sasview-fit-data-in-its-i-vs-q-representation-or-as-log-i-vs-log-q)

[Many models have a _scale_ parameter; what is this?](#what-is-the-scale-parameter-in-models)

[How can I put my data on an absolute intensity scale?](#how-can-i-put-my-data-on-an-absolute-intensity-scale)

[Why do I get non-sensical parameter values if I try to simultaneously model-fit the scale factor and the scattering length densities?](#why-do-i-get-non-sensical-parameter-values-if-i-try-to-simultaneously-model-fit-the-scale-factor-and-the-scattering-length-densities)

[What value should I use to specify polydispersity?](#what-value-should-i-use-to-specify-polydispersity)

[Is the Schulz(-Zimm) polydispersity function used in SasView a number-average or a weight-average distribution?](#is-the-schulz-zimm-polydispersity-function-used-in-sasview-a-number-average-or-a-weight-average-distribution)

[What about the other polydispersity functions used in SasView?](#what-about-the-other-polydispersity-functions-used-in-sasview)

[How do I load an image file as data?](#how-do-i-load-an-image-file-as-data)

[Where do the model parameter uncertainties come from?](#where-do-the-model-parameter-uncertainties-come-from)

[Why do I get different parameter uncertainties using the Simple and Complex fitting engines?](#why-do-i-get-different-parameter-uncertainties-using-the-simple-and-complex-fitting-engines)

[Why do I sometimes get different 'goodness-of-fit' values when pressing Enter or Compute compared to pressing Fit?](#why-do-i-sometimes-get-different-goodness-of-fit-values-when-pressing-enter-or-compute-compared-to-pressing-fit)

[Why have I got several instances of the same model category (eg, 'Shape Independent' and 'Shape-Independent')?](#why-have-i-got-several-instances-of-the-same-model-category-eg-shape-independent-and-shape-independent)

[Why is SasView not loading the model parameters from some of my existing .fitv (Save Fit) files?](#why-is-sasview-not-loading-the-model-parameters-from-some-of-my-existing-fitv-save-fit-files)

[Why is Save Analysis (File menu) greyed out after I fit a model?](#why-is-save-analysis-file-menu-greyed-out-after-i-fit-a-model)

[Why does Check for Updates not work?](#why-does-check-for-updates-not-work)

[Why is SasView no longer able to run my existing custom models?](#why-is-sasview-no-longer-able-to-run-my-existing-custom-models)

[How can I see the separate contributions of the form factor and structure factor?](#how-can-i-see-the-separate-contributions-of-the-form-factor-and-structure-factor)

[How can I include a structure factor in a model?](#how-can-i-include-a-structure-factor-in-a-model)

[What is the Model Marketplace?](#what-is-the-model-marketplace)

[Where does SasView expect to find custom models?](#where-does-sasview-expect-to-find-custom-models)

[Can I use complex numbers in my models?](#can-i-use-complex-numbers-in-my-models)

[Can I run Python scripts inside SasView?](#can-i-run-python-scripts-inside-sasview)

[Why will SasView no longer start? ('cannot execute script sasview')](#why-will-sasview-no-longer-start)

### What is SasView?

*   SasView is software for the analysis of Small-Angle Scattering (SAS) data, including Spin-Echo SANS (SESANS) data.
*   It fits analytic functions describing different types of material microstructure to experimental data in order to determine the shape, size and degree of ordering.
*   SasView also includes tools for calculating scattering length densities, slit sizes, resolution, fringe thicknesses/d-spacings, the (Porod) invariant ('total scattering'), distance distribution functions, and correlation functions.

### Is there a SasView Manual?

*   If you really want to chop down a tree then you can print a [PDF download](/downloads/SasViewDocumentation_4.2.2.pdf) of the full documentation package for version 4.2.2.
*   Otherwise we would recommend that you just visit our extensive [online documentation](/documentation)! This is the same documentation shipped with each release of SasView.

### What platforms does SasView run on?

| Platform | Version | Operating System |
| --- | --- | --- |
| Windows | | |
| | SasView 6.0.x and later | 64-bit only (x64) |
| | SasView 5.0.x           | 64-bit only (x64) |
| | SasView 4.2.x           | 64-bit (x64) only |
| | SasView 4.1.x           | 32-bit (x86) & 64-bit (x64) |
| | SasView 4.0.x           | 32-bit (x86) & 64-bit (x64) |
| | SasView 3.x             | 32-bit (x86) & 64-bit (x64) |
| | SasView 2.x             | 32-bit only (x86) |
| Mac OS | | |
| | SasView 6.0.x and later | 64-bit OSX |
| | SasView 5.0.4 and later | 64-bit OSX (10.15, Catalina or later; but will install on 10.13 by clearing the extended attributes on the package: xattr -cr /Applications/SasView5.app)
| | SasView 5.0.3           | 64-bit OSX (10.13, High Sierra or later) |
| | SasView 5.0.2           | 64-bit OSX |
| | SasView 5.0.1           | 64-bit OSX |
| | SasView 5.0.0           | 64-bit OSX (10.9, Mavericks or later) |
| | SasView 4.x             | 64-bit OSX (10.9, Mavericks or later) |
| | SasView 3.x and earlier | 32-bit OSX (10.6, Snowleopard) |

*   We do not currently _support_ a Linux distribution, but:
    *   An 'official' Flatpak distribution of SasView can be found on [Flathub](https://flathub.org/apps/org.sasview.sasview). This has been tested on a variety of Linux distributions including Ubuntu, Fedora, and Rocky Linux.
    *   The STFC [IDAaaS](https://isis.analysis.stfc.ac.uk/) cloud computing service runs SasView 4.2.2, 5.0.6 and the latest SasView 6 on Rocky Linux (though 4.2.2 and 5.0.6 previously also ran on IDAaaS under CentOS).
    *   And there is also a third-party project developing SasView on [Debian](https://github.com/SasView/sasview/wiki/DevNotes_Projects_Debian)
    *   You are welcome to try [building SasView from the source](https://github.com/SasView/sasview/wiki/DevNotes_CondaDevEnviroment) available on the release pages: [https://github.com/SasView/sasview/releases](https://github.com/SasView/sasview/releases). Please note, you will need to download our 'sasmodels' repository from [https://github.com/SasView/sasmodels](https://github.com/SasView/sasmodels) before you try this. But also note that our Wiki instructions direct you to use Conda. Anaconda changed their Terms of Service in 2020, and updated them again in 2024, and certain organisations now need to pay to use it. We are looking at other tools and will update the instructions at a later date.

### Do I need to install Python or C or any compilers before I install SasView?

*   If you intend to use SasView on a Windows computer, then No: Our packaged installer ships with everything you need to run SasView.
*   If you intend to use SasView on a Mac OS computer, you do not need to install Python but you _do_ need to pre-install the Xcode command line tools as SasView makes use of the C compiler in them. If Xcode is not installed the SasView console or log file may contain messages about 'xcrun: error' or 'missing xcrun at:'.
    *  _You should not need to install the full Xcode package_, just a subset of it; try the command: __xcode-select -install__.
    *  If this command does not subsequently allow you to use SasView, or, if you require the full Xcode package for other purposes, you can get Xcode from the Apple AppStore. However, **be aware that attempting to install the latest version of Xcode may require you to upgrade your version of MacOS**. If you do not want to do that you will need to install a version of Xcode that is compatible with your current version of MacOS. [This site](https://xcodereleases.com/) may be useful in this respect.

### What do xcrun errors mean?
*   You will get these errors if you are trying to use SasView on a Mac and do not have the Xcode command line tools installed. See the preceding answer.

### Can SasView make use of my GPUs?

*   GPU support is only available in SasView 4.x and later.
*   Click on Fitting > GPU Options. If a potential GPU is present it will be displayed. Click on the Test button to have SasView check the suitability of the device and its drivers. For more information, see the [SasView Help documentation](https://www.sasview.org/docs/user/qtgui/Perspectives/Fitting/gpu_setup.html).

### Can I stop SasView trying to use my GPUs?

*   Yes. Create a system environment variable called SAS\_OPENCL and give it the value 'None'.

### Can I use SasView to analyse SANS or USANS data?

*   Yes.

### Can I use SasView to analyse SAXS or USAXS data?

*   Yes, especially if your intensity data is in absolute units (/cm).

### Can I use SasView to analyse SESANS data?

*   Yes. SasView can apply a [Hankel Transform](https://www.sasview.org/docs/user/qtgui/Perspectives/Fitting/sesans/sans_to_sesans.html) to a normal fitting model.

### Can SasView be used in a commercial environment?

*   Yes, provided you accept the terms of our [license](https://github.com/SasView/sasview/blob/master/LICENSE.TXT). There is no license fee.

### What format should my data be in?

*   SasView recognizes 1D data supplied in a number of specific formats, as identified by the file extensions below (which are not case-sensitive). It also incorporates a 'generic loader' which is called if all else fails. The generic loader will attempt to read data files of any extension provided the file is in ASCII ('text') format (i.e. not binary). So this includes, for example, comma-separated variable (CSV) files from a spreadsheet.
    *  .ABS (NIST format)
    *  .ASC (NIST format)
    *  .COR (CanSAS XML v1.0 and v1.1 formats only)
    *  .DAT (NIST format)
    *  .H5, .NXS, .HDF, or .HDF5 (in NXcanSAS v1.0 and v1.1 formats only)
    *  .PDH (Anton Paar SAXSess format)
    *  .XML (CanSAS XML v1.0 and 1.1 formats only)

*   SasView recognizes 2D data only when supplied in ASCII ('text') files or HDF5 files in the NeXus NXcanSAS format with the extensions below (which are not case-sensitive):
    *  .ASC (NIST format)
    *  .DAT (NIST format)
    *  .H5, .NXS, .HDF, or .HDF5 (in NXcanSAS v1.0 and v1.1 formats only)

*   2D image data can be translated into 2D 'pseudo-data' using the [Image Viewer Tool](https://www.sasview.org/docs/user/qtgui/Calculators/image_viewer_help.html).

*   SasView also recognizes 1D SESANS data arranged in separated columns in ASCII files with the following extensions (which are not case-sensitive):
    *  .SES (in ISIS/RID format)
	*  .SESANS (in ISIS/RID format)
	
*   And the Generic Scattering Calculator tool in SasView recognises coordinate in ASCII data files with the following extensions (which are not case-sensitive):
    *  .PDB (Protein Data Bank format)
    *  .OMF (OOMMF micromagnetic simulation format)
    *  .SLD (Spin-Lattice Dynamics simulation format)
	*  .VTK (Visualisation ToolKit format - from SasView v5.0.5)
	
*   Since SasView 4.1, the File Converter tool in SasView will convert data in the following legacy formats to the CanSAS .XML (for 1D data) or NXcanSAS .H5 (for 2D data) formats:
    *  BSL/OTOKO
    *  FIT2D and some other 'by analogy' SAXS-oriented software
	*  COLETTE (or 'RKH') 2D
	*  The first two of these are notable for containing the Q and I(Q) data in separate files.
	
#### 1D data (I(Q) vs Q)

*   The ASCII ('text') files are expected to have 2, 3, or 4 columns of values, separated by whitespaces or commas or semicolons, in the order Q, I(Q), ( dI(Q), dQ(Q) ), where dI(Q) is the uncertainty on the intensity value, and dQ(Q) is the instrumental resolution in Q, assumed to have arisen from pinhole geometry. Slit-smeared data can also be handled but is more involved. See the [Data Formats](https://www.sasview.org/docs/user/qtgui/MainWindow/data_formats_help.html) help for more information.

#### 2D data (I(Qx,Qy) vs Qx & Qy)
    
*   Most of the header lines in the NIST 2D format can be removed _except the last line_, and only the first three columns (i.e. Qx, Qy, and I(Qx,Qy)) are actually required.

#### SESANS data (P(z) vs z)

*   SasView currently recognises the data format used on the LARMOR instrument at the ISIS Pulsed Neutron & Muon Source and the SESANS at the RID, Technical University Delft whilst discussions take place under the auspices of CanSAS on extensions to the NXcanSAS format (see 2D data above).
*   The file format starts with a list of name-value pairs which detail the general experimental parameters necessary for fitting and analyzing the data. This list should contain all the information necessary for the file to be 'portable' between users.
*   Note that the SESANS reader in SasView checks for, and requires, a subset of the name-value pairs. Specifically:
    * "FileFormatVersion" - The version of the SESANS data format used. The current version is 1.0.
    * SpinEchoLength_unit - The unit for the spin-echo length. The default is Angstroms.
    * Wavelength_unit - The wavelength unit. The default is Angstroms^-2 cm^-1.
    * BEGIN_DATA -  A flag immediately before the data header.
*   Following the header are up to 8 space-delimited columns of experimental variables of which the first 4 columns are required. For example:

```
  FileFormatVersion       1.0
  DataFileTitle           <text string>
  Sample                  <text string>
  Settings                <text string>
  Operator                <text string>
  Date                    <text string>
  ScanType                <text string>
  Thickness               x.xxE-xx
  Thickness_unit          <mm/cm/etc>
  Theta_zmax              <decimal number>
  Theta_zmax_unit         <radians/degrees>
  Theta_ymax              <decimal number>
  Theta_ymax_unit         <radians/degrees>
  Orientation             <Z/Y/X>
  SpinEchoLength_unit     <A/nm/um/etc>
  Depolarisation_unit     <A-2 cm-1/nm-2 cm-1/etc>
  Wavelength_unit         <A/nm>

  BEGIN_DATA
  SpinEchoLength Depolarisation Depolarisation_error SpinEchoLength_error Wavelength Wavelength_error Polarisation  Polarisation_error
  391.56 0.0041929 0.0036894 19.578 2.11 0.1055 1.0037 0.0032974
  etc
```

#### Further Information

[ASCII](https://en.wikipedia.org/wiki/ASCII)

[HDF](https://en.wikipedia.org/wiki/Hierarchical_Data_Format)

[NeXuS](https://en.wikipedia.org/wiki/Nexus_(data_format))

[NeXus format](https://www.nexusformat.org/)

[CanSAS SASXML format](http://www.cansas.org/formats/canSAS1d/1.1/doc/) Also available as a [PDF document](http://www.cansas.org/trac/export/265/1dwg/tags/v1.0/doc/cansas-1d-1_0-manual.pdf)

[NXcanSAS format](https://manual.nexusformat.org/classes/applications/NXcanSAS.html)

[NIST 1D/2D formats](https://github.com/sansigormacros/ncnrsansigormacros/wiki)

[COLETTE (or 'RKH') 1D/2D formats](https://www.isis.stfc.ac.uk/Pages/colette-ascii-file-format-descriptions.pdf)

[BSL/OTOKO format](http://www.diamond.ac.uk/Beamlines/Soft-Condensed-Matter/small-angle/SAXS-Software/CCP13/BSL.html)

### What units should my data be in?

#### Q data

*   SasView assumes that Q data is in units of /Angstroms. If your Q data is in units of /nm (or anything else) you will get incorrect parameters from your model fits. _However_ if your data is in [canSAS](http://www.cansas.org) format and the Q unit is specified as /nm - ie, the XML specifies Q unit="1/nm" - SasView will internally convert the Q data to Å.

#### I(Q) data

*   SasView makes no assumptions about the units of I(Q) data, _but_ your model fits will only return meaningful scale parameters (ie, volume fractions) if the I(Q) data is in absolute units (/cm) and on an absolute scale (ie, the I(Q) values have been calibrated against a standard).

### Why is SasView no longer loading my data?

*   Any data files that used to load in SasView 4.x should load in SasView 5.x, but there are a small number of exceptions:

    *  The NeXus data loader was removed in version 5.0 as it was superseded by the integration of a loader for [NXcanSAS format](https://manual.nexusformat.org/classes/applications/NXcanSAS.html?highlight=nxcansas) files with the extension .h5.
    *  SasView 4.x was built with Python 2, but SasView 5.x is built with Python 3. The [Python Software Foundation](https://www.python.org/psf-landing/) decided to fundamentally change the way that character strings are represented internally in Python 3 and, thereby, the assumptions that Python 3 makes about the encoding (the byte-level representation) of characters. If the character encoding of your data file does not match those assumptions it is possible that SasView will throw an error. Depending on the version of SasView you are running you may see an error such as the following in the Message Log, Console or Log File:
    ```
      14:26:27 - ERROR: 'utf-8' codec can't decode byte 0xc5 in position 2: invalid continuation byte
    ```
    *  We are attempting to trap and process such cases, but this is not straightforward. In such instances, try changing/fixing the encoding of your file to UTF-8. A simple way to do this (for Windows users) is to install [Notepad++](https://notepad-plus-plus.org/). Open your data file in it, then navigate to Encoding > Convert to UTF-8, and save the file. Then try loading the file in SasView.

### Does SasView fit data in its I vs Q representation, or as Log I vs Log Q?

*   SasView assumes that the data values it loads are _not_ Log values. But the default behaviour of the program is to display the data and fit as Log I vs Log Q.
*   If you want to change how the data and fit are displayed, right-click on the plot and choose _Change Scale_.
    *   _NB: when using log representation, SasView applies `Log10` and not `Loge`._
*   However, SasView has no way of knowing if the data it has loaded is actually I vs Q. It will happily load and fit, for example, Reflectivity vs Q, but simply label the Y-axis as Intensity.

### What is the scale parameter in models?

*   If your I(Q) data is in absolute units (/cm) and on an absolute scale (ie, the I(Q) values have been calibrated against a standard) the scale parameter will be equal to the volume fraction. In all other instances the scale factor will be a number proportional to the volume fraction. Some models have both volume fraction and scale parameters. In these models the scale is just a multiplying factor (equal to 1 if the data is in absolute units on an absolute scale).
  
*   We are aware that some of the model descriptions in the Help documentation are unclear about the meaning of _scale_ and are working to improve the documentation.

### How can I put my data on an absolute intensity scale?

*   By comparing the intensity of scattering from your samples with that from a standard sample measured under identical conditions with the same instrument geometry. In most instances it will be a simple linear scaling, _provided_ the sample and standard transmissions (transmission = 1 - absorbtion) have been accounted for during the data reduction. Consult your beamline scientist/local contact.

### Why do I get non-sensical parameter values if I try to simultaneously model-fit the scale factor and the scattering length densities?

*   Because these parameters are correlated. You must either fix the scale or the scattering length densities (at least, until your fit has almost converged).

### What value should I use to specify polydispersity?

*   This will depend on the actual type of polydispersity function you choose, but will be related to some ratio of the 'width' of the size distribution and the mean value of the parameter that the polydispersity is being enabled for (eg, a particle radius). For example, for a Schulz polydispersity function the PD parameter in SasView is standard\_deviation/average\_value. In most (meaningful) instances 0 <= PD < 1.

### Is the Schulz(-Zimm) polydispersity function used in SasView a number-average or a weight-average distribution?

*   **SasView assumes the underlying polydispersity function is a number-distribution** and therefore the reported mean from that distribution is a number-average parameter. But SasView does properly weight the function by volume when fitting to the scattering data as is required to fit data in absolute units.
*   _However_, it is also clear that the literature has conflicting views about what the correct form of a number-average Schulz distribution should be. In essence there are _two_ different distributions which are being called the Schulz distribution. These are unfortunately related through mass. SasView, like several other well-known and well-used model-fitting packages, uses the form of the distribution given in the M. Kotlarchyk & S-H. Chen paper (J. Chem. Phys. 79 (1983) 2461-2469) which specifically identifies it as a number-average distribution. This is also the same Schulz number-average distribution given by Aragon & Pecora (J. Chem. Phys. 1976) and Bartlett and Ottewill (J. Chem. Phys. 1992), among others. On the other hand, the earlier papers using this distribution were specifically applied to degrees of polymerization and were clear that they viewed the equivalent formula to be a weight-average distribution. It now seems that at least Welch & Bloomfield (J. Pol. Sci. 1973) and Huber (2012) use the same equation as Aragon & Pecora's number-average formula but define it as a weight-average formula and then derive a new number-average formula from this.
*   (February 2015) After further investigation we have concluded that our implementation of the Schulz polydispersity function is sound. Our definition of the _z_ parameter, describing the width of the distribution, has exactly the same mathematical form whether defined as a number-average of a number-average distribution or as a weight-average of a weight-average distribution. But in some papers _z_ is defined as _z+1_ which clearly would give a different mathematical behaviour.

### What about the other polydispersity functions used in SasView?

*   These are implemented as number-distributions also.

### How do I load an image file as data?

*   Use 'Tool' > 'Image Viewer' and **not** 'File' > 'Load Data File(s)' or the 'Load Data' button on the Data Explorer.
*   SasView will load images in .BMP, .GIF, .JPG, .PNG and .TIF formats. The file extension is not case-sensitive.

### Where do the model parameter uncertainties come from?

*   How the parameter uncertainties (commonly, but wrongly, called the parameter errors) are estimated depends on the fitting algorithm used. One estimate of uncertainty is to use the square root of the diagonal of the covariance matrix. This can give a good estimate if the uncertainty is well behaved, with no significant correlation between the parameters. The covariance matrix is calculated as part of the commonly used Levenberg-Marquardt optimizer, which is provided by the [Python SciPy library](http://docs.scipy.org/doc/scipy/reference/generated/scipy.optimize.leastsq.html)). Otherwise the covariance matrix is estimated using the numerical derivative at the best point. If you _really_ want to know more, check out this [handy tutorial](http://www.aps.anl.gov/Xray_Science_Division/Powder_Diffraction_Crystallography/3LeastSquaresIntro/3LeastSquaresIntro.pdf) by Brian Toby at APS. The DREAM optimizer uses a Monte Carlo approach which provides a more realistic estimate of the uncertainties for the case when uncertainties are not well behaved.

### Why do I get different parameter uncertainties using the Simple and Complex fitting engines?

*   _This only applies to SasView 3.0.0 and earlier._
*   To a first approximation, the two fitting engines should return similar, but not identical, parameter uncertainties. The Simple engine uses the Python SciPy library which computes the Jacobian using the _forward difference formula_ and evaluates the covariance matrix by QR decomposition. The Complex engine computes the Jacobian using the _centre point formula_ and evaluates the covariance matrix by singular value decomposition (SV). Both methods will also be affected by the accuracy of the numerical differentiation procedures and the precision of the floating point computations.
*   (July 2014) We have discovered an inconsistency in the way that the Simple and Complex fitting engines define the reduced chi-square in SasView 3.0.0 and earlier. The consequence of this is that the Complex engine is not performing as many iterations as it should and is thus returning parameter uncertainties that are perhaps a factor 5 to 10 larger than expected.

### Why do I sometimes get different 'goodness-of-fit' values when pressing Enter or Compute compared to pressing Fit?

*   The SasView FitPage displays a 'normalized chi-square' computed as chi-square divided by the number of points. But the fitting engines compute chi-square divided by the number of points minus the number of fit parameters. So the more parameters you fit, the worse the apparent goodness-of-fit. Conversely, if you just press Enter or Compute the effective number of parameters is zero so the goodness-of-fit may appear to go down.

### Why have I got several instances of the same model category (eg, 'Shape Independent' and 'Shape-Independent')?

*   This is most likely because you have previously installed earlier versions of SasView and the category file needs rebuilding.
    *   If open, close SasView. Then go to your profile folder (eg, on Windows: `C:\Users\user_name`) and open the `.sasview` folder. Delete the file `categories.json`. Then run SasView again.

### Why is SasView not loading the model parameters from some of my existing .fitv (Save Fit) files?

*   As the number of models implemented in SasView increased it became necessary to add additional categorisation. At the same time we gave the user the ability to customise the categorisation (the Modify Category button). Unfortunately this does mean that the categorisation of _some_ models will have changed between earlier versions of SasView (when it was still called SansView) and recent releases. When SasView cannot determine the model categorisation from a .fitv file it attempts to default to the first model in the first category. There are two workarounds to this issue:
    1. Open the .fitv file in a text editor and scroll down to the section headed _Attributes_. Above the entry _formfactorcombobox_ create a new entry _categorycombobox categorycombobox="type"_, where _type_ is the category that the model was originally in (current categories are: Shape-Independent, Shapes, Structure Factor, Uncategorized, Custom Models). Make sure you enclose your new entry in angle brackets just like the existing entries!
    2. Use the Modify Category button in the recent version of SasView to move the model you want to use to the category it used to be in.

### Why is Save Analysis (File menu) greyed out after I fit a model?

*   _This only applies to SasView 4.2.2 and earlier._
*   At present Save Analysis gets greyed out if you click on a graph window after fitting a model. We agree this is not very sensible behaviour and will rectify it in a future bug release. In the meantime, use the 'Save' icon in the graphical toolbar to generate .fitv files.

### Why does Check for Updates not work?

*   Check for Updates compares the version (not build) number of your copy of SasView with that in the code repository. If SasView cannot access the remote server to perfom this check then the message _'Cannot connect to the application server'_ may be displayed in the status bar _or_ the SasView log file will contain lines implicating a file called proxy.pyc (see [Why will SasView no longer start? ('cannot execute script sasview')](#why-will-sasview-no-longer-start) below).
*   Unhelpfully, it is entirely possible to be able to use a web browser to surf the internet but find that SasView cannot read the current version number from the code repository!
*   The most common reason for Check for Updates failing is that your internet connection uses a proxy server and your computer is either not configured to use that proxy server _or_ that an exception for the SasView server needs to be added to the local policies on the proxy server. The latter case is more likely to be necessary in corporate/secure environments. Please contact your local IT Helpesk.

*   How you configure your computer to use a proxy server will depend on your operating system. The following worked in Windows 7:

    **Warning! The following procedure involves changing system settings. If you are not confident about doing so, consult your local IT Helpdesk.**
*   If you are not sure if your internet connect uses a proxy server, click on the Start button, select 'Network and Internet' and then 'Internet Options'. Now click the 'Connections' tab and then the button 'LAN settings'.

    1.  Click on the Start button. In the 'search programs and files' box type 'regedit' and press {return}.
    2.  In the Registry Editor, navigate to the registry key (be careful not to find find a similar key by mistake) `HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Internet Settings`. Look for a setting named 'ProxyServer'. If it exists, ensure it both points to your proxy server and has a port number appended. If it is missing create this setting as follows:
        *   Edit > New > String Value. Right-click on 'New Value' and rename it to `ProxyServer`. Right-click again, choose 'Modify', and in the 'Value data' box type the address and port number of your proxy server (eg, `http://proxy.uni.edu:port`).
    4.  If your internet connection _also_ uses a proxy auto-configuration (or .pac) file (see the instructions above for how to check), also check for the presence of a setting 'AutoConfigURL'. Again, if this exists, ensure it points at the right address and file. If it is missing, create this setting (eg, `http://proxy.uni.edu/configproxy.pac`) in the same manner as above.
    5.  Note that the value (0 or 1) of the `REG_DWORD` called 'ProxyEnable' appears to be irrelevant!
    6.  Close the Registry Editor.
    7.  Click on the Start button. In the 'search programs and files' box type 'environment variables' and press {return}.
    8.  In the Environment Variables panel, check the _User_ variables (not System variables) for `HTTP_PROXY` and `HTTPS_PROXY`. If they exist, ensure that both specify your username, proxy server and port. If they are missing, create these variables as follows:
        *   Click 'New'. Enter `HTTP_PROXY` as the 'Variable name'. Enter a 'Variable value' of the form: username@proxy.uni.edu:port. Click 'Ok'. Repeat the process to create the variable `HTTPS_PROXY`. Click 'Ok'.
*   Check for Updates should now work.

### Why is SasView no longer able to run my existing custom models?

*   There may be two reasons for this. From release 4.0 the structure of plug-in models altered considerably in order to provide the enhanced functionality (access to polydispersity, etc) many of our users had demanded. Though we have attempted to provide some degree of internal translation, the reality is that this will likely only be truly successful for simple models. We recommend that old models be re-written to comply with the requirements of the new architcture. New models can then be contributed through our new [Model Marketplace](https://marketplace.sasview.org).
*   The last vestiges of the old SansView name leftover from the genesis of the application were removed for release 3.1. While most visible parts of the application had already been converted to sasview prior to version 3.0, some of the packages still had the prefix "sans", including unfortunately the package used in custom models "sans.models.pluginmodel." In order to fix this simply apply the following fix. We appologize for the inconvenience.
    *    under _Fitting --> Edit Custom Model --> Advanced_ (on the menu bar) open the offending custom model. Find any import statements (should be at the beginning) including the `from sans.models.pluginmodel import Model1DPlungin` and replace "sans" with "sas." Save the model. It should now work

### How can I see the separate contributions of the form factor and structure factor?

#### SasView 2.x.x / SasView 3.x.x / SasView 4.0.x:

*   Load the data and perform the fit as normal, including the structure factor. Go to the menubar and select _Edit --> Copy Params..._.
*   Then open two new Fit Pages (_Fitting --> New Fit Page_). In one of the new Fit Pages select the form factor model you used in the first Fit Page, in the other new Fit Page select the structure factor model you used in the first Fit Page.
*   In each of the two new Fit Pages, select _Edit --> Paste Params..._.
    *   _NB: depending on the version of SasView you are using (4.0.x versus earlier versions), it may be necessary to manually adjust the scale factors or volume fraction parameter so that only one or other reports the volume fraction._
*   In each of the two new Fit Pages, click Compute. The form factor and structure factor will appear as Theories in the Data Explorer panel.

#### SasView 4.1 and later:

*   Once a fit has been performed P(Q), and S(Q) if included in the fit, will appear under Theories in the Data Explorer panel.

### How can I include a structure factor in a model?

*   There are two ways to include an S(Q) in a model:
    *   By clicking on the S(Q) drop-down box adjacent to the P(Q) model choice in a FitPage
    *   Using the Sum\|Multi function under Custom/Plugin Model operations.
*   However, these two methods are not equivalent.
*   When you choose to implement S(Q) from the FitPage, the effective radius for the particle described by P(Q) is calculated automatically and the volume fraction used in S(Q) is set to be the volume fraction of the particles (ie, the 'scale' parameter). Behind the scenes, the model calculates the radius of a sphere that would have the same second virial coefficient as the chosen particles and uses that in the S(Q) calculation as the effective radius for the interaction potential. This method works well for particles with an axial ratio up to about a 3-to-1 but beyond that is not correct.
*   When you make a Custom/Plugin model, the full set of parameters for calculating S(Q) are made available and you need to have an idea of what the effective radius and effective volume fraction for your chosen particles should be.
*   All S(Q) functions available in SasView were derived for spherical particles.
*   Also be aware that if you create a Custom/Plugin model from two other Custom/Plugin models with S(Q) included, for example, something like P1(Q)S1(Q) + P2(Q)S2(Q), SasView will only take account of the 'self' interactions. If you _also_ need to properly account for the 'cross' interactions you will need to program a Custom/Plugin model from first principles.
*   From release 5.0.3, when a S(Q) function is selected the FitPage allows you to select a _radius_effctive_mode_ and/or a _structure_factor_mode_.
    *   _radius_effective_mode_ determines whether the interaction radius value in the S(Q) should be the same as the radius in the P(Q) or not.
	*   _structure_factor_mode_ determines whether the calculation should use the 'beta approximation' for non-sphericity or not.

### What is the Model Marketplace?

*   The [Model Marketplace](https://marketplace.sasview.org) is an open repository of SasView fitting models we have set up to allow the SAS Community to contribute and share models.
*   Despite its name, it is free to use!

### Where does SasView expect to find custom models?

*   Custom (or plugin) models should be placed in the SasView plugin folder:

    *   C:\Users\\username\\.sasview\plugin_models (Windows)
    *   ~.sasview\plugin_models (Mac)
    
*   The next time SasView is started all model files in this folder will be compiled. Alternatively, on-the-fly compilation is possible by selecting:

    * Fitting > Plugin Model Operations > Load Plugin Models (in SasView 3.x/4.x)
    * Fitting > Manage Custom Models > Add  file... (In SasView 5.x)

*   If the required custom model does not appear in the drop-down list of Plugin Models in the FitPage then compilation is likely to have failed. Check the Console (in SasView 3.x/4.x) or Log Explorer (in SasView 5.x) or sasview.log file (all versions) for clues to the reason why.

### Can I use complex numbers in my models?

*   Yes, you can. Please download and unzip this [C++ header file](https://github.com/SasView/sasview.github.io/blob/master/downloads/cl_complex.zip) to your plugin model folder and add it to your source list before your .c file.
*   OpenCL 3.0 will allow the direct use of complex numbers, but it is not yet widely supported by GPU devices.

### Can I run Python scripts inside SasView?

*  Yes, you can. Start SasView and navigate to Tools > Python Shell/Editor. Then enter (note the use of \\\ in the path to the script):
```
 exec(open('C:\\Temp\\scriptname.py').read())
```
 or, better (as it will close the file after reading it)
```
 from pathlib import Path
 exec(Path('C:\\Temp\\scriptname.py').read_text())
```
*  Scripts executed like this will have access to all SasView libraries.

### Why will SasView no longer start?

*   There appear to be some situations where SasView fails to start. Either a message 'cannot execute script sasview' appears, or the 'splash screen' appears but nothing further happens. One or more of the following conditions is usually present:
     *   SasView was installed on a Windows 10 machine.
     *   A new or fresh install of SasView 5.x has been performed.
     *   The machine already had an existing installation of an earlier version of SasView (typically SasView 4.x).
     *   Your external internet connection is routed through a proxy server with particularly restrictive policies.

*   It is perfectly fine to install multiple versions of SasView on the same machine as long as they are installed to separate folders. From SasView 5.0.3 this happens automatically during installation, but earlier versions of SasView will need a unique installation folder name to be specified (eg, C:\SasView-v422).

*   All versions of SasView, however, use two common shared folders in the users profile:
    *   (On Windows):  C:\Users\\username\\.sasview and C:\Users\\username\\.sasmodels
    *   (on MacOS)  :  ~.sasview\ and ~.sasmodels\

*   The failure to start SasView appears to have one of five causes:
    *   (Windows 10 and later) During the Windows setup process the default save location for the users files (ie, anything normally expected to go into C:\Users\\username\\ and any sub-folders thereof) was redirected to the users OneDrive. See [here](https://support.microsoft.com/en-us/office/files-save-to-onedrive-by-default-in-windows-10-33da0077-770c-4bda-b61e-8c8e8ca70ac7) for details. In essence, this means that Windows changes the locations of the SasView shared folders FROM C:\Users\\username\\.sasview and C:\Users\\username\\.sasmodels TO C:\Users\\username\\OneDrive\\.sasview and C:\Users\\username\\OneDrive\\.sasmodels!
    *   (Windows 10 and later with SasView 5.0.x upto 5.0.4) The installation of a wholly separate software application has created an environment variable called HOME with a location that is different to the intended SasView installation folder.
    *   The installation process is unable to copy all of the required files to the shared folders.
    *   The new installation corrupts the contents of the shared folders.
    *   SasView is unable to perform an automatic check to see if the version you are using is the latest version of the program.

*   Determining which of these circumstances is the cause may not be entirely straightforward but the following procedure *should* cover all eventualities:
    1.  (Windows 10 and later) Check to see if the SasView shared folders have been created in your local OneDrive folder (C:\Users\\username\\OneDrive\\). If they *have*, copy them **up** one level and delete them from the OneDrive folder. Now try running SasView.

    2.  If Step i) does not apply/work, bring up a Windows shell (type 'cmd' in the Windows search bar) and type 'set'. This will alphabetically list all the environment variables in use. Look for one called HOME (NB: Windows *only* creates HOMEDRIVE and HOMEPATH). If HOME exists, try uninstalling SasView, deleting the HOME variable (you will probably need local administrator permission to do this), and then re-installing SasView. Now try running SasView. If SasView runs, then try running the other software application that created the HOME variable. If the other application now does not start, try re-creating the HOME variable, and then re-test both SasView and the other application. 
    
    3.  If Steps i) & ii) do not apply/work, locate the the SasView log file **sasview.log** (on Windows this should be in C:\Users\\username\\). Open it in a text editor and search for recent occurrences of the string 'Could not copy'. Any matches will look something like this (an actual example reported to the Development Team):
        ```
        2020-08-29 10:57:05,906 : ERROR : sas._config (_config.py:94) :: Could not copy default custom config.
        ```
        In this example the error indicates that the installation process had been unable to copy the file **custom_config.py** into the folder C:\Users\\username\\.sasview\\config\\ for some reason. Manually copying the missing file from the SasView installation folder to C:\Users\\username\\.sasview\\config\\ then allowed SasView to start.
       
        **Note: if it is unclear what file is missing, where it can be found, or where it should be copied too, please contact the Development Team at [help@sasview.org](mailto:help@sasview.org), attaching a copy of your sasview.log file.**
    
    4.  If you installed SasView 'For All Users (recommended)', uninstall it, delete *all* folders that were created by that installation, then try re-installing SasView as 'Just for Me'.
        
        **Warning! the .sasview folder may contain a sub-folder with existing plugin models (particularly if you have had other versions of SasView installed). To preserve those plugin models, make temporary copies of them before deleting the .sasview folder!**
        
    5.  If Step iv) does not work/apply, delete the shared folders .sasview and .sasmodels and then try running SasView again. If it starts it will re-create the folders.

    6.  If you are using SasView on a corporate computer and/or in a corporate/secure environment, it is possible that your local IT policy routes external internet access through something called a proxy server. When SasView starts it attempts to connect to one of our servers to determine if there is a more recent version of the program. If this check cannot be performed then the program may fail to start. You may be able to verify if this is happening. Locate the SasView log file **sasview.log** (on Windows this should be in C:\Users\\username\\). Open it in a text editor and search for recent occurrences of the string 'proxy.pyc'. Any matches will look something like this (an actual example reported to the Development Team):
        ```
        2022-05-20 15:22:32,920 : DEBUG : sas.sasgui.guiframe.proxy (proxy.pyc:127) :: Trying Direct connection to http://www.sasview.org/latestversion.json...
        2022-05-20 15:22:32,920 : DEBUG : sas.sasgui.guiframe.proxy (proxy.pyc:130) :: Failed!
        2022-05-20 15:22:32,920 : DEBUG : sas.sasgui.guiframe.proxy (proxy.pyc:131) :: <urlopen error [Errno 11001] getaddrinfo failed>
        2022-05-20 15:22:32,920 : DEBUG : sas.sasgui.guiframe.proxy (proxy.pyc:133) :: Trying to use system proxy if it exists...
        2022-05-20 15:22:32,920 : DEBUG : sas.sasgui.guiframe.proxy (proxy.pyc:137) :: Failed!
        2022-05-20 15:22:32,920 : DEBUG : sas.sasgui.guiframe.proxy (proxy.pyc:138) :: <urlopen error [Errno 11001] getaddrinfo failed>
        2022-05-20 15:22:32,920 : DEBUG : sas.sasgui.guiframe.proxy (proxy.pyc:78) :: Trying pac file (http://proxy.xxxxx.xxxx.xx/proxy.pac)...
        2022-05-20 15:22:32,920 : DEBUG : sas.sasgui.guiframe.proxy (proxy.pyc:84) :: Failled (http://proxy.xxxxx.xxxx.xx/proxy.pac)...
        ```
        Note that in this example the address of the organisations proxy server has been anonymised. If these messages are present in the log file you should request a proxy exception for http://www.sasview.org/latestversion.json through your local IT Helpdesk. Also see [Why does Check for Updates not work?](#why-does-check-for-updates-not-work).
	
