# cms-machinelearning-notebooks
These are notebooks that our PhD candidate Andrew Wildridge created to teach incoming freshman/undergraduates machine learning for performing research with the Compact Muon Solenoid experiment at Purdue University. 

Some of this has been inspired from: https://github.com/Atcold/pytorch-Deep-Learning, Thank you Alfredo for this amazing resource and being one of the first people to truly introduce me to machine learning. However, a lot of the mathematics and details in this course I felt were assumed. Since this is for freshman I decided to create my own resource to try and build the foundations of machine learning from the ground up in a nice and conversational approach through Jupyter notebooks. Hopefully others will find these useful.

Lab 0 has some information specific to students taking the research class at Purdue, but may be a nice Bash introduction for some people. 
Lab 1 is mostly Alfredo's PyTorch notebook with some added explanations here and there to try and bridge the knowledge gap.

Lab x is the spiral classifier adapted from Alfredo's PyTorch minicouse. However, I have greatly expanded upon this as I think this is a very nice, simple example that is non-trivial to get very high generalization with a deep neural network and therefore excellent for educating newcomers to machine learning on the limitations and the challenges to using deep learning effectively.

# Connecting to Jupyter Lab/Notebook
First <br>
```
ssh <user_name>@scholar.rcac.purdue.edu -L <port_number>:localhost:<port_number>
```
The default port is 8888, however, sometimes it will fail if it is occupied locally. Try any other number above 8000. <br>
For example:
```
ssh he614@scholar.rcac.purdue.edu -L 8868:localhost:8868
```

After logging in, do <br>
```
module load anaconda
```
```
jupyter lab --port 8868
```
Then copy the url to your favorite browser. It's the best to practice to connect to a remote server via ssh-keys: https://www.rcac.purdue.edu/knowledge/scholar/accounts/login/sshkeys. <br>

-Ling 
