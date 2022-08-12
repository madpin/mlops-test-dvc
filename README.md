# MLOpst Testing DVC
Test DVC training skills

## Starting

Check your python version:
```bash
python --version
```
The minimal Python version is 3.7+  

```bash
python3 -m venv ./venv
source venv/bin/activate
pip install -r requirements.txt
```

---
Initializing DVC:
```bash
dvc init
```
---
To add the data:
```bash
dvc add data/titanic_test.csv
```

I'll run with "Auto Staging" so, I'm running `dvc config core.autostage true`.

## Adding Google Drive as remote
[More Info](https://dvc.org/doc/user-guide/setup-google-drive-remote)  
In production, we should use GCS or S3, but for this experiment, I'm using Google Drive.

```bash
dvc remote add --default gdrive \
gdrive://1CwZ_iO51ID2_LUOOc77NMzHUff9VreBb
```

The address: `1CwZ_iO51ID2_LUOOc77NMzHUff9VreBb` is comming from the Google Drive URL, in my case:
https://drive.google.com/drive/u/0/folders/1CwZ_iO51ID2_LUOOc77NMzHUff9VreBb  
And the last piece, is the address.

When trying to run `dvc push`, got an error, that I need `dvc[gdrive]`.
> Changed requirements.txt

Yey, our data is in GDrive 🥳.