# Czech insolvency datase

To restore the CID DB from the SD Card, follow these steps:
1. Concatenate the parts into one archive file: `cat * >> cid_db.sql.gz`
2. Copy the archive `cid_db.sql.gz` into a local folder.
3. Decompress the database SQL archive: `gzip -d cid_db.sql.zip`
4. Restore the CID DB into an empty PostgresSQL database: `pg_restore -U $USERNAME -d $DB_NAME -1 cidd_db.sql`
