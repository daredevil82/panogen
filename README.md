Panorama Generation
===================

A set of scripts to simplify the installation of dependencies required to batch-generate
a set of panoramas from a fixed folder location and output to a second fixed folder location.
These scripts are tested and compatible with Ubuntu > 10.10 and OSX Snow Leopard.

pano_hugin uses the [Hugin](http://hugin.sourceforge.net/) software to perform the stitch operations.

pano_gigapan uses the [Gigapan Stitch](http://www.gigapan.com/cms/shop/software/gigapan-stitch) >= 2.2.1 software to perform the same results on a Mac.  
Be aware that the Hugin command line scripts rely on the dev versions of the JPEG, PNG and TIFF 
libraries, of which there are no compatible OSX binaries and therefore the pano_hugin script will 
not execute.

Speed-wise, the Gigapan proprietary software executes much faster and has better results from
indoor sequences, particularly when blending together walls and ceilings without distortions.
I averaged ~20 minutes per 50 image panorama using the Hugin script on a 4 core Xeon workstation 
with 4 GIB RAM, while the gigapan software needed < 5 minutes on a basic 2011 dual core iMac with 
2 GIB RAM.

Prior to executing the scripts, make sure all required dependencies are installed and set the fixed
file path for the input and output file locations.  If necessary, run as root as the script requires
file-creation permissions