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

### Section 2. Graph Modeling
TODO: [Edwin] add a example about the final graph

### Section 3. Graph creation with `BioCypher`

#### Step 1. Configuration

##### Configure `BioCypher` behavior
TODO: [Shuangshuang] explain a little bit how we are going to configure BioCypher for this example:
```yaml
biocypher:
   offline: true
   debug: false
   ... etc
```

##### Create a schema for your graph
TODO: [Shuangshuang] explain a little bit how to produce this schema based on data and modeling section
```yaml
protein:
    represented_as: node
    input_label: uniprot_protein

protein protein interaction:
    is_a: pairwise molecular interaction
    represented as edge: edege
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

