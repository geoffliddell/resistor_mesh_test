# resistor mesh test!

Checking that igraph's ```laplacian_matrix()``` function works correctly. Comparing with solving using ngspice

1. solve_grid       -> solves the 10x10 resistor mesh problem posed on rosettacode.org
2. solve_line       -> sets up a string of resistors of length N with shunt resistors between each pair and solves for the currents
3. solve_line_spice -> same as above but do it both using ngspice and igraph, compare the results
4. figure_timings   -> same as solve_line_spice but increase N gradually to see how the comptutation time scales with N
