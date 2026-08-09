# 📦 SupplyChain OS

### Graph-Powered Logistics Intelligence Platform

**SupplyChain OS** is an intelligent supply chain analysis and optimization system built using **Java, Java Swing, MySQL, and advanced Data Structures & Algorithms (DSA)**.

The platform models a real-world logistics network where **suppliers, factories, warehouses, and retailers** are represented as nodes in a directed graph and connected through logistics routes.

It allows users to:

- Build and manage supply chain networks
- Visualize logistics networks interactively
- Simulate supply chain disruptions
- Detect bottlenecks and critical nodes
- Analyze supplier risks
- Generate recovery plans and alternative routes
- Monitor supply chain analytics

The project demonstrates how **Data Structures and Algorithms can be applied to real-world enterprise logistics and optimization problems**.

---

# 🧠 Project Theme

## Enterprise Systems & Process Optimization

The goal of SupplyChain OS is to create smart systems that help businesses operate efficiently by applying data structures and algorithms to real-world problems such as:

- Supply chain disruptions
- Resource allocation
- Logistics planning
- Network optimization
- Risk analytics

---

# 🔗 System Overview

The supply chain network is represented using a **directed graph**:

```text
Supplier → Factory → Warehouse → Retailer
```

### Example Network

```text
S1 → F1 → W1 → R1
S2 → F1
S3 → F2 → W3 → R3
```

This graph-based representation allows the system to analyze:

- Cascading disruptions
- Critical nodes
- Bottlenecks
- Alternative recovery routes

---

# ⚙️ Key Features

## 1. 🏭 Supply Chain Network Builder

Users can build and manage supply chain networks.

### Supported Operations

- Add Node
- Edit Node
- Delete Node
- Connect Nodes (Edges)
- Remove Connections

### Node Types

- Supplier
- Factory
- Warehouse
- Retailer

### Node Attributes

- Capacity
- Health
- Type
- Name

### Edge Attributes

- Cost
- Time
- Capacity

---

## 2. 🕸️ Interactive Graph Visualization

The system visualizes the supply chain using an interactive graph canvas.

### Features

- Drag nodes to reposition
- Click nodes to simulate failure
- Click edges to view logistics details
- Visual legend for node types

### Graph Color Legend

| Color | Meaning |
|---|---|
| 🟢 Green | Supplier |
| 🔵 Blue | Factory |
| 🟣 Purple | Warehouse |
| 🟠 Orange | Retailer |
| 🔴 Red | Affected Node |
| 🟠 Orange Highlight | Bottleneck Node |
| ⚫ Black | Critical Node |

---

## 3. 🚨 Disruption Simulation

Users can simulate failures in the supply chain.

### Steps

1. Click any node in the graph
2. Select **Simulate Failure**
3. System runs BFS cascade analysis
4. Affected nodes are highlighted

### Example

```text
Supplier Failure
      ↓
Factory affected
      ↓
Warehouse affected
      ↓
Retailer affected
```

### Algorithm Used

**Breadth First Search (BFS)**

### Time Complexity

```text
O(V + E)
```

---

## 4. 🚧 Bottleneck Detection

Identifies nodes with high dependency load that can create logistics congestion.

### Algorithm

**Graph degree analysis using HashMap**

---

## 5. ⚠️ Critical Node Detection

Detects single points of failure in the supply chain.

### Algorithm

**Incoming edge dependency analysis**

---

## 6. 🛣️ Recovery Planner

When disruptions occur, the system generates recovery routes to help restore supply chain operations.

### Recovery Strategies

- Fastest Path
- Cheapest Path
- Most Reliable Path

Users can apply recovery strategies directly.

---

## 7. 📊 Analytics Dashboard

The analytics module provides supply chain intelligence.

### Metrics

- Total Network Cost
- Estimated Loss per Hour
- Total Nodes
- High Risk Suppliers
- Historical Loss

### Additional Modules

- Supplier Risk Analysis
- Alerts
- Supplier Search

---

# 🧮 Data Structures & Algorithms Used

SupplyChain OS applies multiple Data Structures and Algorithms to solve different supply chain analysis and optimization problems.

## Graph — Adjacency List

The supply chain network is represented using:

```text
Map<Node, List<Edge>>
```

### Benefits

- Efficient traversal
- Dynamic updates
- Supports analytics

---

## Breadth First Search (BFS)

Used for:

- Disruption propagation
- Failure cascade analysis

### Time Complexity

```text
O(V + E)
```

---

## Depth First Search (DFS)

Used for:

- Connectivity analysis
- Route exploration

---

## Priority Queue

Used in:

- `PriorityQueueManager`
- `RecoveryPlanner`
- `RouteOptimizer`

---

## Bloom Filter

Used for:

- Fast supplier risk detection

---

## Segment Tree

Used for:

- Efficient range queries

---

## Trie

Used for:

- Fast supplier search

---

## Max Heap

Used to:

- Track highest-risk suppliers

---

# 🏗️ Project Architecture

