# Object Graph

* generic knowledge representation: anything can be described by objects and
  their relations
* universal software/code form (Abstract Syntax Tree/Graph)
* grouped objects forms oriented object graph, which can be treated as EDS:
  Executable Data Structure
* any mainstream language (Java, Python,..) can be used as-is for
    * forming such executable structures directly in memory and 
    * executing them by its interpretation
* object graph also works as an effective universal representation for databases
    * some node types also can be used for representing data in external RDBMS:
      databases, connections, tables, records, stored procedures,...
    * data presistence layer

```py
# base graph node class / generic knowledge representation (AST/ASG)
class Object:

    # named node constructor
    def __init__(self, V):

        # node class/type tag
        self.type = self.__class__.__name__.lower()

        # node name / scalar value
        self.value = V

        # slot{}s / attributes / associative array
        self.slot = {}

        # nest[]ed elements / ordered container
        self.nest = []
```


See also:

* Marvin Minsky
    [A Framework for Representing Knowledge](https://web.media.mit.edu/~minsky/papers/Frames/frames.html)<br>
    MIT-AI Laboratory Memo 306, June, 1974.
* Enn H. Tyugu
    [Conceptual programming](https://scholar.google.com/scholar?cluster=4867029609080902758)<br>
    M.: Nauka, 1984
