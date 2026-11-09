<!-- omit in toc -->

# Awesome DICOM with stars

> International standard for storing, exchanging and displaying medical images and related information.

The [DICOM Standard](https://www.dicomstandard.org/) defines the formats for medical images that can be exchanged with the data and quality necessary for clinical use.[^1] This list collects open source DICOM libraries, viewers, servers, converters and de-identification tools, along with datasets and learning resources.

<!-- omit in toc -->

## Contents

* [Datasets](#datasets)
* [Hosted Tools](#hosted-tools)
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

## Datasets

* [The Cancer Imaging Archive (TCIA)](https://www.cancerimagingarchive.net/) - Freely available radiology and pathology cancer imaging datasets.
* [Imaging Data Commons (IDC)](https://datacommons.cancer.gov/repository/imaging-data-commons) - Cloud-based repository of public cancer imaging data in DICOM, covering radiology, digital pathology and analysis results. Mirrors all public radiology DICOM collections in TCIA.
* [Medical Imaging and Data Resource Center (MIDRC)](https://www.midrc.org/) - Repository of de-identified medical imaging data in DICOM, first assembled for COVID-19 research.

## Hosted Tools

Free tools that run in the browser, with no installation or account. Their source code is not necessarily public.

* [MiniPACS Free DICOM Viewer](https://minipacs.net/free-dicom-viewer/) - Viewer that decodes JPEG, JPEG-LS, JPEG 2000, RLE and Deflated transfer syntaxes. Files are parsed locally and never uploaded.
* [RadRobin](https://radrobin.com) - Client-side viewer with multiplanar and 3D rendering. Opens local files without uploading them, streams from DICOMweb servers, and reads and writes DICOM SR and SEG.
* [tresD DICOM](https://tresddicom.com) - CBCT viewer with volume rendering presets, panoramic and cephalometric reconstructions, airway views, T0/T1 superimposition and alignment of STL/PLY intraoral scans. Files never leave the computer.

## Learning Resources

* [The DICOM Standard](https://www.dicomstandard.org/current) - Current edition of every part of the standard, in PDF, HTML, DOCX, ODT and XML.
* [DICOM Library](https://www.dicomlibrary.com/) - Free online service for sharing DICOM images and videos for education and research.
* [DICOM Standard Browser](https://dicom.innolitics.com/ciods) - Browsable tree of the information object definitions, modules and attributes in Part 3 of the standard.
* [Saga DICOM Standard Browser](https://saga-it.com/dicom/spec) - Cross-linked index of PS3 covering attributes, CIODs, modules, SOP classes, transfer syntaxes and VRs, alongside HL7 v2 and FHIR mapping references.
* [DICOM Transfer Syntax Registry and Viewer Decode Matrix](https://minipacs.net/dicom-transfer-syntax/) - Every PS3.6 transfer syntax UID, with a tested matrix of which free viewers decode which syntaxes, screenshots and CSV downloads (CC BY 4.0).
* [DICOM is Easy](https://dicomiseasy.blogspot.com/2011/10/introduction-to-dicom-chapter-1.html) - Blog with a series of introductory DICOM tutorials.
* [Work with medical imaging data and DICOM](https://learn.microsoft.com/en-us/training/modules/medical-imaging-data/) - Short Microsoft Learn module on medical imaging data in general and DICOM in particular.
* [Saravanan Subramanian's DICOM tutorials](https://saravanansubramanian.com/dicom/) - Articles and tutorials on working with DICOM in Java and .NET.

## Libraries

### C\#

#### General

* [fo-dicom](https://github.com/fo-dicom/fo-dicom) ⭐ 1,220 | 🐛 84 | 🌐 C# | 📅 2026-11-02 - Fellow Oak DICOM, a .NET toolkit for reading, writing, rendering and networking DICOM.

#### Visualization

* [UnityVolumeRendering](https://github.com/mlavik1/UnityVolumeRendering) ⭐ 563 | 🐛 70 | 🌐 C# | 📅 2026-11-07 - Volume renderer for Unity3D that imports DICOM and NRRD datasets.

### C++

#### General

* [SimpleITK](https://github.com/SimpleITK/SimpleITK) ⭐ 1,096 | 🐛 103 | 🌐 C++ | 📅 2026-11-07 - Simplified interface to the [Insight Toolkit (ITK)](https://itk.org/) for filtering, segmentation and registration, including reading and writing DICOM series.
* [CTK](https://github.com/commontk/CTK) ⭐ 969 | 🐛 232 | 🌐 C++ | 📅 2026-11-03 - Common Toolkit of support code for medical image analysis and surgical navigation, including Qt widgets for browsing, querying and retrieving DICOM data.
* [DCMTK](https://github.com/DCMTK/dcmtk) ⭐ 920 | 🐛 12 | 🌐 C++ | 📅 2026-11-07 - Libraries and command-line tools for DICOM file handling, networking and image processing.
* [MITK](https://github.com/MITK/MITK) ⭐ 848 | 🐛 2 | 🌐 C++ | 📅 2026-11-06 - Medical Imaging Interaction Toolkit, a framework built on ITK and VTK for developing interactive medical image processing software.
* [GDCM](https://github.com/malaterre/GDCM) ⭐ 399 | 🐛 13 | 🌐 C++ | 📅 2026-08-21 - Grassroots DICOM, a library for reading, writing and transcoding DICOM files and for DICOM networking, with bindings for Python, C#, Java and PHP.
* [vtk-dicom](https://github.com/dgobbi/vtk-dicom) ⭐ 287 | 🐛 68 | 🌐 C++ | 📅 2026-10-15 - VTK classes for reading and writing DICOM files and metadata, plus utilities for inspecting and converting DICOM files.
* [dcmqi](https://github.com/QIICR/dcmqi) ⭐ 282 | 🐛 73 | 🌐 C++ | 📅 2026-10-26 - Libraries and command-line tools for converting quantitative image analysis results, such as segmentations and parametric maps, to and from DICOM.
* [Orthanc](https://github.com/jodogne/OrthancMirror) ⭐ 44 | 🐛 0 | 🌐 C++ | 📅 2026-11-09 - Lightweight standalone DICOM server with a REST API and a plugin system.

#### Conversion

* [dcm2niix](https://github.com/rordenlab/dcm2niix) ⭐ 1,210 | 🐛 1 | 🌐 C++ | 📅 2026-11-06 - Convert neuroimaging data from DICOM to [NIfTI](https://nifti.nimh.nih.gov/).
* [DicomToMesh](https://github.com/eidelen/DicomToMesh) ⭐ 532 | 🐛 6 | 🌐 C++ | 📅 2026-03-28 - Command-line tool that turns a DICOM volume into a 3D surface mesh (OBJ, STL or PLY), with optional mesh reduction, smoothing and cleaning.

#### Other

* [DICOMautomaton](https://github.com/hdclark/DICOMautomaton) ⭐ 91 | 🐛 35 | 🌐 C++ | 📅 2026-09-24 - Multipurpose tool for analyzing medical physics data, with a focus on automation.
* [dovo](https://github.com/DraconPern/dovo) ⭐ 43 | 🐛 2 | 🌐 C++ | 📅 2026-03-30 - Cross-platform software for importing DICOM CDs and files and sending them to a PACS.

### Go

* [dicom](https://github.com/suyashkumar/dicom) ⭐ 1,097 | 🐛 140 | 🌐 Go | 📅 2026-06-21 - High-performance DICOM parser for Go.

### Java

#### General

* [dcm4che](https://github.com/dcm4che/dcm4che) ⭐ 1,465 | 🐛 174 | 🌐 Java | 📅 2026-11-06 - DICOM toolkit and library with command-line utilities for file handling and networking.
* [Dicoogle](https://github.com/dicoogle/dicoogle) ⭐ 535 | 🐛 63 | 🌐 Java | 📅 2026-10-29 - Extensible PACS archive that indexes DICOM metadata for flexible search and retrieval instead of relying on a traditional centralized database.
* [healthcare-dicom-dicomweb-adapter](https://github.com/GoogleCloudPlatform/healthcare-dicom-dicomweb-adapter) ⭐ 146 | 🐛 27 | 🌐 Java | 📅 2026-11-06 - Components that translate between traditional DICOM DIMSE protocols, such as C-STORE, and DICOMweb, such as STOW-RS.

#### Visualization

* [Weasis](https://github.com/nroduit/Weasis) ⭐ 1,440 | 🐛 44 | 🌐 Java | 📅 2026-11-08 - Multipurpose standalone and web-based DICOM viewer with a modular architecture.

### JavaScript

#### General

* [dicomParser](https://github.com/cornerstonejs/dicomParser) ⭐ 753 | 🐛 47 | 🌐 JavaScript | 📅 2024-05-16 - Dependency-free parser for DICOM Part 10 and raw byte streams in browsers and Node.js.
* [dcmjs](https://github.com/dcmjs-org/dcmjs) ⭐ 356 | 🐛 157 | 🌐 JavaScript | 📅 2026-11-06 - Read, write and manipulate DICOM objects, including segmentations and structured reports, in browsers and Node.js.
* [dicomweb-client](https://github.com/dcmjs-org/dicomweb-client) ⭐ 160 | 🐛 32 | 🌐 JavaScript | 📅 2026-10-27 - JavaScript client for DICOMweb services.
* [dicomweb-pacs](https://github.com/knopkem/dicomweb-pacs) ⭐ 127 | 🐛 6 | 🌐 TypeScript | 📅 2026-03-22 - DICOMweb-enabled PACS with DIMSE services, backed by an SQLite database.
* [dcmjs-dimse](https://github.com/PantelisGeorgiadis/dcmjs-dimse) ⭐ 88 | 🐛 4 | 🌐 JavaScript | 📅 2026-10-20 - DICOM DIMSE implementation for Node.js using dcmjs.
* [Efferent.Dicom](https://github.com/Efferent-Health/Dicom.js) ⭐ 11 | 🐛 0 | 🌐 TypeScript | 📅 2026-06-03 - Lightweight JavaScript and TypeScript library for reading and writing DICOM files in browsers and Node.js.
* [dcmjs-codecs](https://github.com/PantelisGeorgiadis/dcmjs-codecs) ⭐ 5 | 🐛 1 | 🌐 JavaScript | 📅 2026-04-17 - DICOM file and dataset transcoding for Node.js and browsers using dcmjs.
* [@cosyte/dicom](https://github.com/cosyte/dicom) ⭐ 1 | 🐛 1 | 🌐 TypeScript | 📅 2026-11-09 - Dependency-free DICOM Part 10 parser and serializer for Node.js and TypeScript, built to read metadata from vendor-quirky files without decoding pixel data.

#### Visualization

* [OHIF Viewer](https://github.com/OHIF/Viewers) ⭐ 4,402 | 🐛 615 | 🌐 TypeScript | 📅 2026-11-05 - Zero-footprint, extensible web viewer from the [Open Health Imaging Foundation](https://ohif.org/) that works with DICOMweb archives.
* [DWV](https://github.com/ivmartel/dwv) ⭐ 1,854 | 🐛 42 | 🌐 JavaScript | 📅 2026-11-09 - Zero-footprint medical image viewer library in JavaScript and HTML5 that runs in any modern browser, on desktop or mobile.
* [Cornerstone3D](https://github.com/cornerstonejs/cornerstone3D) ⭐ 1,166 | 🐛 590 | 🌐 TypeScript | 📅 2026-11-05 - Libraries for building web-based medical imaging applications, with GPU-accelerated stack, MPR and volume rendering, annotation and segmentation tools, and a DICOM image loader.
* [NiiVue](https://github.com/niivue/niivue) ⭐ 506 | 🐛 29 | 🌐 TypeScript | 📅 2026-10-06 - WebGL viewer for voxel images (including DICOM and NIfTI), meshes and tractography that embeds in any web framework ([demos](https://niivue.com/demos/)).
* [VolView](https://github.com/Kitware/VolView) ⭐ 306 | 🐛 87 | 🌐 TypeScript | 📅 2026-11-08 - Web-based radiological viewer built with [Vue.js](https://vuejs.org/) and [VTK.js](https://github.com/Kitware/vtk-js) ⭐ 1,548 | 🐛 340 | 🌐 JavaScript | 📅 2026-11-07.
* [dicomviewer](https://github.com/ayselafsar/dicomviewer) ⭐ 269 | 🐛 7 | 🌐 JavaScript | 📅 2026-11-06 - Nextcloud app for viewing DICOM files, built on the OHIF Viewer.
* [bluelight](https://github.com/cylab-tw/bluelight) ⭐ 159 | 🐛 4 | 🌐 JavaScript | 📅 2026-11-03 - Lightweight browser-based DICOM viewer that runs as a single-page application on any HTTP server, with plugins for MPR, MIP, volume rendering and DICOM SEG editing.
* [dwv-react](https://github.com/ivmartel/dwv-react) ⭐ 134 | 🐛 2 | 🌐 JavaScript | 📅 2026-05-19 - Medical viewer using DWV and [React](https://react.dev/).
* [dicom-microscopy-viewer](https://github.com/ImagingDataCommons/dicom-microscopy-viewer) ⭐ 130 | 🐛 26 | 🌐 JavaScript | 📅 2026-11-04 - JavaScript library for web-based visualization of DICOM VL Whole Slide Microscopy Image datasets and derived information.
* [dcmjs-imaging](https://github.com/PantelisGeorgiadis/dcmjs-imaging) ⭐ 50 | 🐛 1 | 🌐 JavaScript | 📅 2026-10-20 - DICOM image and overlay rendering pipeline for Node.js and browsers using dcmjs.
* [dicom.ts](https://github.com/wearemothership/dicom.ts) ⭐ 48 | 🐛 16 | 🌐 TypeScript | 📅 2026-01-22 - Small DICOM parser and WebGL renderer for fast image display in the browser.
* [dcmjs-ecg](https://github.com/PantelisGeorgiadis/dcmjs-ecg) ⭐ 9 | 🐛 0 | 🌐 JavaScript | 📅 2026-05-19 - DICOM electrocardiography (ECG) rendering for Node.js and browsers using dcmjs.
* [dicom-nifti-viewer-vscode](https://github.com/theluckystrike/dicom-nifti-viewer-vscode) ⭐ 0 | 🐛 0 | 🌐 JavaScript | 📅 2026-11-07 - VS Code extension that opens DICOM, DICOMDIR and NIfTI files with CT window presets, axial, coronal and sagittal views and a searchable tag table.

#### Other

* [dicomweb-proxy](https://github.com/knopkem/dicomweb-proxy) ⭐ 82 | 🐛 2 | 🌐 TypeScript | 📅 2026-03-22 - Translates between DICOMweb and traditional DICOM DIMSE services.

### MATLAB

#### Conversion

* [dicm2nii](https://github.com/xiangruili/dicm2nii) ⭐ 103 | 🐛 0 | 🌐 MATLAB | 📅 2026-10-14 - Convert DICOM, as well as PAR/XML/REC, HEAD/BRIK, MGZ and BrainVoyager files, to NIfTI.

### Python

#### General

* [pydicom](https://github.com/pydicom/pydicom) ⭐ 2,234 | 🐛 69 | 🌐 Python | 📅 2026-11-08 - Pure Python package for reading, modifying and writing DICOM files.
* [pynetdicom](https://github.com/pydicom/pynetdicom) ⭐ 578 | 🐛 23 | 🌐 Python | 📅 2026-11-05 - Pure Python implementation of the DICOM networking protocol, used with pydicom to build Service Class Users (SCUs) and Service Class Providers (SCPs).
* [highdicom](https://github.com/ImagingDataCommons/highdicom) ⭐ 243 | 🐛 40 | 🌐 Python | 📅 2026-11-04 - High-level abstractions for creating and reading DICOM objects that hold image-derived information, such as annotations, segmentations and analysis results.
* [dicomweb-client](https://github.com/ImagingDataCommons/dicomweb-client) ⭐ 130 | 🐛 17 | 🌐 Python | 📅 2026-08-17 - Python client for the DICOMweb services QIDO-RS, WADO-RS and STOW-RS, to search, retrieve and store DICOM objects.

#### Conversion

* [dicom2nifti](https://github.com/icometrix/dicom2nifti) ⭐ 403 | 🐛 64 | 🌐 Python | 📅 2025-06-23 - Convert MR and CT-derived DICOM files to NIfTI.
* [heudiconv](https://github.com/nipy/heudiconv) ⭐ 287 | 🐛 219 | 🌐 Python | 📅 2026-10-05 - Flexible DICOM converter for organizing brain imaging data into structured directory layouts.
* [dicom2stl](https://github.com/dave3d/dicom2stl) ⭐ 218 | 🐛 9 | 🌐 Python | 📅 2026-10-16 - Convert a DICOM series to an [STL](https://en.wikipedia.org/wiki/STL_\(file_format\)) surface mesh.
* [wsidicomizer](https://github.com/imi-bigpicture/wsidicomizer) ⭐ 92 | 🐛 9 | 🌐 Python | 📅 2026-11-06 - Convert proprietary whole slide image formats to DICOM, reusing the original compressed tiles where possible.
* [dcmstack](https://github.com/moloney/dcmstack) ⭐ 78 | 🐛 19 | 🌐 Python | 📅 2026-03-24 - DICOM to NIfTI conversion with the added ability to extract and summarize metadata from the source files.
* [bidskit](https://github.com/jmtyszka/bidskit) ⭐ 65 | 🐛 19 | 🌐 Python | 📅 2026-05-29 - CLI for converting a directory of DICOM files into a [BIDS](https://bids.neuroimaging.io/)-compliant dataset.
* [Dicomifier](https://github.com/lamyj/dicomifier) ⭐ 32 | 🐛 7 | 🌐 Python | 📅 2025-07-20 - Tools to convert Bruker data to DICOM files, and DICOM files to NIfTI.

#### Anonymization

* [deid](https://github.com/pydicom/deid) ⭐ 181 | 🐛 29 | 🌐 Python | 📅 2026-11-07 - Best-effort de-identification of medical images, driven by recipe files.
* [dicom-anonymizer](https://github.com/KitwareMedical/dicom-anonymizer) ⭐ 146 | 🐛 5 | 🌐 Python | 📅 2026-09-04 - Command-line tool that anonymizes DICOM files following the DICOM standard.
* [dcm-anon](https://github.com/Ces107/dcm-anon) ⭐ 5 | 🐛 0 | 🌐 Python | 📅 2026-06-07 - PS3.15 Basic Profile anonymizer that emits a hash-chained GDPR/HIPAA compliance manifest and an independent post-run residual-PHI scan.

#### Sorting

* [dicomsort](https://github.com/pieper/dicomsort) ⭐ 87 | 🐛 8 | 🌐 Python | 📅 2025-05-06 - Copies DICOM files from any folder layout into a user-defined folder hierarchy, renaming them from their metadata.
* [MIA Toolkit](https://github.com/Fritanga-Collective/mia-toolkit) ⭐ 0 | 🐛 3 | 🌐 Python | 📅 2026-11-08 - Desktop app that consolidates DICOM studies from multiple CDs and USB drives into a single de-duplicated, verified DICOMDIR archive.

#### Visualization

* [MRIcroGL](https://github.com/rordenlab/MRIcroGL) ⭐ 296 | 🐛 3 | 🌐 Python | 📅 2025-11-23 - Cross-platform volume renderer for DICOM, NIfTI and other voxel formats, with a drag-and-drop interface and Python scripting.
* [dicom-ecg-plot](https://github.com/marcodebe/dicom-ecg-plot) ⭐ 161 | 🐛 4 | 🌐 Python | 📅 2026-04-28 - Plot ECG data from DICOM ([demo](https://ecg.galliera.it/)).
* [OnkoDICOM](https://github.com/didymo/OnkoDICOM) ⭐ 73 | 🐛 35 | 🌐 Python | 📅 2026-11-08 - DICOM RT viewer with tools for radiation oncology research.
* [FSLeyes](https://github.com/pauldmccarthy/fsleyes) ⭐ 29 | 🐛 15 | 🌐 Python | 📅 2026-08-25 - Cross-platform viewer for NIfTI and DICOM images, from the FSL neuroimaging suite.

#### Other

* [dicom-standard](https://github.com/innolitics/dicom-standard) ⭐ 133 | 🐛 54 | 🌐 HTML | 📅 2026-04-17 - Parses the web version of the DICOM standard into human- and machine-readable JSON files.

### Rust

* [DICOM-rs](https://github.com/Enet4/dicom-rs) ⭐ 574 | 🐛 68 | 🌐 Rust | 📅 2026-10-27 - Pure Rust implementation of the DICOM standard for working with DICOM objects and communicating with DICOM applications.

### Other/Combination

#### Machine Learning

* [mercure](https://github.com/mercure-imaging/mercure) ⭐ 105 | 🐛 20 | 🌐 JavaScript | 📅 2026-11-09 - DICOM routing and processing platform with a web interface and extensive monitoring.

#### Validation

* [DVTk](https://github.com/dvtk-org/DVTk) ⭐ 194 | 🐛 24 | 🌐 C# | 📅 2026-08-06 - Testing, validating and diagnosing DICOM communication in medical environments.

#### Visualization

* [AlizaMS](https://github.com/AlizaMedicalImaging/AlizaMS) ⭐ 318 | 🐛 3 | 🌐 C++ | 📅 2026-09-18 - Cross-platform DICOM viewer with 2D and 3D views, MPR and volume rendering.

#### Image Computing Platforms

* [3D Slicer](https://github.com/Slicer/Slicer) ⭐ 2,712 | 🐛 672 | 🌐 C++ | 📅 2026-11-08 - Desktop platform for medical image visualization, segmentation and registration, with a DICOM browser and support for many clinical DICOM object types.

## Contributing

Contributions welcome! Read the [contribution guidelines](contributing.md) first. Projects that are no longer maintained are listed in the [archive](archive.md).

[^1]: [About the DICOM Standard](https://www.dicomstandard.org/about-home), NEMA.

***

> _Enhansomed by [enhansome](https://github.com/enhansome) on 2026-11-09._
