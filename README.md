# CommonLit-Evaluate-Student-Summaries
Kaggle competition to evaluate summaries written by students 

#Context . 

The competition describe the most common type of ML problem which is regression . But in this case we need to predict two labels namely content and wording. 
Go given a passage and title written by a student aim is to predict the two given labels . So its a regression problem.

#Model Approach<br> 

I have used Roberta-base model as the embedding model . The weights of this model where kept frozen and Neural network was build on top of it to predict the labels


# What I learned from this project 

Usually I have tensorflow higher level api to build and train NN . But for this model I plan to deep dive a bit deeper in TF.
-  I build custom Dataloaders
- Metric 
- Loss function <br>

Some of this was required since the compition asked for metrics and loss function which where not standard . <br>
Also to speed up traning I went with GPU and I learned to used mixed-precision trainng . <br>

To enable mixed precision I had to write custom training loop in TF as well . 

# Result 

The metric for this competition is given below . 
MCRMSE=1𝑁𝑡∑𝑗=1𝑁𝑡(1𝑛∑𝑖=1𝑛(𝑦𝑖𝑗−𝑦̂ 𝑖𝑗)2)1/2

My first submission gave me a score of 0.546 with the no 1 rank being at 0.42 
