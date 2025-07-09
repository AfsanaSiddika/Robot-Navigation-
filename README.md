# 🤖 Robot Navigation System with A\* Pathfinding

A Python-based visual simulation of robot navigation in a 2D terrain grid using the A\* (A-star) algorithm.
This project demonstrates intelligent pathfinding by accounting for **terrain types**, **obstacles**, and **movement costs** — making it ideal for robotics, game AI, or grid-based route planning applications.

---

## 📌 Objective

To develop a smart navigation system for a robot that finds the most efficient path from a **start point** to a **goal point** in a terrain map filled with **obstacles** and **varied terrain costs** using the A\* search algorithm.

---

## 🚀 Features

* 🔍 **A\* Pathfinding Algorithm**: Finds the shortest path using cost and heuristic (Euclidean distance).
* 🌄 **Terrain-Aware Navigation**:

  * `NORMAL_FLOOR` = 1
  * `CARPET` = 2
  * `SLIPPERY` = 3
  * `OBSTACLE` = -1 (non-traversable)
* 🧠 **Diagonal Movement Support**: Diagonal moves cost `√2 * terrain cost`.
* 📊 **Grid Visualization with Matplotlib**:

  * Terrain types are color-coded.
  * Start & goal cells clearly marked.
  * Path is shown with a blue trail.
* 📈 **Cost Calculation**: Calculates total cost of the path.
* ⏱️ **Performance Metrics**: Displays total execution time for pathfinding.
* 📁 **File-based Input**: Input taken from a structured `input.txt` file.

---

## 🗂️ Input Format (`input.txt`)

```
<grid_rows> <grid_columns>
<number_of_obstacles>
<x1> <y1>   # Obstacle positions
<x2> <y2>
...
<start_x> <start_y>
<goal_x> <goal_y>
```

**Example:**

```
9 9
5
1 1
2 2
3 3
4 4
5 5
0 0
8 8
```

---

## 🧪 How It Works

1. **Grid Generation**: A 2D grid is generated with varied terrain types.
2. **Obstacle Placement**: Obstacles are marked based on input.
3. **A\* Execution**: The robot uses the A\* algorithm to calculate the most optimal path.
4. **Visualization**: The entire grid, terrain, obstacles, path, and nodes are visualized using `matplotlib`.

---

## 🖼️ Visualization Output

* 🟥 Goal Cell
* 🟩 Start Cell
* ⚫ Obstacles
* 🟦 Path Trail
* 🟫 Carpet, 🩵 Slippery floor, ⬜ Normal floor

> Dynamic labels and color-coded tiles make the output intuitive and easy to understand.

---

## 📦 Dependencies

Make sure you have the following installed:

```bash
pip install matplotlib numpy
```

---

## ▶️ Run the Program

```bash
python robot_navigation.py
```

> You can also run the code in a Jupyter Notebook or Google Colab.

---

## 📊 Sample Output

```bash
Path found: [(0, 0), (1, 1), ..., (8, 8)]
Total Cost: 13.4
Execution Time: 0.0023 seconds
```

A full-color visual grid with the computed path will be displayed.

---

## 🛠 Technologies Used

* 🐍 Python 3
* 📈 Matplotlib (for visualization)
* 📊 NumPy
* 💡 A\* Pathfinding Algorithm

---

## 🧠 UML Diagram

```text
+------------------+
|      Node        |
+------------------+
| position         |
| parent           |
| g, h, f          |
+------------------+
| __lt__()         |
+------------------+

+-------------------------+
|       Functions         |
+-------------------------+
| a_star(grid, start, goal) |
| euclidean_distance(a, b) |
| generate_grid(m, n, obs) |
| load_input(file_path)    |
| visualize_grid(...)      |
| main()                   |
+-------------------------+
```

---

## 🎞️ Demo Preview

You can preview the project in action through this [Google Colab Notebook](https://colab.research.google.com/drive/1sO-wNiFzsF4afZ745-wJTn2VAvWjv85s).

![Robot Navigation Demo GIF](https://yourdomain.com/demo.gif) <!-- Replace with your hosted .gif if available -->

---

## 💡 Future Enhancements

* 🔁 Dynamic obstacles or real-time updates
* 🧭 Dijkstra or other heuristic algorithms
* 💬 Voice or GUI-based input system
* 🤖 Integration with a robotic simulation environment

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).

---

> 🎓 Ideal for robotics students, AI pathfinding practice, or anyone interested in intelligent grid navigation.

