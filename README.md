Step 1: Find chrome extension ID that is unique to local machine and the extension. Type chrome://extensions/ in chrome address bar. Your extension id is the long string as highlighted in picture below.
<img width="1280" alt="Screenshot 2024-03-17 at 7 18 58 PM" src="https://github.com/lynnlynn2023/accompaniment/assets/128745013/17bb535d-6541-4854-9e43-76eb6318eb31">

Step 2: Edit com.republech.accompaniment.json in TextEdit as shown below. Replace [your_user_name] with the your macos user name. Replace [your_extension_id] with the extension id found in Step 1. Then copy this .json file to /Library/Google/Chrome/NativeMessagingHosts/
    
    "path": "/Users/[your_user_name]/Library/Application Support/Google/Chrome/Default/Extensions/[your_extension_id]/1.2_0/host/host.sh",

    "allowed_origins": : ["chrome-extension://[your_extension_id]/"]


Step 3: Create a conda virtual environment that has the required libraries in Terminal. Execute the following one by one.
  
    cd /path/to/requirements.txt
    
    conda create -n accompaniment python=3.9 -y

    conda activate accompaniment
    
    conda install -n accompaniment pip -y
    
    pip install -r requirements.txt
    
Step 4: When the last step of step 3 is finished, type ````which python```` in terminal. The resulting line is the python interpreter path you should put in accompaniment text box.
<img width="1280" alt="Screenshot 2024-03-17 at 9 07 11 PM" src="https://github.com/lynnlynn2023/accompaniment/assets/128745013/4946cae9-0bb9-4884-b860-0398b8f2ded9">
