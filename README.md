Step 1: Download [com.republech.accompaniment.json](https://github.com/lynnlynn2023/accompaniment/blob/main/README.md). Edit com.republech.accompaniment.json in TextEdit as shown below. Replace [your_user_name] with the your macos user name. Then copy this .json file to /Library/Google/Chrome/NativeMessagingHosts/
    
    "path": "/Users/[your_user_name]/Library/Application Support/Google/Chrome/Default/Extensions/jpoebpbdhohkboaehnkenbihdiebfhde/1.2_0/host/host.sh",

Step 2: In terminal, use the following two commands to grant execution right to all necessary files. Replace [your_user_name] with the your macos user name.

    cd "/Users/[your_user_name]/Library/Application Support/Google/Chrome/Default/Extensions/jpoebpbdhohkboaehnkenbihdiebfhde/1.2_0/host"
    
    chmod +x *

Step 3: Download [requirements.txt](https://github.com/lynnlynn2023/accompaniment/blob/main/requirements.txt). Execute the following one by one to create a conda virtual environment that has the required libraries in Terminal. Replace [your_download_path] to your real path that contains requirements.txt.
  
    cd /[your_download_path]/requirements.txt
    
    conda create -n accompaniment python=3.9 -y

    conda activate accompaniment
    
    conda install -n accompaniment pip -y
    
    pip install -r requirements.txt
    
Step 4: When the last step of step 3 is finished, type ````which python```` in terminal. The resulting line is the python interpreter path you should put in accompaniment text box.
<img width="1280" alt="Screenshot 2024-03-17 at 9 07 11 PM" src="https://github.com/lynnlynn2023/accompaniment/assets/128745013/4946cae9-0bb9-4884-b860-0398b8f2ded9">
