# 開始一個專案

使用 [https://github.com/francescomalatesta/laravel-api-boilerplate-jwt](https://github.com/francescomalatesta/laravel-api-boilerplate-jwt)

`composer create-project francescomalatesta/laravel-api-boilerplate-jwt 專案名稱`

這個boilerplat包含了

* jwt-auth
* dingoapi
* laravel-cors

安裝完後會看到此專案裡面已經有幾個寫好的controller（登入、註冊、忘記密碼、重設密碼）

已經和laravel的auth做了整合

與原本laravel不同的是 routing 寫在 route/api.php 下指令 php artisan api:routes 可在console看到所有的rule

config/boilerplate.php 裡面有預設controller的一些驗證規則，可在此修改

要啟用cors的話可添加在middleware

ex:$api-&gt;group\(\['middleware' =&gt; \[jwt.auth,cors\]\], function\(Router $api...

新增一個.env檔案，設定資料庫連線資訊，config/database.php會吃到這些資訊，.env檔案不上git在專案成員中自己互傳

最後，下指令 php artisan migrate 會將預設的幾個table建立好，可以開始開發了

