# Dataset Introduction
This is the Two-hop Factual Reasoning for Knowledge Neurons (TFRKN) dataset from the paper [Unveiling Factual Recall Behaviors of Large Language Models through Knowledge Neurons](https://arxiv.org/abs/2408.03247).
## Data format
The dataset is saved as a list of dicts, each of which represents a data instance. An example in `TFRKN` is shown below.

```
{
  "case_id": 3,
  'two_hop': 'What is the notable work written by the author of "Paradiso"?',
  'fact1_query': [
                  'Who authored Paradiso?',
                  'To whom is the creation of Paradiso attributed?',
                  'Whose mind conceived Paradiso?',
                  'Who penned the words that comprise Paradiso?',
                  'Which literary genius brought Paradiso into existence?',
                  'From whose imagination did Paradiso spring?',
                  'Who crafted the narrative world of Paradiso?'
  ],
 'fact1_ans': 'Dante Alighieri',
 'fact2_query': [
                "What is Dante Alighieri's most famous work?",
                'Which work brought Dante Alighieri the most recognition?',
                'For which work is Dante Alighieri best known?',
                "What is the title of Dante Alighieri's magnum opus?",
                "Which literary creation stands as Dante Alighieri's crowning achievement?",
                'What is the name of the work that immortalized Dante Alighieri?'
  ],
 'fact2_ans': 'The Divine Comedy',
 'two_hop_id': [
              ['Q2713307', 'P50', 'Q1067'],
              ['Q1067', 'P800', 'Q40185']
  ],
 'two_hop_label': [
              ['Paradiso', 'author', 'Dante Alighieri'],
              ['Dante Alighieri', 'notable work', 'The Divine Comedy']
  ]
}
```
* `two-hop`: two-hop factual questions
* `fact1_query`: natural questions for the first-hop fact triplet
* `fact1_ans`: answers to natural questions for the first-hop fact triplet
* `fact2_query`: natural questions for the second-hop fact triplet
* `fact2_ans`: answers to natural questions for the second-hop fact triplet
* `two_hop_id`: the corresponding list of `(s, r_1, o_1)` and `(o_1, r_2, o_3)` fact triples
* `two_hop_label`: the corresponding labels for `(s, r_1, o_1)` and `(o_1, r_2, o_3)` fact triples

