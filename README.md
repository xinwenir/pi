# pi
1. Download files from server:
   
    scp username@servername:/path/filename /var/www/local_dir (local directory)
   
Example:

    scp root@192.168.1.100:/var/www/text.txt /var/www/local_dir
    
3. Upload local files to server:
   
    scp /path/filename username@servername:/path
   
Example:

    scp /var/www/text.php root@192.168.1.100:/var/www/server_dir (server directory)    
    
5. Download the entire directory from server:
   
    scp -r lab321@172.21.243.181:/home/lab321/zxw/project/ (remote directory) /mnt/e/Users/xinwe/Desktop/Recent_file/GLFtest_V2_0 (local directory)

7. Upload the local entire director to server:
   
    scp -r  /mnt/e/Users/xinwe/Desktop/Recent_file/GLFtest_V2_0 (local directory) lab321@172.21.243.181:/home/lab321/zxw/project/ (remote directory)

Send files to server:

    scp -r  /mnt/e/Users/xinwe/Desktop/Recent_file/GLFtest_V2_0 lab321@172.21.243.181:/home/lab321/zxw/project/

    scp -r  /mnt/d/Desktop/NCFOSMC_CTRL_V1 lab321@172.21.149.232:/home/lab321/zxw/project/

Request files from server:

    scp -r lab321@172.21.243.181:/home/lab321/zxw/project/GLFtest_V2_0 /mnt/e/Users/xinwe/Desktop/Recent_file/

    scp -r lab321@172.21.243.181:/home/lab321/zxw/project/SSM_Implement_test_V3_2_2_3 /mnt/e/Users/xinwe/Desktop/Recentfiles/Revised_Submitting_TCAS-I
