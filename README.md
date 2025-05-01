# Data Warehouse Project – ETL & OLAP

This project was completed as part of the Advanced Databases course (M1, University of Caen Normandy).  
It consists of two main parts:

- **ETL Part**: Designing and populating a data warehouse using Apache Hop and SQLite.
- **OLAP Part**: Building and querying a multidimensional cube using Pentaho Mondrian and MDX.

---

## ETL Part (`projet_hop` folder)

This part is located in the `projet_hop/projet_hop` directory. It includes everything needed to create and populate the data warehouse using Apache Hop and SQLite3.

### File Organization

- `datawarehouse.txt`: SQL script used to create the data warehouse tables with SQLite.

- ETL Pipelines:
  - `pipeline1.hpl`, `pipeline2.hpl`, `pipeline3.hpl`: Hop pipelines used to load data into the warehouse.

- `data_in/` folder – Contains input files used to populate the data warehouse:
  - `dates.csv`
  - `geographie.csv`
  - `operational_data.db`
  - `prestations.csv`

- `data_out/` folder – Contains output files generated after processing:
  - `datawarehouse.db`: Final SQLite database representing the data warehouse.
  - `Errors.csv.txt`: File containing errors encountered during the data loading process.

In the root `projet_hop` directory, you will also find the file `diagramme.png`, which illustrates the schema used to design the data warehouse.  
For more details, refer to the report.

---

## OLAP Part (`tp_olap` folder)

We placed a copy of our `datawarehouse.db` in the `tp_olap/datawarehouse` folder.

The XML schema is located in the `exercices` folder, along with all the required MDX queries.  
Each MDX query is written in a separate file (`ex2.mdx`, `ex3.mdx`, ..., `ex11.mdx`), allowing you to execute each query individually.

### Instructions to execute MDX queries

1. Navigate to the `tp_olap` directory.
2. Execute the following command for each MDX query (replace the filename with the one you want to run):
   ```bash
   sh run.sh -p exercices/exercice.properties -f exercices/ex9.mdx | java -jar lib/mondrian_view.jar
