Miracle

scenario1_silent_failure
Issues: The problem was that the config.yml file was locked(it had no permission at all when i checked with ls -l). Also,the restart script wouln't run.

WHAT I DID : I used chmod 644 on the app/config.yml file so the system could read it. Then i used chmod +x on the restart_service.sh script to make it work.

RESULT: The service finally started.



scenario 2 problem: The backup script was failing because it couldn't get into the secure_data folder and couldn't read the app_key.pem file

WHAT I DID:I gave the folder permission using chom +x so i could enter it. then i used the chmod 400 on the key file to make it readable but safe. i also had to use chmod +x on the backuo.sh script itself.

RESULT: The server is now online


Scenario 3: Issues; the web was showing "forbidden" error. This was because the public_thml folder and the index.html file were not open to the public.

WHAT I DID: I used chmod 755 on the folder and chmod 644 on the index.html file so the web server could see them.

RESULT:The server is now online.
