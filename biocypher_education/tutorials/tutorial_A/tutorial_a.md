# Title

## Overview

This tutorial will help you get started with BioCypher. You will learn how to bring together different types of biomedical data and create a simple knowledge graph about proteins and their connections.

By the end of this tutorial, you will be able to:

- Set up BioCypher for a basic project.
- Collect and organize example protein data.
- Build a small knowledge graph from the data.
- View and search the graph using Neo4j.

## Pre-requisites

1. Poetry.
2. Python >= 3.10

## Setup

In this section, you will set up your working environment using the BioCypher Project Template. This template provides a ready-to-use folder structure and example files, so you can focus on building your application.

**Before you start:**
- Make sure you have [Poetry](https://python-poetry.org/docs/#installation) and Python 3.10 or higher installed. If not, follow the official installation guides.

**Steps:**

1. Clone the BioCypher Project Template and rename the folder as `tutorial-basics-biocypher`:
```bash
git clone https://github.com/biocypher/project-template.git
mv project-template tutorial-basics-biocypher
cd tutorial-basics-biocypher
```

2. Initialize your own Git repository:
```bash
rm -rf .git
git init
git add .
git commit -m "Initial commit"
```

3. Install the dependencies using Poetry (or use pip/conda if you prefer; dependencies are listed in `pyproject.toml`):
```bash
poetry install
```

**Tip:** If you have trouble with Poetry or Python, check the official documentation or use your system's package manager to install them.

**Check your setup:**
Run the following command to confirm your environment is ready:
```bash
poetry run python --version
```
You should see your Python version (3.10 or higher).

### Section 1. Exploratory Data Analysis
TODO: [Edwin] add a description about the dummy dataset we are going to use.

TODO: [Edwin] provide a link to the data possible in Zenodo?

### Section 2. Graph Modeling
TODO: [Edwin] add a example about the final graph

### Section 3. Graph creation with `BioCypher`

#### Step 1. Configuration

##### Configure `BioCypher` behavior
TODO: [Shuangshuang] explain a little bit how we are going to configure BioCypher for this example:

BioCypher includes a default set of configuration parameters(you can see in [Default Configuration](https://biocypher.org/BioCypher/reference/biocypher-config/#default-configuration)), which you can overwrite them by creating a `biocypher_config.yaml` file in the root directory or the `config` directory of your project. You only need to specify the ones you wish to override from default. 
Now we use the following `biocypher_config.yaml` as an example:
```yaml
biocypher:
  offline: true
  debug: false
  schema_config_path: config/schema_config.yaml
  cache_directory: .cache

neo4j:
  delimiter: '\t'
  array_delimiter: "|"
  skip_duplicate_nodes: true
  skip_bad_relationships: true
  import_call_bin_prefix: /usr/bin/
```
The first block is the BioCypher Core Settings, which starts with `biocypher:`

```yaml
  offline: true
```
Whether to run in offline mode (no running DBMS or in-memory object)
```yaml
  debug: false
```
Whether to enable debug logging
```yaml
  schema_config_path: config/schema_config.yaml
```
Path to the schema configuration file
```yaml
  cache_directory: .cache
```
Directory for cache files

The second block is the Database Management System Settings, which starts with the name of the DBMS, in this case it's `neo4j:`

```yaml
  delimiter: '\t'
```
Field delimiter for CSV import files
```yaml
  array_delimiter: "|"
```
Delimiter for array values
```yaml
  skip_duplicate_nodes: true
```
Whether to skip duplicate nodes during import
```yaml
  skip_bad_relationships: true
```
Whether to skip relationships with missing endpoints
```yaml
  import_call_bin_prefix: /usr/bin/
```
Prefix for the import command binary (optional)

For more configuration parameters for the Settings, please check [BioCypher Configuration Reference](https://biocypher.org/BioCypher/reference/biocypher-config/)


##### Create a schema for your graph
TODO: [Shuangshuang] explain a little bit how to produce this schema based on data and modeling section

Except the [BioCypher configuration](#configure-biocypher-behavior) we mentioned in the above, there is another Schema configuration to configure the BioCypher graph structure with YAML file, which is named as `schema_config.yaml`.

Now we use the following proteins import `schema_config.yaml` as an example:

```yaml
protein:
    represented_as: node
    input_label: uniprot_protein

protein protein interaction:
    is_a: pairwise molecular interaction
    represented as edge: edge
```
TODO: [Edwin] explain a little bit about how to express the ontological backbone Biolink model

The first block is the node settings, which starts with `protein:` since we import proteins in this case.

```yaml

```

#### Step 2. Create an adapter

#### Step 4. Create a knowledge graph script

- Create a BioCypher object


- Instantiate your adapter


- Write data from your adapter to BioCypher
  
### Section 4. Interacting with your graph using Neo4j
#### Load the graph using an import script
#### Visualize the graph
#### Execute cypher queries

