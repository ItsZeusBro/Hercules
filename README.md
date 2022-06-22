# Hercules
## Test Driven Function Framework using Hydra Abstract Syntax and Hercules support for Hydra Syntax Plugins
![420px-Hercules_killing_the_hydra_headed_monster](https://user-images.githubusercontent.com/107733608/174702298-353afad3-96be-44c2-bf1a-b9f3cca65d54.jpg)


## Hercules uses Boolean Invariants, Regex Invariants (for string patterns), and Query Selectors for filtering (and piping) leading to Terminating Boolean Invariants 
### Basic Example of Hydra Abstract Syntax with Hercules Plugin enabled:
    someFunc = {
        out: "some/file/someWhere.js" //you can use .py and Hydra will generate python files
        inv: {
            inv1: "(p1 >= 10)" ,
            inv2: "(/ab+c/ == p2)",
            inv3: p4->(i<100)->(p4.size<=10)
            inv4: (objP1.disjointset(objP2).difference(objP3))->(i<100)
        }
        params:{
            p1: <int>,
            p2: <string>,
            p3: <function>,
            p4: <intCollection>
            p5: {
                //This parameter is an Object
                objP1: <int_collection>,
                objP2: <int_collection>,
                objP3: <int_collection>,
                pFunc: <function>
            }
        }
    }

### Additional Info:
1. Hercules takes the assignment to someFunc and creates a Hydra Object called someFunc. This object generates test code, and is also callable from Hydras supported languages
2. Remember, Hydra uses it's own Native File Type to give more Semantical Meaning to an otherwise JSON like Syntax, in this case with Hercules plugins enabled
