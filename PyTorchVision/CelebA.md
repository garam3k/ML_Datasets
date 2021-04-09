# CelebA Dataset
### [Large-scale CelebFaces Attributes (CelebA) Dataset](http://mmlab.ie.cuhk.edu.hk/projects/CelebA.html)

10k명의 유명인 얼굴사진 200k장으로 이뤄진 데이터셋.

이미지당 눈코입 위치(landmark)와 특징(attribute, 그림자,대머리 등)이 주어짐.

->-예시이미지-<-

---

## Dataset 설명
 - ### Identity  
    총 10,177 명의 유명인 사진 202,599장이 있다.  
    Identity 값(1~10,177)이 사진마다 표시되어있다.
    ```
    000001.jpg 2880
    000002.jpg 2937
    ```
- ### 5 Landmarks  
    Left eye, Right eye, nose, Left mouse, Right mouse 의 위치가 x,y좌표로 주어진다.
    ```
    lefteye_x lefteye_y righteye_x righteye_y nose_x nose_y leftmouth_x leftmouth_y rightmouth_x rightmouth_y
    000001.jpg 165  184  244  176  196  249  194  271  266  260
    000002.jpg 140  204  220  204  168  254  146  289  226  289
    ```
- ### Attributes  
    40개의 특징유무가 Binary로 주어진다.

    |5_o_Clock_Shadow|Arched_Eyebrows| Attractive| Bags_Under_Eyes| Bald|
    |:--:|:--:|:--:|:--:|:--:|
    |Bangs| Big_Lips| Big_Nose| Black_Hair| Blond_Hair|
    |Blurry| Brown_Hair| Bushy_Eyebrows| Chubby| Double_Chin|
    |Eyeglasses| Goatee| Gray_Hair| Heavy_Makeup| High_Cheekbones|
    |Male| Mouth_Slightly_Open| Mustache| Narrow_Eyes|No_Beard| 
    |Oval_Face| Pale_Skin| Pointy_Nose| Receding_Hairline| Rosy_Cheeks|
    |Sideburns| Smiling| Straight_Hair| Wavy_Hair| Wearing_Earrings|
    |Wearing_Hat| Wearing_Lipstick| Wearing_Necklace| Wearing_Necktie| Young|
    ```
    000001.jpg -1  1  1 -1 -1 -1 -1 -1 -1 -1 -1  1 -1 -1 -1 -1 -1 -1  1  1 -1  1 -1 -1  1 -1 -1  1 -1 -1 -1  1  1 -1  1 -1  1 -1 -1  1
    000002.jpg -1 -1 -1  1 -1 -1 -1  1 -1 -1 -1  1 -1 -1 -1 -1 -1 -1 -1  1 -1  1 -1 -1  1 -1 -1 -1 -1 -1 -1  1 -1 -1 -1 -1 -1 -1 -1  1
    ```
- ### BBox  
    얼굴의 위치가 Box로 주어진다.  
    ```
    image_id x_1 y_1 width height
    000001.jpg    95  71 226 313
    000002.jpg    72  94 221 306
    ```

- ### Align & Crop Images
    예시이미지<<<>>>


## 사용방법 (TorchVsion)

TorchVision.dataset 에서 기본 제공되는 데이터셋으로 다음과 같이 불러올 수 있다.  
colab codes
