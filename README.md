# sc2-basics
## 1. Requirements
python 3.6 <br>
tensorflow 1.4+ <br>
pysc2(v1.2) <br>
## 2. Quick Start Guide
### Get StarCraft II
**Linux:**  Follow [Blizzard's documentation](https://github.com/Blizzard/s2client-proto#downloads) to get the linux version (e.g. 4.0.2) and save in ~/StarCraftII/. <br>
**Windows:** Install of the StarCraft2 as normal from [Battle.net] (https://battle.net/). <br>
**Maps:**  Download the [ladder-maps](https://github.com/Blizzard/s2client-proto#downloads) and the [mini-games](https://github.com/deepmind/pysc2/releases/download/v1.2/mini_games.zip) and extract them to your StarcraftII/Maps/ directory. <br>
### Get PySC2
Install the PySC2 by pip:
```
pip3 install pysc2==1.2
```
Test the PySC2 as:
```
python -m pysc2.bin.agent --map CollectMineralShards
```
### Debug
#### 1
When System requires Python '>=2.6,<3', please update futures:
```
pip3 install futures==3.1.1
```
then install PySC2 again.<br>

#### 2
When raise _exceptions.UnparesedFlagAccessError,
Please open ...\site-packages\pysc2\sun_configs\__init__.py (windows), and add 
```
import sys
FLAGS(sys.argv)
```
under **FLAGS =flags.FLAGS** <br>

**update by parap1uie-s @ 20180730**
```
In fact, you don't have the needs to edit __init__.py as above.

Modify the enter main script like main.py will be fine.

For example: https://github.com/DeeCamp18-RL/pysc2-rl-agent-edited
```
#### 3
**screen_size_px** and **minimap_size_px** are the features in PySC2 v1.2. They are deprecated in PySC2 v2.0. One can change the pysc2 to the version 1.2(recommend), or use **agent_interface_format** to replace **screen_size_px** and **minimap_size_px**.

#### 4
when raise the error of atari_py of baselines installation, like *HINT:are you sure make/cmake is installed*, you can install atari-py independently as
```
pip install --no-index -f https://github.com/Kojoley/atari-py/releases atari_py
```
then install baselines:
```
pip install baselines
```
