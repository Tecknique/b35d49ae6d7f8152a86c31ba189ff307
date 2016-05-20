# ComStore
This is my solution to the Comscore programming challenge. The program is written in Python3 and relies on 
- `python-xdg`
- `argparse`.

```
./bin/store ./indata.psv
```
changes the `pipe seperated values` file into a resource tree of `/date/setbox/title`. Each entry is stored as a labeled csv.

```
./bin/query -h
```
Allows you to query the store.

```
./bin/purge
```
deletes the entire store without question. In order to insure safety of your system, know that the location of the store as defined in `utility.py` is generated by:

```python
import xdg.BaseDirectory
LOCATION=xdg.BaseDirectory.save_data_path('PHILIPROBINSON.ComStore')
```
This location usually exists in linux systems at `~/.local/share/PHILIPROBINSON.ComStore`.

