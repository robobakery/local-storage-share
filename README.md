# About this project
Example of sharing localStorage between cross-domain using iframe & postMessage.

# What it does?
- www will request token stored in localStorage of userhome.
- userhome will respond every 10s.

# Getting Started

## Serve each domains
```
// open a new tab to run userhome.
$ cd userhome
$ python -m SimpleHTTPServer 8000

// open another tab to run www.
$ cd www
$ python -m SimpleHTTPServer 8001
```

## Test it!
- connect to userhome: `http://localhost:8000`
- in console, type `localStorage.setItem('token', [ANY_VALUE_YOU_WANT]);
- then, connect to www: `http://localhost:8001`
- and you will see tokens transferred from userhome
- any changes made to userhome will be detected.
- done!
