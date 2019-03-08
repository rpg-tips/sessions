Mythic Play Example
================

``` r
library(RPGTips)
seed_counter <- 777
```

Scene 1
=======

Setting: Norvos is in a tavern.

Opening Scene
-------------

Why is Norvos in this tavern?

``` r
roll_table(gme_detail_check)
```

    ## [1] "Disfavors NPC"

Who is he trying to disfavor?

``` r
roll_table(gme_description_table)
```

    ## [1] "Violently Damaged"

Is Norvos evil?

``` r
roll_table(gme_fate_check)
```

    ## [1] "No"

Is it a man?

``` r
roll_table(gme_fate_check)
```

    ## [1] "No"

Why is he pursuing this woman?

``` r
roll_table(gme_actions_table)
```

    ## [1] "Desert Wishes"

He is pursuing a witch who grants wishes to people and then takes their souls as a payment. Norvos' daughter's soul was taken. He found her and fought her, but she fled. He tracked her and found her in this village in the forest.

Scene setting
-------------

NPCs: - The witch. - Norvos' daughter.

Thread: - Find and kill the witch.

Setting: Norvos has arrived in the village tavern after a long trip through the forest.

Chaos Factor: 5.

Scene Development
-----------------

We first check if the scene is altered or interrupted rolling a 1d10 and comparing it against the Chaos Factor.

``` r
set.seed(seed_counter)
roll(1, 10)
```

    ## [1] 3

As it´s lower and odd, the scene is altered: the tavern is empty. Does it look abandoned?

``` r
roll_table(gme_fate_check)
```

    ## [1] "Random Event and Exceptional No"

There are still drinks and food in plates in most of the tables, but there is not a soul to be found.

``` r
roll_table(gme_event_check)
```

    ## [1] "PC Positive"

``` r
roll_table(gme_description_table)
```

    ## [1] "Calmly Ugly"

The witch seems to have just passed around the city and people were actually hiding! Once the tavern door opens and people see that it´s a foreigner, they sigh, relaxed, and go to meet him. Norvos tries to befriend them to get them to talk about the witch.

*Charisma check*

``` r
set.seed(seed_counter)
roll(1,20)
```

    ## [1] 17

*To generate what the people know about the witch, I will roll a detail check*

``` r
roll_table(gme_detail_check)
```

    ## [1] "Favors NPC"

They respect her! She is the village protector. She's made a deal with them, in which they don't bother her and she protects the village from intruders and wild animals.

*Now Norvos has two options: either he declares openly he wants to know where she lives or he tries to get a room for the night and he will explore during the next day, safely knowing that the witch lives around the village. What will he do (1-5: ask for the witch, 6-10: get a room for the night)?*

``` r
set.seed(seed_counter)
roll(1,10)
```

    ## [1] 9

*He will get a room!*

He pays for a room for three days, hoping to finish this whole ordeal in less than that.

*Scene finished! Chaos Factor goes down to 4*

Scene 2
=======

Scene Setting
-------------

### NPCs

-   The witch.
-   Norvos' daughter.
-   People from Oxland.

### Threads

-   Find the witch and recover his daughter's soul.
