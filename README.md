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