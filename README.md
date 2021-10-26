# darktable-compat
compatibility utilities for using darktable

## requirements
1. convert Lightroom database to darktable database
2. auto-import photos and relevant XMP files (if available)
3. optionally move raw files

## important LR tables and variables
1. Adobe_variablesTable
   1. Adobe_DBVersion (require 1000000)
   2. Adobe_lastScannedCatalogPath
   3. AgMetadata_autoWriteXmp (require TRUE)
2. Adobe_images
3. Adobe_imageProperties
4. Adobe_imageDevelopBeforeSettings
5. Adobe_imageDevelopSettings
6. Adobe_AdditionalMetadata
7. AgHarvestedDNGMetadata
8. AgHarvestedExifMetadata
9. AgHarvestedIptcMetadata
10. AgHarvestedMetadataWorklist
11. AgInternedExifCameraModel
12. AgInternedExifCameraSN
13. AgInternedExifLens
14. AgInternedIptcCity
15. AgInternedIptcCountry
16. AgInternedIptcCreator
17. AgInternedIptcCountryCode
18. AgInternedIptcJobIdentifier
19. AgInternedIptcLocation
20. AgInternedIptcState
21. AgLastcatalogExport
22. AgLibraryCollection
    1. creationId
    2. imageCount
    3. name
    4. parent (does DT support groups?)
23. AgLibraryFile
    1. id_local
    2. id_global
    3. baseName
    4. extension
    5. folder
    6. idx_filename
    7. sidecarExtensions (check after XMP export)
24. AgLibraryFolder
    1. id_local
    2. id_global
    3. parentId
    4. pathFromRoot
    5. rootFolder
    6. visibility
25. AgLibraryIPTC
26. AgLibraryRootFolder
    1. id_local
    2. id_global
    3. absolutePath

## Known and Unsupported LR tables
* Adobe_libraryImageDevelop3DLUTColorTable
* Adobe_libraryImageDevelopHistoryStep
* Adobe_libraryImageDevelopSnapshot
* Adobe_libraryImageFaceProcessHistory
* Adobe_namedIdentityPlate
* Adobe_variables