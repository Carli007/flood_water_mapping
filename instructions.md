
## **Activate the environment and right path**
```
conda activate gpu
```
```
cd /home/projects/mapella_fm
```
### **Training**
```
python project/train.py  \
    --root_dir /home/projects/mapella_fm/ \
    --dataset_dir /home/projects/mapella_fm/data/ \
    --model_name unet \
    --epochs 2 \
    --batch_size 3 \
    --patch_size 256 \
    --experiment waterbody_mapping 
    
```

### **Testing**

```
python project/test.py \
    --dataset_dir /home/projects/mapella_fm/data/ \
    --model_name unet \
    --load_model_name unet_tvl_unet_ep_1000_17-Jul-23.hdf5 \
    --experiment waterbody_mapping_test 
```

```
python project/test.py \
    --dataset_dir /home/projects/mapella_fm/data/ \
    --model_name unet \
    --load_model_name unet_bjl_unet_ep_300_23-Jul-23.hdf5 \
    --experiment waterbody_mapping_test 
```

