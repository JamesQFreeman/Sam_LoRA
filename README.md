# LoRA for SAM (meta's segment-anything)

## Usage
```
from segment_anything import build_sam, SamAutomaticMaskGenerator 
from segment_anything import sam_model_registry
from sam_lora import LoRA_Sam
import torch
sam = sam_model_registry["vit_b"](checkpoint="sam_vit_b_01ec64.pth")
lora_sam = LoRA_Sam(sam,r = 4)
result = lora_sam.sam.image_encoder(torch.rand(size=(1,3,1024,1024)))
print(result.shape)
```

## Train
Coming soon and welcome pull request.

## Thanks
The code for LoRA ViT comes form
https://github.com/JamesQFreeman/LoRA-ViT