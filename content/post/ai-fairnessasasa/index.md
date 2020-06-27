# Are Algorithms Racist and Sexist?



After the end of the war, the Nuremberg trials laid bare the atrocities conducted in medical research by the Nazis. In the aftermath of the trials, the medical sciences established a set of rules — The Nuremberg Code — to control future experiments involving human subjects. The Nuremberg Code has influenced medical codes of ethics around the world, as has the exposure of experiments that had failed to follow it even three decades later, such as the infamous [Tuskegee syphilis experiment](https://en.wikipedia.org/wiki/Tuskegee_syphilis_experiment). 

The direct impact of AI experiments and applications on users isn't quite as inhumane as the Tuskegee and Nazi experimentations, but in the face of an overwhelming and growing body of evidence of algorithms being biased against certain demographic cohorts, it is important that the discussion happens sooner or later. AI systems can be biased based on who builds them, the way they are developed, and how they’re eventually deployed. This is known as algorithmic bias. 

While the data sciences have not developed a Nuremberg Code of their own yet, the social implications of research in artificial intelligence are starting to be addressed in some curricula. But even as the debates are starting to sprout up, what is still lacking is a discipline-wide discussion to grapple with questions of how to tackle societal and historical inequities that are reinforced by AI algorithms.

We are flawed creatures. Every single decision we make involves a certain kind of bias. However, algorithms haven't proven to be much better. Ideally, we would want our algorithms to make better-informed decisions devoid of biases so as to ensure better social justice, i.e., equal opportunities for individuals and groups (such as minorities) within society to access resources, have their voices heard, and be represented in society.

When these algorithms do the job of amplifying racial, social and gender inequality, instead of alleviating it; it becomes necessary to take stock of the ethical ramifications and potential malevolence of the technology.

This essay was motivated by two flashpoints : the racial inequality discussion that is now raging on worldwide, and the Yann LeCun v/s Timnit Gebru beef on Twitter caused due to a disagreement over a downsampled image of Barack Obama which was depixelated to a picture of a white man by a face upsampling machine learning (ML) model. 



![Image](https://pbs.twimg.com/media/EbACRFtUYAAjNya?format=jpg&name=large)

The (rather explosive) argument was sparked by this tweet by LeCun where he says that the resulting face was that of a white man because of a bias in data that trained the algorithm. Gebru responded sharply that the harms of ML systems cannot be reduced to biased data. 

Never mind Obama, the model even depixelized a **dog's face** to a caucasian man's. It sure loves the white man.



<center><blockquote class="twitter-tweet" data-theme="dark"><p lang="en" dir="ltr">This is how that depixelizing algorithm reconstructed my dog, Tank <a href="https://t.co/XHgdNwRmXy">pic.twitter.com/XHgdNwRmXy</a></p>&mdash; Jiahao Chen @ 🏡🗽 (@acidflask) <a href="https://twitter.com/acidflask/status/1274889347356069888?ref_src=twsrc%5Etfw">June 22, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script></center>



The misunderstanding clearly seems to emanate over the interpretation of the word "bias" - which in any discussion about the social impact of ML/AI seems to get crushed under the burden of its own weight. 

As Sebastian Raschka puts it, "the term **bias** in ML is heavily overloaded". It has multiple senses that can all be mistaken for each other and a lot of gaps in communication could be covered by just being a little more precise.

​	(1) **bias** (as in mathematical **bias** unit) 
​	(2) "Fairness" **bias** (also called societal **bias**) 
​	(3) ML **bias** (also known as inductive **bias**, which is dependent on decisions taken to build the model.) 
​	(4) **bias**-variance decomposition of a loss function  
​	(5) Dataset **bias** (usually causing 2)



<center><blockquote class="twitter-tweet" data-theme="dark"><p lang="en" dir="ltr">ML systems are biased when data is biased.<br>This face upsampling system makes everyone look white because the network was pretrained on FlickFaceHQ, which mainly contains white people pics.<br>Train the *exact* same system on a dataset from Senegal, and everyone will look African. <a href="https://t.co/jKbPyWYu4N">https://t.co/jKbPyWYu4N</a></p>&mdash; Yann LeCun (@ylecun) <a href="https://twitter.com/ylecun/status/1274782757907030016?ref_src=twsrc%5Etfw">June 21, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script></center>



LeCun wasn't wrong because in the case of that specific model, training the model on a dataset that contains faces of black people (as opposed to one that contains mainly white faces) would not have given rise to an output as absurd as that. But the upside of the godfather of modern AI getting dragged into a spat (albeit unfairly) has meant that more researchers will now be aware of the implications of their research.

Learning algorithms have inductive biases going beyond the biases in data too, sure. But if the data has a little bias, it is amplified by these systems, thereby causing high biases to be learnt by the model. Simply put, creating a 100% non-biased dataset is practically impossible. Any dataset picked by humans is cherry-picked and non-exhaustive. Our social cognitive biases result in inadvertent cherry-picking of data. This biased data, when fed to a data-variant model (a model whose decisions are heavily influenced by the data it sees) encodes these societal, racial, gender, cultural and politicial biases and bakes them into the ML model. 

These problems **exacerbate**, once they are applied to products.
A couple of years ago, Jacky Alciné [pointed out](https://twitter.com/jackyalcine/status/615329515909156865) that the image recognition algorithms in Google Photos were classifying his black friends as “gorillas.” Google apologised for the blunder and assured to resolve the issue. However, instead of coming up with a proper solution, it simply blocked the algorithm from identifying gorillas at all.

Google said it was “appalled” at the mistake, apologized to Alciné, and promised to fix the problem. But, as a [new report from Wired](https://www.wired.com/story/when-it-comes-to-gorillas-google-photos-remains-blind/) shows, nearly three years on and Google hasn’t really fixed anything. The company has simply blocked its image recognition algorithms from identifying gorillas altogether.

It might seem surprising that a company of Google's size was unable to come up with a solution to this. But this only goes to show how that training an algorithm to be consistent and fair isn't an easy proposition, not least when it is not trained and tested on a diverse set of categories.



<center><blockquote class="twitter-tweet" data-theme="dark"><p lang="en" dir="ltr">Facial recognition is the prime example. Amazon&#39;s Rekognition correctly identifies light-skinned males with an accuracy of 99% but the accuracy drops drastically for females, who are identified as men 19% of the time. It mistakes dark-skinned women for men 39% of the time.</p>&mdash; Karan (@IntrepidIndian) <a href="https://twitter.com/IntrepidIndian/status/1136048103008690176?ref_src=twsrc%5Etfw">June 4, 2019</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script></center>



[Another disastrous episode][https://www.npr.org/2020/06/24/882683463/the-computer-got-it-wrong-how-facial-recognition-led-to-a-false-arrest-in-michig] of facial recognition tech getting it terribly wrong came as recently as last week when a faulty facial recognition match led to a Michigan man’s arrest for a crime he did not commit. Recent studies by [M.I.T.](https://www.nytimes.com/2018/02/09/technology/facial-recognition-race-artificial-intelligence.html) and the [National Institute of Standards and Technology](https://www.nytimes.com/2019/12/19/technology/facial-recognition-bias.html), or NIST, found that even though face recognition works well on white men, the results are not good enough for other demographics, in part because of a lack of diversity in the images used to develop the underlying databases.


Problems of algorithmic bias are not limited to image/video tasks and they manifest themselves in language tasks too. 

[Language is always "situated"][https://web.stanford.edu/~mjkay/LifeOfLanguage.pdf], i.e., it depends on external references for its understanding and the receiver(s) must be in a position to resolve these references. This therefore means that the text used to train models carries latent information about the author and the situation, albeit to varying degrees.

Due to the situatedness of language, any language data set inevitably carries with it a demographic bias. For example, speech to text transcription tends to have higher error rates for African Americans, Arabs and South Asians as compared to Americans and Europeans.  Another example in this space is the gender biases in existing word embeddings (which are learned through a neural networks) that show females having a higher association with "less-cerebral" occupations while males tend to be associated with traditionally "more-cerebral" or higher paying occupations.



<center><blockquote class="twitter-tweet" data-conversation="none" data-theme="dark"><p lang="en" dir="ltr">For instance - in existing embeddings, it&#39;s observed that women &amp; men are associated with different professions, with men associated with leaderships roles and professions like doctor, programmer and women closer to professions like receptionist or nurse.</p>&mdash; Karan (@IntrepidIndian) <a href="https://twitter.com/IntrepidIndian/status/1134415294162538497?ref_src=twsrc%5Etfw">May 31, 2019</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script></center>



![image-20200627134204432](/Users/karanpraharaj/Library/Application Support/typora-user-images/image-20200627134204432.png)





While it is easy for ML Researchers to hold their hands up and absolve themselves of all responsibility, they are preparing the foundations of products of a lot of companies that are devoid of AI expertise. These companies, without the knowledge of fine-tuning and tweaking, use pre-trained models put out on the internet by ML researchers (like GloVe, BERT, ResNet, YOLO etc). Deploying these models without explicitly recalibrating them to account for demographic differences can thus lead to issues of exclusion and overgeneralisation of people along the way. The buck stops with the researchers who must own up responsibility for the other side of the coin.

It is also easy to blame the data and not the algorithm. (It reminds me of the Republican stance on the second amendment debate :  "Guns don't kill people, people kill people.") But what is indisputable is that more than the need to improve the data, it is  the algorithms that need to be more robust and less prone to being biased by the data. In the meantime, de-bias the data.

The guiding question for deployment of algorithms in the real world should always be “would a false answer be worse than no answer?”



























Potential counter-measures to demographic bias can be as simple as downsampling the over-represented group in the training data to even out the distribution.

. 



"Across the country, millions are protesting not just the actions of individual officers, but bias in the systems used to surveil communities and identify people for prosecution."

"Recent studies by [M.I.T.](https://www.nytimes.com/2018/02/09/technology/facial-recognition-race-artificial-intelligence.html) and the [National Institute of Standards and Technology](https://www.nytimes.com/2019/12/19/technology/facial-recognition-bias.html), or NIST, have found that while the technology works relatively well on white men, the results are less accurate for other demographics, in part because of a lack of diversity in the images used to develop the underlying databases." false positives

“I [strongly](https://www.aclu.org/blog/privacy-technology/surveillance-technologies/florida-using-facial-recognition-convict-people) [suspect](https://nymag.com/intelligencer/2019/11/the-future-of-facial-recognition-in-america.html) this is not the first case to misidentify someone to arrest them for a crime they didn’t commit. This is just the first time we know about it.”

"falsely identifying African-American and Asian faces 10 times to 100 times more than Caucasian faces.

“tightens the differences in accuracy between **different demographic cohorts**.”

"Researchers at the Massachusetts Institute of Technology [reported in January](https://www.nytimes.com/2019/01/24/technology/amazon-facial-technology-study.html) that facial recognition software marketed by Amazon **misidentified** darker-skinned women as men 31 percent of the time. Others have shown that algorithms used in facial recognition [return false matches at a higher rate for African-Americans](https://arxiv.org/pdf/1904.07325.pdf) than white people unless **explicitly** **recalibrated** for a black population — in which case their failure rate at finding positive matches for white people climbs. [That study](https://arxiv.org/pdf/1904.07325.pdf), posted in May by computer scientists at the Florida Institute of Technology and the University of Notre Dame, suggests that a single algorithm cannot be applied to both groups with equal accuracy."



https://twitter.com/acidflask/status/1274889347356069888

https://www.nytimes.com/2020/06/24/technology/facial-recognition-arrest.html?smid=tw-share

https://www.nytimes.com/2019/12/19/technology/facial-recognition-bias.html



https://twitter.com/hardmaru/status/1274521216192151552/photo/1

https://web.stanford.edu/~mjkay/LifeOfLanguage.pdf