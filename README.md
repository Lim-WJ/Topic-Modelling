# Topic Modelling

Topic modelling is performed to generate a representation of documents in the topic space. Different topics may share some words and a document can have more than one topic associated with it. To better understand the topic, associated cluster of words are extracted via visualisation.


# Datasets and Pre-processing
HardwareZone is a forum where registered users can repost, share and express their comments and opinions about anything conveniently according to different forum threads. To understand the public sentiments on the Covid-19 situation in Singapore, we focus on the forum thread titled “Eat Drink Man Woman”, EDMW in short, to obtain the contents of each post, as there is no dedicated forum thread on “Covid-19”. 

A total of 184716 threads were scraped from 9326 pages of EDMW . Subsequently, a total of 11277 Covid-19 related threads were extracted through the thread titles containing Covid-19 vocabulary such as “covid19”, “pre-covid19”, “post-covid19” and its variations. As there are close to half a million of posts in these threads, we only obtained the most recent 5 posts in each thread. Hence, a total of 10598 posts are used for the purpose of Topic Modelling. From the posts, all images, html links, emojis, emoticons and non-English words are excluded. Content of the posts are tokenised and POS tags are obtained for each token. Tokens were lemmatised and only nouns are extracted for further analysis. A frequency plot is also plotted to extract the most frequent words. It was found that some of the most common words include “click”, “to”, “expand”, “edmwer”, “app” which reflect the HWZ notation of reposts and “liao" which reflect the prevalent use of colloquial English. These words are added into the stop word lists and removed from each post during pre-processing.

Number of topics	          4	                   5                     	6
C_umass  	          -9.506497974706509	  -9.10533638568538	    -8.908555870270321
C_v  	              0.47487951657782745	  0.45287028371827687	  0.43811157137575596


4-topic model has the worst C_umass value and the best C_v value. 
5-topic model is the middle performing model.
6-topic model has the best C_umass value and the worst C_v value. 

As such, different models were chosen based on the metrics used. Hence, it is prudent to see the top 10 most representative words for each topic through word cloud and pyLDAvis package. From the word cloud and pyLDAvis package, the topics are too broad for the 4-topic model and there are overlapping topics for the 6-topic model. Furthermore, the 5-topic model has a diverse range of topics that illustrates the current Covid-19 situation. Based on the team’s judgement and understanding of the pandemic, the 5-topic model is the most appropriate. 

From the 5-topic model, below is a short summary of what each topic entails.
Topic 1 illustrates the status updates globally.  
Topic 2 illustrates the safe management measures in Singapore.
Topic 3 illustrates the vaccination rates and the protection vaccination offers against Covid-19 and its variants.
Topic 4 illustrates the concerns surrounding the management and seriousness of symptoms of Covid -19.
Topic 5 illustrates the concerns surrounding the number of community case counts, clusters and the infection rates.  

