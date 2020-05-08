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