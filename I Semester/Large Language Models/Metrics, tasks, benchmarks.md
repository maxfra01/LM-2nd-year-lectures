# Metrics

### Perplexity

Perplexity is a metric that quantifies **how uncertain the model is in predicting the (correct) next word**.
- High perplexity: the model is uncertain about the “correct” next word
- Low perplexity: the model is certain about the “correct” next word
For example if we are predicting the next word and the probability of a word is $p(\text{cat})=0.25$ it's as if the model is confused between 4 words.

The perplexity over a sentence $w_{1},w_{2}\dots w_{N}$ tokens is computed as follows:
$$
\text{PPL} = \exp\left( -\frac{1}{N} \sum_{i}^N \log(p(w_{i}|w_{< i})) \right)
$$
If the model is **always confident**, then we have $\text{PPL}=1$.

![[Pasted image 20241016123517.png]]

### BLEU

BLEU (Bilingual Evaluation Understudy) is a metric used to evaluate a generated sequence, when a reference one is available.
If a model generates a very short sequence (w.r.t. the reference), it is easier to obtain a larger precision!