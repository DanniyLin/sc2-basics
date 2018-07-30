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
When System requires Python '>=2.6,<3', please update futures:
```
pip3 install futures==3.1.1
```
then install PySC2 again.<br>

When raise _exceptions.UnparesedFlagAccessError,
Please open ...\site-packages\pysc2\sun_configs\__init__.py (windows), and add 
```
import sys
FLAGS(sys.argv)
```
under **FLAGS =flags.FLAGS** <br>






