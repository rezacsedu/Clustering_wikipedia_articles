# In-clumps-of-six
### Clustering wikipedia articles

![final cluster](https://user-images.githubusercontent.com/39884389/44083875-c8f28116-9fd2-11e8-97ca-03c4ec6d1461.png)

The above plot is an output of an analytical pipeline that began by gathering summaries of 60 articles on wikipedia people pages and ended by analyzing the latent topics within each article. In between, the articles were manipulated on their summaries (by stop words removal and tokenization). The manipulated articles were then transformed into a vector space model (tf-idf), and clustered into groups (k-means). The complete code can be found [here](https://github.com/HaripriyaTV/In-clumps-of-six/blob/master/code.py).

### Understanding the clusters

Based on the collected summaries, each article was plotted in relation to its similarity to all other articles contained in the plot. The similarity was measured based on the words found in the article summaries. The similarity was determined by a multi-dimensional scaling of the cosine distance (1 minus cosine similarity) between summaries contained within the term frequency-inverse document frequency (tf-idf) matrix. 

Based on the outcome of clustering, the cluster scores are,

|Cluster|Count|Score|
|-------|-----|-----|
|Titles, world, player|12|5|
|Business, founder, executive |   10 | 6|
|Books, novels, copies  |  10 | 6|
|Actor, film, drama |   10 | 6 |
|President, party, election   |  9 |  6.6 |
|Album, music, number |    9 |  6.6|

The 'Business, founder, executive', 'Books, novels, copies', and 'Actor, film, drama' clusters are scored the best. The 'Titles, world, player' cluster is at the top and has mixed in articles from the 'President, party, election' and 'Album, music, number' clusters.

Below are the clusters with their grouped articles.

|President, party, election|Titles, world, player|Album, music, number|Actor, film, drama|Books, novels, copies|Business, founder, executive|
|--------------------------|---------------------|--------------------|------------------|---------------------|-----------------|
|Xi_Jinping|Dwayne_Johnson|Ed_Sheeran|George_Clooney| James_Patterson|Mark_Zuckerberg |
|Vladimir_Putin| Ilaiyaraaja|A.R.Rahman|Shah_Rukh_Khan|Stephen_King|Jeff_Bezos|          
|Donald_Trump|Lionel_Messi|Bruno_Mars|Leonardo_DiCaprio|J.K.Rowling|Bill_Gates|
|Barack_Obama|Cristiano_Ronaldo|Taylor_Swift|Will_Smith|Dan_Brown|Larry_Page|
|David_Cameron|Tiger_Woods|Eminem |Kamal_Haasan|Agatha_Christie|Jack_Ma |
|Narendra_Modi|Rafael_Nadal|Shakira|Tom_Cruise|Ken_Follett|Tim_Cook| 
|Hillary_Clinton|Usain_Bolt|Ellie_Goulding|Brad_Pitt|Neil_Gaiman|Elon_Musk|
|Bill_Clinton |Stephen_Curry|Michael_Jackson|Johnny_Depp|John_Grisham|Warren_Buffett|
|Rahul_Gandhi |Roger_Federer|Selena_Gomez|Morgan_Freeman|Nora_Roberts|Akio_Toyoda |
||Virat_Kohli||Imran_Khan|Arundhati_Roy|Mukesh_Ambani|
||Serena_Williams|||||
||MS_Dhoni|||||       
        



