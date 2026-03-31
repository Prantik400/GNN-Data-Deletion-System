# GNN-Driven Distributed Data Deletion System

> Published Research Paper (IJFMR)  
> Domain: Distributed Systems | Graph Neural Networks | Cloud Computing  

---

## Overview

This repository presents a research-based approach to solving a critical problem in distributed cloud systems — **incomplete data deletion across multiple nodes**.

In modern cloud infrastructures, data is replicated across several servers to ensure high availability and fault tolerance. However, when a file is deleted from one server, its duplicate copies may still persist in other parts of the network.

This creates serious challenges in:
- Data privacy and security  
- Compliance with regulations (e.g., GDPR)  
- Efficient storage management  

This work explores a conceptual solution by combining **Graph Neural Networks (GNN)** with a **Publish/Subscribe (Pub/Sub)** messaging architecture to improve consistency and intelligence in data deletion.

---

## Problem Statement

In distributed environments:

- Data is replicated across multiple servers  
- Deletion is often local, not global  
- Duplicate copies may remain undetected  

This leads to:
- Potential data leakage  
- Violation of privacy policies  
- Redundant storage consumption  

---

## Proposed Approach

The proposed system integrates two core ideas:

### 1. Pub/Sub-Based Communication
- A deletion event is broadcast from the source node  
- All subscribed nodes receive the update in real-time  
- Ensures system-wide awareness of deletion requests  

### 2. GNN-Based Prediction Mechanism
- The system models servers and data as a graph  
- Nodes represent servers/files, edges represent relationships  
- The GNN learns patterns such as:
  - Data replication  
  - Access frequency  
  - Connectivity  

 This allows the system to **identify possible hidden or indirect duplicates**

---

## Conceptual Workflow

```text
User requests file deletion
↓
File is deleted from local server
↓
Deletion event is broadcast using Pub/Sub
↓
All subscriber nodes receive notification
↓
GNN analyzes graph structure
↓
Predicts possible duplicate locations
↓
Duplicate files are handled (deleted or flagged)
↓
Deletion activity is logged for auditing
```

## Research Paper

Title: Leveraging GNN-Driven Inference with Pub/Sub Messaging for Coherent Data Erasure in Multi-Node Cloud Systems
Journal: International Journal For Multidisciplinary Research (IJFMR)
DOI: https://doi.org/10.36948/ijfmr.2025.v07i04.54019


Read Full Paper: https://www.ijfmr.com/research-paper.php?id=54019
