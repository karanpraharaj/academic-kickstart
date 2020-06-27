---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "How Are Algorithms Biased?"
subtitle: "Algorithms reinforce human biases and stereotypes. This is dangerous."
summary: "Algorithms do what they're taught. Unfortunately some are inadvertently taught prejudices and unethical biases by societal patterns hidden in the  data."
authors: ["Karan Praharaj"]
tags: ["Artificial Intelligence","AI Fairness"]
categories: ["Computer Science"]
date: 2020-06-27T14:24:23+05:30
lastmod: 2020-06-27T14:24:23+05:30
featured: true
draft: false
comments: true
# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: ""
  preview_only: false

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []
---

After the end of the war, the Nuremberg trials laid bare the atrocities conducted in medical research by the Nazis. In the aftermath of the trials, the medical sciences established a set of rules — The Nuremberg Code — to control future experiments involving human subjects. The Nuremberg Code has influenced medical codes of ethics around the world, as has the exposure of experiments that had failed to follow it even three decades later, such as the infamous [Tuskegee syphilis experiment](https://en.wikipedia.org/wiki/Tuskegee_syphilis_experiment). 

The direct potential negative impact of AI experiments and applications on users isn't quite as inhumane as the Tuskegee and Nazi experimentations, but in the face of an overwhelming and growing body of evidence of algorithms being biased against certain demographic cohorts, it is important that a dialogue takes place sooner or later. AI systems can be biased based on who builds them, the way they are developed, and how they’re eventually deployed. This is known as algorithmic bias. 

While the data sciences have not developed a Nuremberg Code of their own yet, the social implications of research in artificial intelligence are starting to be addressed in some curricula. But even as the debates are starting to sprout up, what is still lacking is a discipline-wide discussion to grapple with questions of how to tackle societal and historical inequities that are reinforced by AI algorithms.

We are flawed creatures. Every single decision we make involves a certain kind of bias. However, algorithms haven't proven to be much better. Ideally, we would want our algorithms to make better-informed decisions devoid of biases so as to ensure better social justice, i.e., equal opportunities for individuals and groups (such as minorities) within society to access resources, have their voices heard, and be represented in society.

When these algorithms do the job of amplifying racial, social and gender inequality, instead of alleviating it; it becomes necessary to take stock of the ethical ramifications and potential malevolence of the technology.

This essay was motivated by two flashpoints : the racial inequality discussion that is now raging on worldwide, and Yann LeCun’s altercation with Timnit Gebru on Twitter which was caused due to a disagreement over a downsampled image of Barack Obama that was depixelated to a picture of a white man by a face upsampling machine learning (ML) model.



![Image](https://pbs.twimg.com/media/EbACRFtUYAAjNya?format=jpg&name=large)
The (rather explosive) argument was sparked by this tweet by LeCun where he says that the resulting face was that of a white man because of a bias in data that trained the algorithm. Gebru responded sharply that the harms of ML systems cannot be reduced to biased data. 

<center><blockquote class="twitter-tweet" data-theme="dark"><p lang="en" dir="ltr">ML systems are biased when data is biased.<br>This face upsampling system makes everyone look white because the network was pretrained on FlickFaceHQ, which mainly contains white people pics.<br>Train the *exact* same system on a dataset from Senegal, and everyone will look African. <a href="https://t.co/jKbPyWYu4N">https://t.co/jKbPyWYu4N</a></p>&mdash; Yann LeCun (@ylecun) <a href="https://twitter.com/ylecun/status/1274782757907030016?ref_src=twsrc%5Etfw">June 21, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script></center>

<br/>

LeCun wasn't wrong because in the case of that specific model, training the model on a dataset that contains faces of black people (as opposed to one that contains mainly white faces) would not have given rise to an output as absurd as that. But the upside of the godfather of modern AI getting dragged into a spat (albeit unfairly) has meant that more researchers will now be aware of the implications of their research.

The misunderstanding clearly seems to emanate from the interpretation of the word "bias" - which in any discussion about the social impact of ML/AI seems to get crushed under the burden of its own weight. 

As Sebastian Raschka puts it, "the term **bias** in ML is heavily overloaded". It has multiple senses that can all be mistaken for each other and a lot of gaps in communication could be covered by just being a little more precise.

​	(1) **bias** (as in mathematical **bias** unit) 
​	(2) "Fairness" **bias** (also called societal **bias**) 
​	(3) ML **bias** (also known as inductive **bias**, which is dependent on decisions taken to build the model.) 
​	(4) **bias**-variance decomposition of a loss function  
​	(5) Dataset **bias** (usually causing 2)

Never mind Obama, the model even depixelized a **dog's face** to a caucasian man's. It sure loves the white man.

<br/>

<center><blockquote class="twitter-tweet" data-theme="dark"><p lang="en" dir="ltr">This is how that depixelizing algorithm reconstructed my dog, Tank <a href="https://t.co/XHgdNwRmXy">pic.twitter.com/XHgdNwRmXy</a></p>&mdash; Jiahao Chen @ 🏡🗽 (@acidflask) <a href="https://twitter.com/acidflask/status/1274889347356069888?ref_src=twsrc%5Etfw">June 22, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script></center>

<br/>

Learning algorithms have inductive biases going beyond the biases in data too, sure. But if the data has a little bias, it is amplified by these systems, thereby causing high biases to be learnt by the model. Simply put, creating a 100% non-biased dataset is practically impossible. Any dataset picked by humans is cherry-picked and non-exhaustive. Our social cognitive biases result in inadvertent cherry-picking of data. This biased data, when fed to a data-variant model (a model whose decisions are heavily influenced by the data it sees) encodes these societal, racial, gender, cultural and politicial biases and bakes them into the ML model. 

These problems are exacerbated, once they are applied to products.
A couple of years ago, Jacky Alciné [pointed out](https://twitter.com/jackyalcine/status/615329515909156865) that the image recognition algorithms in Google Photos were classifying his black friends as “gorillas.” Google apologised for the blunder and assured to resolve the issue. However, instead of coming up with a proper solution, it simply blocked the algorithm from identifying gorillas at all.

It might seem surprising that a company of Google's size was unable to come up with a solution to this. But this only goes to show how that training an algorithm to be consistent and fair isn't an easy proposition, not least when it is not trained and tested on a diverse set of categories.



<center><blockquote class="twitter-tweet" data-theme="dark"><p lang="en" dir="ltr">Facial recognition is the prime example. Amazon&#39;s Rekognition correctly identifies light-skinned males with an accuracy of 99% but the accuracy drops drastically for females, who are identified as men 19% of the time. It mistakes dark-skinned women for men 39% of the time.</p>&mdash; Karan (@IntrepidIndian) <a href="https://twitter.com/IntrepidIndian/status/1136048103008690176?ref_src=twsrc%5Etfw">June 4, 2019</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script></center>

<br/>

 of facial recognition tech getting it terribly wrong came as recently as last week when a faulty facial recognition match led to a Michigan man’s arrest for a crime he did not commit. Recent studies by [M.I.T.](https://www.nytimes.com/2018/02/09/technology/facial-recognition-race-artificial-intelligence.html) and the [National Institute of Standards and Technology](https://www.nytimes.com/2019/12/19/technology/facial-recognition-bias.html), or NIST, found that even though face recognition works well on white men, the results are not good enough for other demographics (the misidentification ratio can be more than 10 times worse), in part because of a lack of diversity in the images used to develop the underlying databases.

Problems of algorithmic bias are not limited to image/video tasks and they manifest themselves in language tasks too. 

[Language is always "situated"](https://web.stanford.edu/~mjkay/LifeOfLanguage.pdf), i.e., it depends on external references for its understanding and the receiver(s) must be in a position to resolve these references. This therefore means that the text used to train models carries latent information about the author and the situation, albeit to varying degrees.

Due to the situatedness of language, any language data set inevitably carries with it a demographic bias. For example, speech to text transcription tends to have higher error rates for African Americans, Arabs and South Asians as compared to Americans and Europeans.  Another example in this space is the gender biases in existing word embeddings (which are learned through a neural networks) that show females having a higher association with "less-cerebral" occupations while males tend to be associated with traditionally "more-cerebral" or higher paying occupations.



<center><blockquote class="twitter-tweet" data-conversation="none" data-theme="dark"><p lang="en" dir="ltr">For instance - in existing embeddings, it&#39;s observed that women &amp; men are associated with different professions, with men associated with leaderships roles and professions like doctor, programmer and women closer to professions like receptionist or nurse.</p>&mdash; Karan (@IntrepidIndian) <a href="https://twitter.com/IntrepidIndian/status/1134415294162538497?ref_src=twsrc%5Etfw">May 31, 2019</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script></center>



<img src = "tablefair.png" alt="fair" />



While it is easy for ML Researchers to hold their hands up and absolve themselves of all responsibility, it is imperative for them to acknowledge that they—knowingly or otherwise—build the base layer of AI products for a lot of companies that are devoid of AI expertise. These companies, without the knowledge of fine-tuning and tweaking models, use pre-trained models, as they are, put out on the internet by ML researchers (like GloVe, BERT, ResNet, YOLO etc).

Deploying these models without explicitly recalibrating them to account for demographic differences can thus lead to issues of exclusion and overgeneralisation of people along the way. The buck stops with the researchers who must own up responsibility for the other side of the coin.

It is also easy to blame the data and not the algorithm. (It reminds me of the Republican stance on the second amendment debate : “Guns don’t kill people, people kill people.”) But what is indisputable is that more than we need to improve the data, it is the algorithms that need to be made more robust and less prone to being biased by the data. This needs to be a responsibility for anyone who does research. In the meantime, de-bias the data.

The guiding question for deployment of algorithms in the real world should always be “would a false answer be worse than no answer?”

&nbsp;



-----

&nbsp;

## 

## References

&nbsp;



1) [Facial Recognition Is Accurate, if You’re a White Guy]([)https://www.nytimes.com/2018/02/09/technology/facial-recognition-race-artificial-intelligence.html) by Steve Lohr

2) Krishnapriya, KS., Vangara, K., King, M., Albiero, V., Bowyer, K. [Characterizing the Variability in Face Recognition Accuracy Relative to Race](https://arxiv.org/pdf/1904.07325.pdf) in *The IEEE Conference on Computer Vision and Pattern Recognition (CVPR) Workshops, June 2019.*

3) [Life of Language](https://web.stanford.edu/~mjkay/LifeOfLanguage.pdf) by Martin Kay, Stanford University

4) [Text Embedding Models Contain Bias. Here's Why That Matters.](https://developers.googleblog.com/2018/04/text-embedding-models-contain-bias.html) by Ben Packer, Yoni Halpern, Mario Guajardo-Céspedes & Margaret Mitchell, Google AI

5) Bolukbasi, T., Chang, KW., Zou, J., Saligrama, V., Kalai, A. [Man is to Computer Programmer as Woman is to Homemaker? Debiasing Word Embeddings](http://papers.nips.cc/paper/6228-man-is-to-computer-programmer-as-woman-is-to-homemaker-d) in *Advances in Neural Information Processing Systems 29, 2016.*

&nbsp;

## 



