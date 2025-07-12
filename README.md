# 🤖 Robotic Arm Project  
*A modular, extensible robotic arm platform for research, prototyping, and learning.*

**Build:** Passing &nbsp;|&nbsp; **License:** BSD &nbsp;|&nbsp; **Platform:** ROS 2, Linux

## ✨ Features

- 🦾 **6-DOF Manipulator** for versatile movements
- 🧩 **Modular Design** for easy customization
- 🏗️ **MoveIt Integration** for advanced motion planning
- 🖥️ **Simulation Ready** (Gazebo & RViz support)
- 🛡️ **Collision Detection** and safe operation
- 🖱️ **Interactive Visualization** in RViz
- 🛠️ **ROS2 Control** for both simulation and hardware
- 📦 **Easy Launch Scripts** for demos and testing

## 🧰 Tech Stack

| Language/Tool | Purpose              |
|:-------------:|:---------------------|
| `C++`         | Core robot logic     |
| `Python`      | Scripting, utilities |
| `ROS 2`       | Robotics middleware  |
| `MoveIt 2`    | Motion planning      |
| `Gazebo`      | Simulation           |

## 🗂️ Folder Structure

```bash
📁 robotic_arm/
├── 📄 README.md
├── 📁 move_it_2/
│   ├── 📁 config/
│   ├── 📁 launch/
│   ├── 📄 CMakeLists.txt
│   └── 📄 package.xml
├── 📁 move_it_config/
│   ├── 📁 config/
│   ├── 📁 launch/
│   ├── 📄 CMakeLists.txt
│   └── 📄 package.xml
├── 📁 move_it_config_testing_june_25/
│   ├── 📁 config/
│   ├── 📁 launch/
│   ├── 📄 CMakeLists.txt
│   └── 📄 package.xml
└── 📁 robotic_manipulator_6_dof/
```

## ⚙️ How It Works

1. 📝 **Define:** Model robot structure and joints in URDF/Xacro.
2. 🗂️ **Configure:** Set up planning groups, end-effectors, and collision parameters (SRDF).
3. 🔧 **Connect:** Configure ROS2 Control and MoveIt for simulation/hardware.
4. 🧠 **Plan:** Use MoveIt for kinematics, planning, and execution.
5. 🕹️ **Simulate:** Launch Gazebo and RViz for testing and demonstration.
6. 👁️ **Visualize:** Monitor robot state and planned trajectories in RViz.


🔽 Wireframe Workflow (Text Diagram)

```plaintext
┌────────────────────┐
│  User Input/Script │
└─────────┬──────────┘
          │
          ▼
┌────────────────────┐
│ MoveIt Motion Plan │
└─────────┬──────────┘
          │
          ▼
┌─────────────────────────────┐
│ ROS2 Controllers            │
│  ┌───────────────────────┐  │
│  │  Gazebo Simulation    │  │
│  └───────────────────────┘  │
│  ┌───────────────────────┐  │
│  │  Real Hardware        │  │
│  └───────────────────────┘  │
└─────────┬─────────┬─────────┘
          │         │
          ▼         ▼
   ┌─────────────────────┐
   │ RViz Visualization  │
   └─────────────────────┘
```


## 🚀 Getting Started

**Prerequisites:**  
- ROS 2 Humble  
- MoveIt 2  
- Gazebo (optional for simulation)

**Clone the Repository:**
```bash
git clone https://github.com/yourusername/robotic_arm.git
cd robotic_arm
```

**Install Dependencies:**
```bash
rosdep install --from-paths . --ignore-src -r -y
```

**Build the Workspace:**
```bash
colcon build --symlink-install
source install/setup.bash
```

**Launch Demo (RViz + MoveIt):**
```bash
ros2 launch move_it_config demo.launch.py
```

**Launch Simulation (Gazebo):**
```bash
ros2 launch move_it_config_testing_june_25 demo.launch.py
```

## 🗺️ Roadmap

- 🤖 Add support for more end-effectors and sensors
- 🌐 Web-based dashboard for remote monitoring/control
- 🧠 Integrate AI/ML for advanced manipulation
- 🏭 Real hardware driver support
- 📊 Enhanced logging and analytics

## 🧑‍💻 Contributors

| Name      | GitHub                    | Role           |
|-----------|---------------------------|----------------|
| Rohit     | @rohitjangra7370          | Maintainer     |
| You?      | _Open for contributions!_ | Contributor    |

## 📄 License

BSD License. See [LICENSE](LICENSE) for details.

> _Have ideas or feedback? Open an issue or submit a pull request!_
