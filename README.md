# exoplayer_extra
fix exoplayer skip frame .
when first frame is not I-Frame/KeyFrame,ExoPlayer skip some P/B frame.

当视频的第一帧不是关键帧时，exo播放器会跳过部分P/B帧，导致视频卡住/冻结，只有声音。
