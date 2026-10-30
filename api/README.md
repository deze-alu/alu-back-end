# API

Python scripts that consume the
[JSONPlaceholder](https://jsonplaceholder.typicode.com/) REST API to gather
employee TODO list data and export it to different data structures.

## Requirements

- Ubuntu 14.04 LTS
- Python 3.4.3
- `requests` module
- PEP 8 style

## Files

| File | Description |
| ---- | ----------- |
| `0-gather_data_from_an_API.py` | Display an employee's TODO list progress for a given employee ID |
| `1-export_to_CSV.py` | Export all tasks of an employee to `USER_ID.csv` |
| `2-export_to_JSON.py` | Export all tasks of an employee to `USER_ID.json` |
| `3-dictionary_of_list_of_dictionaries.py` | Export all tasks of all employees to `todo_all_employees.json` |

## Usage

```
$ python3 0-gather_data_from_an_API.py 2
Employee Ervin Howell is done with tasks(8/20):
	 distinctio vitae autem nihil ut molestias quo
	 ...

$ python3 1-export_to_CSV.py 2
$ head -n 2 2.csv
"2","Antonette","False","suscipit repellat esse quibusdam voluptatem incidunt"
"2","Antonette","True","distinctio vitae autem nihil ut molestias quo"

$ python3 2-export_to_JSON.py 2
$ cat 2.json
{"2": [{"task": "suscipit repellat esse quibusdam voluptatem incidunt", "completed": false, "username": "Antonette"}, ...]}

$ python3 3-dictionary_of_list_of_dictionaries.py
$ cat todo_all_employees.json
{"1": [{"username": "Bret", "task": "delectus aut autem", "completed": false}, ...], "2": [...], ...}
```
