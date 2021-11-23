# Topic Modelling

Topic modelling is performed to generate a representation of documents in the topic space. Different topics may share some words and a document can have more than one topic associated with it. To better understand the topic, associated cluster of words are extracted via visualisation.


# Datasets and Pre-processing
HardwareZone is a forum where registered users can repost, share and express their comments and opinions about anything conveniently according to different forum threads. To understand the public sentiments on the Covid-19 situation in Singapore, we focus on the forum thread titled “Eat Drink Man Woman”, EDMW in short, to obtain the contents of each post, as there is no dedicated forum thread on “Covid-19”. 

A total of 184716 threads were scraped from 9326 pages of EDMW . Subsequently, a total of 11277 Covid-19 related threads were extracted through the thread titles containing Covid-19 vocabulary such as “covid19”, “pre-covid19”, “post-covid19” and its variations. As there are close to half a million of posts in these threads, we only obtained the most recent 5 posts in each thread. Hence, a total of 10598 posts are used for the purpose of Topic Modelling. From the posts, all images, html links, emojis, emoticons and non-English words are excluded. Content of the posts are tokenised and POS tags are obtained for each token. Tokens were lemmatised and only nouns are extracted for further analysis. A frequency plot is also plotted to extract the most frequent words. It was found that some of the most common words include “click”, “to”, “expand”, “edmwer”, “app” which reflect the HWZ notation of reposts and “liao" which reflect the prevalent use of colloquial English. These words are added into the stop word lists and removed from each post during pre-processing.

Number of topics	          4	                   5                     	6
C_umass  	          -9.506497974706509	  -9.10533638568538	    -8.908555870270321
C_v  	              0.47487951657782745	  0.45287028371827687	  0.43811157137575596
