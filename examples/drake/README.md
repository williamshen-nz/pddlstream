# PDDLStream Drake Integration

Trying to describe what the files do. The whole integration relied on Python2 
and a very old version of Drake which I am trying to fix. 

I spent a good amount of time trying to make this compatible with current Drake but there
is just too many bits to be changed. 

- `manipulation_station`
- `models`
- `debug`
- `domain.pddl`
  - move, pick, place, pull, clean, cook operators and general domain PDDL description
- `generators.py`
- `iiwa_utils.py`
- `motion.py`
- `problems.py`
  - generating scenes for Drake and all associated PDDL objects, propositions, etc.
- `run.py`
- `simulation.py`
- `systems.py`
- `utils.py`
