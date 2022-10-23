
## Inference
```bash
python tools/infer.py \
    --weights weights/yolov6s.pt \
    --source data/images/image1.jpg
```

## Export to OpenVINO
```bash
python deploy/OpenVINO/export_openvino.py \
    --weights weights/yolov6s.pt \
    --img 640 \
    --batch 1
```
Speed test
```bash
benchmark_app \
    -m weights/yolov6s_openvino/yolov6s.xml \
    -i data/images/image1.jpg \
    -d CPU \
    -niter 100 \
    -progress
```