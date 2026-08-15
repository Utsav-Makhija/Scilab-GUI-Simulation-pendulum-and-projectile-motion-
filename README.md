# Engineering Simulation Studio

An interactive Scilab-based scientific simulation application for visualizing and exploring fundamental mechanics concepts through simulations, parameter controls, numerical calculations, and graphs.

---

## Overview

Engineering Simulation Studio is an interactive physics simulation application developed using Scilab.

The application currently contains two simulations:

- Pendulum
- Projectile Motion

Users can modify simulation parameters using interactive sliders and observe how those parameters affect the physical system. The application also provides calculated results and graphical representations of the simulations.

The project is designed as an educational STEM and engineering visualization tool, demonstrating how mathematical models can be implemented as interactive computer simulations.

---

## Features

### Pendulum Simulation

The Pendulum module simulates the motion of a simple pendulum.

#### Parameters

- Length (m)
- Mass (kg)
- Angle (deg)

#### Features

- Interactive pendulum animation
- Adjustable physical parameters
- Numerical results
- Results table
- Multiple graphs
- Start and reset controls
- Simulation status display

### Projectile Motion Simulation

The Projectile Motion module simulates the motion of a projectile launched at a specified velocity and angle under constant gravitational acceleration.

#### Parameters

- Initial Velocity (m/s)
- Launch Angle (deg)
- Gravity (m/s²)

#### Calculated Results

- Initial velocity
- Launch angle
- Gravitational acceleration
- Time of flight
- Maximum height
- Horizontal range

#### Features

- Animated projectile
- Real-time projectile movement
- Visible trajectory
- Adjustable parameters
- Results table
- Height vs. Time graph
- Horizontal Distance vs. Time graph
- Projectile Trajectory graph
- Automatic landing calculation
- Simulation status display

---

## Projectile Motion Equations

The projectile simulation is based on standard ideal projectile-motion equations.

### Horizontal Position

x(t) = v₀ cos(θ)t

### Vertical Position

y(t) = v₀ sin(θ)t - ½gt²

### Time of Flight

T = 2v₀ sin(θ) / g

### Maximum Height

Hmax = v₀² sin²(θ) / (2g)

### Horizontal Range

R = v₀² sin(2θ) / g

Where:

| Symbol | Meaning |
|---|---|
| v₀ | Initial velocity |
| θ | Launch angle |
| g | Gravitational acceleration |
| t | Time |
| x | Horizontal position |
| y | Vertical position |
| T | Time of flight |
| Hmax | Maximum height |
| R | Horizontal range |

---

## User Interface

The application uses a dashboard-style graphical interface.

### Simulation Selection

A dropdown menu allows the user to select between:

- Pendulum
- Projectile Motion

### Simulation Panel

The central panel displays the selected simulation and its animation.

### Parameters Panel

Interactive sliders allow the user to modify the parameters associated with the selected simulation.

### Results Panel

The results table displays calculated values based on the current parameters.

### Graph Panels

The graph areas display mathematical relationships associated with the selected simulation.

### Status Display

The status label provides information about the current state of the simulation.

---

## Controls

| Control | Function |
|---|---|
| START | Starts the currently selected simulation |
| RESET | Resets the simulation |
| Simulation Dropdown | Selects the simulation |
| Parameter Sliders | Changes simulation parameters |
| Status Display | Shows the current simulation state |

---

## Project Structure

The project is implemented primarily using a Scilab .sce script.

```text
Engineering Simulation Studio
│
├── GUI Initialization
│
├── Simulation Selection
│
├── Parameter Callbacks
│
├── START Callback
├── RESET Callback
│
├── Pendulum
│   ├── Simulation
│   ├── Results
│   └── Graphs
│
└── Projectile Motion
    ├── Simulation
    ├── Results
    └── Graphs
```

Important GUI components include:

```text
popupBasic
sliderParam1
sliderParam2
sliderParam3

lblParam1
lblParam2
lblParam3

lblStatus
tblResults

simulationArea

graphArea1
graphArea2
graphArea3
```

---

## Technologies Used

- Scilab
- Scilab GUI components
- Scilab graphics and plotting
- Numerical computation
- Mathematical modelling
- Event-driven callbacks
- Interactive sliders
- Data visualization

---

## Requirements

To run the project, you need:

- Scilab
- A desktop operating system supported by Scilab

No additional programming languages, databases, or external frameworks are required.

---

## Installation and Setup

### 1. Install Scilab

Download and install Scilab on your computer.

### 2. Clone the Repository

```bash
git clone <repository-url>
```

