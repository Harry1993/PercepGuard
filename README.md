# PercepGuard

This repository demonstrates the LSTM bounding box sequence classifier of our
[PercepGuard
paper](https://www.usenix.org/conference/usenixsecurity23/presentation/man):

```
@inproceedings{man2023percepguard,
  title={That Person Moves Like A Car: Misclassification Attack Detection for
         Autonomous Systems Using Spatiotemporal Consistency},
  author={Man, Yanmao and Muller, Raymond and  Li, Ming and Celik, Z. Berkay
          and Gerdes, Ryan},
  booktitle={USENIX Security Symposium},
  year={2023}
}
```

The scripts are written in Python 3, with dependencies
```
tensorflow == 2.1.0
numpy == 1.18.5
```

The pre-trained model for the BDD100K MOT dataset can be downloaded from
[Google Drive](https://drive.google.com/file/d/1XBJB4kghlI4ysbiUF5ftGRBPIgVmk6ZF).
Unzip it into `models`:
```
mkdir models
unzip /path/to/bdd100k.zip -d models
```

To use the pre-trained model, see `demo.py` for a simple example:
```
python3 demo.py
```

This outputs `[[0.01 0.04 0.82 0.01 0.12]]`, where the `car` category has
the highest score.
