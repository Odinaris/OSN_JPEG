## Supplementary experiments for manuscript "Towards Versatility: Lossless Data Hiding in JPEG Bitstream via Table-independent Code Mapping"

### Datasets

We select 50 uncompressed (format TIFF) images from the UCID-v2 image database randomly and compress them into JPEG images with different quality factors (QF=30, 50, 70, 90). Note that the Huffman table used in the compression process is the **standard Huffman table**.

Moreover, we select four images (Baboon, Boat, Elaine, and Lena) from USC-SIPI database to show the results.

### Settings

To gain more accurate and up-to-date information, we first upload the selected images from UCID-v2 to two representative online social networks (OSNs), i.e., Facebook and Twitter.  Subsequently, we extract the Huffman tables from the downloaded images. To parse the downloaded images, we use a free decoding tool, [JPEGsnoop](https://www.impulseadventure.com/photo/jpeg-snoop.html). 

### Results

The results of the Huffman table employed in two OSNs are shown in Table 1. According to the results, the Huffman tables employed in the downloaded images are all the optimized Huffman tables.

#### Table 1. Huffman table used in the two OSNs. ("Y" denotes the downloaded image is compressed with the optimized Huffman table; "N" denotes the table is the standard table.)

| Image  | Platform | QF=30 | QF=50 | QF=70 | QF=90 |
| :----: | :------: | :---: | :---: | :---: | :---: |
| Baboon | Facebook |   Y   |   Y   |   Y   |   Y   |
|        | Twitter  |   Y   |   Y   |   Y   |   Y   |
|  Boat  | Facebook |   Y   |   Y   |   Y   |   Y   |
|        | Twitter  |   Y   |   Y   |   Y   |   Y   |
| Elaine | Facebook |   Y   |   Y   |   Y   |   Y   |
|        | Twitter  |   Y   |   Y   |   Y   |   Y   |
|  Lena  | Facebook |   Y   |   Y   |   Y   |   Y   |
|        | Twitter  |   Y   |   Y   |   Y   |   Y   |

For example, the DHT segment information of image Baboon (QF=50, from Facebook) parsed by JPEGsnoop is shown in Fig. 1. It is observed that the length of Huffman codes (i.e., VLCs in our manuscript) is customized, instead of fixed to 162, 

![image-20210523173901771](https://i.loli.net/2021/05/23/KJY25ReSdAMtqbG.png)

Fig. 1. The DHT segment of image Baboon (QF=50, from Facebook) parsed by JPEGsnoop.

We also compare the change in QF from the two OSNs. The results are shown in Table 2. It is observed that the QF will be manipulated in Facebook, while not be manipulated in Twitter.  

#### Table 2. Quality factor change between the two OSNs.

| Image  | Platform | QF=30 | QF=50 | QF=70 | QF=90 |
| :----: | :------: | :---: | :---: | :---: | :---: |
| Baboon | Facebook |  71   |  71   |  75   |  87   |
|        | Twitter  |  30   |  50   |  70   |  90   |
|  Boat  | Facebook |  71   |  71   |  71   |  84   |
|        | Twitter  |  30   |  50   |  70   |  90   |
| Elaine | Facebook |  71   |  71   |  73   |  91   |
|        | Twitter  |  30   |  50   |  70   |  90   |
|  Lena  | Facebook |  71   |  71   |  71   |  77   |
|        | Twitter  |  30   |  50   |  70   |  90   |

### Conclusion

For the representative OSNs, e.g., Facebook and Twitter, the uploaded JPEG images will be recompressed with the optimized Huffman table. Therefore, to meet the various requirements of cloud service or the Internet, for the lossless data hiding (LDH) methods, applying to the JPEG images encoded with the optimized Huffman table is quite necessary.

