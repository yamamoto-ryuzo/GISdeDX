# GISdeDX
　ちょっそ、 **「ＧＩＳでなんで仕事のＤＸ・ＢＰＲが可能なのか？」** を考える機会があったので、まとめてみました。  
　こんな感じのプロダクトに仕上がれば、ＧＩＳはその殻をやぶり違うシステムとして社会の役に立てるのかな？  
　特に、ＧＩＳで扱うデータはいわばデータベース！  
　しかも、その **データを簡単に入力するインターフェイスもノーコードで構築** できる。  
　さらに、細かいところは **エクセル出力して、資料なりなんなり作成できる強者** になれる気がします。  

## STEP.1 QGISの地図をLIZMAPで公開
### 1-1.下記から環境にあったQGISをダウロードください。
・[普通にインストールできる人](https://qgis.org/ja/site/forusers/download.html)  
・[LAN内で複数の人に自動配信及びバージョン管理をしたい人（管理者向け）](https://github.com/yamamoto-ryuzo/yr-qgis-portable-launcher)  
### 1-2.プラグインのインストール  　　
・[‎Lizmap プラグインをインストールする](https://docs.lizmap.com/current/ja/publish/quick_start/lizmap_configuration.html#install-the-lizmap-plugin)  
### 1-3.QGISで地図を作成する  
・[QGISドキュメント](https://qgis.org/ja/docs/index.html)   
・[QGIS初心者質問グループ：質問はこちらへ](https://groups.google.com/g/qgisshitumon01)  
・[QGIS User Group Japan：QGISについて語りたい方はこちらへ](https://www.facebook.com/groups/qgis.jp)   
### 1-4.LIZMAPを設定する
### 1-5.LIZMAPで公開  
## STEP.2 他のシステムとの連携  
[GDAL仮想ファイルシステムについて](https://gdal.org/user/virtual_file_systems.html#)  
### 2-1.グーグルドライブとの連携  
・[スプレッドシートを.CSV形式で公開](https://smellman.hatenablog.com/entry/2021/02/07/191649)  
　　こちがおすすめのようだ！  
・CSVファイルをグーグルドライブで共有 　例）https://drive.google.com/uc?export=download&id=ファイルのID&delimiter=,  
　　QGISで属性を指定する場合、4バイト文字ではなく、2バイト文字で指定する必要がある。（たぶん・・・）   
【現在の課題】  
　QGISサーバーが起動したときか何かのタイミング時点でCSVとの連携を一度行うだけの様子。    
　なので、リアルタイムでの連携が出来ていない・・・これまた勉強が必要！  
　対応策で一番有力なのは、LIZMAPのWPSを利用してサーバーサイドでリロードをするのがよさそう！  
【暫定対応策】  
　毎日サーバーをリセットしているので、一日に一度は連携が可能な状態。  

---

![image](https://github.com/yamamoto-ryuzo/GISdeDX/assets/86514652/ee4ae629-fcfd-4e09-8b15-dd5e55cd5420)
　汎用検索機能（[地図検索](https://github.com/yamamoto-ryuzo/GEO-search-plugin)　：　[汎用地図検索](https://github.com/NationalSecurityAgency/qgis-searchlayers-plugin)  ）　　　 [エクセル連携](https://github.com/yamamoto-ryuzo/QGIS-exportExcel)

![image](https://github.com/yamamoto-ryuzo/GISdeDX/assets/86514652/0b0031d3-62a5-44ff-9935-00f546a5cc67)
![image](https://github.com/yamamoto-ryuzo/GISdeDX/assets/86514652/78fc436b-2338-4ac0-ae30-338c0e186ad2)
![image](https://github.com/yamamoto-ryuzo/GISdeDX/blob/main/image/image04.png)
