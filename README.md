Meta Programming and Reflection - Pharo
====
This repository contains basic code for the course of Meta Programming and Reflection of the Vrije Universiteit Brussel
You might need to update iceberg in your Pharo image through the following code:
```
MetacelloPharoPlatform select.
#(
	'BaselineOfTonel'
	'BaselineOfLibGit'
	'BaselineOfIceberg'
	'Iceberg-UI' 
	'Iceberg-Plugin-GitHub' 
	'Iceberg-Plugin' 
	'Iceberg-Metacello-Integration' 
	'Iceberg-Libgit-Tonel' 
	'Iceberg-Libgit-Filetree' 
	'Iceberg-Libgit' 
	'Iceberg' 
	'LibGit-Core'
	'MonticelloTonel-Tests'
	'MonticelloTonel-Core'
	'MonticelloTonel-FileSystem' ) 
do: [ :each | (each asPackageIfAbsent: [ nil ]) ifNotNil: #removeFromSystem ].
Metacello new
  	baseline: 'Iceberg';
  	repository: 'github://pharo-vcs/iceberg:v0.6.7';
  	load.
```
