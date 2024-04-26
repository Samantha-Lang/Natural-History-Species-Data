# Natural History Species Data
Species Type Data and Computational Analysis from Natural History Museum of London. Looking at 4 types of species at the NHML.


# What is here?
- [Original dataset.csv](https://github.com/Samantha-Lang/Natural-History-Species-Data/blob/main/Original%20dataset.csv): Dataset taken from csv. file of original Natural History Museum dataset

- [Columns_subset.csv](https://github.com/Samantha-Lang/Natural-History-Species-Data/blob/main/code/Columns_subset.csv): Narrowed dataset after coding only those four rows
  
- Data Visualization: Bar graph taking the four species and how many are found in the Natural History Museum of London


## [Hyperlink to coding in CoLab and Procedural Steps](https://colab.research.google.com/drive/1MXLZo8RTayuao2tWTdAyKFj_8XLNjMq2)

# What is the purpose of this?
To draw a comparison between species and their phylum, class, size and type.

# Steps
Dataset Natural History Museum 
1. INITIAL STEPS Start by implementing this instruction into CoLab
[ ]
 import numpy as np
import pandas as pd

2. Naming this CSV file in CoLab. This is in place in order to use "chd" instead of typing out the long address.
[ ]
 chd=pd.read_csv("resource.csv")
 <ipython-input-13-23fcbec2ea1a>:1: DtypeWarning: Columns (22) have mixed types. Specify dtype option on import or set low_memory=False.
  chd=pd.read_csv("resource.csv")
[ ]
 from google.colab import drive
drive.mount('/content/drive')
3. To get the first 4 rows, type:
[ ]
 chd [0:4]
 
4. The chart will show -order -phylum -scientificName -specificEpithet -subfamily -subgenus -suborder -superfamily -taxonRank -type You can also get down to one category you're focusing on. This is important to narrowing down specific interests. For example, if you just want to find PHYLUMS:
[ ]
 chd ["phylum"][0:4]
 0    Arthropoda
1    Arthropoda
2    Arthropoda
3    Arthropoda
Name: phylum, dtype: object
5. You can combine them making a broader search. Sticking with only 4 rows as results:
[ ]
 chd [["phylum" , "scientificName" , "specificEpithet" , "subfamily"]] [0:4] =="Columns"
 
6. Only finding NaN (specific column) This will ONLY narrow down the columns, there are many rows still: 0 NaN 1 NaN 2 NaN 3 NaN 4 NaN ... 824749 NaN 824750 NaN 824751 NaN 824752 NaN 824753 NaN
[ ]
 chd.iloc[:,3]
 0       NaN
1       NaN
2       NaN
3       NaN
4       NaN
         ..
62047   NaN
62048   NaN
62049   NaN
62050   NaN
62051   NaN
Name: associatedMedia.category, Length: 62052, dtype: float64
7. This is another specific search option. This is important because it adds another aspect in the process of narrowing the data down and identifies the #s associated with just TR.
[ ]
chd[chd["taxonRank"]== "TR"]

# Data Visualization 
<img width="624" alt="Screenshot 2024-04-19 at 11 00 43 AM" src="https://github.com/Samantha-Lang/Natural-History-Species-Data/assets/167785490/bada307e-1fd1-4efe-89cb-99348cd60376">

