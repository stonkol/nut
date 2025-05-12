# NUT

nutri calculator and dictionary for the terminal.  
A interactive and colorful cli in application written in Go.  
Nut uses [bubbletea](https://github.com/charmbracelet/bubbletea) for interactivity and [lipgloss]() for colorful UI

## TODO

- [] based on [bubbletea-teplate](https://github.com/charmbracelet/bubbletea-app-template)

## USAGE

```sh
nuts bun
```

## Ways of input

```sh
nut 15          # if a number, it adds proteins, += 15 protein
nut fish        # by default is 100g
nut fish        # by default is 330ml
nut 2x egg      # 2*[default_egg_weight]
nut 2x fish     # 2*100 (there is no default weigth for a *fish* so it defaults to 100g)
nut 350 fish    # += 250g of fish
```

## LIST PRODUCTS

A colorful and interactive way of showing products and their percentage of protein
```sh
> nut --list

MEAT      VEGGIES     DRINKS      OTHERS
beef      veg1        ...         eggs
pork      veg2        ...         ...
lamb      veg2        ...         ...
...       veg2        ...         ...
```

Maybe a way to display, with a sidebar tot list of products

```sh

===============[ list [L] ]============[ find [F] ]==============

               item        protein   fat     vitamin   minerals
[    MEAT ]    chicken     29%       x%      X, Y
    DAIRY      pork        25%       x%      X, Y
   DRINKS      beef        26%       x%      Z, R, O
    GRAIN      egg         13%       x%      
  PROCESS      tuna        25%       x%
     NUTS      salmon      22%       x%
  VEGGIES
   OTHERS

-----------------------------------------------------------------
           select [ ↑ ↓ ]           [ quit [Q] ]

```
