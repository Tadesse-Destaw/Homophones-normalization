# Imacts-of-homopnone-normalization
## All of the resources are publicly available in [Ethiopicmodels repository](https://github.com/uhh-lt/amharicmodels) 

### [Amharic Corpus](https://data.mendeley.com/datasets/dtywyf3sth/1) <br/>
### [Amharic Datasets](https://github.com/uhh-lt/ethiopicmodels/tree/master/am/data) <br/>
### [Preprocessing scripts and tools](https://github.com/uhh-lt/ethiopicmodels/tree/master/am/normalization) <br/>



## Amharic Tokenization and Segmentation

```
pip install amseg
from amseg.amharicSegmenter import AmharicSegmenter
sent_punct = []
word_punct = []
segmenter = AmharicSegmenter(sent_punct,word_punct)
words = segmenter.amharic_tokenizer("እአበበ በሶ በላ።")
sentences = segmenter.tokenize_sentence("እአበበ በሶ በላ። ከበደ ጆንያ፤ ተሸከመ፡!ለምን?")
```

Outputs
```
words = ['እአበበ', 'በሶ', 'በላ', '።']
sentences = ['እአበበ በሶ በላ።', 'ከበደ ጆንያ፤ ተሸከመ፡!', 'ለምን?']
```

## Romanization and Normalization
```
from amseg.amharicNormalizer import AmharicNormalizer as normalizer
from amseg.amharicRomanizer import AmharicRomanizer as romanizer
normalized = normalizer.normalize('ሑለት ሦስት')
romanized = romanizer.romanize('ሑለት ሦስት')
```

Outputs
```
normalized = 'ሁለት ሶስት'
romanized = 'ḥulat śosət'
```

## Citation

If this work helps with your research, please cite our paper:

```bibtex
@INPROCEEDINGS{belay-2021-impacts,
  author={Belay, Tadesse Destaw and Ayele, Abinew Ali and Gelaye, Getie and Yimam, Seid Muhie and Biemann, Chris},
  booktitle={2021 International Conference on Information and Communication Technology for Development for Africa (ICT4DA)}, 
  title={Impacts of Homophone Normalization on Semantic Models for Amharic}, 
  year={2021},
  pages={101-106},
  doi={10.1109/ICT4DA53266.2021.9672229}
}
```

```bibtex@Article{fi13110275,
AUTHOR = {Yimam, Seid Muhie and Ayele, Abinew Ali and Venkatesh, Gopalakrishnan and Gashaw, Ibrahim and Biemann, Chris},
TITLE = {Introducing Various Semantic Models for Amharic: Experimentation and Evaluation with Multiple Tasks and Datasets},
JOURNAL = {Future Internet},
VOLUME = {13},
YEAR = {2021},
NUMBER = {11},
ARTICLE-NUMBER = {275},
URL = {https://www.mdpi.com/1999-5903/13/11/275},
ISSN = {1999-5903},
DOI = {10.3390/fi13110275}
}
```
