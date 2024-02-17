# yuque-to-markdown

> status: it works

Simple convertor, it converts `.lakebook` to markdown files, and all the outputs is in `markdown` format.
The structure of the output folder is the same as the structure of the book in yuque.

## How to install

```bash
# Make sure your Python3 is installed
python3 -V

# Clone this repo
git clone git@github.com:alswl/yuque2markdown.git
cd yuque2markdown

# Install packages
pip3 install -r requirements.txt
```


## How to use

1. Go to your yuque book configuration page, click `设置` button
2. Click `导出` button, and download the `.lakebook` file
3. Using this tool to convert it to markdown files

```bash
# simple ,default, 在本地生成 file_name 目录，内容为你的下载。 默认下载图片。
python3 yuque2markdown.py /path/to/your/lakebook/file_name.lakefile 


python3 yuque2markdown.py /path/to/your/lakebook/file.lakefile /path/to/your/output/folder --download-image

# show your converted files
tree /path/to/your/output/folder
```

CLI Description:

```shell
python yuque2markdown.py --help
usage: yuque2markdown.py [-h] [--download-image] lakebook output

Convert Yuque doc to markdown

positional arguments:
  lakebook          Lakebook file
  output            Output directory

options:
  -h, --help        show this help message and exit
  --download-image  Download images to local
```

## TODO

- [x] Convert HTML to markdown
- [x] Toc structed convert
- [x] Fetch images
