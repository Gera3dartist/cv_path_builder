# cv_path_builder

Monocular visual odometry from handheld walking videos. Draws the walked path (relative scale) from top-down next to the footage.

Pipeline: Shi-Tomasi corners → Lucas-Kanade optical flow → RANSAC homography → decomposition into R, t → fixed-length step along t, accumulated into a path.

## Setup

```bash
brew install exiftool   # required by pyexiftool (reads focal length)
uv sync
```

Put the videos in `data/raw/` (`straight.mov`, `straight_with_yaw.MOV`, `shape.MOV`). `data/` is git-ignored.

## Run

Open `src/main.ipynb` and run all cells. Choose the video with `file_path` in the main loop cell.

## Reference

- [Monocular VO in C++ (Avi Singh)](https://avisingh599.github.io/vision/monocular-vo/)
