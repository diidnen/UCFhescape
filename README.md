so you can download the data through the download.py and I use Professor's token and you may need to path in download.py

<img width="1268" height="85" alt="image" src="https://github.com/user-attachments/assets/7ef2a07c-29b8-4b16-b74f-b8bcdbcb41ee" />


<img width="650" height="205" alt="image" src="https://github.com/user-attachments/assets/d3432b71-a21c-4f90-a3ab-578da72e4a7f" />
I put the file like this to avoid changing some code in train.py, so here create folder like this and download model from huggingface /uni/pytorch_model.bin.


Nearly all the files do not change. But only changing the file in hescape/experiments/configs which is the experiment config(e.g path, model, blabla)

<img width="1666" height="397" alt="image" src="https://github.com/user-attachments/assets/d6868e4f-c7be-472a-b8d1-81663d59a073" />
So here the only thing to do is to change the csv location on your machine(for different panal, we need to change to the real csv location on our local machine,the code in hescape is modified here)
(or you can directly change the csv location in UCFhescape/experiments/configs/local_config.yaml)

(So basically you can directly change the config at hescape/experiments/configs/local_config.yaml)
<img width="854" height="280" alt="image" src="https://github.com/user-attachments/assets/7e89e6b2-fc0a-41d2-8200-28239a1d8382" />
this is just the default.
And we can modify everything at <img width="1605" height="724" alt="image" src="https://github.com/user-attachments/assets/636e1914-ebdd-4b72-836b-182740bf88ac" />

And there may be some bug when conda the enviroment, I encounter problems like two packages conflicts. See the issues I proposed in hescape(e.g drvi)
And you can apply for 4GPU

So in general. The above is just the how to change the config of the experiments

<img width="1627" height="704" alt="image" src="https://github.com/user-attachments/assets/3d8ffa94-34a2-4930-93ad-72887ab81c8e" />
for here it is in hescape/src/hescape/data_modules/image_gexp_dataset.py， we need to modify it, I have uploaded the npy file


and the running code is  "python experiments/hescape_pretrain/train.py --config-name=local_config.yaml"



So now we focus on uni and 
