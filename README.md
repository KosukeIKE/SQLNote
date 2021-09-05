# SQLNote
SQLに関するプログラミングノートです。



　　SQL…DBにあるデータの処理を行うプログラミング言語
　　クエリ…データベースに送る命令のこと

　　
  
  　colmun LIKE "%プリン%";
   
      ワイルドカードで囲っている言葉があるレコードを取得する
      
      
      
    WHERE column = "プリン";
    
    
      一致するレコードを取得する
      
      
      
      
    ORDER BY column ASC/DESC
    　　昇順/降順　でカラムを並び替える
        ⚠ソートする時はカラム名を必ず忘れないようにする




　　LIMIT 5
      取得するレコードを制限することができる
      
      
      
      
   GRUOP BY colmun
   
     カラムをGroupにすることができる
     注意点としては、SLECTで指定したカラムしか取得することができませんん。
     
     
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
    
