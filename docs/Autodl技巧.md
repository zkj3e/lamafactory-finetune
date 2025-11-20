## Notebook环境切换
增加内核facefusion
``` shell
conda activate facefusion
conda install ipykernel
ipython kernel install --user --name=facefusion
```

修改kernel.json

``` shell
vim /root/.local/share/jupyter/kernels/facefusion
```

修改成
``` json
{
 "argv": [
    "/bin/bash",
    "-c",
    "source /root/miniconda3/etc/profile.d/conda.sh && conda activate facefusion && exec python -m ipykernel_launcher -f {connection_file}"
  ],
 "display_name": "facefusion",
 "language": "python",
 "metadata": {
  "debugger": true
 }
}
```