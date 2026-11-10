<!-- omit in toc -->

# Awesome DICOM with stars

> International standard for storing, exchanging and displaying medical images and related information.

The [DICOM Standard](https://www.dicomstandard.org/) defines the formats for medical images that can be exchanged with the data and quality necessary for clinical use.[^1] This list collects open source DICOM libraries, viewers, servers, converters and de-identification tools, along with datasets and learning resources.

<!-- omit in toc -->

## Contents

* [Datasets](#datasets)
  * [Research Collections](#research-collections)
  * [Test Files](#test-files)
* [Hosted Tools](#hosted-tools)
* [Learning Resources](#learning-resources)
  * [The Standard](#the-standard)
  * [Guides and Tutorials](#guides-and-tutorials)
  * [Books](#books)
  * [Community](#community)
* [Libraries](#libraries)
  * [C#](#c)
  * [C and C++](#c-and-c)
  * [Go](#go)
  * [Java](#java)
  * [JavaScript](#javascript)
  * [Python](#python)
  * [R](#r)
  * [Rust](#rust)
* [Tools](#tools)
  * [Conversion](#conversion)
  * [De-identification](#de-identification)
  * [Dose Monitoring](#dose-monitoring)
  * [File Management](#file-management)
  * [Gateways and Routing](#gateways-and-routing)
  * [Radiation Therapy](#radiation-therapy)
  * [Research Platforms](#research-platforms)
  * [Servers and PACS](#servers-and-pacs)
  * [Validation](#validation)
  * [Viewers](#viewers)

## Datasets

### Research Collections

* [The Cancer Imaging Archive (TCIA)](https://www.cancerimagingarchive.net/) - Radiology and pathology cancer imaging collections. Access: open, except a few collections that need a data use agreement through dbGaP.
* [Imaging Data Commons (IDC)](https://datacommons.cancer.gov/repository/imaging-data-commons) - Cloud-based repository of public cancer imaging data in DICOM, covering radiology, digital pathology and analysis results, including every public radiology collection in TCIA. Access: open, with no registration ([portal](https://portal.imaging.datacommons.cancer.gov/)).
* [Medical Imaging and Data Resource Center (MIDRC)](https://www.midrc.org/) - Repository of de-identified medical imaging data in DICOM, first assembled for COVID-19 research. Access: registered users who accept its data use agreement.
* [MIMIC-CXR](https://physionet.org/content/mimic-cxr/) - Chest radiographs in DICOM with free-text radiology reports, from the Beth Israel Deaconess Medical Center. Access: credentialed PhysioNet users who sign its data use agreement.
* [MIMIC-IV-Echo](https://physionet.org/content/mimic-iv-echo/) - Echocardiograms in DICOM from the Beth Israel Deaconess Medical Center, linked to the MIMIC-IV clinical database. Access: credentialed PhysioNet users who sign its data use agreement.
* [VinDr](https://vindr.ai/datasets) - Radiologist-annotated chest X-ray, pediatric chest X-ray, mammography and spine X-ray datasets in DICOM. Access: through PhysioNet, for users who sign a data use agreement, and VinDr-CXR also requires credentialing.
* [fastMRI](https://fastmri.med.nyu.edu/) - Raw MRI k-space data from NYU Langone Health, plus DICOM images from 10,000 clinical knee MRI exams. Access: by application, accepting its data sharing agreement.
* [CheXpert Plus](https://aimi.stanford.edu/datasets/chexpert-plus) - Chest radiographs in DICOM paired with radiology reports and patient demographics, from Stanford. Access: registered Redivis users who accept the dataset's terms.
* [EMBED](https://registry.opendata.aws/emory-breast-imaging-dataset-embed/) - Screening and diagnostic mammograms in DICOM from the Emory Breast Imaging Dataset, with image-level metadata and clinical findings. Access: by request, under a data use agreement.
* [LIDC-IDRI](https://www.cancerimagingarchive.net/collection/lidc-idri/) - Thoracic CT scans with lung nodule annotations from four radiologists, plus some chest radiographs, hosted by TCIA. Access: open.

### Test Files

* [pydicom-data](https://github.com/pydicom/pydicom-data) ⭐ 11 | 🐛 1 | 🌐 Python | 📅 2025-09-14 - Test files used by pydicom's test suite. Access: open.
* [gdcmData](https://github.com/malaterre/gdcmdata) ⭐ 0 | 🐛 0 | 📅 2026-07-03 - GDCM's regression set of vendor-specific and malformed files, many named after the defect they exercise. Access: open.
* [David Clunie's test images](https://www.dclunie.com/#Images) - Test images for character sets, the Deflate transfer syntax, signed pixel ranges, pixel spacing and mammography CAD, among others. Access: open.
* [MIDI-B](https://www.cancerimagingarchive.net/collection/midi-b-test-midi-b-validation/) - Validation and test sets from the MIDI-B de-identification challenge, with synthetic PHI and answer keys. Access: open.
* [OpenSlide DICOM test data](https://openslide.cs.cmu.edu/download/openslide-testdata/DICOM/) - DICOM whole slide images from several scanner vendors, including unusual encodings. Access: open.
* [Pseudo-PHI-DICOM-Data](https://www.cancerimagingarchive.net/collection/pseudo-phi-dicom-data/) - CT, MR, PET and X-ray images with synthetic PHI in standard and private tags, for evaluating de-identification tools. Access: open.
* [Rubo DICOM samples](https://www.rubomedical.com/dicom_files/) - Small X-ray angiography, fluoroscopy, ultrasound and MRI samples, encoded with lossy JPEG, RLE or no compression, including a palette color image. Access: open.

## Hosted Tools

Free tools and services hosted online, with no installation or account. Their source code is not necessarily public.

DICOM files can carry protected health information in their tags, pixel data and filenames. Use de-identified data unless a tool processes files locally, and connect a hosted viewer to an institutional DICOMweb server only with your organization's approval.

* [DICOM Library](https://www.dicomlibrary.com/) - Service for sharing DICOM studies by link, with sample studies by modality. It anonymizes a fixed set of tags in the browser before uploading, but not burned-in text or other tags.
* [Medical Connections DICOM Server](https://www.dicomserver.co.uk/) - Public server for testing C-STORE, C-FIND, C-GET, C-MOVE and Modality Worklist, which accepts any AE title. Uploaded files are visible to all users and deleted weekly, and DIMSE traffic is not encrypted, so send only test data.
* [MiniPACS Free DICOM Viewer](https://minipacs.net/free-dicom-viewer/) - Viewer that decodes JPEG, JPEG-LS, JPEG 2000, RLE and Deflated transfer syntaxes. Files are parsed locally and never uploaded.
* [RadRobin](https://radrobin.com) - Client-side viewer with multiplanar and 3D rendering. Opens local files without uploading them, streams from DICOMweb servers, and reads and writes DICOM SR and SEG.
* [tresD DICOM](https://tresddicom.com) - CBCT viewer with volume rendering presets, panoramic and cephalometric reconstructions, airway views, T0/T1 superimposition and alignment of STL/PLY intraoral scans. Files never leave the computer.

## Learning Resources

### The Standard

* [dicom-standard](https://github.com/innolitics/dicom-standard) ⭐ 133 | 🐛 54 | 🌐 HTML | 📅 2026-04-17 - Parses the web version of the DICOM standard into human- and machine-readable JSON files, last published for release 2024b.
* [The DICOM Standard](https://www.dicomstandard.org/current) - Current edition of every part of the standard, in PDF, HTML, DOCX, ODT and XML.
* [DICOM Standard Browser](https://dicom.innolitics.com/ciods) - Browsable tree of the information object definitions, modules and attributes in Part 3 of the standard.
* [Saga DICOM Standard Browser](https://saga-it.com/dicom/spec) - Cross-linked index of PS3 covering attributes, CIODs, modules, SOP classes, transfer syntaxes and VRs, alongside HL7 v2 and FHIR mapping references.
* [DICOM Transfer Syntax Registry and Viewer Decode Matrix](https://minipacs.net/dicom-transfer-syntax/) - Every PS3.6 transfer syntax UID, with a tested matrix of which free viewers decode which syntaxes, screenshots and CSV downloads (CC BY 4.0).
* [PS3.5 Data Structures and Encoding](https://dicom.nema.org/medical/dicom/current/output/html/part05.html) - Value representations, transfer syntaxes, character sets and the encoding of data sets.
* [PS3.6 Data Dictionary](https://dicom.nema.org/medical/dicom/current/output/html/part06.html) - Registry of every standard data element, with its tag, VR and multiplicity, and of every registered UID.
* [PS3.15 Security and System Management Profiles](https://dicom.nema.org/medical/dicom/current/output/html/part15.html) - Security profiles, including the attribute confidentiality profiles that de-identification tools follow.
* [PS3.18 Web Services](https://dicom.nema.org/medical/dicom/current/output/html/part18.html) - Specification of DICOMweb, including QIDO-RS, WADO-RS, STOW-RS and UPS-RS, and of the DICOM JSON model.
* [DICOM Conformance Statement Template](https://dicom.nema.org/medical/dicom/current/output/chtml/part02/chapter_N.html) - Annex N of PS3.2, the normative template that conformance statements follow.
* [DICOMweb](https://www.dicomstandard.org/using/dicomweb) - Official overview of the DICOMweb services, with a downloadable cheat sheet.
* [DICOM Standard Status](https://www.dclunie.com/dicom-status/status.html) - David Clunie's tracker of the status of every part, supplement and change proposal.

### Guides and Tutorials

* [IDC-Tutorials](https://github.com/ImagingDataCommons/IDC-Tutorials) ⭐ 50 | 🐛 25 | 🌐 Jupyter Notebook | 📅 2026-10-22 - Notebooks for finding, downloading and analyzing DICOM data from Imaging Data Commons.
* [DICOM is Easy](https://dicomiseasy.blogspot.com/2011/10/introduction-to-dicom-chapter-1.html) - Blog with a series of introductory DICOM tutorials.
* [Work with medical imaging data and DICOM](https://learn.microsoft.com/en-us/training/modules/medical-imaging-data/) - Short Microsoft Learn module on medical imaging data in general and DICOM in particular.
* [Saravanan Subramanian's DICOM tutorials](https://saravanansubramanian.com/dicom/) - Articles and tutorials on working with DICOM in Java and .NET.
* [Understanding DICOM with Orthanc](https://orthanc.uclouvain.be/book/dicom-guide.html) - Introduction to the DICOM file format, model of the real world, identifiers and network protocol, with hands-on examples using Orthanc.
* [dcm4che DICOMweb guide](https://dcm4che.github.io/dicomweb/) - Overview of the DICOMweb services and their DIMSE equivalents, with curl examples against dcm4chee-arc.
* [Introduction to DICOM](https://learn.canceridc.dev/dicom/introduction) - DICOM and its data model, from the Imaging Data Commons user guide.
* [DICOM presentations](https://www.dicomstandard.org/presentations) - Archive of slides from DICOM Standards Committee conferences and tutorials, from 2000 to 2018.
* [IHE Radiology Technical Framework](https://profiles.ihe.net/RAD/index.html) - Integration profiles, such as Scheduled Workflow, that define how radiology systems use DICOM and HL7 together.

### Books

* [Digital Imaging and Communications in Medicine (DICOM)](https://link.springer.com/book/10.1007/978-3-642-10850-1) - Oleg Pianykh's practical introduction to the standard (Springer, 2nd edition, 2012).
* [DICOM Structured Reporting](https://www.dclunie.com/pixelmed/DICOMSR.book.pdf) - David Clunie's book on DICOM SR (PixelMed Publishing, 2000), free as a PDF.

### Community

* [pydicom Discussions](https://github.com/pydicom/pydicom/discussions) ⭐ 2,234 | 🐛 69 | 🌐 Python | 📅 2026-11-09 - Questions and answers about pydicom.
* [comp.protocols.dicom](https://groups.google.com/g/comp.protocols.dicom) - Read-only archive of the long-running Usenet group for DICOM implementation questions.
* [dcm4che group](https://groups.google.com/g/dcm4che) - Discussion group for the dcm4che toolkit and the dcm4chee archive.
* [IDC Forum](https://discourse.canceridc.dev/) - Forum for questions about Imaging Data Commons data and tools.
* [OHIF Community](https://community.ohif.org/) - Forum for users and developers of the OHIF Viewer.
* [Orthanc Discourse](https://discourse.orthanc-server.org/) - Forum for users and developers of Orthanc, where new accounts are by invitation.

## Libraries

Packages to use in your own code, grouped by language.

### C\#

* [fo-dicom](https://github.com/fo-dicom/fo-dicom) ⭐ 1,220 | 🐛 84 | 🌐 C# | 📅 2026-11-02 - Fellow Oak DICOM, a .NET toolkit for reading, writing, rendering and networking DICOM.
* [MingRay (UnityVolumeRendering)](https://github.com/mlavik1/UnityVolumeRendering) ⭐ 563 | 🐛 70 | 🌐 C# | 📅 2026-11-07 - Volume renderer for Unity3D that imports DICOM and NRRD datasets.
* [fo-dicom.Codecs](https://github.com/Efferent-Health/fo-dicom.Codecs) ⭐ 80 | 🐛 5 | 🌐 C | 📅 2026-11-09 - Native JPEG, JPEG-LS, JPEG 2000, HTJ2K and RLE codecs for fo-dicom on Windows, Linux and macOS.

### C and C++

* [SimpleITK](https://github.com/SimpleITK/SimpleITK) ⭐ 1,096 | 🐛 105 | 🌐 C++ | 📅 2026-11-09 - Simplified interface to the [Insight Toolkit (ITK)](https://itk.org/) for filtering, segmentation and registration, including reading and writing DICOM series.
* [CTK](https://github.com/commontk/CTK) ⭐ 970 | 🐛 232 | 🌐 C++ | 📅 2026-11-03 - Common Toolkit of support code for medical image analysis and surgical navigation, including Qt widgets for browsing, querying and retrieving DICOM data.
* [DCMTK](https://github.com/DCMTK/dcmtk) ⭐ 919 | 🐛 12 | 🌐 C++ | 📅 2026-11-07 - Libraries and command-line tools for DICOM file handling, networking and image processing.
* [MITK](https://github.com/MITK/MITK) ⭐ 848 | 🐛 1 | 🌐 C++ | 📅 2026-11-06 - Medical Imaging Interaction Toolkit, a framework built on ITK and VTK for developing interactive medical image processing software.
* [GDCM](https://github.com/malaterre/GDCM) ⭐ 400 | 🐛 13 | 🌐 C++ | 📅 2026-08-21 - Grassroots DICOM, a library for reading, writing and transcoding DICOM files and for DICOM networking, with bindings for Python, C#, Java and PHP.
* [vtk-dicom](https://github.com/dgobbi/vtk-dicom) ⭐ 287 | 🐛 68 | 🌐 C++ | 📅 2026-10-15 - VTK classes for reading and writing DICOM files and metadata, plus utilities for inspecting and converting DICOM files.
* [libdicom](https://github.com/ImagingDataCommons/libdicom) ⭐ 40 | 🐛 7 | 🌐 C | 📅 2026-07-01 - C library for reading DICOM files, with efficient access to individual frames of whole slide microscopy images.

### Go

* [dicom](https://github.com/suyashkumar/dicom) ⭐ 1,097 | 🐛 140 | 🌐 Go | 📅 2026-06-21 - High-performance DICOM parser for Go.

### Java

* [dcm4che](https://github.com/dcm4che/dcm4che) ⭐ 1,465 | 🐛 174 | 🌐 Java | 📅 2026-11-06 - DICOM toolkit and library with command-line utilities for file handling and networking.
* [PixelMed Java DICOM Toolkit](https://www.dclunie.com/pixelmed/software/index.html) - Toolkit and applications for DICOM files and networking, validation, structured reports and de-identification.

### JavaScript

* [DWV](https://github.com/ivmartel/dwv) ⭐ 1,855 | 🐛 42 | 🌐 JavaScript | 📅 2026-11-10 - Zero-footprint medical image viewer library in JavaScript and HTML5 that runs in any modern browser, on desktop or mobile ([demo](https://ivmartel.github.io/dwv/)).
* [Cornerstone3D](https://github.com/cornerstonejs/cornerstone3D) ⭐ 1,166 | 🐛 600 | 🌐 TypeScript | 📅 2026-11-10 - Libraries for building web-based medical imaging applications, with GPU-accelerated stack, MPR and volume rendering, annotation and segmentation tools, and a DICOM image loader.
* [dicomParser](https://github.com/cornerstonejs/dicomParser) ⭐ 754 | 🐛 47 | 🌐 JavaScript | 📅 2024-05-16 - Dependency-free parser for DICOM Part 10 and raw byte streams in browsers and Node.js ([demo](https://cornerstonejs.github.io/dicomParser/examples/dumpWithDataDictionary/index.html)).
* [NiiVue](https://github.com/niivue/niivue) ⭐ 506 | 🐛 29 | 🌐 TypeScript | 📅 2026-10-06 - WebGL viewer for voxel images (including DICOM and NIfTI), meshes and tractography that embeds in any web framework ([demos](https://niivue.com/demos/)).
* [dcmjs](https://github.com/dcmjs-org/dcmjs) ⭐ 357 | 🐛 157 | 🌐 JavaScript | 📅 2026-11-06 - Read, write and manipulate DICOM objects, including segmentations and structured reports, in browsers and Node.js.
* [@itk-wasm/dicom](https://github.com/InsightSoftwareConsortium/ITK-Wasm/tree/main/packages/dicom/typescript) ⭐ 235 | 🐛 134 | 🌐 Python | 📅 2026-11-09 - WebAssembly builds of DCMTK and GDCM functions for reading DICOM series, tags and encapsulated PDFs, rendering structured reports and applying presentation states, in browsers and Node.js.
* [dicomweb-client](https://github.com/dcmjs-org/dicomweb-client) ⭐ 160 | 🐛 32 | 🌐 JavaScript | 📅 2026-10-27 - JavaScript client for DICOMweb services.
* [dicom-microscopy-viewer](https://github.com/ImagingDataCommons/dicom-microscopy-viewer) ⭐ 130 | 🐛 26 | 🌐 JavaScript | 📅 2026-11-04 - JavaScript library for web-based visualization of DICOM VL Whole Slide Microscopy Image datasets and derived information.
* [dcmjs-dimse](https://github.com/PantelisGeorgiadis/dcmjs-dimse) ⭐ 88 | 🐛 4 | 🌐 JavaScript | 📅 2026-10-20 - DICOM DIMSE implementation for Node.js using dcmjs.
* [dcmjs-imaging](https://github.com/PantelisGeorgiadis/dcmjs-imaging) ⭐ 50 | 🐛 1 | 🌐 JavaScript | 📅 2026-10-20 - DICOM image and overlay rendering pipeline for Node.js and browsers using dcmjs.
* [dicom.ts](https://github.com/wearemothership/dicom.ts) ⭐ 48 | 🐛 16 | 🌐 TypeScript | 📅 2026-01-22 - Small DICOM parser and WebGL renderer for fast image display in the browser.
* [Efferent.Dicom](https://github.com/Efferent-Health/Dicom.js) ⭐ 11 | 🐛 0 | 🌐 TypeScript | 📅 2026-06-03 - Lightweight JavaScript and TypeScript library for reading and writing DICOM files in browsers and Node.js.
* [dcmjs-ecg](https://github.com/PantelisGeorgiadis/dcmjs-ecg) ⭐ 9 | 🐛 0 | 🌐 JavaScript | 📅 2026-05-19 - DICOM electrocardiography (ECG) rendering for Node.js and browsers using dcmjs.
* [dcmjs-codecs](https://github.com/PantelisGeorgiadis/dcmjs-codecs) ⭐ 5 | 🐛 1 | 🌐 JavaScript | 📅 2026-04-17 - DICOM file and dataset transcoding for Node.js and browsers using dcmjs.
* [@cosyte/dicom](https://github.com/cosyte/dicom) ⭐ 1 | 🐛 1 | 🌐 TypeScript | 📅 2026-11-10 - Dependency-free DICOM Part 10 parser and serializer for Node.js and TypeScript, built to read metadata from vendor-quirky files without decoding pixel data.

### Python

* [pydicom](https://github.com/pydicom/pydicom) ⭐ 2,234 | 🐛 69 | 🌐 Python | 📅 2026-11-09 - Pure Python package for reading, modifying and writing DICOM files.
* [pynetdicom](https://github.com/pydicom/pynetdicom) ⭐ 579 | 🐛 23 | 🌐 Python | 📅 2026-11-05 - Pure Python implementation of the DICOM networking protocol, used with pydicom to build Service Class Users (SCUs) and Service Class Providers (SCPs).
* [rt-utils](https://github.com/qurit/rt-utils) ⭐ 257 | 🐛 66 | 🌐 Python | 📅 2026-09-30 - Creates DICOM RT structure sets from NumPy masks, and extracts masks from existing ones.
* [highdicom](https://github.com/ImagingDataCommons/highdicom) ⭐ 243 | 🐛 40 | 🌐 Python | 📅 2026-11-04 - High-level abstractions for creating and reading DICOM objects that hold image-derived information, such as annotations, segmentations and analysis results.
* [MONAI Deploy App SDK](https://github.com/Project-MONAI/monai-deploy-app-sdk) ⭐ 145 | 🐛 59 | 🌐 Python | 📅 2026-10-28 - Framework for packaging AI inference pipelines that load DICOM series and write results as DICOM segmentations and structured reports.
* [dicomweb-client](https://github.com/ImagingDataCommons/dicomweb-client) ⭐ 130 | 🐛 17 | 🌐 Python | 📅 2026-08-17 - Python client for the DICOMweb services QIDO-RS, WADO-RS and STOW-RS, to search, retrieve and store DICOM objects.
* [pyorthanc](https://github.com/gacou54/pyorthanc) ⭐ 65 | 🐛 7 | 🌐 Python | 📅 2026-10-16 - Client for the Orthanc REST API, with helpers for finding, anonymizing and downloading patients, studies and series.
* [pylibjpeg](https://github.com/pydicom/pylibjpeg) ⭐ 53 | 🐛 2 | 🌐 Python | 📅 2026-04-01 - Plugin framework that lets pydicom decode JPEG, JPEG-LS, JPEG 2000, HTJ2K and RLE compressed pixel data.
* [wsidicom](https://github.com/imi-bigpicture/wsidicom) ⭐ 53 | 🐛 3 | 🌐 Python | 📅 2026-11-10 - Reads and writes DICOM whole slide images from disk or DICOMweb, with access to regions, tiles and annotations.
* [EZ-WSI DICOMweb](https://github.com/GoogleCloudPlatform/EZ-WSI-DICOMweb) ⭐ 44 | 🐛 10 | 🌐 Python | 📅 2026-05-19 - Extracts image patches from DICOM whole slide images stored on a DICOMweb server, for pathology machine learning.
* [idc-index](https://github.com/ImagingDataCommons/idc-index) ⭐ 31 | 🐛 31 | 🌐 Python | 📅 2026-11-09 - Searches and downloads DICOM data from NCI Imaging Data Commons using a bundled metadata index, without a cloud account.
* [python-gdcm](https://github.com/tfmoraes/python-gdcm) ⭐ 22 | 🐛 8 | 🌐 Python | 📅 2026-10-20 - Prebuilt Python wheels of GDCM, which pydicom can use to decode compressed pixel data.

### R

* [divest](https://github.com/jonclayden/divest) ⭐ 15 | 🐛 0 | 🌐 C++ | 📅 2026-10-30 - Sorts DICOM files and converts them to NIfTI-compatible images with their metadata, using dcm2niix.

### Rust

* [DICOM-rs](https://github.com/Enet4/dicom-rs) ⭐ 575 | 🐛 68 | 🌐 Rust | 📅 2026-10-27 - Pure Rust implementation of the DICOM standard for working with DICOM objects and communicating with DICOM applications.

## Tools

Applications and command-line tools to run, grouped by task.

### Conversion

* [dcm2niix](https://github.com/rordenlab/dcm2niix) ⭐ 1,210 | 🐛 0 | 🌐 C++ | 📅 2026-11-06 - Convert neuroimaging data from DICOM to [NIfTI](https://nifti.nimh.nih.gov/) ([demo](https://niivue.github.io/niivue-dcm2niix/)).
* [DicomToMesh](https://github.com/eidelen/DicomToMesh) ⭐ 532 | 🐛 6 | 🌐 C++ | 📅 2026-03-28 - Command-line tool that turns a DICOM volume into a 3D surface mesh (OBJ, STL or PLY), with optional mesh reduction, smoothing and cleaning.
* [dicom2nifti](https://github.com/icometrix/dicom2nifti) ⭐ 403 | 🐛 64 | 🌐 Python | 📅 2025-06-23 - Convert MR and CT-derived DICOM files to NIfTI.
* [heudiconv](https://github.com/nipy/heudiconv) ⭐ 287 | 🐛 219 | 🌐 Python | 📅 2026-10-05 - Flexible DICOM converter for organizing brain imaging data into structured directory layouts.
* [dcmqi](https://github.com/QIICR/dcmqi) ⭐ 282 | 🐛 73 | 🌐 C++ | 📅 2026-10-26 - Libraries and command-line tools for converting quantitative image analysis results, such as segmentations and parametric maps, to and from DICOM.
* [dicom2stl](https://github.com/dave3d/dicom2stl) ⭐ 218 | 🐛 9 | 🌐 Python | 📅 2026-10-16 - Convert a DICOM series to an [STL](https://en.wikipedia.org/wiki/STL_\(file_format\)) surface mesh.
* [Dcm2Bids](https://github.com/UNFmontreal/Dcm2Bids) ⭐ 209 | 🐛 4 | 🌐 Python | 📅 2026-10-26 - Converts DICOM to a BIDS dataset by running dcm2niix, using a configuration file that maps series metadata to BIDS names.
* [BIDScoin](https://github.com/Donders-Institute/bidscoin) ⭐ 162 | 🐛 17 | 🌐 Python | 📅 2026-10-22 - Converts DICOM and other neuroimaging source data to BIDS, with a GUI for mapping series to BIDS names.
* [dicom-ecg-plot](https://github.com/marcodebe/dicom-ecg-plot) ⭐ 161 | 🐛 4 | 🌐 Python | 📅 2026-04-28 - Render 12-lead ECG waveforms from DICOM files to PDF, PNG, SVG and other formats ([demo](https://ecg.galliera.it/)).
* [dicm2nii](https://github.com/xiangruili/dicm2nii) ⭐ 104 | 🐛 0 | 🌐 MATLAB | 📅 2026-10-14 - MATLAB tool that converts DICOM, as well as PAR/XML/REC, HEAD/BRIK, MGZ and BrainVoyager files, to NIfTI.
* [wsidicomizer](https://github.com/imi-bigpicture/wsidicomizer) ⭐ 92 | 🐛 8 | 🌐 Python | 📅 2026-11-10 - Convert proprietary whole slide image formats to DICOM, reusing the original compressed tiles where possible.
* [dcmstack](https://github.com/moloney/dcmstack) ⭐ 78 | 🐛 19 | 🌐 Python | 📅 2026-03-24 - DICOM to NIfTI conversion with the added ability to extract and summarize metadata from the source files.
* [bidskit](https://github.com/jmtyszka/bidskit) ⭐ 65 | 🐛 19 | 🌐 Python | 📅 2026-05-29 - CLI for converting a directory of DICOM files into a [BIDS](https://bids.neuroimaging.io/)-compliant dataset.
* [Dicomifier](https://github.com/lamyj/dicomifier) ⭐ 32 | 🐛 7 | 🌐 Python | 📅 2025-07-20 - Tools to convert Bruker data to DICOM files, and DICOM files to NIfTI.

### De-identification

* [deid](https://github.com/pydicom/deid) ⭐ 181 | 🐛 29 | 🌐 Python | 📅 2026-11-07 - Best-effort de-identification of medical images, driven by recipe files.
* [dicom-anonymizer](https://github.com/KitwareMedical/dicom-anonymizer) ⭐ 146 | 🐛 5 | 🌐 Python | 📅 2026-09-04 - Command-line tool that anonymizes DICOM files following the DICOM standard.
* [RSNA Anonymizer](https://github.com/RSNA/anonymizer) ⭐ 80 | 🐛 6 | 🌐 Python | 📅 2026-11-09 - Desktop application that imports studies from local folders or a PACS, de-identifies them, and exports them to a DICOM node or AWS S3.
* [Karnak](https://github.com/nroduit/karnak) ⭐ 55 | 🐛 8 | 🌐 Java | 📅 2026-11-03 - DICOM gateway that de-identifies or modifies the tags of studies in transit, configured through profiles in a web interface.
* [dicognito](https://github.com/blairconrad/dicognito) ⭐ 31 | 🐛 3 | 🌐 Python | 📅 2026-10-31 - Replaces identifying attributes with realistic fake values, consistently across all the files of a study.
* [dcm-anon](https://github.com/Ces107/dcm-anon) ⭐ 5 | 🐛 0 | 🌐 Python | 📅 2026-06-07 - PS3.15 Basic Profile anonymizer that emits a hash-chained GDPR/HIPAA compliance manifest and an independent post-run residual-PHI scan.

### Dose Monitoring

* [OpenREM](https://gitlab.com/openrem/OpenREM) - Web application that collects patient radiation dose data from DICOM Radiation Dose Structured Reports and image headers, for auditing.

### File Management

* [dicomsort](https://github.com/pieper/dicomsort) ⭐ 87 | 🐛 8 | 🌐 Python | 📅 2025-05-06 - Copies DICOM files from any folder layout into a user-defined folder hierarchy, renaming them from their metadata.
* [dovo](https://github.com/DraconPern/dovo) ⭐ 43 | 🐛 2 | 🌐 C++ | 📅 2026-03-30 - Cross-platform software for importing DICOM CDs and files and sending them to a PACS.
* [MIA Toolkit](https://github.com/Fritanga-Collective/mia-toolkit) ⭐ 0 | 🐛 3 | 🌐 Python | 📅 2026-11-09 - Desktop app that consolidates DICOM studies from multiple CDs and USB drives into a single de-duplicated, verified DICOMDIR archive.

### Gateways and Routing

* [healthcare-dicom-dicomweb-adapter](https://github.com/GoogleCloudPlatform/healthcare-dicom-dicomweb-adapter) ⭐ 146 | 🐛 27 | 🌐 Java | 📅 2026-11-06 - Components that translate between traditional DICOM DIMSE protocols, such as C-STORE, and DICOMweb, such as STOW-RS.
* [dicom-mcp](https://github.com/ChristianHinge/dicom-mcp) ⭐ 107 | 🐛 4 | 🌐 Python | 📅 2026-10-29 - Model Context Protocol server that lets AI assistants query, read and move data on PACS and other DICOM nodes.
* [mercure](https://github.com/mercure-imaging/mercure) ⭐ 105 | 🐛 20 | 🌐 JavaScript | 📅 2026-11-09 - DICOM routing and processing platform with a web interface and extensive monitoring.
* [dicomweb-proxy](https://github.com/knopkem/dicomweb-proxy) ⭐ 82 | 🐛 2 | 🌐 TypeScript | 📅 2026-03-22 - Translates between DICOMweb and traditional DICOM DIMSE services.
* [DICOM-RST](https://github.com/UMEssen/DICOM-RST) ⭐ 29 | 🐛 20 | 🌐 Rust | 📅 2026-11-02 - DICOMweb gateway server that serves data from DIMSE nodes or S3 storage.

### Radiation Therapy

* [SlicerRT](https://github.com/SlicerRt/SlicerRT) ⭐ 157 | 🐛 86 | 🌐 C++ | 📅 2026-10-28 - 3D Slicer extension that imports DICOM RT structure sets, doses, plans and images and exports structure sets and doses, with dose analysis, contour analysis and treatment planning tools.
* [PlatiPy](https://github.com/pyplati/platipy) ⭐ 150 | 🐛 49 | 🌐 Python | 📅 2026-10-23 - Python toolkit and command-line tools for medical image processing and analysis, many designed for radiation therapy, including conversion of DICOM images and RT structure sets to and from NIfTI, auto-segmentation and visualization.
* [DICOMautomaton](https://github.com/hdclark/DICOMautomaton) ⭐ 91 | 🐛 35 | 🌐 C++ | 📅 2026-09-24 - Multipurpose tool for analyzing medical physics data, with a focus on automation.
* [OnkoDICOM](https://github.com/didymo/OnkoDICOM) ⭐ 73 | 🐛 36 | 🌐 Python | 📅 2026-11-08 - DICOM RT viewer with tools for radiation oncology research.
* [Plastimatch](https://gitlab.com/plastimatch/plastimatch) - Command-line toolkit for image registration and processing in radiotherapy, which converts DICOM RT structure sets and doses to and from other formats.

### Research Platforms

* [3D Slicer](https://github.com/Slicer/Slicer) ⭐ 2,714 | 🐛 674 | 🌐 C++ | 📅 2026-11-10 - Desktop platform for medical image visualization, segmentation and registration, with a DICOM browser and support for many clinical DICOM object types.
* [Kaapana](https://github.com/kaapana/kaapana) ⭐ 278 | 🐛 1 | 🌐 Python | 📅 2026-11-10 - Kubernetes-based platform that combines a DICOM archive, a web viewer and a workflow engine for AI processing and federated learning on medical images.
* [XNAT](https://github.com/NrgXnat/xnat) ⭐ 8 | 🐛 50 | 🌐 Java | 📅 2026-11-09 - Imaging research platform that receives DICOM through a built-in SCP, anonymizes and archives imaging sessions, and runs processing pipelines.

### Servers and PACS

* [Dicoogle](https://github.com/dicoogle/dicoogle) ⭐ 536 | 🐛 63 | 🌐 Java | 📅 2026-10-29 - Extensible PACS archive that indexes DICOM metadata for flexible search and retrieval instead of relying on a traditional centralized database.
* [dcm4chee-arc-light](https://github.com/dcm4che/dcm4chee-arc-light) ⭐ 507 | 🐛 208 | 🌐 Java | 📅 2026-11-06 - DICOM archive and PACS built on dcm4che, with DIMSE, DICOMweb and HL7 services and a web interface.
* [Conquest DICOM Server](https://github.com/marcelvanherk/Conquest-DICOM-Server) ⭐ 154 | 🐛 5 | 🌐 C | 📅 2026-11-04 - DICOM server and PACS with SQL database backends, Lua scripting for automating workflows, and a web interface.
* [dicomweb-pacs](https://github.com/knopkem/dicomweb-pacs) ⭐ 127 | 🐛 6 | 🌐 TypeScript | 📅 2026-03-22 - DICOMweb-enabled PACS with DIMSE services, backed by an SQLite database.
* [Orthanc Explorer 2](https://github.com/orthanc-server/orthanc-explorer-2) ⭐ 76 | 🐛 11 | 🌐 Vue | 📅 2026-11-10 - Web interface for browsing, uploading, modifying and sharing studies stored in Orthanc, with links to OHIF, Stone and other viewers ([demo](https://orthanc.uclouvain.be/demo/ui/app/)).
* [Static DICOMweb](https://github.com/RadicalImaging/Static-DICOMWeb) ⭐ 66 | 🐛 40 | 🌐 JavaScript | 📅 2026-11-09 - Command-line tools that convert DICOM files into static DICOMweb files and serve them from disk or the cloud, optimized for the OHIF Viewer.
* [Orthanc](https://github.com/jodogne/OrthancMirror) ⭐ 44 | 🐛 0 | 🌐 C++ | 📅 2026-11-10 - Lightweight standalone DICOM server with a REST API and a plugin system ([demo](https://orthanc.uclouvain.be/demo/)).

### Validation

* [DVTk](https://github.com/dvtk-org/DVTk) ⭐ 194 | 🐛 24 | 🌐 C# | 📅 2026-08-06 - Testing, validating and diagnosing DICOM communication in medical environments.
* [dicom-validator](https://github.com/pydicom/dicom-validator) ⭐ 39 | 🐛 0 | 🌐 Python | 📅 2026-11-09 - Checks DICOM files against the IOD and module requirements of the standard, parsed from its DocBook edition.
* [dicom3tools](https://www.dclunie.com/dicom3tools.html) - Command-line utilities for dumping, converting and validating DICOM files, including the dciodvfy validator.

### Viewers

#### Desktop

* [Weasis](https://github.com/nroduit/Weasis) ⭐ 1,443 | 🐛 44 | 🌐 Java | 📅 2026-11-08 - Multipurpose standalone and web-based DICOM viewer with a modular architecture.
* [InVesalius](https://github.com/invesalius/invesalius3) ⭐ 815 | 🐛 295 | 🌐 Python | 📅 2026-11-10 - Reconstructs 3D surfaces from CT and MRI DICOM series, with segmentation, STL export and neuronavigation.
* [Horos](https://github.com/horosproject/horos) ⭐ 648 | 🐛 562 | 🌐 C++ | 📅 2026-02-09 - macOS viewer based on OsiriX, with PACS query and retrieve, MPR, volume rendering and plugins.
* [AlizaMS](https://github.com/AlizaMedicalImaging/AlizaMS) ⭐ 318 | 🐛 3 | 🌐 C++ | 📅 2026-09-18 - Cross-platform DICOM viewer with 2D and 3D views, MPR and volume rendering.
* [MRIcroGL](https://github.com/rordenlab/MRIcroGL) ⭐ 296 | 🐛 3 | 🌐 Python | 📅 2025-11-23 - Cross-platform volume renderer for DICOM, NIfTI and other voxel formats, with a drag-and-drop interface and Python scripting.
* [FSLeyes](https://github.com/pauldmccarthy/fsleyes) ⭐ 29 | 🐛 15 | 🌐 Python | 📅 2026-08-25 - Cross-platform viewer for NIfTI and DICOM images, from the FSL neuroimaging suite.
* [dicom-nifti-viewer-vscode](https://github.com/theluckystrike/dicom-nifti-viewer-vscode) ⭐ 0 | 🐛 0 | 🌐 JavaScript | 📅 2026-11-07 - VS Code extension that opens DICOM, DICOMDIR and NIfTI files with CT window presets, axial, coronal and sagittal views and a searchable tag table.

#### Web

* [OHIF Viewer](https://github.com/OHIF/Viewers) ⭐ 4,404 | 🐛 615 | 🌐 TypeScript | 📅 2026-11-10 - Zero-footprint, extensible web viewer from the [Open Health Imaging Foundation](https://ohif.org/) that works with DICOMweb archives ([demo](https://viewer.ohif.org/)).
* [VolView](https://github.com/Kitware/VolView) ⭐ 306 | 🐛 89 | 🌐 TypeScript | 📅 2026-11-09 - Web-based radiological viewer built with [Vue.js](https://vuejs.org/) and [VTK.js](https://github.com/Kitware/vtk-js) ⭐ 1,548 | 🐛 335 | 🌐 JavaScript | 📅 2026-11-09 ([demo](https://volview.kitware.app/)).
* [dicomviewer](https://github.com/ayselafsar/dicomviewer) ⭐ 269 | 🐛 7 | 🌐 JavaScript | 📅 2026-11-06 - Nextcloud app for viewing DICOM files, built on the OHIF Viewer.
* [Slim](https://github.com/ImagingDataCommons/slim) ⭐ 174 | 🐛 78 | 🌐 TypeScript | 📅 2026-11-03 - Web viewer and annotation tool for DICOM whole slide microscopy images served over DICOMweb.
* [bluelight](https://github.com/cylab-tw/bluelight) ⭐ 159 | 🐛 4 | 🌐 JavaScript | 📅 2026-11-03 - Lightweight browser-based DICOM viewer that runs as a single-page application on any HTTP server, with plugins for MPR, MIP, volume rendering and DICOM SEG editing.
* [dwv-react](https://github.com/ivmartel/dwv-react) ⭐ 134 | 🐛 2 | 🌐 JavaScript | 📅 2026-05-19 - Medical viewer using DWV and [React](https://react.dev/).
* [Stone Web Viewer](https://github.com/jodogne/mirror-orthanc-stone) ⭐ 0 | 🐛 0 | 🌐 C++ | 📅 2026-11-10 - WebAssembly viewer from the Orthanc project for studies stored in Orthanc or on any DICOMweb server.

## Related Lists

* [Awesome Health](https://github.com/kakoni/awesome-healthcare) ⭐ 4,044 | 🐛 7 | 📅 2026-11-03 - Open source healthcare software, libraries, tools and resources.
* [Awesome Medical Dataset](https://github.com/openmedlab/Awesome-Medical-Dataset) ⭐ 2,222 | 🐛 65 | 📅 2026-10-02 - Medical imaging and health record datasets, with tools and tutorials for working with them.
* [Awesome Digital and Computational Pathology](https://github.com/open-pathology/awesome-pathology) ⭐ 140 | 🐛 2 | 📅 2026-02-11 - Software, datasets and publications for digital and computational pathology, including whole slide image viewers.
* [Awesome Neuroimaging](https://github.com/NPACore/awesome-neuroimaging) ⭐ 52 | 🐛 1 | 🌐 Makefile | 📅 2026-08-24 - Tools for exploring, organizing and analyzing brain images and recordings, with a focus on MRI.
* [Awesome HL7 and DICOM](https://github.com/MichaelLeeHobbs/awesome-hl7-dicom) ⭐ 15 | 🐛 1 | 📅 2026-11-03 - HL7 and DICOM resources, tools and field notes for healthcare integration.

## Contributing

Contributions welcome! Read the [contribution guidelines](contributing.md) first. Projects that are no longer maintained are listed in the [archive](archive.md).

[^1]: [About the DICOM Standard](https://www.dicomstandard.org/about-home), NEMA.

***

> _Enhansomed by [enhansome](https://github.com/enhansome) on 2026-11-10._
