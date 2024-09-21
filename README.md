## Datasets for Shot Sequence Order

*Note: These datasets are from the recently submitted paper "In-depth Exploring Shot Sequence Ordering: Benchmarks, Metrics and Methods".*

## Datasets List

### AVE-Order

Files:

- ave_dataset_split.json
- ave_order_dataset.json

For details on obtaining the AVE dataset and the shot segmentation method, please refer to this [repository](https://github.com/dawitmureja/AVE). Following the approach described in this [paper](https://www.ecva.net/papers/eccv_2022/papers_ECCV/papers/136680195.pdf), we split the dataset into training, validation, and test sets (see `ave_dataset_split.json`) and provided the shot sequences along with the corresponding order labels used in our paper (`ave_order_dataset.json`). Please note that during training, we employed data augmentation to rearrange the shot sequences.

### ActivityNet100-Order

Files:

- acn_dataset_split.json
- acn_order_annotations.json
- acn_order_dataset.json

To obtain the ActivityNet100 videos, please refer to this [link](http://activity-net.org/download.html). We used [TransnetV2](https://github.com/soCzech/TransNetV2) to perform shot segmentation on the videos within this dataset and filtered out the invalid shots, providing the shot segmentation results (`acn_order_annotations.json`). You can use [scenes_to_shots.py](https://github.com/dawitmureja/AVE/blob/main/scenes_to_shots.py) to process the videos in ActivityNet100 into individual shots.

The splits of the training, validation, and test sets for ActivityNet100-Order (`acn_dataset_split.json`) follow the original dataset’s partitioning. We also provided the shot sequences and corresponding order labels used in our paper (`acn_order_dataset.json`).

### AVE-Meta

File:

- ave_meta_annotations.json

The [AVE](https://github.com/dawitmureja/AVE) dataset has been extended to create AVE-Meta. The AVE dataset is derived from the [Movieclips](https://www.youtube.com/c/MOVIECLIPS) channel. We collected the corresponding movie names for each scene video and obtained public information about these movies from the IMDb website, including:

- imdb_id
- name
- description
- ratingCount
- ratingValue
- contentRating
- genre
- datePublished
- keywords
- duration (str/min)
- actor
- director
- creator

This dataset can be further utilized for movie analysis tasks.

