# funktion-nodejs-example

A simple project using nodejs functions.

## Running 

* [download the funktion binary for your platform](https://github.com/funktionio/funktion/releases) and add it to your `$PATH` ensuring that its executable. 
* ensure you have access to a kubernetes or openshift cluster so that you can type commands like these (depending on if you use kubernetes or openshift):

```
kubectl get pod
oc get pod
```
* install funktion into your current namespace via:

```
funktion install platform
```

* clone this git repository
```
git clone https://github.com/funktionio/funktion-nodejs-quickstart.git
cd funktion-nodejs-quickstart
```

* now create your function(s) and watch for local changes to your files type:

```
funktion apply -f src
```

* you should be able to view the functions created via

```
funktion get fn
```

* to watch the pods startup for your functions you can try:

```
kubectl get pod -w
```

* to enter watch mode where you can keep editing the source code and the functions update in real time try add `-w`:

```
funktion apply -f src -w
```

* then if you change a source file in the `src` folder you should see the pod for the function restart and load the new source.
