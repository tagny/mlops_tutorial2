# mlops_tutorial2
https://www.youtube.com/watch?v=kZKAuShWF0s&amp;ab_channel=DVCorg


* create a py36 env
* install dvc: `pip install dvc`
* clone your git repo
* init dvc: `dvc init`
* setup a google drive directory: `data/remote`
* copy the ID of the google drive dir: https://drive.google.com/drive/folders/**1RivB9UUkDDlr2gpfl7l5zxSNdqPmx3kO** 
* add that dir as a dvc remote dir: `dvc remote add -d myremote gdrive://1RivB9UUkDDlr2gpfl7l5zxSNdqPmx3kO`
  * `-d`: means the default remote