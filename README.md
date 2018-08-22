# mysqlmon

        ussage ./mysqlmon.sh [username] [password] [host] [sid:mysql] <port=3306> <runtime=3600>
  
output is either all global stats or just read/delete/update/insert/log_write_bytes
which depend on the flag in the script  all_global_status

        all_global_status=0
  
output looks like

         ------------------------- 
        Innodb_buffer_pool_read_requests        ,          0
        Innodb_buffer_pool_load_status          ,          0
        Innodb_log_write_requests               ,          0
        Innodb_data_writes                      ,          0
        ...
        
all global stats

        all_global_status=1
  
output looks like

            deleted   inserted    updated os_log_written       read
                  0         50          0          0         52
                942       1012       2826    2720768     395195
                852        887       2558    2364416     357332
