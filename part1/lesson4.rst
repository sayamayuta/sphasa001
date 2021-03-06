.. _label-lesson4:

====================================
Lesson4: ハイパーリンク
====================================

   :保存ファイル名: lesson4.rst
   :必要な操作: ファイルの作成、編集

Webブラウザで表示させた状態で以降の行をテキストエディタにコピーの上、
レイアウト等を再現するよう編集してください。

ハイパーリンク
==============

このLesson4ではリンクおよびリファレンスについて説明します。
( http://sphinx-users.jp/doc10/markup/inline.html を参考にしています。 )

外部URIへのリンク
------------------

httpから始まるURIを記述すると自動的にリンクとして扱われます。

   * http://www.google.com/

また、 ```google.com <http://www.google.com/>`_`` と書くと、
「 `google.com <http://www.google.com/>`_ にジャンプする」、という風な
表記が可能です。

次のようにして、ターゲット定義と、リンクを分割することもできます:

   :: 

      このパラグラフは `リンク`_ を含みます。
      
      .. _リンク: http://example.com


自由な場所へのリンク
--------------------

自在に参照先へのリンクを設けるには、 飛び先ページの指定の場所にアンカー
を設置します。 ``.. _my-reference-label:``

ジャンプさせたい場所で ``:ref:`my-reference-label``` と表記します。

   ::

      .. _my-reference-label:
      
      クロスリファレンスのセクション
      ------------------------------
      
      これはセクションのテキストです。
      
      これはセクションそのものを参照します。 :ref:`my-reference-label`

