------

# Enhancing Deep Learning Based Classifiers with Inpainting Anatomical Side Markers (L/R Markers) for Multi-center Trials

![https://user-images.githubusercontent.com/46750574/149261819-4a7878aa-643f-4309-b301-96add4405b3a.png](https://user-images.githubusercontent.com/46750574/149261819-4a7878aa-643f-4309-b301-96add4405b3a.png)

# **Requirements:**

- Install python3.
- Install [tensorflow](https://www.tensorflow.org/install/) (tested on Release 1.3.0, 1.4.0, 1.5.0, 1.6.0, 1.7.0).
- Install tensorflow toolkit [neuralgym](https://github.com/JiahuiYu/neuralgym) (run `pip install git+https://github.com/JiahuiYu/neuralgym`).
- Install MI2RLNet v1 L/R mark detection model (https://github.com/mi2rl/MI2RLNet)

## **Directory Architecture**

|---------- inpaint_ops.py (inpainting operator)

|---------- checkpoint (input our pretrained model)

|---------- inpaint_model.py (inpainting model)

|---------- inpaint.yml (hyper parameter)

------

## **Preprocessing**

- minmax scaling (npy format)
- image size : 1024 x 1024 x 1

------

## Weight link

https://drive.google.com/drive/folders/17IiClqWW2YHUzPtKmgL4dR6RIKLoYNxK?usp=sharing

------

## Inference

```python
CUDA_VISIBLE_DEVICES='gpu_id' python [test.py](<http://test.py/>) \\
--image 'image path' \\
--mask 'detection mask path' \\
--output 'output path' \\
--checkpoint_dir './checkpoint/pretrained model path'
```

---

## Result

![https://user-images.githubusercontent.com/46750574/149261595-5e997a81-79ae-4fe3-9329-c5a715e6d88e.png](https://user-images.githubusercontent.com/46750574/149261595-5e997a81-79ae-4fe3-9329-c5a715e6d88e.png)

---

## **References**

[1] **Generative Image Inpainting with Contextual Attention**; https://arxiv.org/abs/2111.06377. https://github.com/JiahuiYu/generative_inpainting

[2] **An Open Medical Platform to Share Source Code and Various Pre-Trained Weights for Models to Use in Deep Learning Research** https://kjronline.org/DOIx.php?id=10.3348/kjr.2021.0170, https://github.com/mi2rl/MI2RLNet

---

## Contributing**

If you'd like to have any suggestions for these guidelines, you can contact us at [namkugkim@gmail.com](mailto:namkugkim@gmail.com) or open an issue on this GitHub repository.

All contributions welcome!