# #TidyTuesday

## What is it all about?

Excerpt from the official [tidytuesday](https://github.com/rfordatascience/tidytuesday) project on GitHub:

The #tidytuesday project is a weekly data project aimed at the `R` ecosystem. An emphasis will be placed on understanding how to summarize and arrange data to make meaningful charts with `ggplot2`, `tidyr`, `dplyr`, and other tools in the `tidyverse` ecosystem.

## Code

This repository is a collection of some code snippets used for wrangling, aggregating and visualizing data with `tidyverse` to create a meaningful insight about the underlying weekly data sets.

**Important** _The code is minimalized and its focus is to show how data is prepared, aggregated and visualized (without distraction of styling and modifying theme, fonts, etc.). Sometimes charts in the `images` folder are created with the code shown here with additional theme modifications._

Following package versions are used in `tidyverse`:

```
── Attaching packages ─────────────────────────────────────── tidyverse 1.2.1 ──
✔ ggplot2 3.1.0          ✔ purrr   0.3.0     
✔ tibble  2.0.1          ✔ dplyr   0.8.0.1   
✔ tidyr   0.8.3.9000     ✔ stringr 1.3.1.9000
✔ readr   1.3.1          ✔ forcats 0.4.0
```

## Submit attachments on twitter

### Video file conversion (to .mp4)

```
ffmpeg -y -i input.mov -vf "setpts=0.5*PTS,scale=-1:1080" -r 40000/1001 output.mp4
```

### Video file conversion (to .gif)

In order to get a high resolution gif file, use `gifski`.
On macOS:

```
brew install gifski
ffmpeg -y -i input.mov -vf "setpts=0.5*PTS" frames/frame%04d.png
gifski -o output.gif frames/frame*.png
```

Change `fps`

```
gifski --fps 1 -o output.gif frames/frame*.png
```