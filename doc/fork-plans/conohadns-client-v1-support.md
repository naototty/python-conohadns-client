# load to conohadns client v1 support

original版 "python-designateclient" は、下記のような対応になっている。
  * v1 APIは "obsoleta" なものなので、単独のclientとしてのみ動作する
  * v2 APIは "up to date" なので、osclientとしてのみ動作する

ConoHa DNS client APIとしては、v1 APIが主体、v2 APIはzone create/export(dump)のみが使える

なので、開発の優先順位としては、v1 API対応は下記のように対応する

* 1) conohadns clientとして、単独で動くV1 APIをまず動くようにいる
  * これについては、forkして、json supportを変更することで、ある程度実現することを確認済み
* 2) conohadns clientとして、単独で動くV2 APIを動くように機能追加する
  * 2.a) endpoint v1, v2両方を利用することになるので、その対応が必要
  * 2.b) v2 APIで cli単体で動かしたい機能は下記の機能
    * v2 zone export : 既存 domain zonesの出力
    * v2 zone create (import) : 新規 domain zonesの取り込み
    * v1 modified zone update : 既存 domain zonesのupdate
      * v1 APIを組み合わせて、client basedで "v2 zone update(PUT /zones)" 相当の機能を実装する 
* 3) osclient v2 API対応
  * osclientに "conohadns" というclassが見えるようにする
  * zone create(import) / zone export がとりあえず使えるようにする
    * 現状、forkでの修正である程度問題なさそうであることは確認している 
* 4) osclient v1 API対応
  * v2 zone APIを手本に、v1 endpointを osclientとして使えるようにする
  * osclientの仕様としては、sub-classではなく、object名 = コマンドになるけど、os conohadns domains みたいに sub-command対応でやってみる
    * /v1/domains
    * /v1/domains/<dom id>/recoards

## updates

  * 1st MEMO記述

  