## Altering commands

## Updating primary key
`ALTER TABLE person ADD PRIMARY KEY (id);`

## Updating constraint key
`ALTER TABLE person ADD CONSTRAINT unique_email UNIQUE(columnName);`

## Check Constraint
`ALTER TABLE ADD CONSTRAINT gender_constraint CHECK (gender = 'MALE' OR gender = 'FEMALE');`

## ON CONFLICT DO NOTHING

When we add a record where id is the primary key and this might throw error
To handle this error, we need to add ON CONFLICT (column name) DO NOTHING
This will only take column name where it is primary constraint or is the primary key.

## Upsert
