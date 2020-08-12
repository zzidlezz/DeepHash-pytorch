# DeepHash-pytorch
Implementation of Some Deep Hash Algorithms.
#### Any Pull Request is highly welcomed

#### Any Issues is highly welcomed

# How to run
My environment is python==3.7.0  torchvision==0.5.0  pytorch==1.4.0  
You can easily train and test any algorithm just by
```
pyhon DSH.py  
pyhon DPSH.py  
pyhon HashNet.py  
pyhon DHN.py  
pyhon DFH.py  
pyhon DTSH.py   
pyhon DSDH.py  
```
 
# Dataset
You can download  ImageNet, NUS-WIDE-m and COCO dataset [here](https://github.com/thuml/HashNet/tree/master/pytorch)  
    
download cifar10(Lossless PNG format) [here](https://drive.google.com/open?id=1NZ5QKW2zqzN-RQ4VDpuOAb-UgcsTPUJK)
  
and download   NUS-WIDE [here](https://github.com/TreezzZ/DSDH_PyTorch)
  
NUS-WIDE-m is different from  NUS-WIDE, so i made a distinction.  

269,648 images in NUS-WIDE , and 195834 images which are associated with 21 most frequent concepts.     

NUS-WIDE-m has 223,496 images,and  NUS-WIDE-m  is used in [HashNet(ICCV2017)](http://openaccess.thecvf.com/content_ICCV_2017/papers/Cao_HashNet_Deep_Learning_ICCV_2017_paper.pdf) and code [HashNet caffe and pytorch](https://github.com/thuml/HashNet)    

download [mirflickr](https://press.liacs.nl/mirflickr/mirdownload.html) , and use ./data/mirflickr/code.py to randomly select 1000 images as the test query set and 4000 images as the train set.
 
# Paper And Code
It is difficult to implement all by myself, so I made some modifications based on these codes  
DSH(CVPR2016)  
paper [Deep Supervised Hashing for Fast Image Retrieval](https://www.cv-foundation.org/openaccess/content_cvpr_2016/papers/Liu_Deep_Supervised_Hashing_CVPR_2016_paper.pdf)  
code [DSH-pytorch](https://github.com/weixu000/DSH-pytorch)

HashNet(ICCV2017)  
paper [HashNet: Deep Learning to Hash by Continuation](http://openaccess.thecvf.com/content_ICCV_2017/papers/Cao_HashNet_Deep_Learning_ICCV_2017_paper.pdf)  
code [HashNet caffe and pytorch](https://github.com/thuml/HashNet)

DPSH(IJCAI2016)  
paper [Feature Learning based Deep Supervised Hashing with Pairwise Labels](https://cs.nju.edu.cn/lwj/paper/IJCAI16_DPSH.pdf)   
code [DPSH-pytorch](https://github.com/jiangqy/DPSH-pytorch)

DHN(AAAI2016)  
paper [Deep Hashing Network for Efficient Similarity Retrieval](http://ise.thss.tsinghua.edu.cn/~mlong/doc/deep-hashing-network-aaai16.pdf)  
code [DeepHash-tensorflow](https://github.com/thulab/DeepHash)

DFH(BMVC2019)  
paper [Push for Quantization: Deep Fisher Hashing](https://arxiv.org/abs/1909.00206)  
code [Push-for-Quantization-Deep-Fisher-Hashing](https://github.com/liyunqianggyn/Push-for-Quantization-Deep-Fisher-Hashing)

DTSH(ACCV2016)  
paper [Deep Supervised Hashing with Triplet Labels](https://arxiv.org/abs/1612.03900)  
code [DTSH](https://github.com/Minione/DTSH)  

DSDH(NIPS2017)  
paper [Deep Supervised Discrete Hashing](https://papers.nips.cc/paper/6842-deep-supervised-discrete-hashing.pdf)  
code [DSDH_PyTorch](https://github.com/TreezzZ/DSDH_PyTorch)

GreedyHash(NIPS2018)  
paper [Greedy Hash: Towards Fast Optimization for Accurate Hash Coding in CNN](https://papers.nips.cc/paper/7360-greedy-hash-towards-fast-optimization-for-accurate-hash-coding-in-cnn.pdf)  
code [GreedyHash](https://github.com/ssppp/GreedyHash) 

ISDH(arxiv2018)  
paper [Instance Similarity Deep Hashing for Multi-Label Image Retrieval](https://arxiv.org/abs/1803.02987v1)  
code [ISDH-Tensorflow](https://github.com/pectinid16/ISDH-Tensorflow)

IDHN(TMM2019)  
paper [Improved Deep Hashing with Soft Pairwise Similarity for Multi-label Image Retrieval](https://arxiv.org/abs/1803.02987)  
code [IDHN-Tensorflow](https://github.com/pectinid16/IDHN)

# Mean Average Precision,48 bits[AlexNet].


<table>
    <tr>
        <td>Algorithms</td><td>dataset</td><td>this impl.</td><td>paper</td>
    </tr>
    <tr>
        <td >DSH</td><td >cifar10</td> <td >0.774</td> <td >0.6755</td>
    </tr>
    <tr>
        <td ></td><td >nus_wide_21</td> <td >0.766</td> <td >0.5621</td>
    </tr>
    <tr>
        <td ></td><td >ms coco</td> <td >0.655</td> <td >-</td>
    </tr>
    <tr>
        <td ></td><td >imagenet</td> <td >0.576</td> <td >-</td>
    </tr>
    <tr>
        <td ></td><td >mirflickr</td> <td >0.735</td> <td >-</td>
    </tr>
    <tr>
        <td >DPSH</td><td >cifar10</td> <td >0.775</td> <td >0.757</td>
    </tr>
    <tr>
        <td ></td><td >nus_wide_21</td> <td >0.839</td> <td >0.851(0.812*)</td>
    </tr>
    <tr>
        <td ></td><td >imagenet</td> <td >0.502</td> <td >-</td>
    </tr>
    <tr>
        <td ></td><td >ms coco</td> <td >0.711</td> <td >-</td>
    </tr>
    <tr>
        <td ></td><td >voc2012</td> <td >0.608</td> <td >-</td>
    </tr>
    <tr>
        <td ></td><td >mirflickr</td> <td >0.781</td> <td >-</td>
    </tr>
    <tr>
        <td >HashNet</td><td >cifar10</td> <td >0.782</td> <td >-</td>
    </tr>
    <tr>
        <td ></td><td >nus wide81 m</td> <td >0.764</td> <td >0.7114</td>
    </tr>
    <tr>
        <td ></td><td >nus_wide_21</td> <td >0.830</td> <td >-</td>
    </tr>
    <tr>
        <td ></td><td >imagenet</td> <td >0.644</td> <td >0.6633</td>
    </tr>
    <tr>
        <td ></td><td >ms coco</td> <td >0.724</td> <td >0.7301</td>
    </tr>
    <tr>
        <td >DHN</td><td >cifar10</td> <td >0.781</td> <td >0.621</td>
    </tr>
    <tr>
        <td ></td><td >nus_wide_21</td> <td >0.841</td> <td >0.758</td>
    </tr>
    <tr>
        <td ></td><td >imagenet</td> <td >0.486</td> <td >-</td>
    </tr>
    <tr>
        <td ></td><td >ms coco</td> <td >0.712</td> <td >-</td>
    </tr>
    <tr>
        <td ></td><td >mirflickr</td> <td >0.775</td> <td >-</td>
    </tr>
    <tr>
        <td >DSDH</td><td >cifar10</td> <td >0.755</td> <td >0.820</td>
    </tr>
    <tr>
        <td ></td><td >nus_wide_21</td> <td >0.819</td> <td >0.829</td>
    </tr>
    <tr>
        <td ></td><td >imagenet</td> <td >0.300</td> <td >-</td>
    </tr>
    <tr>
        <td ></td><td >ms coco</td> <td >0.681</td> <td >-</td>
    </tr>
    <tr>
        <td ></td><td >mirflickr</td> <td >0.765</td> <td >-</td>
    </tr>
    <tr>
        <td >DTSH</td><td >cifar 10</td> <td >0.800</td> <td >0.774</td>
    </tr>
    <tr>
        <td ></td><td >nus_wide_21</td> <td >0.829</td> <td >0.824</td>
    </tr>
    <tr>
        <td ></td><td >ms coco</td> <td >0.760</td> <td >-</td>
    </tr>
    <tr>
        <td ></td><td >imagenet</td> <td >0.631</td> <td >-</td>
    </tr>
    <tr>
        <td ></td><td >mirflickr</td> <td >0.753</td> <td >-</td>
    </tr>
    <tr>
        <td >DFH</td><td >cifar 10</td> <td >0.783</td> <td >0.844</td>
    </tr>
    <tr>
        <td ></td><td >nus_wide_21</td> <td >0.834</td> <td >0.842</td>
    </tr>
    <tr>
        <td ></td><td >ms coco</td> <td >0.717</td> <td >-</td>
    </tr>
    <tr>
        <td ></td><td >imagenet</td> <td >0.519</td> <td >0.747</td>
    </tr>
    <tr>
        <td ></td><td >mirflickr</td> <td >0.766</td> <td >-</td>
    </tr>
    <tr>
        <td >GreedyHash</td><td >cifar 10</td> <td >0.798</td> <td >0.822</td>
    </tr>
    <tr>
        <td ></td><td >imagenet</td> <td >0.678</td> <td >0.688</td>
    </tr>
    <tr>
        <td ></td><td >ms coco</td> <td >0.728</td> <td >-</td>
    </tr>
    <tr>
        <td ></td><td >nuswide_21</td> <td >0.793</td> <td >-</td>
    </tr>
</table>
Due to time constraints, I can't test many hyper-parameters  

"DPSH 0.812 *" denotes re-running the code provided by they authors of DPSH (said in [Deep Supervised Discrete Hashing](https://papers.nips.cc/paper/6842-deep-supervised-discrete-hashing.pdf))  
