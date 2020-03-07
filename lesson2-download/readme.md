# fast.ai-course


## Lesson 2: Download Images, Train Classifier
Note: I've only included the final weights file and the exported model to reduce storage.

### Dataset 
Simple image dataset (small, <100 images in total) gathered from Google image searches:
* `sunny weather -glass -icon -clipart -cartoon -drawing -diagram -text -clothing -window -umbrella`
* `raining -glass -icon -clipart -cartoon -drawing -diagram -text -clothing -window -umbrella`

Then used this Chrome extension to manually refine the selection & download the images:
* https://chrome.google.com/webstore/detail/fatkun-batch-download-ima/nnjjahlikiabnchcpehcpkdeckfgnohf

I failed to capture the original URLs of the "raining" dataset (bad practice as for real-world we should have attribution/sourcing covered).
I do have the URLs for the "sunny" dataset though in `sunny.csv`.

#### Alternative, Existing Datasets
* https://ieee-dataport.org/documents/five-class-weather-image-dataset
* https://data.mendeley.com/datasets/4drtyfjtfy/1

#### Image Dataset Advice
* https://forums.fast.ai/t/generating-image-datasets-quickly/19079/9
* https://forums.fast.ai/t/tips-for-building-large-image-datasets/26688
* https://chrome.google.com/webstore/detail/curlwget/jmocjfidanebdlinpbcdkcmgdifblncg?hl=en


## Environment Setup
I created a Conda environemnt, set up to run locally on CPU.

It runs much faster on GPUs on cloud services, but I was getting frustrated with having to start certain things from scratch if I left the Google Colab notebook idle over nuight etc. (should be possible to save out weights etc. but the norebook isn't really set up for quickly resuming - again, do-able, it would just need some work).

some help - https://medium.com/@pierre_guillou/how-to-install-fastai-v1-on-windows-10-ca1bc370dce4

### Jupyter Setup for Image Widgets
`jupyter nbextension install --py widgetsnbextension --user`
`jupyter nbextension enable --py widgetsnbextension --sys-prefix`
`jupyter trust lesson2-download.ipynb` - this was the key step to get it running locally
