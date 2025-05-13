# NUT

nutri calculator and dictionary for the terminal.  
A interactive and colorful cli in application written in Go.  
Nut uses [bubbletea](https://github.com/charmbracelet/bubbletea) for interactivity and [lipgloss]() for colorful UI


## USAGE

```sh
nuts bun
```

## Add

There are different ways of add food:

1. by 
1. by nutrients alone


```sh
nut egg         # by default eggs are one medium size egg
nut fish        # by default meat are 100g
nut oatmilk     # by default drinks are 330ml

nut 15p         # if a number, it adds proteins, += 15 protein
nut 10p 0.1va   # if a number, it adds proteins, += 15 protein +=vitamin_a
nut 2x egg      # 2*[default_egg_weight]
nut 2x fish     # 2*100 (there is no default weigth for a *fish* so it defaults to 100g)
nut 350 fish    # += 350g of fish
```

## Remove

### Selecting method

After enter `nut rm`, and it will show you the items added today

```sh
> nut rm
egg
beef
25 protein drink

```

## Today

List the items ate with today, `-t`, `--today`, list is like it is recepit
Also there is yesterday, `-y`, `--yesterday`.


```sh
> nut today

item     protein  fat   sugars  salt    vitamin   minerals 
[item1]  26%       4%     4%      3%    A         Fe
item2    26%       3%    14%      3%    B12, B6   Fe
item3    26%      10%     0%       -    A, C      Fe
item4     1%       1%     4%      3%    -         Fe
...
==================== total =============================
DRI      22%      22%     2%    112%    32%       40%                  
         30g      21g   30mg    110mg Z,R,O
---------------------------------------------------------
   mode [m]   save [S]     print [P]      quit [Q]
```
mode alternate between weight and dri

## Print 

Print it on your printer, wait, is this even possible?

## Config

Let the user configure `-c` or `--config`

1. Set your weight, height.
1. Select nutrients you want to be shown in the list.
1. Set a new item, or a set.
   - A set is a combination of items, for example
     the usual items that you add to your salad. Then buy `nut salad` you will add all those ingridients to your list

## NUTRITION ENCYCLOPEDIA

A colorful and interactive way of showing products and their percentage of nutrients.

### List

Display with a sidebar a list of some common products. Accessed by `nut`, `nut -l` or `nut --list`
If the nutrients are overflow horizontally you can use the arrow keys to flip between pages


#### Example

```sh
> nut -l

==========( list [L] )======( find [F] )======( ref [R] )=========

               item        protein   fat(sat\unsat)   calories      
[    MEAT ]    chicken     29%       1% (1.2%\0.4%)      -             
    DAIRY      pork        25%       2% ( -  \  2%)      -         vitamin
   DRINKS      beef        26%       4%  \  5%        ?         →  minerals
    GRAIN      egg         13%       2%  \  2%                     carb(salt)  
  VEGGIES      tuna        25%       2%  \  2%                     
  PROCESS      salmon      22%       2%  \  2%                      
   OTHERS
   
                                    ← ... →
-----------------------------------------------------------------
   select [↑ ↓]    pages [← →]    grams ↔ % [g]    quit [Q] 
```

#### Properties

Protein, Fat 

#### Values

The If it is `?

### find

Use some API like maybe [openfoodfacts](https://github.com/openfoodfacts/openfoodfacts-go) to access to a bigger data for the nutrition of specific products.

### references

`-r` `--ref` show the sources of the nutrition and their links.

## Colors

The numbers can be color coded in two ways:

### monochrome

Following the category of the product.
Meat are reddish. Drinks are
Dairy are bluish. Process are pink-purple-ish.
And so on.

For example If it is a *good* vitamin or protein:

- >100% will be shown in green
- 99~80% will be shown in white
- 79~60% will be shown in yellow
- 59~40% will be shown in orange
- 39~20% will be shown in red
- <20% will be shown in purple


## TODO

- [ ] based on [bubbletea-teplate](https://github.com/charmbracelet/bubbletea-app-template)
- [ ] use [bubbles](https://github.com/charmbracelet/bubbles)
- [ ] let users change the default values of the items
- [ ] let user set where they want to place the folder to store
