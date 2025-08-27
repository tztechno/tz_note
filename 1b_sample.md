

---

### 例2: 車のナンバープレート画像

次に、車のナンバープレートを題材にします。
ナンバープレートの写った車およびその周囲が映り込んだ写真を用いて
従来型OCR **EasyOCR** と **Gemma3** の結果を比較しました。

* **EasyOCR の結果**

```
LICENSE PLATE OCR RESULTS
----------------------------------------
Detected text 1: 'Cjpiana' (Confidence: 0.45)
Detected text 2: 'Ibi' (Confidence: 0.12)
Detected text 3: ''1BY3737' (Confidence: 0.50)
Detected text 4: ''HRS' (Confidence: 0.70)

Full license plate text: 'Cjpiana Ibi '1BY3737 'HRS'
```
* Number Plate文字抽出はかなり出来ているが若干誤りがある。Number Plate以外の文字も抽出してしまう。
* Number Plateを正確に読み取るには、目視による修正が必須。

* **Gemma3 の結果**

```
Question 1: What is this?
----------------------------------------
Answer: This image shows a white Suzuki Swift car stuck in traffic. The sign on the left reads "Hathi" which means "Elephant" in Hindi, a common sign used to warn drivers of potential animal crossings, particularly in areas with wildlife.

Question 2: What is the number of the licence plate?
----------------------------------------
Answer: The license plate number is **HR51BV3737**.
```

* Number Plate情報を正しく読み取った。
* 画像から車の車種、周囲の道路状況まで推定した。

---

まとめると、

* EasyOCR =「ナンバープレートの文字などをある程度抽出できるが不正確」
* Gemma3 = 「ナンバープレート文字を正確に読み取る。加えて、車種、道路の周辺状況までを把握し説明可能」

つまり、AI OCR は「文字の認識」にとどまらず、**画像全体の意味理解に基づいた説明**を生成できることが分かります。

---

