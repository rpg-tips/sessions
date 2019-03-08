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

Is he pursuing someone bad?

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

The tavern is extremely full of people having dinner and lively conversations. The random event...

``` r
roll_table(gme_event_check)
```

    ## [1] "PC Positive"

``` r
roll_table(gme_description_table)
```

    ## [1] "Calmly Ugly"

An old, ugly woman with a revealing dress gets too close to him and offers to have a night he won't remember for just a few coins. Norvos rejects her politely and gets close to the bar to try to get a room for the night. How does the bartender look?

``` r
roll_table(gme_detail_check)
```

    ## [1] "Favors NPC"

*A result that favors NPC will be interpreted as favoring the Witch. So how does someone look to be favorable to a witch? As someone that would sell his soul for a wish. He is very greedy! He looks like a bulky, brawny, bald guy with lots of fake jewelry*

The bartender greets Norvos with a slimy smile, asking him what he is doing in Oxland.

*To summarize how the conversation goes, I will roll charisma*

``` r
set.seed(seed_counter)
roll(1,20)
```

    ## [1] 17

Norvos talks about his interest in staying for a long time at the inn, which sparks the greed of our friend, **Subild**. He's not here to make friends, though, so he asks him right away about the Witch. Does he react positively?

``` r
roll_table(gme_fate_check)
```

    ## [1] "Yes"

What does he know?

``` r
roll_table(gme_detail_check)
```

    ## [1] "Focus NPC"

*I will ignore that result*

Does he know where the witch lives?

``` r
set.seed(seed_counter)
sample(c("Yes", "No", "Doesn´t know", "Prefers to stop talking"), size = 1)
```

    ## [1] "Yes"

``` r
seed_counter <- seed_counter + 1
```

Does he know how to find her?

``` r
set.seed(seed_counter)
sample(c("Yes", "No", "Doesn´t know", "Prefers to stop talking"), size = 1)
```

    ## [1] "Doesn´t know"

Who knows about her?

``` r
roll_table(gme_description_table)
```

    ## [1] "Loosely Clean"

The Glass Enchanter may know about her! He's always dabbling into spooky stuff with his magic. He lives in a hut in the forest, past the village, close to the Black Mountain, along the River Tamors. Everything is engulfed in the Hollow Woods.

Scene 2
=======

Setting
-------

### NPCS

-   The Witch.
-   Norvos' daughter.
-   Subild.
-   The Glass Enchanter.
-   People of Oxland.

### Threads

-   Find and kill the Witch.
-   Find the Glass Enchanter.
