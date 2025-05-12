# NUTS

nutri calculator and dictionary for the terminal.  
A interactive and colorful cli in application written in Go.

## USAGE

```sh
pro bun
```

## Ways of input

```sh
pro 15          # if a number, it adds proteins, += 15 protein
pro fish        # by default is 100g
pro fish        # by default is 330ml
pro 2x egg      # 2*[default_egg_weight]
pro 2x fish     # 2*100 (there is no default weigth for a *fish* so it defaults to 100g)
pro 350 fish    # += 250g of fish
```

## LIST PRODUCTS

A colorful 
```sh
--list  show products and their percentage of protein

MEAT      VEGGIES     DRINKS      OTHERS
beef      veg1        ...         eggs
pork      veg2        ...         ...
lamb      veg2        ...         ...
...       veg2        ...         ...
```

Maybe a way to display, with a sidebar tot list of products

```sh
               item        protein   fat     vitamin   minerals
[    MEAT ]    chicken     29%       x%      X, Y
    DAIRY      pork        25%       x%
   DRINKS      beef        26%       x%      Z, R, O
    GRAIN      egg         13%       x%
  PROCESS      tuna        25%       x%
     NUTS      salmon      22%       x%
  VEGGIES
   OTHERS      
```
