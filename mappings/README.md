## Mappings

Runtime permission have been introduced since Android 6.0(API 23) , and now evolved to Android 10. In order to explore the evolution and problems that arise, it is necessary to have a more detailed mapping relationship for each version.

We extract mappings from two ways, so for each version there are also two mappings provided(`annotations-Mappings.txt` and `docs-Mappings.txt`).

### Annotation

In this way, the main method of annotating the need for permission is extracted . The form of the annotation is like :`@RequiresPermission(android.Manifest.permission.PERMISSION_NAME)`. 

### Java Doc

In this way, the method of including`Requires Permission:{@link android.Manifest.permission# PERMISSION_NAME}` in the Java Doc is extracted.



These APIs can be used by developers, so APPs using these APIs are more likely to have permission-related problems, and the reliability of these mapping relationships provides more accurate results .

### Shortcoming

The mappings we extracted from the Java Doc are not very accurate, because some methods may require certain permissions when certain parameters are passed in, but our manner lacks analysis in this scenario and is one of the plans for subsequent improvements.
