# Tay
Trained GPT-2 bot on 4chan /pol/ shitposts.

120 MB 4chan.txt used to train the bot (Inside /src/ folder)

This is the trained model, on gpt-2.

10100 epochs, trained on google collab pro.

Edit TAY WORKING CODE.py with the folder location inside the script (the %cd jupiter command).

Try to run it on google collab or jupiter notebook.

If running directly on python, remove the lines starting with !pip which you need to run them on console, using python 3.5 (because gpt-2 uses tensorflow 1.15 and it can only be installed with pip from python 3.5)

The cannot find tensorflow.contrib error means you have tensorflow 2 which removed .contrib, you need tensorflow 1.15


# TUTORIAL FOR DUMMIES

0) Make sure you can run Tensorflow with your GPU

1) Install these:

Anaconda 4.2 https://repo.anaconda.com/archive/

Visual Tools for C++ 14 https://visualstudio.microsoft.com/thank-you-downloading-visual-studio/?sku=BuildTools&rel=16

2) Run these commands on your console:

cd (copy paste the repository folder address here)

conda install python==3.5

py -m conda install tensorflow==1.5.0

py -m conda install numpy

pip install -r requirements.txt

export PYTHONIOENCODING=UTF-8

cd /src/

3) Run this command (inside the /src/ folder) if you want just random samples:

py generate_unconditional_samples.py --length=20

4) Run this command to have interactivity with the model (change length number to your liking):

py interactive_conditional_samples.py --length=60 --top_k=40
