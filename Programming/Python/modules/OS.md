
---
# OS Module

[Back to index](../CS/OS/index.md)

---

```python
os.getcwd() # Get current working directory
os.chdir('path') # Change current working directory
os.listdir() # List current working directory

os.mkdir('dir') # Make a directory
os.makedirs('path/dir') # Make a directory (creates sublevels)

os.rmdir('dir') # Remove a directory
os.removedirs('path/dir') # Remove a directory (removes sublevels)

os.rename('olddir', 'newdir') # Rename directory

os.stat('file') # Gives the status (info) of a file

os.walk('path')
# returns a generator of a tree of paths, subdirectories and files

os.eviron.get('env') # Returns the environment path

os.path.join('path', 'path') # Joins the paths in the proper format
os.path.filename('path') # Returns the filename in the path
os.path.dirname('path') # Returns the directory name in the path
os.path.split('path') # Returns the p
```