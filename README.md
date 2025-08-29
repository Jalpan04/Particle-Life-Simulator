# Particle Life Simulator

This is a simple, browser-based particle life simulator where you can observe emergent behavior from simple rules of attraction and repulsion between different groups of particles.

## Features

* **Customizable Simulation:** Easily adjust the number of particles, the number of particle groups, and the interaction radius.
* **Interactive Rule Engine:** Define the interaction rules between different groups of particles. Set whether they attract or repel each other using a simple slider-based interface.
* **Real-time Visualization:** Watch the particles interact and form complex patterns in real-time.
* **Repelling Force on Click:** Click on the canvas to apply a temporary repelling force to the particles.
* **Responsive Canvas:** The simulation canvas resizes with the browser window.

## How to Use

1.  Open the `index.html` file in a web browser.
2.  The simulation will start automatically.
3.  Use the controls in the right-hand sidebar to adjust the simulation parameters.

## Controls

The sidebar provides the following controls to manipulate the simulation:

### Global Settings

* **Particles:** Adjust the total number of particles in the simulation.
* **Groups:** Set the number of distinct particle groups. Each group has its own color.
* **Radius:** Controls the interaction radius for all particles. Particles will only interact with other particles within this distance.

### Rules

For each pair of particle groups, a slider allows you to set the interaction rule.
* A **positive value** makes the first group attract the second group.
* A **negative value** makes the first group repel the second group.
* A **value of zero** means no interaction.

### Reset Button

* Click the "Reset" button to re-initialize the simulation with the current settings and randomize the interaction rules.

## Underlying Concepts

The simulation is based on a simple physics model:

* Each particle is influenced by other particles within its `interactionRadius`.
* The force between two particles is determined by the rule set for their respective groups.
* Particles also have a small collision force to prevent them from overlapping.
* A damping factor (`0.85`) is applied to the velocity of the particles to prevent them from moving too fast and to allow for more stable structures to form.
