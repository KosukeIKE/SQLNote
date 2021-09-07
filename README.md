# SQLNote
SQLに関するプログラミングノートです。



　　SQL…DBにあるデータの処理を行うプログラミング言語
　　クエリ…データベースに送る命令のこと

　　
  
  　colmun LIKE "%プリン%";
   
      ワイルドカードで囲っている言葉があるレコードを取得する
      
      
     ■条件指定
    WHERE column = "プリン";
    
    
      一致するレコードを取得する
      
      ⚠日付型はダブルクォーテーションではなく、シングルクォーテーション
      
      
    ORDER BY column ASC/DESC
    　　昇順/降順　でカラムを並び替える
        ⚠ソートする時はカラム名を必ず忘れないようにする



　　■レコード数を制限する
　　LIMIT 5
      取得するレコードを制限することができる
      
      
      
      
   GRUOP BY colmun
   
     カラムをGroupにすることができる
     ⚠SELECTで指定したカラムしか取得することができませんん。
     
     
   サブクエリ
      クエリの中にもう一つのクエリを書くこと
   
      SLECT * FROM tabeles WHERE name = (
      
      SLECT name FROM tacles WHERE height >=150
      )


  ■データの追加
    INSERT INTO tables() VALUES ()
    
  ■データの更新
    UPDATE tables SET name = "Kate", course = "C#" WHERE id = 6;
      更新するレコードを指定する
      ⚠更新するレコードを指定しないと全データが更新される
      ⚠UPDATE後は戻すことができないので更新前に必ずSELECT文で確認してからにする
  
  ■データの削除
    DELETE FROM tables WHERE id = 6;
    ⚠削除するレコードを指定しないと全データが削除される
      
  ■データの追加
  
  
  
  ■以外の抽出
  　-> SELECT *
    -> FROM countries
    -> WHERE group_name != "c" (WHERE group_name <> "C")(WHERE group_name NOT IN ("C"))

     →上の３つならどれでも良い。
     
     
  ■範囲の条件決め
  　SELECT *
　　FROM count
　　WHERE rankking BETWEEN A AND B
　　LIMIT 10;
    
     A以上B以下の値を取得する
     前問のように抽出結果にイコールを含めたくない場合には、BETWEEN句を使用することはできません。
     
     
   ■WHERE句の複数選択
   　WHERE position IN("MF", "GK", "DF")
    
      
      複数選択することができる
      
      
   ■AND　OR条件（混合の場合は必ず括弧を付ける）
   　　mysql> SELECT *
    -> FROM players
    -> WHERE (position = "MF" OR position = "FW")　//必ず括弧を付ける必要がある
    -> AND height < 170
    -> ;
    
    　⚠SQLでは「AND演算子の方がOR演算子より先に評価される」というルールがある
     
     
  ■重複をなくす
  
  　SELECT DISTINCT position(カラム名)
   
   
 ■文字列結合方法
  ①CONCAT（）関数を使う場合②「＋」で結合する場合の2パターンある
 
 mysql> SELECT CONCAT(name, '選手のポジションは', position, 'はです')
     -> FROM players;
     
     
     ⚠SQLでの文字列リテラルは「シングルクォート」で括るというルール
   
   　
      
      
     
     
   
  
     



  　
    
