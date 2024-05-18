1 from scipy . stats import binom
2
3 class Production :
4 def __init__ ( self , variable , terminal ) :
5 self . variable = variable
6 self . terminal = terminal
7
8 def print_production ( prod ) :
9 print ( prod . variable , " ->", prod . terminal )
10
11 def main () :
12 productions = {}
13
14 non_terminals = []
15 terminals = []
16
17 num_terminals = int( input (" Ingrese el n m e r o de variables
terminales : ") )
18 print (" Ingrese cada una de las variables terminales :")
19 for _ in range ( num_terminals ) :
20 terminal = input ()
21 terminals . append ( terminal )
22
23 num_non_terminals = int( input (" Ingrese el n m e r o de variables no
terminales : ") )
24 print (" Ingrese cada una de las variables no terminales :")
25 for _ in range ( num_non_terminals ) :
26 non_terminal = input ()
27 non_terminals . append ( non_terminal )
28
29 num_productions = int( input (" Ingrese el n m e r o de producciones : ")
)
30 print (" Ingrese las producciones una por una:")
31 for i in range ( num_productions ) :
32 variable = input ( f" P r o d u c c i n {i +1}: ")
33 production = input ()
34 if variable not in productions :
35 productions [ variable ] = []
36 productions [ variable ]. append ( production )
37
38 print ("\ n G r a m t i c a ingresada :")
39 for non_terminal in non_terminals :
40 print ( non_terminal , end =" -> ")
41 for production in productions . get ( non_terminal , []) :
42 print ( production , end =" ")
43 print ()
44
45 if __name__ == " __main__ ":
46 main ()