### 3. Open the Project

Open Scilab and load the main .sce file.

### 4. Run the Application

Execute the Scilab script.

The Engineering Simulation Studio GUI will launch.

---

## How to Use

### Pendulum

1. Open the application.
2. Select Pendulum from the dropdown.
3. Adjust the available parameters using the sliders.
4. Press START.
5. Observe the pendulum animation.
6. Review the calculated results.
7. Examine the generated graphs.
8. Use RESET when required.
9. Modify the parameters and run the simulation again.

### Projectile Motion

1. Open the application.
2. Select Projectile Motion.
3. Adjust:
   - Initial Velocity
   - Launch Angle
   - Gravity
4. Review the calculated results.
5. Press START.
6. Observe the projectile being launched.
7. Watch the projectile rise and descend.
8. Observe the visible trajectory.
9. Review the three graphs.
10. Change the parameters and run the simulation again.

---

## Example Projectile Calculation

For:

- Initial Velocity = 20 m/s
- Launch Angle = 45°
- Gravity = 9.81 m/s²

The approximate results are:

- Time of Flight ≈ 2.88 s
- Maximum Height ≈ 10.19 m
- Range ≈ 40.77 m

These values may vary slightly depending on numerical precision.

---

## Projectile Animation

The projectile animation calculates the position of the projectile at regular time intervals.

The horizontal and vertical positions are calculated using:

x = v₀ cos(θ)t

y = v₀ sin(θ)t - ½gt²

The animation:

1. Calculates the projectile's position.
2. Updates the position of the projectile.
3. Updates the trajectory.
4. Refreshes the graphics.
5. Continues until the calculated flight time is reached.
6. Places the projectile at its final landing position.

The animation uses a fixed number of frames to provide consistent rendering.

---

## Scientific Assumptions

### Projectile Motion

The projectile model assumes:

- Constant gravitational acceleration
- No air resistance
- No wind
- Uniform gravitational field
- Flat ground
- Projectile treated as a point mass

Therefore, the simulation represents ideal projectile motion rather than a complete real-world aerodynamic model.

### Pendulum

The pendulum is represented using an idealized physical model intended for educational visualization.

---

## Educational Purpose

The project demonstrates how mathematical and physical concepts can be converted into interactive computational models.

It combines:

- Physics
- Mathematics
- Programming
- Graphical User Interface development
- Numerical computation
- Data visualization
- Scientific simulation

It can be used for:

- STEM education
- Engineering demonstrations
- Physics experiments
- Classroom demonstrations
- Student projects
- Computational physics learning

---

## Learning Outcomes

This project demonstrates practical implementation of:

- Mathematical equations
- Physics-based modelling
- Interactive GUI development
- Event-driven programming
- Numerical calculations
- Data visualization
- Animation
- Parameter-based simulations
- Scientific computing using Scilab

---

## Current Scope

The current version intentionally contains two simulations only.

| Simulation | Status |
|---|---|
| Pendulum | Implemented |
| Projectile Motion | Implemented |
| Spring Oscillator | Removed |
| Engineering Simulations | Not included |

The Spring Oscillator module and other engineering simulations were intentionally removed to keep the project focused and manageable.

---

## Future Improvements

Potential future enhancements include:

- Pause/resume functionality
- More advanced reset functionality
- Real-time graph updates during animation
- Air-resistance modelling
- Wind simulation
- Energy visualization
- Advanced pendulum models
- Data export
- Saving simulation configurations
- Additional physics simulations
- Improved UI responsiveness
- Improved visual styling
- Performance optimization
- User-defined simulation parameters

These features are potential future additions and are not necessarily implemented in the current version.

---

## Error Handling and Stability

The projectile animation includes safeguards for small calculated ranges and heights.

The animation also:

- Uses a fixed number of frames
- Refreshes the graphics during animation
- Prevents extremely small graph boundaries
- Handles the final landing position explicitly
- Maintains a visible projectile trajectory

These measures improve the reliability of the projectile visualization.

---

## Project Information

**Project Name:** Engineering Simulation Studio

**Platform:** Scilab

**Project Type:** Scientific / Engineering Simulation

**Category:** Interactive Physics Visualization

**Primary Focus:** Computational simulation and visualization of fundamental mechanics concepts

---

## License

No specific open-source license is currently defined for this project.

If this project is distributed publicly, an appropriate open-source license can be added to the repository.

---

## Acknowledgement

This project was developed as an educational engineering/scientific simulation application using Scilab's GUI, numerical computation, and visualization capabilities.
