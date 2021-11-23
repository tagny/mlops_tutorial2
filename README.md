# mlops_tutorial2
https://www.youtube.com/watch?v=kZKAuShWF0s&amp;ab_channel=DVCorg


* create a py36 env
* install dvc: `pip install dvc[gdrive]`  
  * `[gdrive]` to enable dvc to push data changes to Google Drive
* clone your git repo
* init dvc: `dvc init`
* setup a google drive directory: `data/remote`
* copy the ID of the google drive dir: https://drive.google.com/drive/folders/**1RivB9UUkDDlr2gpfl7l5zxSNdqPmx3kO** 
* add that dir as a dvc remote dir: `dvc remote add -d myremote gdrive://1RivB9UUkDDlr2gpfl7l5zxSNdqPmx3kO`
  * `-d`: means the default remote
* See what have been created by dvc
  * `git add .`
  * `git commit -m "first commit"`
  * `git push`
  * go check on GitHub repo
* Download the data: `python get_data.py`
* list the files with their size: `ls -lh`
* add data to dvc stage: `dvc add data.csv`
* start tracking the changes: 
  * `git add .gitignore data.csv.dvc`
  * `git commit -m "start tracking data"`
  * `git push`
* push data: 
  * `dvc push`
  * then give permission to dvc to access your Google Drive
  
  
* on a new computer, to recover the source code and the data
  * for source-code: `git clone https://github.com/tagny/mlops_tutorial2.git`
  * for data: 
    * `cd mlops_tutorial2`
    * `dvc pull data.csv`
    * then give permission to dvc to access your Google Drive