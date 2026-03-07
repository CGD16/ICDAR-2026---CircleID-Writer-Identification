Um die in der environment.yml aufgelisteten Pakete zu installieren und die Umgebung exakt so nachzubauen, nutzt du diesen Befehl:

```
conda create -n vit python=3.12 -y 
conda activate vit`
pip3 install torch torchvision --index-url https://download.pytorch.org/whl/cu128
conda install -c conda-forge numpy scipy pandas matplotlib seaborn
conda install conda-forge::torchmetrics
conda install conda-forge::pytorch-lightning
conda install -c conda-forge ipykernel tqdm
conda install conda-forge::scikit-learn
conda install conda-forge::plotly
```

Kernel aufsetzen:
`conda activate vit`
`python -m ipykernel install --user --name vit --display-name "vit"`

zum Testen:
```
import sys
print(sys.executable)
```

Link zum Kaggle-Dataset:
https://www.kaggle.com/competitions/icdar-2026-circleid-writer-identification/data