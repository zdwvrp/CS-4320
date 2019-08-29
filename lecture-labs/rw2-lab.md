# TW2 - Wednesday Lab, Week 2

## In Pairs, make sure you have figured out how to construct your repositories for the course

## Tuesday Review
### Resources
1. Markdown Syntax Reference: https://daringfireball.net/projects/markdown/syntax
2. [Markdown Syntax Reference](https://daringfireball.net/projects/markdown/syntax)

### Lab Directory Structure
1. Create a directory structure in the personal repository you created for assignment called `lecture-labs`, and underneath that directory, create two other directories to start: `tw2` (Tuesday, Week 2) and `rw2` (Thursday Week 2): 
	- lecture-labs
		- tw2
		- rw2
2. Inside of the `tw2` directory, build a markdown document listing three ethical considerations you are concerned about. 

## Building a Database
1. [This is what a substantial relational data model looks like](../readings/new-augur.0.0.77.5.pdf)
2. [Here is what the SQL for creating that looks like](./code/augur_data.sql)
3. [... but wait, there's another schema](./code/augur_operations.sql)
4. [.. AND another!](./code/spdx.sql)
5. BUT, to run these programs: 
6. You need to create a database user
    - For Linux**
```
    -- sudo -u postgres psql
    create database augur;
    create user augur with encrypted password 'mypass';
    grant all privileges on database augur to augur;

```
    - For Mac OSX**  
```
    create database augur;
    create user augur with encrypted password 'mypass';
    grant all privileges on database augur to augur;
```
8. Then you need to create the schema, and give the user permission to create things!
```

        CREATE SCHEMA augur_data;
        CREATE SCHEMA augur_operations;
        CREATE SCHEMA spdx;

	GRANT ALL PRIVILEGES ON ALL TABLES IN SCHEMA augur_data TO augur;
        GRANT ALL PRIVILEGES ON ALL SEQUENCES IN SCHEMA augur_data TO augur;
        GRANT ALL PRIVILEGES ON ALL TABLES IN SCHEMA augur_operations TO augur;
        GRANT ALL PRIVILEGES ON ALL SEQUENCES IN SCHEMA augur_operations TO augur;
        GRANT ALL PRIVILEGES ON ALL TABLES IN SCHEMA spdx TO augur;
        GRANT ALL PRIVILEGES ON ALL SEQUENCES IN SCHEMA spdx TO augur;
```
9. Run SQL: (MOST PEOPLE did this in class using a web tool or other GUI. So, if you have done that, running this at the command line will not work, because the objects already exist). 
	`\i /Users/sgoggins/github/computationalmystic/sengfs19/lecture-labs/code/spdx.sql`
10. Commit what your progress under the 
            - lecture-labs
                - rw2
directory. 


