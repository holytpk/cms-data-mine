# cms-machinelearning-notebooks
These are notebooks that our PhD candidate Andrew Wildridge and Lingqiang He created to teach incoming freshman/undergraduates machine learning for performing research with the Compact Muon Solenoid experiment at Purdue University. 

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

# Other Comments:

If you run into unsupported software dependency issues, try this: <br>
Go to your scholar notebook terminal, do: <br>
```module load anaconda``` <br>
load a common kernel from the common area, for example, my kernel: <br>
```source activate /depot/cms/conda_envs/he614/Coffea-he614``` <br>
then register this kernel to jupyter: <br>
```python -m ipykernel install --user --name=Coffea-Ling``` <br>
Refresh your notebook then you will see this new kernel with customized conda packages <br>

For those who don't have access to scholar yet ... here's a solution: <br>
1. Go to Google Colab <br>
2. Download HW3.ipynb from Github (https://github.com/holytpk/cms-machinelearning-notebooks/blob/master/HW/HW3.ipynb) and upload it to Colab <br>
3. Install the missing modules <br>
```
!pip3 install vector
!pip3 install hist
!pip3 install uproot
```
4. Get this input.root file and upload it to the session, then change the path of the input file. Make sure the 638M file is completely uploaded before you run the uproot.open command.
