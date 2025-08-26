
---

## 例1: Trump’s Letter

まずは、手紙画像を題材にします。従来型OCR **EasyOCR**　を比較に使います。同一の画像（参照）から、解析を実施し、結果を比較しました。

### **EasyOCR の結果**

全文抽出
```
It is & Great Honor for me to send you this letter in that it demonstrales the strength and commitment of our Trading Relationship, and the fact that the United Stales of America has agrced to continue working with Japan. despite having significant Trade Deficit with your grcat Country:
```
スペルミスも時折見受けられます。しかし従来型OCRは、文脈を理解して自動で修正することはできません。

### **Gemma3 の結果**

* 全文抽出
```
It is a great honor for me to send you this letter in that it demonstrates the strength and commitment of our Trading Relationship, and in that the United States of America has agreed to continue working with Japan, despite having a significant Trade Deficit with your great Country.
```

* 要約作成
```
The United States is urging Japan to maintain its trade relationship, despite a significant trade deficit. The U.S. proposes a 25% tariff on Japanese goods entering the U.S., arguing this is necessary to correct Japan’s tariffs and trade barriers which are causing a major trade deficit for the United States. The U.S. emphasizes the need for a swift and professional agreement to resolve this issue.
```

文脈に基づいた補正が入っているため、誤りがほとんど目立ちません。「要約」など別のタスクを指示することで同時に結果が取得可能です。

### **まとめ**

```
EasyOCR =「文字起こしとしては高性能です、しかし文脈理解は出来ず誤りはそのまま残ります」
Gemma3 = 「文字起こししながら、文脈を理解し誤りを補正できます。さらに要約など別のタスクに対応可能です」
```

従来型OCRとAI OCRを比較してみました。AI OCRの有用性がお分かりいただけたかと思います。

---

