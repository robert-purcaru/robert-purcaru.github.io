---
title: "Acrobot: swing-up and balancing controller"
section: projects
order: 1
org: "Personal project"
images:
  - src: "acrobot_rest.jpg"
    caption: "At rest"
  - src: "acrobot_upright.jpg"
    caption: "Balancing"
extra_image:
  src: "acrobot_dynamics.jpg"
  caption: "Acrobot model: two links, actuated only at the elbow"
---

An acrobot is a two-link pendulum with a single motor at the elbow and a free
shoulder joint, so the controller has to pump energy in through the second link
to swing up from the rest position. Then, it has to catch and hold itself balanced
upright. I wrote two controllers for these two different regimes, one that generates
trajectories for the swing up using estimates from a non-linear sum-of-squares solver,
and another LQR controller for the upright position, using a linearization of the
dynamics.

The pendulum hardware is custom, with the arms being 3D-printed and the electronics 
built on perf boards. A drone motor drives the elbow joint, a Teensy 4.1 is the main
processor running the solvers, and a separate STM32 B-G431B-ESC1 board runs the
embedded FOC controller.
