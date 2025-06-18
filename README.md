# Csub Jetracer
This is meant to be a detailed Guidelines for future classes who can edit this code to improve it.

# Athena Server
## SSH into Athena
```bash
ssh <username>@athena.cs.csubak.edu
```
## Create and Activate a Virtual Environment (if not already created)

```
# Install virtualenv locally (if not already installed)

pip3 install --user virtualenv


# Create virtual environment

~/.local/bin/virtualenv jupyter_env


# Activate the environment

source jupyter_env/bin/activate

```
## Install JupyterLab
```
pip install --upgrade pip
pip install jupyterlab
```
## Launch JupyterLab
```
jupyter lab --ip=0.0.0.0 --port=9001 --no-browser
```
- If port 9001 is busy, it will auto-assign another open port.
![image](https://github.com/user-attachments/assets/081d2dc7-f11d-4149-9fc0-9d4a4ce88992)
## Open Jupyter in Your Browser

After launching, you'll see a URL like this:
```
http://athena:9001/lab?token=YOUR_UNIQUE_TOKEN
```
- If accessing from another device, replace athena with the full hostname or IP address:
```
http://athena.cs.csubak.edu:9001/lab?token=YOUR_UNIQUE_TOKEN
```
Copy and paste the link into your browser to access JupyterLab.
# Athena JupyterLab
Once you are in the Athena jupyterlab you need to upload your training data and training notebook. You can do this by using
```
git clone https://github.com/ErikGastelum/csubjetracer
```
And going to the notebooks folder and using the modified training jupyter notebooks.
### To transfer files use
```
scp –r /path/to/source_directory <username>@athena.cs.csub.edu:/path/to/target_directory

# Example
# scp –r jetracer/notebooks/road_following_G egastelum@athena.cs.csub.edu:csubjetracer/notebooks/modified training  
```
## Change directory
**It will not work if you do not do this**
![image](https://github.com/user-attachments/assets/8978502c-0005-4570-aecc-67aa1f1f82d6)

## Transfer Model
You can transfer the model using the upload button shown in the picture on your Jetracer. Alternatively you can use
```
scp username@athena.cs.csubak.edu:home/username/jetracer/notebooks/road_following_model#.pth home/jetson/jetracer/notebooks
```
![Screenshot 2025-06-18 at 14-27-53 interactive_… (2) - JupyterLab](https://github.com/user-attachments/assets/8beabf66-ae39-441d-bbe1-c25b803d979d)


Parts of this project are adapted from [jetracer-CollisionAvoidance by chentyra](https://github.com/chentyra/jetracer-CollisionAvoidance) under the MIT License.
