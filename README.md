# FPBT 2027: figure with code

`postcondition.pdf` is the detailed version of Figure 2 of the FPBT 2027 talk abstract on postcondition-aware residual risk estimation for property-based testing. It draws the code that checks the postcondition of the ndindex test `test_slice_reduce_no_shape_hypothesis` (`tests/test_slice.py`, lines 177–203) as an interprocedural control-flow graph, with the code of every node. An ending node is added for each way an execution can end: *pass*, where the test returns, and a *violation* for every check, where the check fails. Branches are blue diamonds, checks are red boxes, and other statements are grey boxes. Dashed edges lead to a violation, and the failing inputs of the fault in the paper take the bold one.

`postcondition.dot` is its Graphviz source: `dot -Tpdf postcondition.dot -o postcondition.pdf`.
