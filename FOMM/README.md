# 静止画から動画を作成

##　概要

・静止画から動画を作成
![](https://user-images.githubusercontent.com/73522021/97411942-3d30a200-1944-11eb-8efc-43dbe1836b51.gif)

・FOMMの中身

![https___qiita-image-store s3 ap-northeast-1 amazonaws com_0_209705_4a90e42f-47bb-a26b-19b3-dc6c66289e06](https://user-images.githubusercontent.com/73522021/97694020-60df1e00-1ae5-11eb-9c38-968c0e75fc27.png)

・大きく分けてMotion ModuleとGeneration Moduleの２つで構成されている。

・Motion ModuleはSource(静止画)とDrivingFrame(動画)を入力とし、Keypoint Detectorで、その2つの画像のキーポイントを推定し、Affine Transformationを作成する。Affine Transformationというのは簡単に言うとSourceのキーポイントをDriving Frameのキーポイントの位置に変換するための行列。

・Generation ModuleではSourceとOcclusion maskを入力として、最終的なアウトプットとしてSourceをDriving Frameと同じ動きになっている画像を生成する。

## 環境

・Google Colaboratory上で試せます。

・学習済みモデルやtestデータなどが[こちら](https://drive.google.com/drive/folders/1kZ1gCnpfU0BnpdU47pLM_TQ6RypDDqgw)のGoogle Driveで公開されている。

・自分のGoogle Driveの直下にfirst-order-motion-modelというフォルダを作成し、公開されているGoogle Drive内のそれぞれのファイルのコピーを作成し、
それをfirst-order-motion-modelフォルダに移動する
