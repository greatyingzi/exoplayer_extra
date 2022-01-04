# exoplayer_extra
fix exoplayer skip frame .
when first frame is not I-Frame/KeyFrame,ExoPlayer skip some P/B frame.

当视频的第一帧不是关键帧时，exo播放器会跳过部分P/B帧，导致视频卡住/冻结，只有声音。

[修改的关键代码](https://github.com/greatyingzi/exoplayer_extra/blob/107fe49e655859c09f3c38a62b865f446be32ab6/custom/src/main/java/com/google/android/exoplayer2/extractor/mp4/AtomParsers2.java#L657)
```
startIndices[i] = 0;
```


用法
```
使用CustomExtractorsFactory替换掉默认的DefaultExtractorsFactory
```

添加
```
allprojects {
		repositories {
			...
			maven { url 'https://jitpack.io' }
		}
	}
	
```
引入依赖
```
    implementation 'com.github.greatyingzi:exoplayer_extra:v1.0.3'
```
