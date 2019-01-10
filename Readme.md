# Automatic Labeled LiDAR Data for Human detection

Automatic Labeled LiDAR Data (ALLD) are novel data with human label. The data contain various generated LiDAR scenes with human label. To download ALLD, please check free disk space over than 405GB and run 'ALL_IN_ONE.sh'.

---

* HumanDetection_ver01.tar.gz
	* h5file : *containing 500K hdf5 files*
	* xml : *containing 500K xml files*

* TestSet_for_HumanDetection_ver01.tar.gz
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
