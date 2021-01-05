---
course_slug: mysql-console
tutorial_number: 15
type: note
---
The `UPPER` MySQL function converts a string to uppercase. This is an alias to the `UCASE` function

The following SQL will return all the first names from the `tbl_user` table as upper case

```sql
SELECT UPPER(`first_name`) FROM `tbl_user`;
```