```text
com.supplychain
│
├── analytics
│   ├── AnalyticsEngine
│   ├── BloomFilter
│   ├── MaxHeap
│   ├── SegmentTree
│   ├── SupplierManager
│   └── TrieNode
│
├── db
│   ├── DBConnection
│   ├── EdgeDAO
│   └── NodeDAO
│
├── logic
│   ├── BottleneckAnalyzer
│   ├── DisruptionSimulator
│   ├── GraphTraversal
│   ├── PathResult
│   ├── PriorityQueueManager
│   ├── RecoveryPlanner
│   └── RouteOptimizer
│
├── model
│   ├── Graph
│   ├── Node
│   └── Edge
│
├── ui
│   ├── MainMenuUI
│   ├── GraphPanel
│   ├── GraphVisualizerUI
│   ├── DashboardUI
│   ├── AddNodeUI
│   ├── EditNodeUI
│   ├── DeleteNodeUI
│   ├── AddEdgeUI
│   ├── DeleteEdgeUI
│   ├── RecoveryUI
│   └── ViewGraphUI
│
└── main
    └── MainTest
```

---

# 💻 Technology Stack

| Technology | Purpose |
|---|---|
| **Java** | Core application development |
| **Java Swing** | Graphical User Interface |
| **MySQL** | Database and persistent data storage |
| **Data Structures & Algorithms** | Network analysis and optimization |

### Concepts Used

- Object-Oriented Programming
- Graph Algorithms
- Data Structures
- Database Integration
- Interactive Visualization

---

# 🗄️ Database

SupplyChain OS uses **MySQL** for storing supply chain network data.

### Main Tables

```text
nodes
edges
```

The database stores the information required to represent supply chain nodes, connections, and logistics relationships.

---

# ▶️ How to Run

## 1. Setup Database

Create the MySQL database:

```sql
CREATE DATABASE supplychain;
```

Create the required tables:

```text
nodes
edges
```

---

## 2. Configure Database

Open:

```text
DBConnection.java
```

Set the following database details:

```text
username
password
database URL
```

Make sure the MySQL server is running before starting the application.

---

## 3. Run Application

Run:

```text
MainTest.java
```

The application will launch the SupplyChain OS graphical interface.

---

# 🎥 Demo

**Demo Video:**  
https://drive.google.com/file/d/1tUbs1a57bl-q7BK6v4wOkfTNvYrI3P2-/view?usp=sharing

---
<img width="1919" height="1021" alt="image" src="https://github.com/user-attachments/assets/9eb845c4-fa6f-4804-bd85-f901b695908f" />
<img width="1919" height="1021" alt="image" src="https://github.com/user-attachments/assets/e4b59b1d-8de6-4a4f-8b80-bf873817798d" />
<img width="1919" height="1019" alt="image" src="https://github.com/user-attachments/assets/ada736e9-e381-4a1c-a322-969999039688" />
<img width="1917" height="1040" alt="image" src="https://github.com/user-attachments/assets/9d2a3e79-f694-4df2-ba6c-3dd392eb4109" />
<img width="1919" height="1019" alt="image" src="https://github.com/user-attachments/assets/1baccc0d-aa40-4b4c-8f6e-bc00a88aa735" />
<img width="663" height="774" alt="image" src="https://github.com/user-attachments/assets/db2a6ec4-b19b-4d78-a3b9-d32c99cf32b3" />
<img width="674" height="694" alt="image" src="https://github.com/user-attachments/assets/2a0d3b91-efd8-4dec-8161-c6405f187430" />
<img width="1919" height="1020" alt="image" src="https://github.com/user-attachments/assets/c85fad1a-1b4d-4275-822a-b4a0433f940f" />
<img width="655" height="483" alt="image" src="https://github.com/user-attachments/assets/4e968540-45b0-4bf4-a984-3894c7b701af" />
<img width="790" height="668" alt="image" src="https://github.com/user-attachments/assets/8634c5bc-5d81-4924-ac7c-adeb6c434761" />
<img width="885" height="720" alt="image" src="https://github.com/user-attachments/assets/8eda9d04-7535-4627-80eb-e8151113fa2c" />
<img width="888" height="721" alt="image" src="https://github.com/user-attachments/assets/3b9065db-ff2c-4777-a163-63d80a349142" />
<img width="1919" height="1022" alt="image" src="https://github.com/user-attachments/assets/d6449809-327c-4a87-b154-22cc8ae42d22" />
<img width="1919" height="1022" alt="image" src="https://github.com/user-attachments/assets/2ab16b64-c510-4ffc-b5d7-869a1df2f23e" />
<img width="1919" height="1016" alt="image" src="https://github.com/user-attachments/assets/b423c26f-0192-461a-a4d2-f73823aa585b" />

---

# ⭐ Key Highlights

- Real-world supply chain simulation
- Graph-based logistics network
- Adjacency List graph representation
- BFS-based disruption cascade analysis
- DFS-based connectivity analysis
- Bottleneck detection
- Critical node detection
- Multiple recovery strategies
- Priority Queue-based route optimization
- Bloom Filter for supplier risk detection
- Segment Tree for range queries
- Trie-based supplier search
- Max Heap for high-risk supplier tracking
- Analytics dashboard
- Interactive Java Swing visualization
- MySQL database integration
