# Shop the Look Dataset

This repository contains the Pinterest shop the look data used in the following paper:

[Wang-Cheng Kang](http://kwc-oliver.com), Eric Kim, [Jure Leskovec](https://cs.stanford.edu/people/jure/), Charles Rosenberg, [Julian McAuley](http://cseweb.ucsd.edu/~jmcauley/) (2019). *[Complete the Look: Scene-based Complementary Product Recommendation.](https://arxiv.org/pdf/1812.01748.pdf)* In Proceedings of IEEE Conference on Computer Vision and Pattern Recognition (CVPR'19)

Please cite our paper if you use the datasets.


### Datasets

We provide the two datasets for `fashion` and `home` respectively. Each dataset contains the scene-product pairs in the following format:

```json
Example (fashion.json):
{
    "product": "0027e30879ce3d87f82f699f148bff7e", 
    "scene": "cdab9160072dd1800038227960ff6467", 
    "bbox": [
        0.434097, 
        0.859363, 
        0.560254, 
        1.0
    ]
}
```

The scene and product images are represented by a signature, and the corresponding image URL can be obtained via:

```python
def convert_to_url(signature):
    prefix = 'http://i.pinimg.com/400x/%s/%s/%s/%s.jpg'
    return prefix % (signature[0:2], signature[2:4], signature[4:6], signature)
```   

Also, product category is also provided (e.g. fashion-cat.json). Please refer to the paper for more statistics and details. You could contact me (wckang#ucsd.edu) if there is any question. 

### Bounding Box

The bounding box is represented by four numbers: `(left, top, right, bottom)`. All the numbers are normalized. The coordinates of the top left corner is `(0,0)`.

### TODO
- Add an illustrative example.
