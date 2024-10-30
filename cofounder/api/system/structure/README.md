# Structure Documentation

This directory contains YAML files that define the structure of nodes and sequences used in the system. These files provide a clear understanding of how different components interact with each other.

## Nodes

Nodes are individual units of functionality that perform specific tasks. Each node is defined in a YAML file and includes details such as the node's description, input parameters, output parameters, and queue settings.

### Example Node Definition

```yaml
nodes:
  op:LLM::GEN:
    desc: "Generate text using a language model"
    in: [model, messages, preparser, parser, query, stream]
    out: [generated, usage]
    queue:
      concurrency: 1
```

In this example, the node `op:LLM::GEN` is defined with a description, input parameters (`in`), output parameters (`out`), and queue settings (`queue`).

## Sequences

Sequences are collections of nodes that are executed in a specific order. Each sequence is defined in a YAML file and includes details such as the sequence's description, the nodes involved, and the relationships between the nodes.

### Example Sequence Definition

```yaml
sequences:
  "seq:project:init:v1":
    desc: "Initialize a new project"
    nodes:
      - op:PROJECT::STATE:SETUP
      - PM:PRD::ANALYSIS
      - PM:FRD::ANALYSIS
      - PM:DRD::ANALYSIS
    relations:
      parents:
        PM:PRD::ANALYSIS: ["op:PROJECT::STATE:SETUP"]
        PM:FRD::ANALYSIS: ["PM:PRD::ANALYSIS"]
        PM:DRD::ANALYSIS: ["PM:FRD::ANALYSIS"]
```

In this example, the sequence `seq:project:init:v1` is defined with a description, a list of nodes, and the relationships between the nodes.

## Purpose and Usage

The purpose of these YAML files is to provide a clear and organized structure for the system's functionality. By defining nodes and sequences in this way, it becomes easier to understand how different components interact and how tasks are executed within the system.

To use these definitions, the system reads the YAML files and constructs the necessary nodes and sequences based on the provided information. This allows for a modular and scalable approach to building and managing the system's functionality.
