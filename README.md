# flickr8k_dataset
Flickr 8K dataset direct download from Kaggle

To download Flickr 8k dataset follow the below steps
1. Go to the below link
   https://www.kaggle.com/datasets/adityajn105/flickr8k

2. Click the download link given above, which will directly download the dataset to your device.

If you do not want to download the dataset to your device, you can save it to your drive from Kaggle by following the below steps
1. Open your Python IDE. Here, I have choosen Google Colab for easy and future reference.
2. Now, mount your drive to Colab so that the path for download directory becomes easy. The code for mounting Google Drive to Google Colab is as follows

   from google.colab import drive
   drive.mount('/gdrive',force_remount=True)  #force remount so that in case if the drive is not mounted, we can successfully mount by force
   %cd /gdrive   #access any path, you can also create a folder or directory of your choice and mention the path of it here

The output may resemble as below

Traceback (most recent call last):
  File "/usr/local/lib/python3.10/dist-packages/IPython/core/interactiveshell.py", line 3553, in run_code
    exec(code_obj, self.user_global_ns, self.user_ns)
  File "<ipython-input-9-830c3a1798b1>", line 1, in <cell line: 1>
    get_ipython().run_line_magic('cd', '"/content/drive/MyDrive/Kaggle"')
  File "/usr/local/lib/python3.10/dist-packages/IPython/core/interactiveshell.py", line 2418, in run_line_magic
    result = fn(*args, **kwargs)
  File "<decorator-gen-85>", line 2, in cd
  File "/usr/local/lib/python3.10/dist-packages/IPython/core/magic.py", line 187, in <lambda>
    call = lambda f, *a, **k: f(*a, **k)
  File "/usr/local/lib/python3.10/dist-packages/IPython/core/magics/osm.py", line 342, in cd
    oldcwd = os.getcwd()

  If any OSError is encountered, add the below code

  import os
  os.environ['KAGGLE_CONFIG_DIR']="/content/drive/MyDrive/Kaggle"   #intialising os environment in the created directory in drive

3. Now, go to kaggle dataset page, and click the 'more options menu' or the 'overflow menu' beside the Download button. Then, copy the API command and execute as below
   #api token of the dataset to be downloaded

  !kaggle datasets download -d adityajn105/flickr8k 

4. The dataset will get downloaded in the drive in zip file format
5. Unzip the folder by using the command below

   !unzip \*.zip  && rm *.zip

Thus, the dataset is now downloaded in your drive and you can access it using the paths of directories in the drive.


