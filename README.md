# ARP-Mappings

This repository includes the mapping relationship between permissions  and API in Android API 23 to API 29.  The data acquisition depends on the content provided by annotations  and  Java Doc in the source code .

These mappings are mainly used in our paper to explore the issues of Android runtime permission. The mapping relationship is extracted from source code, so these mapping relationships are more reliable and help the issues of out paper research more accurate.

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



## Mapping Difference

We compared the differences in mappings related to dangerous permissions in different versions, and got these results.

### Change of permission-protected APIs

- ADD

  If `permission-protected API not in API VERSION_X && permission-protected API in API VERSION_Y` is identified as `ADD`

- DELETE

  If `permission-protected API in API VERSION_X && permission-protected API  not in API VERSION_Y` is identified as `DELETE`

### Change of mapping relationships

- CHANGE

  For `permission-protected API`，if the required permission in `VERSION_X` is `List_X`，the required permission in `VERSION_Y` is `List_Y`，if `List_X != List_Y`，then the identifier is `CHANGE`.

### Change of dangerous permissions

As the title says, the difference in dangerous permissions between different versions is recorded here. For example, the permission added in API 29 `android.permission.ACCESS_BACKGROUND_LOCATION`.