---
course_slug: mysql-console
tutorial_number: 15
type: note
---

The `LOWER` MySQL function converts a string to lowercase. This is an alias to the `LCASE` function

The following SQL will return all the first names from the `tbl_user` table as lower case

```sql
SELECT LOWER(`first_name`) FROM `tbl_user`;
```
