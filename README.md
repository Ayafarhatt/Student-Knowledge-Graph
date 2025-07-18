# 🎓 Student Knowledge Graph

This project builds a **Knowledge Graph** to represent student information based on their personal and academic attributes. The goal is to visually demonstrate the relationships between each student and their characteristics.

## 📁 Project Structure

* `dataset.csv` – Contains student data (age, gender, GPA, study hours, etc.)
* `graph_builder.py` – Python code that builds the knowledge graph.
* `utils.py` – Includes helper functions like `classify_age`, `classify_gpa`, `classify_study_hours`.
* `README.md` – Project documentation (this file).

## 🧠 What is a Knowledge Graph?

A knowledge graph is a way to represent data using **nodes** (entities) and **edges** (relationships). In this project:

* Each student is represented as a `Student` node.
* Attributes like `Gender`, `Age Group`, `GPA level`, and `Study Hours` are connected to the student via labeled edges.

## ⚙️ How It Works

1. **Data Classification**
   The raw data is classified into groups:

   * Age → `Age_Under_20`, `Age_20_29`, `Age_30_plus`
   * GPA → `Low_GPA`, `Medium_GPA`, `High_GPA`
   * Study Hours → `Low_Study_Hours`, `Medium_Study_Hours`, `High_Study_Hours`

2. **Graph Construction**
   For each student:

   * A node is created with label `Student_n`.
   * Nodes for classified attributes are added.
   * Edges are drawn to connect the student to their attributes using relations like:

     * `has_gender`
     * `has_age_group`
     * `has_study_hours`
     * `has_gpa`

3. **Visualization**
   The graph is visualized using `networkx` and `matplotlib`. Nodes are colored based on their type.

## 🖼 Example Output

The final graph shows how each student is connected to shared attributes. For instance, multiple students may be linked to the same node `High_GPA`, revealing common patterns.

## 📦 Requirements

* Python 3.x
* pandas
* networkx
* matplotlib

Install them with:

```bash
pip install pandas networkx matplotlib
```

## 🚀 Run the Project

```bash
python graph_builder.py
```

This will load the dataset, build the graph, and display it.

## 📜 License

This project is open-source and free to use under the [MIT License](LICENSE).


