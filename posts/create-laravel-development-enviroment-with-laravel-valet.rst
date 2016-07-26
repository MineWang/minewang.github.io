.. title: 使用Laravel Valet快速建立簡單的開發環境
.. slug: create-laravel-development-enviroment-with-laravel-valet
.. date: 2016-07-27 00:24:04 UTC+08:00
.. tags: laravel, valet, php
.. category: 
.. link: 
.. description: 透過Laravel Valet建立簡易開發環境
.. type: text

本篇要來紀錄一下如何使用 `Laravel Valet <https://laravel.com/docs/5.2/valet>`__ 來建立一個簡易的開發環境。Laravel Valet是Laravel針對Mac環境所開發的一套工具，不需要額外安裝VM、Nginx與修改 ``/etc/hosts`` 文件等等，讓我們可以更加專注在開發上。

.. TEASER_END

有使用過Laravel開發的朋友應該會知道Laravel提供的另一個強大的本地開發環境 **Homestead** ，最早之前我也是使用Homestead來進行開發的，參照 `官方文件 <https://laravel.com/docs/5.2/homestead>`__ 即可打造出一個事先配置好的虛擬環境。

然而Homestead在啟動的速度較慢，且因為Homestead本身就是個完整的Ubuntu虛擬機器，所以安裝所需的空間也較大，對於單純想專注於網頁開發與資料庫的人來說有點殺雞焉用牛刀了，如果只是純粹想要能在本地快速開發網頁的話，那Valet是一個好選擇。

Laravel Valet目前只支援Mac系統，安裝上十分簡單，只要事先裝好PHP與SQL資料庫即可，在Mac上可以簡單透過 `Homebrew <http://brew.sh>` 來完成，詳細請參考官方的 `說明文件 <https://laravel.com/docs/5.2/valet>`__ ，這邊就不再多說明安裝流程。另外要注意的是確保沒有程式佔用80 port, 否則安裝可能會失敗。

Serving Sites
-------------

當Valet安裝好後，可以透過兩個指令來執行我們的Laravel網站: **park** 與 **link** 。

* park指令可以執行某個資料夾底下新建的所有Laravel專案。
* link指令可以執行單一Laravel專案，而非選擇所有專案。

使用其他Domain
--------------

Valet預設的domain使用 ** .dev ** 結尾，其網址的結構為 `http://<Folder Name>.dev` ，我們可以透過下面的指令更改想要的網域:

.. code:: bash

    valet domain <name>

將網站啟用TLS
-------------

Valet預設專案網站皆走HTTP，我們也可將網站啟用TLS來使用HTTP/2，例如現有一透過Valet執行的網站 `blog.dev` ，可以簡單透過下面指令來啟用TLS加密服務:

.. code:: bash

    valet secure blog

當然我們也可以隨時取消加密服務:

.. code:: bash

    valet unsecure blog


以上，為使用Valet的一些紀錄與心得，透過Valet，可以很快地在本地端開發與查看，不需要額外安裝與設定，也不需要每次都丟上網頁空間就能直接收到回饋，推薦給只是想單純開發網頁但覺得裝虛擬機很麻煩，或不希望將環境弄的太複雜髒亂的人參考~

    
