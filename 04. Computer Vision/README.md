# Classical Computer Vision

Este curso é baseado na disciplina [Introdução a Visão Computacional da Georgia Tech](https://omscs.gatech.edu/cs-6476-computer-vision), cujas aulas estão disponveis online gratuitamente na [plataforma da Udacity](https://www.udacity.com/course/introduction-to-computer-vision--ud810).

## Descrição

Este curso fornece uma introdução à visão computacional, incluindo: detecção e correspondência de *features*; estimativa de movimento e rastreamento; e classificação. 

O foco do curso é desenvolver as intuições e matemática dos métodos em aula expositiva, e então aprender sobre a diferença entre teoria e prática nos conjuntos de problemas. Todos os algoritmos funcionam perfeitamente nos slides. Mas lembre-se do que Yogi Berra disse: Em teoria, não há diferença entre teoria e prática. Na prática, sim.

## Cronograma dos Módulos

|         Use        | Week | Module |     Number    | Name                               | Semana |
|:------------------:|:----:|:------:|:-------------:|------------------------------------|:------:|
| :heavy_check_mark: |   1  |   1A   |   Lesson 01   | Introduction                       |    1   |
| :heavy_check_mark: |   1  |   2A   |   Lesson 02   | Images as functions                |    1   |
| :heavy_check_mark: |   1  |   2A   |   Lesson 03   | Filtering                          |    1   |
|                    |   1  |   2A   | ~~Lesson 04~~ | Linearity and convolution          |        |
| :heavy_check_mark: |   1  |   2A   |   Lesson 05   | Filter as templates                |    1   |
| :heavy_check_mark: |   1  |   2A   |   Lesson 06   | Edge Detection: gradients          |    1   |
| :heavy_check_mark: |   1  |   2A   |   Lesson 07   | Edge Detection: 2D operators       |    1   |
| :heavy_check_mark: |   2  |   2B   |   Lesson 08   | Hough transform: Lines             |    1   |
| :heavy_check_mark: |   2  |   2B   |   Lesson 09   | Hough transform: Circles           |    1   |
|                    |   2  |   2B   | ~~Lesson 10~~ | Generalized Hough transform        |        |
|                    |   2  |   2C   | ~~Lesson 11~~ | Fourier Transform                  |        |
|                    |   2  |   2C   | ~~Lesson 12~~ | Convolution in frequency domain    |        |
|                    |   2  |   2C   | ~~Lesson 13~~ | Aliasing                           |        |
|                    |   3  |   3A   | ~~Lesson 14~~ | Cameras and images                 |        |
|                    |   3  |   3A   | ~~Lesson 15~~ | Perspective imaging                |        |
|                    |   3  |   3B   | ~~Lesson 16~~ | Stereo geometry                    |        |
|                    |   3  |   3B   | ~~Lesson 17~~ | Epipolar geometry                  |        |
|                    |   3  |   3B   | ~~Lesson 18~~ | Stereo correspondence              |        |
|                    |   4  |   3C   | ~~Lesson 19~~ | Extrinsic camera parameters        |        |
|                    |   4  |   3C   | ~~Lesson 20~~ | Intrinsic camera parameters        |        |
|                    |   4  |   3C   | ~~Lesson 21~~ | Calibrating cameras                |        |
|                    |   5  |   3D   | ~~Lesson 22~~ | Image to image projections         |        |
|                    |   5  |   3D   | ~~Lesson 23~~ | Homographies and mosaics           |        |
|                    |   5  |   3D   | ~~Lesson 24~~ | Projective geometry                |        |
|                    |   5  |   3D   | ~~Lesson 25~~ | Essential matrix                   |        |
|                    |   5  |   3D   | ~~Lesson 26~~ | Fundamental matrix                 |        |
| :heavy_check_mark: |   6  |   4A   |   Lesson 27   | Introduction to "features"         |    2   |
| :heavy_check_mark: |   6  |   4A   |   Lesson 28   | Finding corners                    |    2   |
| :heavy_check_mark: |   6  |   4A   |   Lesson 29   | Scale invariance                   |    2   |
| :heavy_check_mark: |   6  |   4B   |   Lesson 30   | SIFT descriptor                    |    2   |
|                    |   6  |   4B   | ~~Lesson 31~~ | Matching feature points (a little) |    2   |
| :heavy_check_mark: |   6  |   4C   |   Lesson 32   | Robust error functions             |    2   |
| :heavy_check_mark: |   6  |   4C   |   Lesson 33   | RANSAC                             |    2   |
|                    |   7  |   5A   | ~~Lesson 34~~ | Photometry                         |        |
|                    |   7  |   5B   | ~~Lesson 35~~ | Lightness                          |        |
|                    |   7  |   5C   | ~~Lesson 36~~ | Shape from shading                 |        |
| :heavy_check_mark: |   8  |   6A   |   Lesson 37   | Introduction to motion             |    3   |
| :heavy_check_mark: |   8  |   6B   |   Lesson 38   | Dense flow: Brightness contraint   |    3   |
| :heavy_check_mark: |   8  |   6B   |   Lesson 39   | Dense flow: Lucas and Kanade       |    3   |
|                    |   8  |   6B   | ~~Lesson 40~~ | Hierarchical LK                    |        |
|                    |   8  |   6B   | ~~Lesson 41~~ | Motion models                      |        |
| :heavy_check_mark: |   9  |   7A   |   Lesson 42   | Introduction to tracking           |    3   |
| :heavy_check_mark: |   9  |   7B   |   Lesson 43   | Tracking as inference              |    3   |
| :heavy_check_mark: |   9  |   7B   |   Lesson 44   | The Kalman filter                  |    3   |
|                    |  10  |   7C   | ~~Lesson 45~~ | Bayes filters                      |        |
|                    |  10  |   7C   | ~~Lesson 46~~ | Particle filters                   |        |
|                    |  10  |   7C   | ~~Lesson 47~~ | Particle filters for localization  |        |
|                    |  10  |   7C   | ~~Lesson 48~~ | Particle filters for real          |        |
| :heavy_check_mark: |  11  |   7D   |   Lesson 49   | Tracking considerations            |    4   |
| :heavy_check_mark: |  11  |   8A   |   Lesson 50   | Introduction to recognition        |    4   |
| :heavy_check_mark: |  11  |   8B   |   Lesson 51   | Classification: Generative models  |    4   |
| :heavy_check_mark: |  11  |   8B   |   Lesson 52   | Principal component analysis       |    4   |
|                    |  11  |   8B   | ~~Lesson 53~~ | Appearance-based tracking          |        |
| :heavy_check_mark: |  12  |   8C   |   Lesson 54   | Discriminative classifiers         |    5   |
| :heavy_check_mark: |  12  |   8C   |   Lesson 55   | Boosting and face detection        |    5   |
| :heavy_check_mark: |  12  |   8C   |   Lesson 56   | Support vector machines            |    5   |
| :heavy_check_mark: |  12  |   8C   |   Lesson 57   | Bag of visual words                |    5   |
| :heavy_check_mark: |  13  |   8D   |   Lesson 58   | Introduction to video analysis     |    5   |
|                    |  13  |   8D   | ~~Lesson 59~~ | Activity recognition               |        |
|                    |  13  |   8D   | ~~Lesson 60~~ | Hidden Markov models               |        |
| :heavy_check_mark: |  14  |   9A   |   Lesson 61   | Color spaces                       |    6   |
| :heavy_check_mark: |  14  |   9A   |   Lesson 62   | Segmentation                       |    6   |
|                    |  14  |   9A   | ~~Lesson 63~~ | Mean shift segmentation            |        |
|                    |  14  |   9A   | ~~Lesson 64~~ | Segmentation by graph partitioning |        |
| :heavy_check_mark: |  15  |   9B   |   Lesson 65   | Binary morphology                  |    6   |
|                    |  15  |   9C   | ~~Lesson 66~~ | 3D perception                      |        |
|                    |  15  |   10A  | ~~Lesson 67~~ | The retina                         |        |
|                    |  15  |   10B  | ~~Lesson 68~~ | Vision in the brain                |        |
| :heavy_check_mark: |      |   --   |   Lesson 69   | We're done!                        |        |
|                    |      |   --   | ~~Lesson 70~~ | Sandbox                            |        |


## Materiais

### Listas de Exercício

| Use                | Código | Nome                            | Semana |
|--------------------|--------|---------------------------------|--------|
| :heavy_check_mark: | PS0    | [Images as Functions](https://docs.google.com/document/d/1PO9SuHMYhx6nDbB38ByB1QANasP1UaEiXaeGeHmp3II/pub?embedded=true)             | 1      |
| :heavy_check_mark: | PS1    | [Edges and Lines](https://docs.google.com/document/d/13CJgtDr8kIX9KIrs6BYFDF6-N7cfAyX0R54v8CWoqmQ/pub?embedded=true)                 | 1      |
|                    | PS2    | [Window-Based Stereo Matching](https://docs.google.com/document/d/1WcljLaRxL-Pj3VWYz7JtYysYoZtRZoLIrTG2x48uVWE/pub?embedded=true)     |        |
|                    | PS3    | [Geometry](https://docs.google.com/document/u/3/d/1XsW9k_exgVwCy6CdwgUV3wLKwmFliVdmfAH74Ba4drc/pub?embedded=true)                        |        |
| :heavy_check_mark: | PS4    | [Harris Corners, SIFT and RANSAC](https://docs.google.com/document/d/1DlyziyQB163r1Lx3F4-Tanm8Oq4O9-W3X5Hpdw4QGUE/pub?embedded=true) | 2      |
| :heavy_check_mark: | PS5    | [Optic Flow](https://docs.google.com/document/d/1Bi2_CThMfoLEf4TCMhyFR7cls6t3LAiSz7YYYV89eoE/pub?embedded=true)                      | 3      |
|                    | PS6    | [Particle Tracking](https://docs.google.com/document/d/1ZGdXBjLgr9U-6wdIgcEyRmDHckJFlyhnSWXK8OsduS4/pub?embedded=true)               |        |
|                    | PS7    | [Motion History Images](https://docs.google.com/document/d/1ri0YKEKL63WUcFtq0AGyrlMl2d8auzZI424dOXVsDGg/view)           |        |

### Tutoriais

O objetivo dos tutoriais é dar um gosto a mais do que é possivel fazer, motivando o aluno sem exigir tanto quanto um exercício propriamente dito. Neste curso, vamos usar tutoriais selecionados do [PyImageSearch](https://www.pyimagesearch.com/), que se encontram listados abaixo de acordo com a periodização das aulas:

| Semana | Tutoriais PyImageSearch   |
|-------:|---------------------------|
|      0 | [Basic image manipulations](https://www.pyimagesearch.com/2014/01/20/basic-image-manipulations-in-python-and-opencv-resizing-scaling-rotating-and-cropping/) |
|      1 | [Blur detection](https://www.pyimagesearch.com/2015/09/07/blur-detection-with-opencv/)                                                                       |
|      1 | [Detecting circles](https://www.pyimagesearch.com/2014/07/21/detecting-circles-images-using-opencv-hough-circles/)                                           |
|      2 | [Panorama stitching](https://www.pyimagesearch.com/2016/01/11/opencv-panorama-stitching/)                                                                    |
|      3 | [Ball tracking](https://www.pyimagesearch.com/2015/09/14/ball-tracking-with-opencv/)                                                                         |
|      5 | [Detecting parkinson](https://www.pyimagesearch.com/2019/04/29/detecting-parkinsons-disease-with-opencv-computer-vision-and-the-spiral-wave-test/)           |
|      6 | [Color quantization](https://www.pyimagesearch.com/2014/07/07/color-quantization-opencv-using-k-means-clustering/)                                           |
|  EXTRA | [Non-maximum suppresion](https://www.pyimagesearch.com/2014/11/17/non-maximum-suppression-object-detection-python/)                                          |
|  EXTRA | [Superpixel](https://www.pyimagesearch.com/2014/07/28/a-slic-superpixel-tutorial-using-python/)                                                              |


### Demais Recursos

 - [Slides e problemas](https://d[Iocs.google.com/spreadsheets/d/1ecUGIyhYOfQPi3HPXb-7NndrLgpX_zgkwsqzfqHPaus/pubhtml)
 - [Imagens para os exercícios](https://drive.google.com/drive/u/0/folders/0Bwmlk4kFF5RzNzRMbzRWX0hhMXc)
 - [Jupyter notebook das aulas](https://github.com/jalalirs/Introduction-to-Computer-Vision)
