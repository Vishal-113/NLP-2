###NAME; Vishal Vusnagiri
###Student Id; 7000763454
###Course; Natural Language Processing

## 📚 Bigram Language Model Implementation

This project implements a simple Bigram Language Model using Maximum Likelihood Estimation (MLE) for estimating bigram probabilities. The model is trained on a small corpus and can compute the probability of any input sentence. It also compares which of two test sentences is more probable under the trained model.

---

## 📝 Project Description

Given a training corpus:

```
<s> I love NLP </s>  
<s> I love deep learning </s>  
<s> deep learning is fun </s>
```

The system:

* Computes unigram and bigram counts.
* Estimates bigram probabilities using **MLE**.
* Implements a function to calculate the probability of a sentence using the trained model.
* Tests the model on:

  * `<s> I love NLP </s>`
  * `<s> I love deep learning </s>`
* Outputs which sentence is more probable and **why** (based on computed probabilities).

---

## 📂 Files

* `bigram_model.py`: Main implementation script.
* `README.md`: This documentation file.

---

## ⚙️ Requirements

This project runs on Python 3.6+. No external libraries are required.

---

## 🚀 How to Run

1. Clone or download this repository.
2. Run the script from the command line:

   ```bash
   python bigram_model.py
   ```

---

## 🔍 Output

The program prints:

* Unigram and bigram counts.
* Bigram probabilities (MLE).
* Sentence probabilities for:

  * `<s> I love NLP </s>`
  * `<s> I love deep learning </s>`
* The sentence that is more probable and **why**, based on the calculated bigram probabilities.

---

## 🧠 Notes

* Probabilities are calculated using:

  ```
  P(w2 | w1) = count(w1 w2) / count(w1)
  ```
* The model uses `<s>` and `</s>` to mark sentence boundaries.
* This is a basic implementation and does **not** handle smoothing or unknown words.

---

## 📈 Sample Output

```
Unigram Counts: {'<s>': 3, 'I': 2, 'love': 2, 'NLP': 1, '</s>': 3, 'deep': 2, 'learning': 2, 'is': 1, 'fun': 1}
Bigram Counts: {('<s>', 'I'): 2, ('I', 'love'): 2, ('love', 'NLP'): 1, ('NLP', '</s>'): 1, ('love', 'deep'): 1, ('deep', 'learning'): 2, ('learning', '</s>'): 1, ('learning', 'is'): 1, ('is', 'fun'): 1, ('fun', '</s>'): 1}

P(<s> I love NLP </s>) = 2/3 * 2/2 * 1/2 * 1/1 = 0.3333
P(<s> I love deep learning </s>) = 2/3 * 2/2 * 1/2 * 2/2 * 1/2 = 0.1667

Most probable sentence: <s> I love NLP </s>
```

---

## 🤝 Acknowledgements

This project is based on coursework and lecture materials from **Natural Language Processing** classes involving n-gram language modeling.

