# Proxie-Assessment

A coin denomination detection system using RF-DETR, a real-time object detection transformer optimized for efficiency.

NOTEBOOK LINK: https://colab.research.google.com/drive/1Z1cA2EVS2tE9GeQIM9GbTtV52X8md--d?usp=sharing

## DATASET 
Source: Roboflow Universe
Dataset: coins-mio6z by Amit Singh
Format: COCO JSON 

The dataset contains five coin labels
- ₹1
- ₹2
- ₹5
- ₹10
- ₹20
- 'coins' - a supercategory

The dataset is already split in train, test and validation subsets.

## MODEL
RF-DETR-Small was chosen as the optimal model variant due to lower memory requirement compared to other larger options.

## TRAINING CONFIGURATION
| Parameter              | Value          |
| ---------------------- | -------------- |
| Model                  | RF-DETR-Small  |
| Image Resolution       | 640 × 640      |
| Batch Size             | 2–4            |
| Gradient Accumulation  | 4–8            |
| Learning Rate          | 1e-4           |
| Epochs                 | ~30            |
| Mixed Precision        | Enabled (FP16) |
| Gradient Checkpointing | Enabled        |
| EMA                    | Enabled        |
| Early Stopping         | Enabled        |

## PERFORMANCE RESULT
**mAP@50:** ~0.89
**mAP@50–95:** ~0.75
**Precision:** ~0.80
**Recall:** ~1.00

<img width="200" height="200" alt="pp" src="https://github.com/user-attachments/assets/3e5c4bee-aecc-4b79-9269-f8193d04a3ca" />


PER-CLASS SUMMARY
- Best Performing class: 1, 10 and 20
- Worst Performing class: 5
- Moderate: 2

