# README
## How to connect GPU at `gpulab` to Jupyter Notebook?
1. Request a GPU:
```
srun --mem=32gb --gres=gpu:1 -p gpu-bio -A ksibio --time=5:00:00 --pty bash
```

2. activate appropriate python environment
```
source /path/to/venv/activate
```
3. Run Jupyter kernel (make sure that you have installed the `notebook` package):
```
jupyter notebook --ip 0.0.0.0 --port 7021
```
This will produce URL address where the kernel can be found, such as:
```
http://ampere02.gpulab.local:7021/tree?token=518dbf3c01e221ea71cb5978c95ff0b55fc1ac751dc132d3
```
4. Use the URL to set the kernel within the Jupyter Notebook
