"# stack-captioning" 
# preprocess data

Download all the images(train and val) into a folder "images" (http://mscoco.org/dataset/#download) and dataset_coco.json (http://cs.stanford.edu/people/karpathy/deepimagesent/caption_datasets.zip)
If it's full dataset set run 

```bash
$ python prepro_labels.py --iscmplt 1 --input_json dataset_coco.json --output_json cocotalk.json --output_h5 cocotalk
$ python prepro_feats.py --iscmplt 1 --input_json dataset_coco.json --output_dir cocotalk --images_root images
```

else run

```bash
$ python prepro_labels.py --iscmplt 0 --input_json dataset_coco.json --output_json cocotalk.json --output_h5 cocotalk
$ python prepro_feats.py --iscmplt 0 --input_json dataset_coco.json --output_dir cocotalk --images_root images
```