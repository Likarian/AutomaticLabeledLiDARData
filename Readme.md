# Automatic Labeled LiDAR Data for Human detection

Automatic Labeled LiDAR Data are novel data with human label. The data contain various generated LiDAR scenes with human label. To download the data, please check your free disk space enough and run 'DownloadAndUnzip.sh'. You can also download the data by the following url.

* HumanDetectionVer01 (377GB) : https://data.airc.aist.go.jp/AutomaticLabeledLiDARData/HumanDetectionVer01.tar.gz
* TestSetForHumanDetectionVer01 (1.3GB) : https://data.airc.aist.go.jp/AutomaticLabeledLiDARData/TestSetForHumanDetectionVer01.tar.gz
* EtcDataVer01 (11.1GB) : https://data.airc.aist.go.jp/AutomaticLabeledLiDARData/EtcDataVer01.tar.gz
  
The paper of Ver01:  
 **Wonjik Kim, Masayuki Tanaka, Masatoshi Okutomi, Yoko Sasaki, "Automatic Labeled LiDAR Data Generation based on Precise Human Model", International Conference on Robotics and Automation (ICRA), 2019.** ([pdf]())

---
# How to use
### Dependencies
* Python 3.6.5
* Tensorflow 1.9.0
* Keras 2.2.4
* Cuda 9.0

### Run DownloadAndUnzip.sh
In your own directory, please run the following command in terminal.
<br>
> bash ./DownloadAndUnzip.sh 

### Sample code
In directory of './TestSetForHumanDetectionVer01/NetworkWeight/*specific network*/', you can see sample code for performance evaluation. When you want to check sample code, please run the following command in that directory.
<br>
> python SampleTest***.py 

---
### Directory Specification

* HumanDetectionVer01
	* h5file : *containing 500K hdf5 files*
	* xml : *containing 500K xml files*

* TestSetForHumanDetectionVer01
	* NetworkWeight
		* FCDN
			* fcdn-depth.hdf5 : *trained weight of fcdn by depth*
			* fcdn-depth_model.json : *model description of fcdn*
			* mtinitializers.py
			* mtutil
			* SampleTestFcdn.py : *sample code for test*
		* FCN
			* fcn.py : *trained weight of fcn by depth*
			* fcn_depth.hdf5 : *model description of fcn*
			* mtinitializers.py
			* mtutil.py
			* padding.py
			* SampleTestFcn.py : *sample code for test*
		* POINTNET
			* mtutil_xyz.py
			* pointnet.py : *model description of pointnet*
			* pointnet_xyz.hdf5 : *trained weight of pointnet by xyz coordinate*
			* SampleTestPointnet.py : *sample code for test*
		* UNET
			* mtinitializers.py
			* mtutil.py
			* SampleTestUnet.py : *sample code for test*
			* unet-depth.hdf5 : *trained weight of unet by depth*
			* unetmodel.py : *model description of unet*

	* TestData
		* TestDataReal
			* 0.1K hdf5 files
		* TestDataSim
			* 1K hdf5 files
* EtcDataVer01
	* Section4C2 : *containing 10K hdf5 files*
	* Section4C3_100012 : *containing 1K hdf5 files*
	* Section4C3_140020 : *containing 1K hdf5 files*
	* Section4C3_150050 : *containing 1K hdf5 files*
	* Section4C3_160050 : *containing 1K hdf5 files*
	* Section4C3_170080 : *containing 1K hdf5 files*
	* Section4C3_200080 : *containing 1K hdf5 files*
	* Section4C4 : *containing 1K hdf5 files*


---
# License
Automatic Labeled LiDAR Data are allowed only for noncommercial usage. Please cite our paper if our data were used in your work.
You can see specific terms of use in the LICENSE.md.

