# PDDLStream Drake Integration

Trying to describe what the files do. The whole integration relied on Python2 
and a very old version of Drake which I am trying to fix. 

I spent a good amount of time trying to make this compatible with current Drake but there
is just too many bits to be changed. 

- `manipulation_station/`
  - `kuka_multibody_controllers.py`
    - iiwa joint space controller, gripper controller and an overarching one which seems to connect the two.
    - Connection is done in `systems.py`
  - `manipulation_station_plan_runner.py`
    - A LeafSystem for actually running the plan, I'm not quite sure how this relates to the kuka multibody controllers
    - Seems to be more of a wrapper around the robot plans to execute them, get the current one, etc. 
  - `robot_plans.py`
    - plans for the robots themselves (i.e., subplans / operators)
    - e.g. joint space control
- `models/`
  - SDFs and description for the iiwa
- `debug.py`
  - For debugging the generators only
- `domain.pddl`
  - move, pick, place, pull, clean, cook operators and general domain PDDL description
- `generators.py`
  - generator functions for sampling and some helper classes like Pose, Trajectory, Conf
- `iiwa_utils.py`
  - Mostly grasp utils, includes generating grasps/poses for box/cylinder
- `motion.py`
  - Seems to be planning motions using RRT
- `problems.py`
  - generating scenes for Drake and all associated PDDL objects, propositions, etc.
- `run.py`
  - Overarching script that setups problem by adding objects and planning trajectories
- `simulation.py`
  - Unclear but seems like it is stepping through trajectories and computing splines
- `stream.pddl`
  - Streams for sampling purposes
- `systems.py`
  - Building manipulation system and connecting the controllers to it. Also building diagram. 
- `utils.py`
  - Miscellaneous helper functions
