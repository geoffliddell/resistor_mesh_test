# resistor mesh test!

Checking that igraph's ```laplacian_matrix()``` function works correctly. Comparing with solving using ngspice

1. solve_grid       -> solves the 10x10 resistor mesh problem posed on rosettacode.org
2. solve_line       -> sets up a string of resistors of length N with shunt resistors between each pair and solves for the currents
3. solve_line_spice -> same as above but do it both using ngspice and igraph, compare the results
4. figure_timings   -> same as solve_line_spice but increase N gradually to see how the computation time scales with N
5. potential-divider_resistor-bridge -> picking the most basic possible resistor networks with 2 to 5 resistors to solve by hand and check that currents are calculated correctly

```laplacian_matrix(A)``` tidily arranges all the nodes of ```A``` by weighted degree, so that size of the diagonal elements is in descending order. Therefore necessary to specify that the nodes should be arranged in the correct order so that when solving ```Lp = q```, all the nodes in ```L``` match up with the order in ```q```! this is done with ```laplacian_matrix(A, vertices = Vert$label)``` where ```Vert``` is the node list containing labels and co-ordinates (x,y)
