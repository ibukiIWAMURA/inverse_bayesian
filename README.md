郡司ぺギオ幸夫が提唱する「逆ベイズ推論」を実装した．ただし，逆ベイズ推論単独ではなく，「ベイズ推論＋逆ベイズ推論」の実装である．
逆ベイズ推論とは，ベイズ推論における条件付き確率を無条件確率に置換する操作を「逆」にし，無条件確率を条件付き確率に置換する操作である．
逆ベイズ推論において置換する確率は，データの無条件確率$p(d)$と，データの条件付き確率$p(d|h)$である．
データの無条件確率$p(d)$の計算は，ある時間間隙Mにおいて相互情報量が飽和する（今回のセッティングでは最大値を取る）区間における，データの累積和の平均の時間平均（単純な頻度）である．
データの条件付き確率$p(d|h)$の計算は，最不適仮説(the least optimal hypothesis)をサンプリングする手法を採用した．データの条件付き確率$p(d|h)$とは尤度であり，つまるところ，どの仮説$h$を選択するかという問題である．
そこで，確率が一番低い（最も不適な）仮説をランダムにサンプリングするため，$1-p(h_i)$を全ての仮説で計算し足し合わせ（例えば3），その区間（0~3）からランダムに実数$r$(例えば，1.8)をサンプリングし，その実数$r$がどの区間（0~3)の存在するかを検出する．
何をしているかと言うと，確率が一番低いということは，区間内で一番大きい区間を取っていることであり，その区間に実数$r$が入っている確率が高いということである．これにより，最も不適な仮説を見つけ，その尤度を見つける．

内容に関しては，以下の文献か，私岩村入吹のまとめ資料（作成途中）を参考にしてください．https://drive.google.com/file/d/1V6HwXwCF5_aHJkm8oB_QKOXAUD0-9Thi/view?usp=sharing





参照文献は， 
1．郡司ぺギオ幸夫. 知覚と記憶の接続・脱接続: デジャビュ・逆ベイズ推論. 書肆心水, 2016.
2．Yukio-Pegio Gunji, Shuji Shinohara, Taichi Haruna, and Vasileios Basios. Inverse bayesian inference as a key of consciousness featuring a macroscopic quantum logical structure. Biosystems, Vol. 152, pp. 44–65, 2017.
3. Yukio-Pegio Gunji. Connection and disconnection of perception and memory: D´ej`a vu, bayesian and inverse bayesian inference. Bergson’s Scientific Metaphysics: Matter and Memory Today, p. 195, 2023.
である．
