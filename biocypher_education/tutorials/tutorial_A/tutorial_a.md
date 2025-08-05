# Title

## Overview

## Setup

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

