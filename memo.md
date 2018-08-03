### 全天カメラからの風覚再現

- 位置補正（フレーム内座標によるベクトルの長さの補正）
- 視点補正（HMDによる頭部角度による風到来方向の変化）

- [HOFの実装](https://github.com/dhvanikotak/Emotion-Detection-in-Videos)が必要？
	- これは密なオプティカルフローだから，疎なオプティカルフローなら自分で実装する必要がある？
	- 多分，密な方は，ベクトル（u, v），つまりベクトル出発地点～終了地点のｘ，ｙそれぞれの長さを返す関数
	- 疎な方は，それを計算してから，密な方と同じ関数に投げてやればいい
	- [cv2.calcOpticalFlowFarneback](http://labs.eecs.tottori-u.ac.jp/sd/Member/oyamada/OpenCV/html/py_tutorials/py_video/py_lucas_kanade/py_lucas_kanade.html)の結果をよく見ないといけない


まずは風の方向と強度を出す．細かいことはそれから