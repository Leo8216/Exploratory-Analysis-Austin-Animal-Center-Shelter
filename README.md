# Exploratory-Analysis-Austin-Animal-Center-Shelter

Exploratory analysis of Austin Animal Center Shelter dataset using python 3.6. The Austin Animal Center is the largest no-kill animal shelter in the United States that provides care and shelter to over 18,000 animals each year. The time frame for all visualizations is from 2013 Q4 to 2018 Q1.

## Summary & Insights

### Inspiration

I wanted to do exploratory analysis on something that interested me, and found this dataset for the Austin Animal Shelter. I think what animal shelters do is great, and this one in particular is a no-kill shelter, that had some data on Pit Bulls so I decided to explore it a bit. Unlike many, I want to adopt a Pit Bull because after living with one, I think they are great dogs. One hypothesis I wanted to test was that Pit Bulls are, in general, less desired than other dog breeds. I think this bad reputation is because there are a number of myths and stereotypes about "pitbull-type" dogs that are either anecdotal and misleading or entirely false. <span style="color:blue"><b> For facts and reliable information about Pit Bull type dogs, refer to https://www.pitbullinfo.org/.</b></span>

### What is the distrubution of Animal type at the shelter?

As expected, dogs and cats are the majority.  Dogs with ~57% an Cats with ~37% for a combined 96% of the total. The other 6% being birds and other types of animals.

![Image of Distribution of Animal Type](https://github.com/Leo8216/Exploratory-Analysis-Austin-Animal-Center-Shelter/blob/master/images/10_Anymal_Type_Distribution_ALL.png)

### Which day of the year has the least/most outcomes?

* We can see that December 25th (Christmas day) is the one with the least number of outcomes for all years (2013 to 2018). This makes sense as adopting an animal may not be in the top priorities for Christmas Day. Please note that Adoption is the most significant contributor to the number of outcomes.
* August 19th is the day with the most Outcomes - with most being Adoption, it is a great day for pets. Also notice that July has several days with a high number of outcomes. After a little bit of research, I found out that some cities waive adoptions fees during July as they prepare for shelters to be filled beyond capacity with lost animals who become frightened by 4th of July fireworks and run away.

![Image of Count of Outcomes by Month and Day of Year](https://github.com/Leo8216/Exploratory-Analysis-Austin-Animal-Center-Shelter/blob/master/images/9_Count_of_Outcomes_by_Month_and_Day_of_Year_All_Years.png)

### What Animals are under the "Other" Animal type category? Which is their most likely outcome?

From donutplot on left - "Top 12 - Other Animal Type":
* Bats and Bats mixes make up more than 50% of the Top 12 in the Other animal type. I was expecting Rabbit to be the one with the majority. 
* Skunk and Guinea Pigs made it to the top 12... impressive. Not sure if I ever met anyone that has one.

From donutplot on right: "Outcome - Other Animal Type":
* Most of this other interesting animals, 71.9%, end up with an outcome of Euthanasia. 
* Only 5% of them are adopted.

![Image of Other Animal type Distribution and Outcomes](https://github.com/Leo8216/Exploratory-Analysis-Austin-Animal-Center-Shelter/blob/master/images/11_Other_Animal_Type_Top12_%26_Outcome.png)

### Are Pit Bull or Pit Bull Mix dogs less desired than other dog breeds?

Pit Bull vs. Other Breeds Insigths:
   1. % Adopted (outcome type): Other dog breeds are more likely to get adopted than Pit Bulls. ~47% vs ~37%.
   2. % Returned to Owner (outcome type): Pit Bulls are more likely to be returned to owner than other dog breeds.  This is more an indication that Pit Bull owners are more attached to their dogs, being more likely to go to shelter looking for their lost pet. 
   3. % Stray (intake type): It is less likely to have a Stray intake type Pit Bull than Other Breed, althought the numbers are really close.  This is also associated about how much pet owners care about them. The more they care, the less the number of Strays.
   4. % Owner Surrender (intake type): Pit Bulls and Other Breeds are surrendered in an equal proportion. This is consistent with the Dog vs. Cat radar, indicating that this decision in not influenced by the animal but rather external considtions such as financial.
   5. Avg time (days) in shelter to Adoption: Avg # days in shelter for Other Breeds is ~20 days, less than half that for Pit Bulls ~50 days. This is an indication they are more desired than Pit Bulls. 
   6. Avg time (days) in shelter to Return to Owner: Avg # days in shelter for other breeds is ~4 days, about half that for Pit Bulls ~8 days. From this one and #2 (% Return to Owner), we conclude that even though Pit Bull owners are more likely to reclaim their dog, they take a little longer than other dog owners.
   
Findings 1 and 5 validate the hypothesis that Pit Bulls are less desired than other Dog breeds. I think this bad reputation is because there are a number of myths and stereotypes about "pitbull-type" dogs that are either anecdotal and misleading or entirely false. <span style="color:blue"><b> For facts and reliable information about Pit Bull type dogs, refer to https://www.pitbullinfo.org/.</b></span> On the flip side, from findings 2 and 3 we can imply that those who took a chance on having a Pit Bull are more attached to them, because they are indeed amazing dogs. 

![Image of Pit Bull vs. Other Breeds radar](https://github.com/Leo8216/Get-Out-Hide-Out-Take-Out/blob/master/images/Gun_Kills_vs_Gun_Laws.PNG)

### Closing Remarks

<b> *If you are considering getting a pet, please consider adopting.  If getting a dog, I strongly suggest you read the facts in link above before swinging by an Animal Shelter, so that you make an informed decision. Pit Bull or not (although, the numbers show Pit Bull owners are more attached to them, wonder why?), as long as you adopt, you will potentially be saving a life that will bring a lot of joy to yours.*</b>

## Required Imports
This was run in Python 3.6
```
import pandas as pd
import numpy as np
import seaborn as sns
import matplotlib.pyplot as plt
from matplotlib import rc
% matplotlib inline
from math import pi
from palettable.colorbrewer.qualitative import Pastel1_7
pd.options.mode.chained_assignment = None
```

## Dataset

* **Austin Animal Shlter Center** [link to Kaggle dataset.](https://www.kaggle.com/aaronschlegel/austin-animal-center-shelter-intakes-and-outcomes) The data contains intakes and outcomes of animals entering the Austin Animal Center from the beginning of October 2013 to the present day. The datasets are also freely available on the Socrata Open Data Access API and are updated daily. The data presented here is only possible through the hard work and dedication of the Austin Animal Center in saving and caring for animal lives.

## Author

* **Leo Barbosa**
