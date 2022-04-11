This is code for CAIL in format of jupyter. it is convident for them who enjoy debugging code in colab or Kaggle
There are a lot codes which cound be found in other MRC task
# How i set the hyperparameters
add or change attribute of ConfigAboutTrainModel
```
class ConfigAboutTrainModel:
    model_path= 'hfl/chinese-electra-180g-base-discriminator'  #huggingface
    train_data_dir='./pocessed_data'
    eval_data_dir='./pocessed_data'
    ground_truth_file='./dev.json'
    output_dir= './output/'
    device = 'cuda'
    batch_size = 8
    #    --do_lower_case \
    #    --logging_steps 200 \
    save_steps = 1000
    gradient_accumulation_steps = 4
    num_train_epochs = 5
    learning_rate = 7e-5
    max_answer_length = 32
    max_seq_length = 512
    max_query_length = 64
    doc_stride = 128
    multi_span_threshold = 0.8
    seed = 42
    weight_decay=0.0
    adam_epsilon=1e-8
    warmup_steps=0
    max_grad_norm=1.0
    logging_steps=50
    save_steps=2000
    
    
args_train=ConfigAboutTrainModel()
```

# CAIL2021_Lee
Notebook version based on https://github.com/china-ai-law-challenge/CAIL2021/tree/main/ydlj
