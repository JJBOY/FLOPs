# FLOPs
Auto compute the  FLOPs of the nerural network with Pytorch.
this Impeletation do not care the batch size.The FLOPs has nothing to do with batch size, it only reletes too the network itself.

## How to use
 ```python
    from torchvision import models
    from FLOPs_counter import print_model_parm_flops
    model = models.resnet50()
    input = torch.randn(1, 3, 224, 224)
    print_model_parm_flops(model, input, detail=True)
 ```  
    
### output
```
+ Number of FLOPs: 8.17G
  + Conv FLOPs: 8.11G
  + Linear FLOPs: 0.00G
  + Batch Norm FLOPs: 0.04G
  + Relu FLOPs: 0.01G
  + Pooling FLOPs: 0.00G
```

you can use make the detail=False to hide the detials, only print the total FLOPs
  
