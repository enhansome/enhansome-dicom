<!-- omit in toc -->

# Awesome DICOM with stars

> A curated list of awesome DICOM resources and libraries.

The [DICOM Standard](https://www.dicomstandard.org/) is *the* international standard for medical images and related information. It defines the formats for medical images that can be exchanged with the data and quality necessary for clinical use <sup>\[[source](https://www.dicomstandard.org/about-home)]</sup>.

<!-- omit in toc -->

## Contents

* [Datasets](#datasets)
* [Learning Resources](#learning-resources)
* [Libraries](#libraries)
  * [C#](#c)
  * [C++](#c-1)
  * [Go](#go)
  * [Java](#java)
  * [JavaScript](#javascript)
  * [MATLAB](#matlab)
  * [Python](#python)
  * [Rust](#rust)
  * [Other/Combination](#othercombination)
* [Contribute](#contribute)

## Datasets

* [The Cancer Imaging Archive (TCIA)](https://www.cancerimagingarchive.net/) - Freely available radiology and pathology cancer imaging datasets.
* [Imaging Data Commons (IDC)](https://datacommons.cancer.gov/repository/imaging-data-commons) - A cloud-based repository of publicly available cancer imaging data. Includes radiology, digital pathology, analysis results all in DICOM format. Mirrors all public radiology DICOM collections available in TCIA.
* [Medical Imaging and Data Resource Center (MIDRC)](https://www.midrc.org/) - This archive contains DICOM imaging for over 67,000 COVID-19 subjects.

## Learning Resources

* [The DICOM Standard](https://www.dicomstandard.org/current)
* [DICOM Library](https://www.dicomlibrary.com/) - A free online medical DICOM image or video file sharing service for educational and scientific purposes.
* [DICOM Standard Browser](https://dicom.innolitics.com/ciods) - Part 3 of the DICOM standard as a tree.
* [DICOM is Easy](https://dicomiseasy.blogspot.com/2011/10/introduction-to-dicom-chapter-1.html) - A personal blog which includes a series of DICOM tutorials.
* [Microsoft training module](https://learn.microsoft.com/en-us/training/modules/medical-imaging-data/) - Short training module about working with medical imaging data in general and DICOM in particular.
* [Saravanan Subramanian's blog](https://saravanansubramanian.com/dicomtutorials/) - A series of articles and tutorials focusing on working with DICOM using Java and .NET.

## Libraries

### C\#

#### General

* [fo-dicom](https://github.com/fo-dicom/fo-dicom) ⭐ 1,208 | 🐛 66 | 🌐 C# | 📅 2026-08-15 - Fellow Oak DICOM, a DICOM toolkit in C# for all .NET Standard 2.0 compatible frameworks.
* [dicom-server](https://github.com/microsoft/dicom-server) ⭐ 512 | 🐛 17 | 🌐 C# | 📅 2026-08-16 - The Medical Imaging Server for DICOM is an open source DICOM server that is easily deployed on Azure.
* [DICOMcloud](https://github.com/DICOMcloud/DICOMcloud) ⭐ 235 | 🐛 30 | 🌐 C# | 📅 2023-12-15 - A standalone DICOMWeb server with RESTful implementation of the DICOMWeb/WADO services. The DICOMcloud server can interface with any DICOMWeb client over the current implemented features (qido-rs, wado-uri, wado-rs and stow-rs).
* [Evil-DICOM](https://github.com/rexcardan/Evil-DICOM) ⭐ 190 | 🐛 26 | 🌐 C# | 📅 2024-08-20 - A simple to use library for reading and manipulating DICOM files.

#### Visualization

* [UnityVolumeRendering](https://github.com/mlavik1/UnityVolumeRendering) ⭐ 560 | 🐛 70 | 🌐 C# | 📅 2026-03-12 - A volume renderer, made with Unity3D.

### C++

#### General

* [SimpleITK](https://github.com/SimpleITK/SimpleITK) ⭐ 1,082 | 🐛 96 | 🌐 C++ | 📅 2026-08-17 - A simplified interface for the Insight Toolkit [ITK](https://itk.org/) with several components supporting general filtering operations, image segmentation, and registration.
* [CTK](https://github.com/commontk/CTK) ⭐ 964 | 🐛 230 | 🌐 C++ | 📅 2026-08-12 - The Common Toolkit is a community effort to provide support code for medical image analysis, surgical navigation, and related projects.
* [DCMTK](https://github.com/DCMTK/dcmtk) ⭐ 900 | 🐛 14 | 🌐 C++ | 📅 2026-08-12 - The DICOM ToolKit (DCMTK) package consists of source code, documentation and installation instructions for a set of software libraries and applications implementing part of the DICOM/MEDICOM Standard.
* [MITK](https://github.com/MITK/MITK) ⭐ 832 | 🐛 0 | 🌐 C++ | 📅 2026-08-10 - The Medical Imaging Interaction Toolkit (MITK) is a free open-source software system for development of interactive medical image processing software. MITK combines the Insight Toolkit (ITK) and the Visualization Toolkit (VTK) with an application framework.
* [GDCM](https://github.com/malaterre/GDCM) ⭐ 398 | 🐛 2 | 🌐 C++ | 📅 2026-07-02 - Grassroots DICOM (GDCM) is an implementation of the DICOM standard designed to be open source, so that researchers may access clinical data directly. GDCM includes a file format definition and a network communications protocol, both of which should be extended to provide a full set of tools for a researcher or small medical imaging vendor to interface with an existing medical database.
* [vtk-dicom](https://github.com/dgobbi/vtk-dicom) ⭐ 286 | 🐛 67 | 🌐 C++ | 📅 2026-02-08 - A set of classes for managing DICOM files and metadata from within VTK, and some utility programs for interrogating and converting DICOM files.
* [dcmqi](https://github.com/QIICR/dcmqi) ⭐ 284 | 🐛 74 | 🌐 C++ | 📅 2026-08-11 - DICOM for Quantitative Imaging (dcmqi) is a collection of libraries and command line tools with minimum dependencies to support standardized communication of quantitative image analysis research data using the DICOM standard.
* [Orthanc](https://github.com/jodogne/OrthancMirror) ⭐ 41 | 🐛 0 | 🌐 C++ | 📅 2026-08-16 - A simple yet powerful standalone DICOM server. It is designed to improve the DICOM flows in hospitals and to support research about the automated analysis of medical images.

#### Conversion

* [dcm2niix](https://github.com/rordenlab/dcm2niix) ⭐ 1,181 | 🐛 3 | 🌐 C++ | 📅 2026-08-13 - Convert neuroimaging data from the DICOM format to the [NIfTI](https://nifti.nimh.nih.gov/) format.
* [DicomToMesh](https://github.com/AOT-AG/DicomToMesh) ⭐ 527 | 🐛 6 | 🌐 C++ | 📅 2026-03-28 - A command line tool to transform a DICOM volume into a 3d surface mesh (*obj*, *stl* or *ply*). Several mesh processing routines can be enabled, such as mesh reduction, smoothing or cleaning.
* [wsi-to-dicom-converter](https://github.com/GoogleCloudPlatform/wsi-to-dicom-converter) ⚠️ Archived - Convert whole slide images (WSIs) to DICOM.

#### Other

* [DICOMautomaton](https://github.com/hdclark/DICOMautomaton) ⭐ 90 | 🐛 34 | 🌐 C++ | 📅 2026-08-14 - A multipurpose tool for analyzing medical physics data with a focus on automation.
* [dovo](https://github.com/DraconPern/dovo) ⭐ 41 | 🐛 2 | 🌐 C++ | 📅 2026-03-30 - Cross-platform software for importing DICOM CD/files and sending to PACS.

### Go

* [dicom](https://github.com/suyashkumar/dicom) ⭐ 1,079 | 🐛 133 | 🌐 Go | 📅 2026-06-21 - High performance Golang DICOM parser.

### Java

#### General

* [dcm4che](https://github.com/dcm4che/dcm4che) ⭐ 1,448 | 🐛 162 | 🌐 Java | 📅 2026-08-07 - A collection of open source applications and utilities for the healthcare enterprise.
* [Dicoogle](https://github.com/bioinformatics-ua/dicoogle) ⭐ 526 | 🐛 61 | 🌐 Java | 📅 2026-07-15 - An extensible, platform-independent and open-source PACS archive software that replaces the traditional centralized database with a more agile indexing and retrieval mechanism.
* [healthcare-dicom-dicomweb-adapter](https://github.com/GoogleCloudPlatform/healthcare-dicom-dicomweb-adapter) ⭐ 146 | 🐛 27 | 🌐 Java | 📅 2026-06-22 - A set of components that translate between traditional DICOM DIMSE protocols (e.g., C-STORE) and the RESTful DICOMWeb protocols (e.g., STOW-RS).

#### Visualization

* [Weasis](https://github.com/nroduit/Weasis) ⭐ 1,310 | 🐛 42 | 🌐 Java | 📅 2026-08-15 - A multipurpose standalone and web-based DICOM viewer with a highly modular architecture.

### JavaScript

#### General

* [dcmjs](https://github.com/dcmjs-org/dcmjs) ⭐ 349 | 🐛 119 | 🌐 JavaScript | 📅 2026-07-18 - JavaScript implementation of DICOM manipulation. This code is an outgrowth of several efforts to implement web applications for medical imaging.
* [Daikon](https://github.com/rii-mango/Daikon) ⭐ 232 | 🐛 3 | 🌐 JavaScript | 📅 2024-01-30 - A pure JavaScript DICOM reader.
* [dicomweb-client](https://github.com/dcmjs-org/dicomweb-client) ⭐ 158 | 🐛 26 | 🌐 JavaScript | 📅 2026-08-13 - JavaScript client implementation of DICOMWeb.
* [dicomweb-pacs](https://github.com/knopkem/dicomweb-pacs) ⭐ 124 | 🐛 6 | 🌐 TypeScript | 📅 2026-03-22 - Easy to use DICOMWeb enabled PACS with DIMSE services based on sqlite database.
* [dicomweb-server](https://github.com/dcmjs-org/dicomweb-server) ⭐ 108 | 🐛 25 | 🌐 JavaScript | 📅 2026-04-14 - Lightweight DICOMWeb Server with CouchDB.
* [dcmjs-dimse](https://github.com/PantelisGeorgiadis/dcmjs-dimse) ⭐ 88 | 🐛 3 | 🌐 JavaScript | 📅 2026-05-17 - DICOM DIMSE implementation for Node.js using the dcmjs library.
* [Efferent.Dicom](https://github.com/Efferent-Health/Dicom) ⭐ 11 | 🐛 0 | 🌐 TypeScript | 📅 2026-06-03 - Ligthweight JS/TS/Node library for reading and writing DICOM files
* [dcmjs-codecs](https://github.com/PantelisGeorgiadis/dcmjs-codecs) ⭐ 5 | 🐛 0 | 🌐 JavaScript | 📅 2026-04-17 - DICOM file and dataset transcoding for Node.js and browser using the dcmjs library.
* [cornerstoneWADOImageLoader](https://tinyurl.com/bcdb4bxa) - A [cornerstone.js](https://github.com/cornerstonejs/) Image Loader for DICOM P10 instances over HTTP (WADO-URI) or DICOMWeb (WADO-RS). This can be used to integrate cornerstone with WADO-URI servers, DICOMWeb servers or any other HTTP based server that returns DICOM P10 instances (e.g., Orthanc or custom servers).
* [dicomParser](https://tinyurl.com/mr39unuk) - Cornerstone.js' lightweight library for parsing DICOM P10 byte streams, as well as raw (not encapsulated in part 10) byte streams, in modern HTML5 based web browsers (IE10+), Node.js and Meteor.

#### Visualization

* [Viewers](https://github.com/OHIF/Viewers) ⭐ 4,297 | 🐛 537 | 🌐 TypeScript | 📅 2026-08-18 - A zero-footprint medical image viewer provided by the [Open Health Imaging Foundation (OHIF)](https://ohif.org/). It is a configurable and extensible progressive web application with out-of-the-box support for image archives which support DICOMWeb.
* [DWV](https://github.com/ivmartel/dwv) ⭐ 1,840 | 🐛 46 | 🌐 JavaScript | 📅 2026-08-15 - DICOM Web Viewer (DWV) is an open source zero footprint medical image viewer library. It uses only JavaScript and HTML5 technologies, meaning that it can be run on any platform that provides a modern browser (laptop, tablet, phone and even modern TVs).
* [NiiVue](https://github.com/niivue/niivue) ⭐ 479 | 🐛 28 | 🌐 TypeScript | 📅 2026-08-07 - A WebGL module that can be embedded into HTML, Vue.js, Angular, React, Electron and Capacitor frameworks. It provides scripting and drag and drop abilities to visualize and render voxel-based images (e.g., DICOM and NIfTI), meshes, and tractography streamlines and connectomes, as well as drawing functions ([demos](https://niivue.github.io/niivue/)).
* [VolView](https://github.com/Kitware/VolView) ⭐ 292 | 🐛 85 | 🌐 TypeScript | 📅 2026-08-17 - Web based radiological viewer for clinical professionals. Built with [Vue.js](https://vuejs.org/) and [VTK.js](https://github.com/Kitware/vtk-js) ⭐ 1,520 | 🐛 300 | 🌐 JavaScript | 📅 2026-08-17.
* [dicomviewer](https://github.com/ayselafsar/dicomviewer) ⭐ 265 | 🐛 13 | 🌐 JavaScript | 📅 2026-08-07 - A DICOM viewer which uses the cornerstone.js library to display DICOM files in Nextcloud.
* [U Dicom Viewer](https://github.com/webnamics/u-dicom-viewer) ⭐ 193 | 🐛 41 | 🌐 JavaScript | 📅 2023-04-13 - A simple but functional DICOM viewer for any device with a web browser. Allows opening and viewing 2D medical images in a wide variety of DICOM formats.
* [bluelight](https://github.com/cylab-tw/bluelight) ⭐ 155 | 🐛 1 | 🌐 JavaScript | 📅 2026-08-11 - Browser-based medical image viewer primarily maintained by the [Imaging Informatics Labs](https://cylab.dicom.tw/). It is a pure single-page application (SPA), lightweight, and using only JavaScript and HTML5 technologies to easily deploy it on any HTTP server.
* [dwv-react](https://github.com/ivmartel/dwv-react) ⭐ 130 | 🐛 2 | 🌐 JavaScript | 📅 2026-05-19 - Medical viewer using DWV and [React](https://react.dev/).
* [dicom-microscopy-viewer](https://github.com/ImagingDataCommons/dicom-microscopy-viewer) ⭐ 128 | 🐛 16 | 🌐 JavaScript | 📅 2026-08-17 - Vanilla JS library for web-based visualization of DICOM VL Whole Slide Microscopy Image datasets and derived information.
* [dcmjs-imaging](https://github.com/PantelisGeorgiadis/dcmjs-imaging) ⭐ 50 | 🐛 1 | 🌐 JavaScript | 📅 2026-04-16 - DICOM image and overlay rendering pipeline for Node.js and browser using the dcmjs library.
* [dicom.ts](https://github.com/wearemothership/dicom.ts) ⭐ 48 | 🐛 16 | 🌐 TypeScript | 📅 2026-01-22 - A small, superfast JS DICOM renderer.
* [dicomViewerLib](https://github.com/fourctv/dicomViewerLib) ⭐ 46 | 🐛 26 | 🌐 JavaScript | 📅 2024-10-29 - An Angular 9+ DICOMWeb viewer component, based on the cornerstone.js project.
* [dcmjs-ecg](https://github.com/PantelisGeorgiadis/dcmjs-ecg) ⭐ 9 | 🐛 0 | 🌐 JavaScript | 📅 2026-05-19 - DICOM electrocardiography (ECG) rendering for Node.js and browser using dcmjs.
* [cornerstone](https://tinyurl.com/2p85awt3) - A complete web based medical imaging platform. This repository contains the cornerstone.js "Core" component which is a lightweight JavaScript library for displaying medical images in modern web browsers that support the HTML5 canvas element.

#### Other

* [dicomweb-proxy](https://github.com/knopkem/dicomweb-proxy) ⭐ 82 | 🐛 2 | 🌐 TypeScript | 📅 2026-03-22 - Translates between DICOMWeb and traditional DICOM DIMSE services.

### MATLAB

#### Conversion

* [dicm2nii](https://github.com/xiangruili/dicm2nii) ⭐ 102 | 🐛 0 | 🌐 MATLAB | 📅 2026-04-01 - Convert DICOM into NIfTI. It can also convert PAR/XML/REC, HEAD/BRIK, MGZ and BrainVoyager files into NIfTI.

### Python

#### General

* [pydicom](https://github.com/pydicom/pydicom) ⭐ 2,194 | 🐛 34 | 🌐 Python | 📅 2026-08-03 - A pure Python package for working with DICOM files. It lets you read, modify and write DICOM data in an easy "pythonic" way.
* [MedPy](https://github.com/loli/medpy) ⭐ 620 | 🐛 4 | 🌐 Jupyter Notebook | 📅 2024-09-03 - An image processing library and collection of scripts targeted towards medical (i.e. high dimensional) image processing.
* [pynetdicom](https://github.com/pydicom/pynetdicom) ⭐ 570 | 🐛 19 | 🌐 Python | 📅 2026-08-03 - A pure Python 3.7+ package that implements the DICOM networking protocol. Working with *pydicom*, it allows the easy creation of DICOM Service Class Users (SCUs) and Service Class Providers (SCPs).
* [highdicom](https://github.com/ImagingDataCommons/highdicom) ⭐ 239 | 🐛 34 | 🌐 Python | 📅 2026-08-07 - Provides high-level DICOM abstractions for the Python programming language to facilitate the creation and handling of DICOM objects for image-derived information, including image annotations, and image analysis results.
* [dicomweb-client](https://github.com/ImagingDataCommons/dicomweb-client) ⭐ 128 | 🐛 13 | 🌐 Python | 📅 2026-08-17 - Provides client interfaces for DICOMWeb RESTful services QIDO-RS, WADO-RS and STOW-RS to search, retrieve and store DICOM objects over the web, respectively.
* [dicompyler](https://github.com/dicompyler/) - An extensible open source radiation therapy research platform based on the DICOM standard. It also functions as a cross-platform DICOM RT viewer.

#### Conversion

* [dicom2nifti](https://github.com/icometrix/dicom2nifti) ⭐ 403 | 🐛 63 | 🌐 Python | 📅 2025-06-23 - Convert MR and CT-derived DICOM files to NIfTI.
* [heudiconv](https://github.com/nipy/heudiconv) ⭐ 283 | 🐛 217 | 🌐 Python | 📅 2026-08-10 - A flexible DICOM converter for organizing brain imaging data into structured directory layouts.
* [dicom2stl](https://github.com/dave3d/dicom2stl) ⭐ 215 | 🐛 9 | 🌐 Python | 📅 2026-07-29 - Convert a DICOM series to an [STL](https://en.wikipedia.org/wiki/STL_\(file_format\)) surface mesh.
* [dcmstack](https://github.com/moloney/dcmstack) ⭐ 78 | 🐛 18 | 🌐 Python | 📅 2026-03-24 - DICOM to NIfTI conversion with the added ability to extract and summarize metadata from the source files.
* [bidskit](https://github.com/jmtyszka/bidskit) ⭐ 67 | 🐛 19 | 🌐 Python | 📅 2026-05-29 - CLI for converting a directory of DICOM files into a [BIDS](https://bids.neuroimaging.io/)-compliant dataset.
* [Dicomifier](https://github.com/lamyj/dicomifier) ⭐ 32 | 🐛 6 | 🌐 Python | 📅 2025-07-20 - A set of tools to convert Bruker data to DICOM files, and DICOM files to NIfTI.

#### Anonymization

* [deid](https://github.com/pydicom/deid) ⭐ 177 | 🐛 25 | 🌐 Python | 📅 2026-01-12 - Best effort anonymization for medical images in Python.
* [dicom-anonymizer](https://github.com/KitwareMedical/dicom-anonymizer) ⭐ 143 | 🐛 6 | 🌐 Python | 📅 2026-07-10 - A tool for anonymizing DICOM files according to the DICOM standard.
* [DICAT](https://github.com/aces/DICAT) ⭐ 44 | 🐛 7 | 🌐 Python | 📅 2024-04-10 - A simple graphical tool that facilitates DICOM de-identification directly on a local workstation.
* [dcm-anon](https://github.com/Ces107/dcm-anon) ⭐ 5 | 🐛 0 | 🌐 Python | 📅 2026-06-07 - PS3.15 Basic Profile anonymizer that emits a hash-chained GDPR/HIPAA compliance manifest and an independent post-run residual-PHI scan.

#### Sorting

* [dicomsort](https://github.com/pieper/dicomsort) ⭐ 86 | 🐛 8 | 🌐 Python | 📅 2025-05-06 - Given DICOM files in a random folder structure, this program copies all into a user-defined folder hierarchy, creating folders as necessary and changing DICOM file names to be more meaningful.

#### Visualization

* [MRIcroGL](https://github.com/rordenlab/MRIcroGL) ⭐ 290 | 🐛 3 | 🌐 Python | 📅 2025-11-23 - A cross-platform tool that supports many voxel-based image formats including DICOM. This natively compiled application provides a drag and drop user interface as well as Python scripting integration.
* [dicom-ecg-plot](https://github.com/marcodebe/dicom-ecg-plot) ⭐ 160 | 🐛 4 | 🌐 Python | 📅 2026-04-28 - Plot ECG data from DICOM ([demo](https://ecg.galliera.it/)).
* [OnkoDICOM](https://github.com/didymo/OnkoDICOM) ⭐ 72 | 🐛 35 | 🌐 Python | 📅 2026-06-22 - DICOM-RT viewer with enhanced capabilities that make it useful for research in the field of Radiation Oncology.
* [FSLeyes](https://fsl.fmrib.ox.ac.uk/fsl/fslwiki/FSLeyes) - A cross-platform visualization tool for NIfTI and DICOM images.

#### Other

* [dicom-standard](https://github.com/innolitics/dicom-standard) ⭐ 131 | 🐛 53 | 🌐 HTML | 📅 2026-04-17 - Parses the web version of the DICOM Standard into human and machine-friendly JSON files.
* [dcmrtstruct2nii](https://github.com/Sikerdebaard/dcmrtstruct2nii) ⭐ 103 | 🐛 9 | 🌐 Python | 📅 2024-02-28 - DICOM RT-Struct to nii-mask. This is a naïve approach to rasterizing rt-struct to masks in the NIfTI format.
* [dicom-numpy](https://github.com/innolitics/dicom-numpy) ⭐ 95 | 🐛 4 | 🌐 Python | 📅 2023-05-10 - A set of utilities for extracting data contained in DICOM files into Numpy ndarrays.

### Rust

* [DICOM-rs](https://github.com/Enet4/dicom-rs) ⭐ 554 | 🐛 77 | 🌐 Rust | 📅 2026-08-06 - A pure Rust implementation of the DICOM standard, allowing users to work with DICOM objects and interact with DICOM applications, while aiming to be fast, safe, and intuitive to use.

### Other/Combination

#### Machine Learning

* [Niffler](https://github.com/Emory-HITI/Niffler) ⭐ 104 | 🐛 3 | 🌐 Python | 📅 2023-10-25 - A lightweight framework to facilitate executing machine learning pipelines and processing workflows on DICOM images and metadata.
* [mercure](https://github.com/mercure-imaging/mercure) ⭐ 100 | 🐛 11 | 🌐 JavaScript | 📅 2026-07-09 - A flexible DICOM routing and processing solution with user-friendly web interface and extensive monitoring functions.

#### Validation

* [DVTk](https://github.com/dvtk-org/DVTk) ⭐ 191 | 🐛 22 | 🌐 C# | 📅 2026-08-06 - Testing, validating and diagnosing DICOM communication in medical environments.

#### Visualization

* [AlizaMS](https://github.com/AlizaMedicalImaging/AlizaMS) ⭐ 308 | 🐛 3 | 🌐 C++ | 📅 2026-08-13 - DICOM viewer.

#### Image Computing Platforms

* [3D Slicer](https://slicer.org) - Free and open source workstation software with tools for many clinical specialies and DICOM datatypes. Supports visualization, registration, segmentation, time series analysis and much more.

## Contribute

Contributions welcome! Read the [contribution guidelines](contributing.md) first.

***

> _Enhansomed by [enhansome](https://github.com/enhansome) on 2026-08-18._
