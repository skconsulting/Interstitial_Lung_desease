# README for patch generator from ILD DB

Sylvain Kritter May 2nd 2016

### Tools used:
1.	RadianDICOM viewer to view dcm files.
  a)	Can also convert dicom images in jpg, bmp,
2.	Total Image Converter to create jpeg, bpm and JPEG 2000 from dcm. I have created in each  ILD_DB-textROIs dataset (35, 65,…) the directories bmp,jp2k,jpg to store equivalent format from dcm files.
3.	Spyder Python 3.5 for Python

### To run the patch generator
1.	3 python files needed:
  a.	final.py (this is the top, parameters are defined in it, no need to touch the 2 others)
  b.	fillshape.py
  c.	generatetabc.py
2.	Preparation
  To run the patch generator, we need first to have the directory ILD_DB-textROIs in the place where Python  is launched.
  In each dataset in directory ILD_DB-textROIs, we need to add a directory named bmp or jpg to store bmp or jpg files generated from dcm
3.	Customization in final.py
  a.	Patch image format: bmp or jpg
  b.	Dicom file size: 512 * 512
  c.	Patch size: 32*32
  d.	Threshold  in % : 0.8 for patch area over ROI
  
### program generate files
1. From where it is launched:
  e.	‘Jpeg’ directory , where jpeg images and text files of all ROI with patches is stored
  f.	‘patch’ directory, where patches are store in sub directories, named after label and localization names in each scan, according to image format declared in top python (jpg or bmp). I think bmp is more accurate.
2.	in each ILD_DB-textROIs dataset (35, 65,…) , a directory named ‘patchfile’  where intermediate data is  stored. Can be deleted afterward.

### Database Analysis
1.	The Dcm files are identical in ILD_DB_txtROIs, ILD_DB_volumeROIs   and  ILD_DB_lungMasks
2.	A ROI text file is in each data set In ILD_DB_txtROIs This Text file: corresponds to ROI in ILD_DB_volumeROIs  roi_mask of each dataset.
3.	There is a set of ROI in roi_mask in each dataset of ILD_DB_lungMasks: this is lung area 

