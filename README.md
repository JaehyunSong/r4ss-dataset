# r4ss-dataset-1

## コードブック

### `F1`〜`F7`：回答者の社会経済要因変数

- `F1`：性別
   - 1：男性
   - 2：女性
- `F2`：年齢
- `F3`：最終学歴（在学中を含む）
   - 1：小学校・中学校
   - 2：高等学校
   - 3：専門学校・短期大学
   - 4：四年制大学・大学院
- `F4`：職業
   - 1：民間企業の正社員
   - 2：公務員
   - 3：自営業
   - 4：派遣社員
   - 5：農林漁業
   - 6：パート・アルバイト（フリーターを含む）
   - 7：専業主婦（夫）
   - 8：学生
   - 9：無職（リタイアを含む）
   - 10：その他
- `F5`：居住地の規模
   - 1：政令指定都市または東京23区
   - 2：政令指定都市以外の市
   - 3：町村
- `F6`：配偶者の有無
   - 1：いる
   - 2：いない
- `F7`：世帯収入（5が抜けていることに注意）
   - 1：200万円未満
   - 2：200万円以上、400万円未満
   - 3：400万円以上、600万円未満
   - 4：600万円以上、800万円未満
   - 6：800万円以上、1000万円未満
   - 7：1000万円以上
   - 8：わからない
   - 9：答えたくない

### `Q1`〜`Q1S2_11`：投票参加

- `Q1`：投票に参加したかどうか
   - 1：投票日当日に投票した。
   - 2：期日前投票/不在者投票をした。
   - 3：投票しようとしたが、行けなかった。
   - 4：棄権した。
   - 5：わからない/答えたくない。
- `Q1S1`：（投票に参加した人のみ）投票した政党
   - 1：A党の候補（与党）
   - 2：B党の候補（与党）
   - 3：C党の候補
   - 4：D党の候補（与党）
   - 5：E党の候補
   - 6：F党の候補
   - 7：G党の候補
   - 8：H党の候補
   - 9：その他の政党の候補
   - 10：無所属の候補
   - 11：覚えていない/答えたくない
- `Q1S2_1`〜`Q1S2_11`：（棄権した人のみ）棄権した理由
   - 複数選択可能な形式であり、選択したら`1`、選択しなかったら`NA`
   - `Q1S2_1`：現居住地に住民票を移していないから  
   - `Q1S2_2`：仕事・冠婚葬祭などで投票所に行く時間がなかったから  
   - `Q1S2_3`：体調不良だったから
   - `Q1S2_4`：旅行などで投票所に行く時間がなかったから  
   - `Q1S2_5`：投票所に行く時間はあったが面倒であったから
   - `Q1S2_6`：どの候補者・政党に投票しても大差がないから
   - `Q1S2_7`：投票日であることを忘れていた・知らなかったから  
   - `Q1S2_8`：その他
   - `Q1S2_9`：特に理由はない

### `Q2`〜`Q3`：党派性

- `Q2`：あなたはふだんどの政党を支持していますか。次の中から１つだけお選びください。選択肢の中に支持する政党がない場合は「その他」をお選びください。
   - 1：政党A
   - 2：政党B
   - 3：政党C
   - 4：政党D
   - 5：政党E
   - 6：政党F
   - 7：政党G
   - 8：政党H
   - 9：政党I
   - 10：その他の政党
   - 11：どの政党も支持しない
   - 12：答えたくない
- `Q2S1`：（支持政党がある場合）あなたはその政党の熱心な支持者ですか、それとも熱心な支持者ではありませんか。
   - 1：熱心な支持者
   - 2：熱心な支持者ではない
- `Q2S2`：（支持政党がない場合）あえて選ぶとすれば、どの政党を支持しますか。
   - 1：政党A
   - 2：政党B
   - 3：政党C
   - 4：政党D
   - 5：政党E
   - 6：政党F
   - 7：政党G
   - 8：政党H
   - 9：政党I
   - 10：その他の政党
   - 11：どの政党も支持しない
   - 12：答えたくない
- `Q3`：あなたが絶対に支持したくないと思う政党はありますか。  以下のうち、支持したくないと思う政党をすべてお選びください。
   - 12項目から複数選ぶ形式の設問であるため、本来12個のダミー変数であるはずだが、一つのcharacter型変数になっている。たとえば、`"1,,1,,,,,,,1,,"`の場合、1、3、10番目の項目を選択したことを意味する。
   - 1：政党A
   - 2：政党B
   - 3：政党C
   - 4：政党D
   - 5：政党E
   - 6：政党F
   - 7：政党G
   - 8：政党H
   - 9：政党I
   - 10：その他の政党
   - 11：特にそのような政党はない
   - 12：わからない

### `Q4_1`〜`Q4_4`：内的政治的有効性感覚

- `Q4_1`：選挙では大勢の人が投票するのだから、自分一人くらい投票しなくてもかまわない。 
- `Q4_2`：自分には政府を左右する力はない。 
- `Q4_3`：政治とか政府とかは、あまりに複雑なので、自分には何をやっているのか理解できないことがある。 
- `Q4_4`：「どちらかといえばそう思う」を選択ください。 
- 選択肢は共通
   - 1：そう思う
   - 2：どちらかといえばそう思う
   - 3：どちらともいえない
   - 4：どちらかといえばそう思わない 
   - 5：そう思わない

### `Q5_1`〜`Q5_3`：実験

**`Q5_1`：**今回の衆議院議員総選挙について伺いします。 あなたは今回の選挙期間中、以下のようなことをした/経験したことがありますか。該当する項目の「個数」を教えてください。

- 今回の選挙で自分の家族が立候補し、選挙運動を手伝った。
- テレビで政見放送を見た。
- 家族と今回の選挙について話した。

**選択肢**

- 1：0個（どれも当てはまらない）
- 2：1個
- 3：2個
- 4：3個（すべて当てはまる）

**`Q5_2`：**今回の衆議院議員総選挙について伺いします。 あなたは今回の選挙期間中、以下のようなことをした/経験したことがありますか。該当する項目の「個数」を教えてください。

- 今回の選挙で自分の家族が立候補し、選挙運動を手伝った。
- テレビで政見放送を見た。
- 家族と今回の選挙について話した。
- 今回の選挙で投票した。

**選択肢**

- 1：0個（どれも当てはまらない）
- 2：1個
- 3：2個
- 4：3個
- 5：4個（すべて当てはまる）

**`Q5_3`：**今回の衆議院議員総選挙について伺いします。 あなたは今回の選挙期間中、以下のようなことをした/経験したことがありますか。該当する項目の「個数」を教えてください。

- 今回の選挙で自分の家族が立候補し、選挙運動を手伝った。
- テレビで政見放送を見た。
- 家族と今回の選挙について話した。
- SNSで特定の候補者、政党の悪口を書き込んだ。

**選択肢**

- 1：0個（どれも当てはまらない）
- 2：1個
- 3：2個
- 4：3個
- 5：4個（すべて当てはまる）
