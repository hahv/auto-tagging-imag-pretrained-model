# auto-tagging-imag-pretrained-model
Auto tagging images with Google OpenImage pre-trained model (v2)

**Links:** [OpenImage](https://github.com/openimages/dataset), [Pretrained model used in this project](https://storage.googleapis.com/openimages/web/extras.html)

### Require Python 2.7, [pip](https://pip.pypa.io/en/stable/installing/)

![GitHub Repo stars](https://img.shields.io/github/stars/hahv/auto-tagging-imag-pretrained-model?style=social), ![Python version](https://img.shields.io/badge/python-2.7-brightgreen)

1. Install python virtual environment

    * Install
    ```
    pip install virtualenv
    ```
    * create folder for virtualen: Go to current project folder **auto-tagging-imag-pretrained-model** folder
    ```
    cd auto-tagging-imag-pretrained-model/
    virtualenv venv
    ```

    Where **venv** is a directory to place the new virtual environment

    * Active virtualen: Go to **venv** folder
    ```
    cd venv/
    source bin/activate
    ```
2. Install all the python packages requirements of the project

    ```
        pip install -r /path/to/requirements.txt

    ```
    The **requirements.txt** is in the project folder.
    You may get SSL problem (unable to install), you should update pip by run this command (after active virtual environment):

      ```
        curl https://bootstrap.pypa.io/get-pip.py | python
    ```
    **NOTE**: This uses **Tensorflow** (An open source machine learning framework) with CPU; if you have GPU please follow this [instruction link](https://www.tensorflow.org/install/install_linux) to install Tensorflow with GPU. Running tagging process on GPU is much **FASTER** than running on CPU.

3. Download OpenImage pretrained model (V2) at the following url:
[Download link](https://www.dropbox.com/s/kx5n8bjwhl9qecx/pretrain_open_images.zip?dl=0)
Unzip the zip file and put all the files inside it into folder **pretrain_open_images** of the project

4. Run the test.py for testing tagging images in folder **test_images** and get the tagging result in **result.json** file. **Note**: Before running, the virtual environment must be active (*see Step 1 above*)
Result in json format looks like this:
![alt text](https://www.dropbox.com/s/ziw2ihn7nxpkmig/tagging_result.png?raw=1 "Tagging result")
