# Cleaning-for-folder
特定フォルダ下の不要ファイルをクリーニングするWindows向けのソフト<BR>
<B>クリーニング処理はプログラムを実行した時にのみ実行されます。</B><BR>
<B>自動に実行したい場合は「使い方3」の手順で設定し、Windowsの起動時に実行してください</B><BR>

## セットアップ
プログラムの本体（f_cleaning.exe）を適当なフォルダにコピーしてください。<BR>
※コピー先のフォルダはクリーニング対象とするフォルダとは別のフォルダを指定してください。<BR>
<BR>
例）<BR>
クリーニングの対象： c:￥Users￥USER￥Downloads<BR>
プログラムのコピー先： c:￥tool￥f_cleaning.exe<BR>

## 使い方1 （画面からクリーニングする）
f_cleaning.exeを実行すると画面が表示されます。<BR>
![image](https://user-images.githubusercontent.com/54971000/210971248-ececdce1-b16f-450c-8390-d2617b0bb291.png)<BR>
①「対象のフォルダー」にクリーニング対象のフォルダを指定します<BR>
②「処理条件」に削除するファイルの条件を指定します<BR>
　ファイル作成日：削除の条件をファイルの作成日を起点にする<BR>
　ファイル更新日：削除の条件をファイルの更新日を起点にする<BR>
　ファイル参照日：削除の条件をファイルの最終アクセス日を起点にする<BR>
　経過日数　　　：上記の起点から経過した日数を削除対象とする<BR>
③「設定＆実行」ボタンを押すと対象フォルダ配下で条件に一致するファイルが削除されます。（なお、サブフォルダも対象となります）<BR>
※設定だけ行う場合は「設定」ボタンを押してください。<BR>
<BR>

## 使い方2 （画面を使わずにコマンドでクリーニングする）
このプログラムの起動オプションに "run"を指定すると、画面を表示せずに設定に従ってクリーニングを実行します。<BR>
<BR>
①使い方1を元に画面から「対象フォルダー」と「処理条件」を指定して、「設定」ボタンを押して設定を行ってください。<BR>
※設定後は「終了」ボタンで画面を閉じてください。<BR>
②設定が完了した後は、オプションにrunを付けてコマンドライン（`c:\tool\f_cleaning.exe run`）からクリーニングを実行できます。<BR>
※コマンドはc:\toolにプログラムを置いた場合の例
 
## 使い方3 （Windowsの起動時に処理を実行させる）
①使い方1を元に画面から「対象フォルダー」と「処理条件」を指定して、「設定」ボタンを押して設定を行ってください。<BR>
※設定後は「終了」ボタンで画面を閉じてください。<BR>
②f_cleaning.exeを右クリックし、メニューからショートカットを作成してください。<BR>
③ショートカットを右クリックしてプロパティを開き、「リンク先」に 起動オプションのrun を追記したら「適用」ボタンを押してください。<BR>
![image](https://user-images.githubusercontent.com/54971000/210976591-6a2464ab-0d33-447f-ac43-49a4ce2a1df5.png)<BR>
④Windows ロゴキー+ R キーを押し、「shell:startup」と入力して [OK] を選択してエクスプローラを表示します<BR>
⑤エクスプローラの「スタートアップ」に作成したショートカットをコピーしてください。
以降はWindowsの起動時に自動的に実行されます。

## 処理結果
このプログラムは処理が実行されると、プログラムをコピーしたフォルダの下にログ（`f_cleaning_log.txt`）が出力されます。<BR>
※ログファイルは5MBを超えると初期化されます。


 
