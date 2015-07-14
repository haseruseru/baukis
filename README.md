# Boukis -顧客管理システム

## 説明

Bauis は企業向けの顧客管理システム(Ruby onRails 学習用サンプル)です

## 推奨されるシステム環境

* CentOS 6.5 または Ubuntu 14.04
* Ruby 2.1.0
* MySQL 5.6 または PostgreSQL 9.3

## 注意点
### railsをproductionモードで起動する際には毎回コマンドが必要

``` export SECRET_KEY_BASE=`cat ~/.baukis_secret_key_base` ```

※バッククオートに注意

### rspec で no match routes　のエラーが出たとき

対処法：

use_route: :コントローラーのフォルダ名

```ruby
it "does something..." do
    get :index, use_route: :my_blog
    ...
  end
```

参考URL= http://pivotallabs.com/writing-rails-engine-rspec-controller-tests/
