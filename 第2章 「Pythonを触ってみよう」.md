# 第2章　「Pythonを触ってみよう」

## LESSON 3

**実行内容**

    書式：print()
- print(1+1)
- print(100-1)
- print(2*5)
- print(10/5)
- print(6//4)
- print(6%4)

**出力結果**

![alt text](screenshots/LESSON03.png)
- 正しい計算の結果が出力された

| 記号 | 計算 |
| ---- | ----- |
| + | 足し算 |
| - | 引き算 |
| * | 掛け算 |
| / | 割り算 |
| // | 割り算（小数部分を切り捨て） |
| % | 割り算の余り |

## LESSON 4

**実行内容**
- print(フタバ)
- print("フタバ")
- print("Hello")
- print("答えは", 10+20)
- print("こんにちは')
- print('私は"おはよう"といった。')

**出力結果**

![alt text](screenshots/LESSON04.png)
- 文字列を表示するには、「'（シングルクォーテーション）」か「"（ダブルクォーテーション）」で囲む
- 囲まれていない場合、もしくは両側で違う記号の場合は、エラーが表示される
- 同じ記号で囲まれていると文字列として認識されるため、2種類を同時に使うこともできる

## LESSON 5

**あいさつプログラム**

①新規ファイルを作る（[File]メニュー→[New File]を選択）

②プログラムを入力するウィンドウが表示される

③プログラムを入力する

    print("こんにちは、フタバさん。")
    print("今日はいい天気ですね。")

④ファイルを保存する（[File]メニュー→[Save]を選択）

⑤ファイル名に拡張子「.py」をつける

⑥[Run]メニュー→[Run Module]を選択で、挨拶を表示してくれる

![alt text](screenshots/LESSON05-1.png)

**おみくじプログラム**

①新規ファイルを作り、プログラムを入力する

    import random
    kuji = ["大吉", "中吉", "小吉", "凶"]
    print(random.choice(kuji))

②ファイルを保存する

③プログラムを実行する（実行するたびに違う結果が表示される）

![alt text](screenshots/LESSON05-2.png)

**BMI値計算プログラム**

①新規ファイルを作り、プログラムを入力する

    h = float(input("身長何㎝ですか？"))/100.0
    w = float(input("体重何㎏ですか？"))
    bmi = w / (h * h)
    print("あなたのBMI値は、",bmi,"です。")

②ファイルを保存する

③プログラムを実行する
- まず「身長何㎝ですか？」と聞いてくるので、身長を入力しEnter
- 次に「体重何㎏ですか？」と聞いてくるので、体重を入力しEnter
- BMI値を計算して表示してくれる

![alt text](screenshots/LESSON05-3.png)

## LESSON 6

タートルグラフィックス：カメをまっすぐ進めて「直線」を表示するプログラム

**カメで直線を描く**

プログラムを入力して実行する

    from turtle import *     
    shape("turtle")
    forward(100)
    done()

![alt text](screenshots/LESSON06-1.png)

- 左から右にカメが動いた
- forward(100)は、前に100進めという意味

**正方形を描く**

プログラムを入力して実行する

「まっすぐ進んで、左に90度曲がる」という行動を4回繰り返して、正方形を描く

    from turtle import *
    shape("turtle')
    for i in range(4):
       forward(100)
       left(90)
    done()

![alt text](screenshots/LESSON06-2.png)

- スペースはインデントという大事な意味があるものだから取ってはいけない（先頭にスペースがあってもエラーになる）

**カラフルな星を描く**

プログラムを入力して実行する

「まっすぐ進んで、左に144度曲がる」という行動を5回繰り返して、星を描く

    from turtle import *
    shape("turtle")
    col = ["orange","limegreen","gold","plum","tomato"]
    for i in range(5):
        color(col[i])
        forward(200)
        left(144)
    done()

![alt text](screenshots/LESSON06-3.png)

- プログラム4行目は、「以下の3行を5回繰り返すこと」を意味している

**カラフルな花を描く**

プログラムを入力して実行する

「半径100の円を描いて、左に72度曲がる」（星形のプログラムの6行目と7行目だけを修正）

    from turtle import *
    shape("turtle")
    col = ["orange","limegreen","gold","plum","tomato"]
    for i in range(5):
        color(col[i])
        circle(100)
        left(72)
    done()

![alt text](screenshots/LESSON06-4.png)

- 半径100の円を描くこと、左に72度曲がることにしただけで、5つの円ができ、花の形になった

**もっと複雑な絵を見てみよう**

①[Help]メニュー→[Turtle Demo]を選択すると、タートルのデモ画面が表示される

②デモ画面の[Examples]メニューから例を選択で、左側にプログラムが表示され、[START]ボタンをクリックで、自動で絵が表示される

