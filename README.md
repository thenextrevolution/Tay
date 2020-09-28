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

1) Install python 3.5

2) Run these commands on your console:
cd (copy paste the repository folder address here)
pip install tensorflow==1.15.0
pip install -r requirements.txt
export PYTHONIOENCODING=UTF-8

2.5) Run this command on the console:
cd /src/

3) Run this command (inside the /src/ folder) if you want just random samples:
python generate_unconditional_samples.py --length=20

4) Run this command to have interactivity with the model (change length number to your liking):
!python interactive_conditional_samples.py --length=60 --top_k=40
