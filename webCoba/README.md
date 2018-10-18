# web_project

tamvan programming


#cek instalasi
C:\>python                                                                                                                   Python 2.7 (r27:82525, Jul  4 2010, 07:43:08) [MSC v.1500 64 bit (AMD64)] on win32                                           Type "help", "copyright", "credits" or "license" for more information.                                                       >>> ^D                                                                                                                       ^C                                 C:\>gcloud -v                                                                                                                Google Cloud SDK 192.0.0                                                                                                     bq 2.0.29                                                                                                                    core 2018.03.02                                                                                                              gsutil 4.28  

#langkah pengerjaan
C:\>cd webCoba 

C:\webCoba>gcloud init 

#pilih project atau buat baru
You must log in to continue. Would you like to log in (Y/n)?                                                                                                                                                                               Your browser has been opened to visit:                                                                                                                                                                                                    https://accounts.google.com/o/oauth2/auth?redirect_uri=http%3A%2F%2Flocalhost%3A8085%2F&prompt=select_account&response_type=code&client_id=32555940559.apps.googleusercontent.com&scope=https%3A%2F%2Fwww.googleapis.com%2Fauth%2Fuserinfo.email+https%3A%2F%2Fwww.googleapis.com%2Fauth%2Fcloud-platform+https%3A%2F%2Fwww.googleapis.com%2Fauth%2Fappengine.admin+https%3A%2F%2Fwww.googleapis.com%2Fauth%2Fcompute+https%3A%2F%2Fwww.googleapis.com%2Fauth%2Faccounts.reauth&access_type=offline                                                                                                                                                                                                                                                                       You are logged in as: [chessatirta@gmail.com].                                                                                                                                                                                                            Pick cloud project to use:                                                                                                    [1] chessatcc155610037                                                                                                 [2] fir-demo-project                                                                                                         [3] hellowordchessa                                                                                                        [4] newsig1-166813                                                                                                         [5] pemjavamobile7-1511144503319                                                                         [6] ptcc13chessa                                                                                                             [7] pwa-deploy-999                                                                                                         [8] sig1-1494074939851                                                                                                 [9] Create a new project                                                                                                 Please enter numeric choice or text value (must exactly match list                     item):  1   

#buat app.yaml 
runtime: php55
api_version: 1
threadsafe: true
handlers:
- url: /img
  static_dir: img
- url: /images
  static_dir: images
- url: /pict
  static_dir: pict
- url: /styles
  static_dir: styles
- url: /vendor
  static_dir: vendor
- url: /css
  static_dir: css
- url: /
  script: index.php
- url: /index.php
  script: index.php
- url: /gallery.php
  script: gallery.php
- url: /about.php
  script: about.php


#jalankan dilokal untuk testing program
C:\webCoba>dev_appserver.py app.yaml  

#melakukan deploy aplikasi dan melihat aplikasi di cloud
C:\webCoba>gcloud app deploy 

#memilih server cloud
Please choose the region where you want your App Engine application                                                          located:                                                                                                                                                                                                                              [1] us-west2      (supports standard and flexible)                                                      [2] us-central    (supports standard and flexible)                                                      [3] europe-west2  (supports standard and flexible)                                                 [4] northamerica-northeast1 (supports standard and flexible)                             [5] us-east1      (supports standard and flexible)                                                     [6] us-east4      (supports standard and flexible)                                 
[7] europe-west   (supports standard and flexible)       
[8] asia-northeast1 (supports standard and flexible)     
[9] europe-west3  (supports standard and flexible)                                                 [10] asia-south1   (supports standard and flexible)                                                  [11] australia-southeast1 (supports standard and flexible)           
[12] southamerica-east1 (supports standard and flexible)                                    [13] cancel                              
Please enter your numeric choice:  10       

#melihat app di cloud
C:\webCoba>gcloud app browse                                                                                  Opening [https://chessatcc155610037.appspot.com] in a new tab in your default browser.          