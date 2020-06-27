---
layout: post
title:      "Animal Crossing Villagers CLI"
date:       2020-06-27 21:11:54 +0000
permalink:  animal_crossing_villagers_cli
---

"Animal Crossing: New Horizons" is a video game for the Nintendo Switch console that saw a huge spike in popularity during the coronavirus quarantine time. A player is given an island to develop and has the ability to invite anthropomorphized animal villagers to come live on the island. This is one of the major features of the game. At present, there are 391 villagers. Because of the large number of villagers, I created an Animal Crossing Villagers CLI project for the Animal Crossing player to easily sort through and discover new villagers to invite to their island.

I scraped this website using the Nokogiri and open-uri gems for information on all the villagers: https://animalcrossing.fandom.com/wiki/Villager_list_(New_Horizons)

Each villager has the following attributes: name, image url, personality, species, birthday, catchphrase, and hobbies. I created Villager instances and created methods to sort the instances by name, species, personality, and birthday month. I also added a feature to open up the villager's wiki page (e.g. https://animalcrossing.fandom.com/wiki/Bob) in a browser using the Launchy gem.

Using the Animal Crossings CLI project, you can view the attributes of all 391 villagers in a more manageable way.

