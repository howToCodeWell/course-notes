---
course_slug: mysql-console
tutorial_number: 9
type: note
---

The following SQL will insert a record in a MySQL table

```sql
INSERT INTO `tbl_user` (`first_name`, `last_name`)
VALUES ('Peter', 'Fisher');
```

Supplying multiple value groups will insert multiple records. Each group of values should be enclosed in brackets and separated by a comma

The following will insert two records.  One for Peter Fisher and one for John Smith. 
```sql
INSERT INTO `tbl_user` (`first_name`, `last_name`)
VALUES ('Peter', 'Fisher'), ('John', 'Smith');
```
