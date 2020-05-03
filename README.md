# Covid-19 Classification

## Dataset 
https://drive.google.com/open?id=1-HQQciKYfwAO3oH7ci6zhg45DduvkpnK
## Weights
https://drive.google.com/open?id=1EvRIr9O-YiphsdCgLvbp6n1dtkgyFfhl

# Covid-19 Classification with Focal Loss and BCEWithLogitsLoss

## Dataset 
https://drive.google.com/open?id=1eytbwaLQBv12psV8I-aMkIli9N3bf8nO
## Weights
https://drive.google.com/open?id=1psKiqAC-yhiw_g9g6oH4nsxrwz5meFQz

## VGG-16 with BCEWithLogitsLoss:
Complete end-to-end architecture is finetuned on the dataset using learning rate of 0.00123 and momentum 0.9

Layer structure used for this model is
- Linear[25088, 4096]
- ReLU
- Dropout[p=0.5]
- Linear[4096, 4096]
- ReLU
- Dropout[p=0.5]
- Linear[4096, 3]

Loss plots for training and validation dataset:

![1](/Images/1.png)
![2](/Images/2.png)
 
Accuracy plots for training and validation dataset:

![3](/Images/3.png)
![4](/Images/4.png)

Confusion matrix for training dataset:

```bash
[6000  190]
[0      10]

[1655  206]
[345  3994]

[3995  350]
[205  1650]
```
Training accuracy 88.95161290322581

Confusion matrix for validation dataset:

```bash
[600  28]
[0     0]

[174  12]
[26  416]

[415  26]
[13  174]
```
Validation accuracy 90.28662420382166

## Resnet18 with BCEWithLogitsLoss:

Complete end-to-end architecture is finetuned on the dataset using learning rate of 0.00125 and momentum 0.9
Layer structure used for this model is

- Linear[519, 390]
- ReLU
- Dropout[p=0.5]
- Linear[390, 3]

Loss plots for training and validation dataset:

![5](/Images/5.png)
![6](/Images/6.png)

Accuracy plots for training and validation dataset:

![7](/Images/7.png)
![8](/Images/8.png)

Confusion matrix for training dataset:

```bash
[5988  126]
[12     74]

[1673  247]
[327  3953]

[3953  325]
[247  1675]
```
Training accuracy 89.2741935483871

Confusion matrix for validation dataset:

```bash
[599  16]
[1    12]

[180  14]
[20  414]

[415  21]
[13  179]
```
Validation accuracy 91.87898089171975

## VGG-16 with Focal Loss:
Complete end-to-end architecture is finetuned on the dataset using learning rate of 0.00123 and momentum 0.9
Layer structure used for this model is

- Linear[25088, 4096]
- ReLU
- Dropout[p=0.5]
- Linear[4096, 4096]
- ReLU
- Dropout[p=0.5]
- Linear[4096, 3]

Loss plots for training and validation dataset:

![9](/Images/9.png)
![10](/Images/10.png)

Accuracy plots for training and validation dataset:

![11](/Images/11.png)
![12](/Images/12.png)

Confusion matrix for training dataset:

```bash
[5998  173]
[2      27]

[1761  385]
[239  3815]

[3823  231]
[377  1769]
```
Training accuracy 88.08064516129032

Confusion matrix for validation dataset:

```bash
[600  28]
[0     0]
[185  18]
[15  410]

[410  18]
[18  182]
```
Validation accuracy 91.24203821656052

## Resnet18 with Focal Loss:
Complete end-to-end architecture is finetuned on the dataset using learning rate of 0.00125 and momentum 0.9
Layer structure used for this model is

Linear[519, 390]
ReLU
Dropout[p=0.5]
Linear[390, 3]

Loss plots for training and validation dataset:

![13](/Images/13.png)
![14](/Images/14.png)

Accuracy plots for training and validation dataset:

![15](/Images/15.png)
![16](/Images/16.png)

Confusion matrix for training dataset:

```bash
[5989  152]
[11     48]

[1554  212]
[446  3988]

[3990  446]
[210  1554]
```

Training Accuracy 87.03225806451613

Confusion matrix for validation dataset:

```bash
[598  19]
[2     9]

[167  17]
[33  411]

[411  33]
[17  167]
```
Validation accuracy 90.44585987261146

## Analysis:

|                   | VGG-16  | Resnet18 |
|-------------------|---------|----------|
| BCEWithLogitsLoss | 90.28 % | 91.24 %  |
| Focal Loss        | 91.87 % | 90.44 %  |
