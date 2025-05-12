# NUT

nutri calculator and dictionary for the terminal.  
A interactive and colorful cli in application written in Go.  
Nut uses [bubbletea](https://github.com/charmbracelet/bubbletea) for interactivity and [lipgloss]() for colorful UI

## TODO

- [ ] based on [bubbletea-teplate](https://github.com/charmbracelet/bubbletea-app-template)
- [ ] use [bubbles](https://github.com/charmbracelet/bubbles)

## USAGE

```sh
nuts bun
```

## Add

There are ways of add food
1. by 


```sh
nut 15p         # if a number, it adds proteins, += 15 protein
nut 10p 0.1va   # if a number, it adds proteins, += 15 protein +=vitamin_a
nut fish        # by default is 100g
nut oatmilk     # drinks by default are 330ml
nut 2x egg      # 2*[default_egg_weight]
nut 2x fish     # 2*100 (there is no default weigth for a *fish* so it defaults to 100g)
nut 350 fish    # += 350g of fish
```

## Remove

### Selecting method

After enter `nut rm`, and it will show you the food added today

```sh
> nut rm
egg
beef
25 protein drink

```

## Today

List the food ate with today, `-t`, `--today`, list is like it is recepit
Also there is yesterday, `-y`, `--yesterday`

```sh
> nut today

item     protein  fat   sugars  salt  vitamin   minerals 
[item1]  26%       4%     4%      3%    Z, R, O   Fe
item2    26%       3%    14%      3%    Z, R, O   Fe
item3    26%      10%     0%       -    Z, R, O   Fe
item4     1%       1%     4%      3%    Z, R, O   Fe
...
==================== total =============================
         22%                         
         30g      21g  30mg    110mg Z,R,O
---------------------------------------------------------
  select [↑ ↓]    save [S]     print [P]      quit [Q] 
```

## Print 



## Config

Let the user configure `-c` or `--config`

## NUTRITION ENCYCLOPEDIA

A colorful and interactive way of showing products and their percentage of nutrients

### List

Display with a sidebar a list of some common products. Accessed by `nut`, `nut -l` or `nut --list`

```sh
> nut -l

==========( list [L] )======( find [F] )======( ref [R] )=========

               item        protein   fat  sugars  salt  vitamin   minerals 
[    MEAT ]    chicken     29%       x%                  X, Y
    DAIRY      pork        25%       x%                  X, Y
   DRINKS      beef        26%       x%                  Z, R, O
    GRAIN      egg         13%       x%      
  PROCESS      tuna        25%       x%
     NUTS      salmon      22%       x%
  VEGGIES
   OTHERS

-----------------------------------------------------------------
            select [↑ ↓]             quit [Q] 
```

### find

Use some API like maybe [openfoodfacts](https://github.com/openfoodfacts/openfoodfacts-go) to access to a bigger data for the nutrition of specific products.

### references

`-r` `--ref` show the sources of the nutrition and their links.
