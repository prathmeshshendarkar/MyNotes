> SQL stands for Structured Query Language

[[Crud Operations in MySQL]]

[[Properties of MySQL]]

## Data Types
1. ![[Pasted image 20240802190817.png]]
2. Check Here : [[MySQL Data Types]]

## Commands
1. ![[Pasted image 20240803193638.png]]
2. Check Here for more details: [[MySQL Commands]]
3. Every Command has a specific structure they follow
```
CREATE : CommandName(CREATE) Whatyouwanttocreate(TABLE) Whatisthenameofthecreation(Student) (
	Whatcolumnyouwanttoinsert(Stud_Id) Whattypeofdatawillbeinserted(INT) Isthereanyotherconstraints(PRIMARY KEY , NOT NULL, UNIQUE, DEFAULT, ),

	Anyotherconstraint(PRIMARY KEY) Attributename(Name of column),
	Anyotherconstraint(FOREIGN KEY) Attirbutename(Name of column) Wheredoyouwanttoattach(REFERENCES) Tablename(placements(stud_college)),
	
	Attheendanyotherconstraints(CONSTRAINT) Constrainname(stud_college_constraint) Whatistheconstraint(CHECK(stud_college == "IIT"));
)
```

[[Execution Contexts]]
[[MySQL Internal Databases]]

## Filtering in MYSQL
1. Please check : 