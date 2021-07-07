# RL_VRP
This implementation is similar to this implementation https://github.com/OptMLGroup/VRP-RL

We added the local neighborhood algorithm 2opt, to improve the final solution.

## Dependencies
* Numpy
* [tensorflow](https://www.tensorflow.org/)>=1.2
* tqdm

## How to Run
### Train
By default, the code is running in the training mode on a single gpu. For running the code, one can use the following command:
```bash
python with2opt.py --task=vrp10
```

### Inference
For running the trained model for inference, it is possible to turn off the training mode. For this, you need to specify the directory of the trained model, otherwise random model will be used for decoding:
```bash
python with2opt.py dataset_name --task=vrp10 --is_train=False --model_dir=./path_to_your_saved_checkpoint
```
where dataset_name is the input dataset

### Logs
All logs are stored in ``result.txt`` file stored in ``./logs/task_date_time`` directory.

Cite: Nazari, M., Oroojlooy, A., Snyder, L. V., and Tak ́ac, M.Deep  reinforcement  learning  for  solving  the  vehiclerouting problem.CoRR, abs/1802.04240, 2018.
URL: http://arxiv.org/abs/1802.04240, https://github.com/OptMLGroup/VRP-RL

