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
    <details><summary>Sample image</summary>
    한국인 유명인 id값과 그 예시 
    id = 0000 (강동원). 사진 몇개
    id = xxxx (누구누구). 사진 몇개

    </details>

- ### 5 Landmarks  
    눈코입의 위치가 x,y좌표로 주어진다.
    ```
    lefteye_x lefteye_y righteye_x righteye_y nose_x nose_y leftmouth_x leftmouth_y rightmouth_x rightmouth_y
    000001.jpg 165  184  244  176  196  249  194  271  266  260
    000002.jpg 140  204  220  204  168  254  146  289  226  289
    ```
    <details><summary>Sample image</summary>
    눈코입 위치 점으로 찍은 예시
    </details>
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
    <details><summary>Sample image</summary>
    특징들에 대한 예시 이미지들
    </details>
- ### BBox  
    얼굴의 위치가 Box로 주어진다.  
    ```
    image_id x_1 y_1 width height
    000001.jpg    95  71 226 313
    000002.jpg    72  94 221 306
    ```
    <details><summary>Sample image</summary>
    box 그린 예시
    </details>

- ### Align & Crop Images
    <details><summary>Sample image</summary>
    원본 사진과 처리된 사진
    </details>

- ### Related Datasets
    <details>
    <summary>CelebAMask-HQ Dataset</summary>
    
    
    dd
    </details>  
    <details>
    <summary>CelebA-Spoof Dataset</summary>
    
    
    </details>  
## 사용방법 (TorchVsion)

TorchVision.dataset 에서 기본 제공되는 데이터셋으로 다음과 같이 불러올 수 있다.  
colab codes
