.. title: 使用Nikola + Github Pages打造個人部落格
.. slug: create-blog-using-nikola
.. date: 2016-06-01 18:55:39 UTC+08:00
.. tags: nikola, python, github pages, blog
.. category: 
.. link: 
.. description: 透過Nikola打照個人的Blog，並佈署到Github上
.. type: text

首先恭喜自己終於生出第一篇文章了XD

很久之前就想開個部落格分享和記錄自己在程式開發與學習上的心得，不過礙於人性怠惰的關係，
以及一些Blog系統在貼程式碼較麻煩，Ex: Wordpress,這套知名的Blog系統雖然功能強大,
但是有太多我不需要的東西,因此不考慮使用。

.. TEASER_END  

因此開始尋找有無適合寫技術Blog(可以貼code+syntax highlight)，參考了一些相關文章後,
我選擇了 `Nikola <https://getnikola.com>`__ ，主要有以下兩點原因:

* 速度快，請參考Chris Warrick寫的針對四個Static Site Generator做的速度測試 
  `文章 <https://chriswarrick.com/blog/2015/07/23/ssg-speed-test/>`__ 。 
* 使用 `Python <https://www.python.org/>`__ 打造，因此我可以直接在裝有Python的系統管理Blog，不需要架設server
  或登入後台操作。

決定好Blog系統後，當然是馬上安裝來使用看看，先簡單介紹我的作業環境:

作業環境
--------

* OS El Capitan 10.11.3
* Python 3.5.1
* Vim & Sublime Text 3

接著當然是安裝Nikola，安裝方式很簡單，這邊就不多做介紹了，參考官方的文件大約5-10分鐘即可完成:

安裝Nikola
------------

* `Getting Started <https://getnikola.com/getting-started.html>`__
* `Handbook <https://getnikola.com/handbook.html>`__

照著官方文件的教學，很快即可建造一個乾淨的Blog，開始撰寫我們的文章了。
然而有了Blog後，接著是決定Blog該放置在哪邊，考量到我的使用習慣，
特地租用一台主機 + domain來管理似乎有點浪費，因此選擇了 `Github Pages <https://pages.github.com>`__ ，
Github Pages提供個人/組織網頁以及專案網頁的建立，此外，由於我們使用的是Github，
除了用來管理我們的source code以外，理所當然的也可以用來管理我們的網頁！
更棒的是，Nikola也支援佈署到Github的功能！

佈署到Github
------------

有關如何佈署我們的Blog到Github上，請參考 `Handbook <https://getnikola.com/handbook.html#deployment>`__ ，
設定好後即可透過簡單的指令將Blog丟上去:

.. code:: bash

    nikola github_deploy

完成後等待Github Pages處理，Github Pages預設提供的網址為 <username.github.io> ， 很快即可看到我們的Blog上線囉！

首篇就先寫到這邊吧，未來要逼自己養成習慣，將所學的一些內容記錄下來(最近真的有感腦容量有限，不記錄下來很快就忘啦!)
並分享給大家，畢竟很多技巧與知識都是拜各大神的文章來的，
除此之外，也期待與大家互相交流，好發現自己一些觀念上或理解上有錯誤的部分！
