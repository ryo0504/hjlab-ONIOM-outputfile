# hjlab-ONIOM-outputfile

ONIOM計算のoutputfileからエネルギー値を取り出すプログラムです。
high_real, low_real, high_model, low_modelを回転させた二面角とともにCSVで出力します。

## ファイルの扱いと環境構築について

### env_build
Dockerfileが入ってます。

### src
ソースコードが入っています。
### ONIOM_energy_values.ipynb
high_real, low_real, high_model, low_modelを回転させた二面角とともにCSVで出力します。
今のところ、二面角はファイル名から判断してます。(座標の情報から二面角を取れたらもっと便利)

### 環境構築の基本的な手順
- git clone <urlを入力>
- cd env_build
- docker build .
- docker run -p <任意のport番号>:8888 -v <srcのディレクトリを指定>/:/work --name <任意のコンテナ名> <コンテナID>
- (例)docker run -p 8888:8888 -v ~/Desktop/test_dir/src/:/work --name test_name XXX
