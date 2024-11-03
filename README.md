# LabelImg Fork with Enhancements

This repository is a fork of the popular image annotation tool, LabelImg, originally created by Tzutalin. This fork includes several improvements and bug fixes contributed by various developers. Below is a summary of the changes and enhancements made in this version:

## Enhancements and Fixes

- **Dark Mode**: Added dark mode support using the `qdarkstyle` library, contributed by [mrzahaki](https://github.com/mrzahaki).
- **Issue 825 Fix**: Resolved the issue where pressing Ctrl+D with no label caused `labelImg.py` to crash, fixed by [aeeeeeep](https://github.com/aeeeeeep).
- **Issue 465 Fix**: Fixed the issue where saving YOLO labels corrupted `classes.txt`, resolved by [POONAM2015](https://github.com/POONAM2015).
- **Popup Position**: Changed the position of pop-up windows, improved by [lsh0902](https://github.com/lsh0902).
- **PyQt4 Deprecation**: Gradual removal of PyQt4 in progress.
- **Polygon Vertex Logic**: Improved logic for finding polygon vertices to enhance clickability.
- **Auto annotate**: Added the function of automatic annotation of the image using the Ultralyrics module.

## About Label Studio

LabelImg is now part of the Label Studio community, a modern, multi-modal data annotation tool. Label Studio is the most flexible open-source data labeling tool for images, text, hypertext, audio, video, and time-series data. To get started, [install Label Studio](https://labelstud.io/guide/install.html) and join the [Slack community](https://label-studio.slack.com/).

### Build from Source (Windows)

1. Install [Python](https://www.python.org/downloads/windows/), [PyQt5](https://www.riverbankcomputing.com/software/pyqt/download5), and [lxml](http://lxml.de/installation.html).
2. Open `cmd` and navigate to the `labelImg` directory.
3. Run the following command to compile resources:

   ```shell
   pyrcc5 -o libs/resources.py resources.qrc
   ```

4. Execute the application:

   ```shell
   python labelImg.py
   ```

## Hotkeys

| Key Combination    | Action                                      |
|--------------------|---------------------------------------------|
| Space              | Auto annotate current image                 |
| Ctrl + u           | Load all images from a directory            |
| Ctrl + r           | Change the default annotation target dir    |
| Ctrl + s           | Save                                        |
| Ctrl + d           | Copy the current label and rect box         |
| Ctrl + Shift + d   | Delete the current image                    |
| Ctrl + Space       | Flag the current image as verified          |
| w                  | Create a rect box                           |
| d                  | Next image                                  |
| a                  | Previous image                              |
| del                | Delete the selected rect box                |
| Ctrl++             | Zoom in                                     |
| Ctrl--             | Zoom out                                    |
| ↑→↓←               | Move selected rect box with keyboard arrows |