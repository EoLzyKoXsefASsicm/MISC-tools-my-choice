# Get help

`> conda config -h`
`> conda -h`

# Pandoc intergraded

run this in Anaconda Powershell Prompt


`> pandoc --help`

pandoc file.xx(support drag-and-drop) -o C:\Users\Administrator\Desktop\file.docx


# Import your own python files in Anaconda3 should follow this routine:

1. get path in iPython:

    `> import sys`<br>
    `> `<br>
    `> sys.path`<br>

    `> ['C:\\Users\\Administrator',`<br>
    `>  'D:\\Administrator\\Anaconda3\\python37.zip',`<br>
    `>  'D:\\Administrator\\Anaconda3\\DLLs',`<br>
    `>  'D:\\Administrator\\Anaconda3\\lib',`<br>
    `>  'D:\\Administrator\\Anaconda3',`<br>
    `>  '',`<br>
    `>  'D:\\Administrator\\Anaconda3\\lib\\site-packages',`<br>
    `>  'D:\\Administrator\\Anaconda3\\lib\\site-packages\\win32',`<br>
    `>  'D:\\Administrator\\Anaconda3\\lib\\site-packages\\win32\\lib',`<br>
    `>  'D:\\Administrator\\Anaconda3\\lib\\site-packages\\Pythonwin',`<br>
    `>  'D:\\Administrator\\Anaconda3\\lib\\site-packages\\IPython\\extensions',`<br>
    `>  'C:\\Users\\Administrator\\.ipython']`<br>
 
 2. put your own python files here:
 
    `~\\Anaconda3\\lib\\site-packages`

# Change channels for faster access:

## Windows:

### Check channels.

`> conda info`

`> conda config --show-sources`

`> conda config --show`

### Change all channels to CN's channels.

1. create the file `.condarc`:

    `> conda config --set show_channel_urls yes`

2. rewrite the file `.condarc` with this:

    ```
	channels:
	  - defaults
	show_channel_urls: true
	default_channels:
	  - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main
	  - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free
	  - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/r
	  - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/pro
	  - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/msys2
	custom_channels:
	  conda-forge: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
	  msys2: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
	  bioconda: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
	  menpo: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
	  pytorch: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
	  simpleitk: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
    ```
3. Run the following cmd to clean cahce.

    `> conda clean -i`

4. Welcome to the 1000hp club！
    
    `> conda install selenium`

### Recover all channels to defaults:

   - delete the file `.condarc`

# Update packages
	> conda update conda
	> conda update anaconda
	> conda update --all
