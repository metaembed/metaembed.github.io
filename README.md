## Why Meta Embeddings?

Representing the meanings of individual words is arguably one of the fundamental tasks in Natural Language Processing (NLP).
If we can accurately represent the meanings of individual words then we can use those representations to compose the meanings
of larger lexical units such as phrases, sentences, paragraphs or entire documents for that matter.

Fortunately, we live in era where numerous different approaches have been proposed in the NLP community to learn word representations (embeddings).
However, word embeddings learnt using different methods have reported different degrees of performance on different tasks.
Simply put, there is no one silver bullet when it comes to word embeddings that solves all NLP problems.
More importantly the quest for better word embeddings continues and new methods for learning word embeddings that capture various aspects
of word semantics are being proposed.

From the NLP practitioners point of view however, this plethora of choices can become a bit of a problem.
How do you pick the best word embeddings to train your NLP application? 
Of course you could try them all and pick the best one. But that is often not a solution because of the time constrants
or sheer numnber of different word embedding methods available. 

Meta embedding comes to your help!

Instead of picking one word embedding why not use them *all!*
At least use few good ones all at once thereby covering various aspects of word semantics and a larger vocabulary. 

The purpose of this web site is to share information about such meta embedding learning methods, publications and pre-trained meta embeddings.

## What makes Meta Embedding Learning Different from Word Embedding Learning?

Meta embedding learning is defined as the process of producing a single (meta) word embedding from a given set of *pre-trained* input (source) word embeddings.

There are several key points in this definition that makes meta embedding learning problem different from that of learning source embeddings.

* Note that we do not re-train any of the source word embedding learning algorithms during meta embedding. In fact, we do *not* even assume the availability of the implementations of the methods that were used to produce the source word embeddings. We simply use pre-trained source word embeddings. This makes the meta embedding learning algorithms independent of the source word embedding learning algorithms, which is great because we can use the same meta embedding learning algorithm to meta embed any given set of word embeddings.

* We do *not* assume the availability of the text corpora that were used to train the source word embeddings. In fact, no text corpus is ever used during the meta embedding learning! This is attractive because sometimes all what you get with source word embeddings is the pre-trained vectors and not the language resources such as text corpora or dictionaries that were used to train those source word embeddings. This could be because, for example, the language resources are proprietery and the authors of the source embedding learning algorithms are not allowed to release the language resources they used. It also makes the meta embedding learning algorithms attractive because they do not require language resources during training. Moreover, even if you had access to the language resources, it might be computationally costly to re-train the source word embedding learning methods on those language resources by yourself, especially if you do not have access to the hardware such as GPU clusters.

## Meta Embedding Learning Methods and Pre-trained Meta Embeddings

Here is a list of papers that propose methods for learning meta embeddings. Where pre-trained meta embeddings produced using those methods are publicly available we provide those links too. If you have a paper on meta embedding learning and would like to get it listed here please let me know.

* James O'Neill and Danushka Bollegala: *Semi-Supervised Multi-Task Word Embeddings* arXiv, 2018. [[arXiv]](https://arxiv.org/abs/1809.05886)

* Cong Bao and Danushka Bollegala: *Learning Word Meta-Embeddings by Autoencoding* Proc. of the 27th International Conference on Computational Linguistics (COLING), pp. 1650-1661, 2018. [[PDF]](http://danushka.net/papers/aeme.pdf) [[CODE]](https://github.com/LivNLP/AEME)

* Danushka Bollegala, Kohei Hayashi and Ken-ichi Kawarabayashi: Think Globally, Embed Locally -- Locally Linear Meta-Embedding of Words, Proc. of International Joint Conference in Artificial Intelligence and European Conference on Artificial Intelligence (IJCAI-ECAI), pp. 3970-3976, 2018. [[PDF]](https://www.ijcai.org/proceedings/2018/0552.pdf) [[CODE]](https://github.com/LivNLP/LLE-MetaEmbed)

* Joshua Coates and Danushka Bollegala: *Frustratingly Easy Meta-Embedding -- Computing Meta-Embeddings by Averaging Source Word Embeddings* Proc. of the 16th Annual Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies (NAACL-HLT), pp. 194-198, 2018. [[PDF]](http://aclweb.org/anthology/N18-2031)

This site is maintained by <a href="https://danushka.net">Danushka Bollegala</a>

