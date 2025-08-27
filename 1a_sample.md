
---

## 例1:トランプの手紙

まずは、手紙画像を題材にします。従来型OCR **EasyOCR**　を比較に使います。あまり鮮明ではない写真画像から、文字解析を実施し結果を比較しました。

### **EasyOCR の結果**

```
It is & Great Honor for me to send you this letter in that it demonstrales the strength and commitment of our Trading Relationship, and the fact that the United Stales of America has agrced to continue working with Japan. despite having significant Trade Deficit with your grcat Country: Nevertheless; We have decided (0 move forward with you; but only with more balanced. and fair; TRADE. Therefore, we invile You to participate in the extraordinary Economy of the United States; the Number One Market in the World: by far: We have had years t0 discuss our Trading Relationship with Japan; and have concluded that we must move away from these longterm. and very persistent; Trade Delicits engendered by Japan"$ Tariff ; and Non TarifE, Policies und Trade Barriers. Our relationship has been; unfortunately: far from Reciprocal. Starting on August [. 2025. we will charge Japan a Tariff of only 25% on any and all Japanese products sent into the United States. scparale from all Sectoral Tarifs. Goods transshipped t0 evade & higher Tarift will be subject t0 that higher Tarifi: Please understand that the 25% number is far less than what is needed t0 eliminate the Trade Delicit disparity we have with your Country. As You are aware. there will be no Tarifrif FJapan. Or companies within your Country. decide t0 build or manufaclure product within the United States and,in fact we will do everything possible t0 get approvals quickly. professionally. and routinely In Olher words. in & maller of wceks
```
スペルミスが多数見受けられます。しかし従来型OCRは、文脈を理解して自動で修正することはできません。

### **Gemma3 の結果**

```
Question 1: Extract all the text from the image.
Answer: Here's the extracted text from the image:

"It is a Great Honor for me to send you this letter in that it demonstrates the strength and commitment of our Trading Relationship, and the fact that the United States of America has agreed to continue working with Japan, despite having a significant Trade Deficit with your great Country. Nevertheless, we have decided to move forward with you, but only with more balanced, and fair, TRADE. Therefore, we invite you to participate in the extraordinary Economy of the United States, the Number One Market in the World, by far. We have had years to discuss our Trading Relationship with Japan, and have concluded that we must move away from these long term, and very persistent, Trade Deficits engendered by Japan’s Tariff, and Non Tariff, Policies and Trade Barriers. Our relationship has been, unfortunately, far Reciprocal. Starting on August 1, 2025, we will charge Japan a Tariff of only 25% on any and all Japanese products sent into the United States, separate from all Sectoral Tariffs. Goods transhipped to evade a higher Tariff will be subject to that higher Tariff. Please understand that the 25% number is far less than what is needed to eliminate the Trade Deficit disparity we have with your Country. As you are aware, there will be no Tariff if Japan, or companies within your Country, decide to build or manufacture product within the United States and, in fact, we will do everything possible to get approvals quickly, professionally, and routinely – In other words, in a matter of weeks."

Question 2: Summarize the content.
Answer: Here's a summary of the letter's content:

The United States is initiating a new, reciprocal trade agreement with Japan to address a significant trade deficit. Starting August 1, 2025, the U.S. will impose a 25% tariff on all Japanese goods entering the country. This tariff is designed to level the playing field and prevent goods transshipped to avoid the tariff from being subject to it. The U.S. intends to encourage Japanese companies to build or manufacture products within the United States, and will provide support to facilitate this.
```

文脈に基づいた補正が入っているため、誤りが見当たりません。「要約」など追加タスクを予め指示することで同時に結果を取得可能です。

### **まとめ**

```
EasyOCR：文字起こしとしてかなり良く出来ていますが、明らかな誤りがそのまま残ります。
Gemma3：文字起こしとして誤りがなく高性能です。さらに要約など別のタスクも同時実行可能です。
```

---

