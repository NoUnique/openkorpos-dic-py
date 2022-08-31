# openkorpos-dic-py

This is a version of [OpenKorPOS-dic](https://github.com/openkorpos/model-mecab) packaged for use in Python with 
[pymecab-ko](https://github.com/NoUnique/pymecab-ko).

OpenKorPOS-dic is developed by [Sangwhan Moon](mailto:sangwhan@iki.fi), [Won Ik Cho](mailto:wicho@hi.snu.ac.kr), [Hyejoo Han](mailto:hyejoo@oddconcepts.kr), [Naoaki Okazaki](mailto:okazaki@c.titech.ac.jp), and [Nam Soo Kim](mailto:nkim@snu.ac.kr) for a comparison target of a new method claimed in [their paper](https://github.com/openkorpos/openkorpos/raw/main/openkorpos.pdf)

## Usage

To install:

```bash
pip install openkorpos-dic
```

To initialize with pymecab-ko:

```python
>>> import mecab_ko as MeCab
>>> import openkorpos_dic
>>> tagger = MeCab.Tagger(openkorpos_dic.MECAB_ARGS)
>>> print(tagger.parse("아버지가방에들어가신다"))

아버지  NNG,*,F,아버지,*,*,*,*
가      JKS,*,F,가,*,*,*,*
방      NNG,*,T,방,*,*,*,*
에      JKB,*,F,에,*,*,*,*
들어가  VV,*,F,들어가,*,*,*,*
신다    EP+EF+VCP,*,F,신다,Inflect,EP,VCP,시/EP/*+ᆫ다/EF/*+이/VCP/*
EOS
```

## Version

- 08/31/2022:  
  The version of the original dictionary is not defined yet.  
  Therefore, I defined the version like the version of other mecab compatible dictionaries. And I added the commit hash id of the original repository to make it distinguishable.
  ```python
  >>> openkorpos_dic.VERSION
  '1.0.0-20220620-c72cb7d'
  ```

# License

OpenKorPOS-dic is available under the GPL-2.0 license, [see here](https://github.com/openkorpos/model-mecab/blob/main/LICENSE).  