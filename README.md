# 📽️ Violence Detection in Cartoons

This project aims to detect **violent scenes in cartoon videos** using computer vision and deep learning techniques. It focuses on short clips (5–10 seconds) and distinguishes between **violent** and **non-violent** content, making it a potential tool for analyzing children's media.

## 📊 Dataset

- **Source**: Collected manually by the author (cartoon/anime clips).
- **Classes**:
  - `Violence`: scenes containing fights, explosions, or aggressive actions.
  - `Non-Violence`: calm or neutral cartoon scenes.
- **Format**: Videos (5–10 seconds).
- **Size**: ~200 videos per class for training/testing (may increase later).

## ⚙️ Preprocessing

- Videos are downsampled to a fixed number of frames (`NUM_FRAMES = 10`).
- Frames are resized to `64x64` pixels.
- Normalization: All frames are scaled to `[0, 1]`.

```python
frames = preprocess_video(video_path, num_frames=10)
```

## 📈 Exploratory Analysis

- Video duration distribution using histograms (with Seaborn).
- Consistency check on number of frames extracted per video.
- Basic sanity checks to ensure no corrupted or empty files.
