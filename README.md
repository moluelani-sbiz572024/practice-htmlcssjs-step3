# HTML/CSS/JS 練習問題 - STEP3

## 概要

1. STEP2で改造したWebページを以下の仕様に基づいて改造する
1. ワイヤフレームと完成スクショを提供する
    1. assetsディレクトリ内のリソース
1. hintsディレクトリに提供ソースコードを格納
    1. sample.app.js：クライアントアプリケーション
    1. sample.lib.js：クライアントアプリケーションが利用する共通処理
1. 作成物は次の通り
    1. HTML = sample.html
    1. CSS = sample.css
    1. JavaScript = sample.app.js, sample.lib.js

<br>

## 仕様

### Webページ

1. 左ボックス
    1. ガイドテキストのdivタグにid属性を追加
    1. ボタンclass属性にbtn-sendを追加
1. 右ボックス
    1. 結果メッセージのdivタグにid属性が設定されているかを確認する

### JavaScript

1. hintsディレクトリ「sample.lib.js」に、次の仕様を満足する内容を実装する
    1. 入力データを保持するクラス「SendData」を作成する
    1. 各入力エリア参照情報を内蔵するオブジェクト「RequestData」を作成する
    1. 結果出力エリアのラベル情報を内蔵するオブジェクト「ResultLabel」を作成する
    1. 結果出力エリア情報を内蔵するオブジェクト「ResultData」を作成する
    1. ボタン情報オブジェクト「ActioButton」を作成する
1. hintsディレクトリ「sample.app.js」に、次の仕様を満足する内容を実装する
    1. dataプロパティに入力データ格納クラスを設定する
    1. guideプロパティに該当オブジェクトを設定する
    1. mesgプロパティに該当オブジェクトを設定する
    1. lblプロパティに該当オブジェクトを設定する
    1. outプロパティに該当オブジェクトを設定する
    1. btnプロパティに該当オブジェクトを設定する
    1. メソッドdoSetupに次のイベントリスナーを実装する
        1. 名前入力フィールドバインド（入力値をクラスSendDataに格納する）
        1. メール入力フィールドバインド
        1. 年齢入力フィールドバインド
        1. アクションボタンイベントハンドラー
    1. メソッドdoSendの実装
        1. 入力チェック
            1. 全ての項目が入力されていること
            1. 未入力項目を検知したらエラーメッセージをガイドに表示する
            1. エラーメッセージはcrimsonで表示する
        1. 入力チェックが通過したらデータを全て右ボックスの結果表示エリアに出力する
        1. 結果表示ラベルを設定する
            1. 送信された名前
            1. 送信されたメール
            1. 送信された年齢
        1. 結果メッセージを右ボックスに表示する
        1. 結果メッセージはsteelblueで表示する
        1. 入力フォームを全てクリアする

<br>

### ワイヤーフレームとスクショ

![ワイヤーフレーム](/assets/step3-01.png)

![画面スクショ](/assets/step3-02.jpg)

<br>

### 提供ソースコード

sample.app.js

![sample.app.js](/assets/step3-03.png)

samole.lib.js
- オブジェクト MessageArea、Utilの内容は[コード](/blob/main/hints/sample.lib.js)確認して下さい

![sample.lib.js](/assets/step3-04.png)
