
---

## 例1:トランプの手紙

まずは、手紙画像を題材にします。従来型OCR **EasyOCR**　を比較に使います。あまり鮮明ではない写真画像から、文字解析を実施し結果を比較しました。

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
The United States is initiating a new, reciprocal trade agreement with Japan to address a significant trade deficit. Starting August 1, 2025, the U.S. will impose a 25% tariff on all Japanese goods entering the country. This tariff is designed to level the playing field and prevent goods transshipped to avoid the tariff from being subject to it. The U.S. intends to encourage Japanese companies to build or manufacture products within the United States, and will provide support to facilitate this.
```

文脈に基づいた補正が入っているため、誤りが見当たりません。「要約」など追加タスクを予め指示することで同時に追加タスク結果を取得可能です。

### **まとめ**

```
EasyOCR：文字起こしとしてはかなり良く出来ています。しかし明らかな誤りがあってもそのまま残ります。
Gemma3：文字起こしとして誤りがなく高性能です。さらに要約など別のタスクも同時実行可能です。
```

---

