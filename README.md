# word_count
A multithreaded program that reads one or more text files and reports frequency of each word found.


## ✨ Feature
- Multithreading using the **pthread** library
- Uses **Pintos doubly-linked lists** to store word counts
- Ensures thread-safe updates using **mutex_locks**

## 🛠️: Build Instructions
```bash
make
```
Running `make` produces four executables
| Executable |              Description                                                      | 
|------------| ------------------------------------------------------------------------------|
|  `words`   | single-threaded word counter using simple linked lists                        |
|  `lwords`  | single-threaded word counter using Pintos doubly linked lists                 |
|  `pwords`  | multi-threaded word counter using Pintos linked lists + mutex synchronization |
|  `pthread` | small demo program showing multiple threads accessing shared global variaable |


## 🚀: Usage
Example (processing all `.txt` files in the `gutenberg/` folder) 
### words
  ``` bash
./words gutenberg/*.txt | tail 
```
```python-repl
2354	you
2837	that
3163	he
3197	in
3420	was
3619	it
5041	of
5499	to
7649	and
12141	the
```

### lwords
  ``` bash
./lwords gutenberg/*.txt | tail 
```
```python-repl
2354	you
2837	that
3163	he
3197	in
3420	was
3619	it
5041	of
5499	to
7649	and
12141	the
```

### pwords
  ``` bash
./pwords gutenberg/*.txt | tail 
```
```python-repl
2354	you
2837	that
3163	he
3197	in
3420	was
3619	it
5041	of
5499	to
7649	and
12141	the
```

All three commands should given **similar results** given the same inputs.

## 🙌 Credits / Acknowledgements
* Skeleton code from UCBerkeley's CS162 coursework

