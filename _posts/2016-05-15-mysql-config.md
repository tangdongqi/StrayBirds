---
layout: post
title: MYSQL配置文件
category: Mysql
comments: true
---
```
[root@localhost 3306]# cat  my.cnf 
[client]
port            = 3306
socket          = /data/3306/mysql.sock
character-set-server = utf8
[mysql]
no-auto-rehash

[mysqld]
character-set-server = utf8
user    = mysql
port    = 3306
socket  = /data/3306/mysql.sock
basedir = /application/mysql
datadir = /data/3306/data
open_files_limit    = 1024
back_log = 600
max_connections = 800
max_connect_errors = 3000
table_cache = 614
external-locking = FALSE
max_allowed_packet =8M
sort_buffer_size = 1M
join_buffer_size = 1M
thread_cache_size = 100
thread_concurrency = 2
query_cache_size = 2M
query_cache_limit = 1M
query_cache_min_res_unit = 2k
#default_table_type = InnoDB
thread_stack = 192K
#transaction_isolation = READ-COMMITTED
tmp_table_size = 2M
max_heap_table_size = 2M
long_query_time = 1
#log_long_format
#log-error = /data/3306/error.log
#log-slow-queries = /data/3306/slow.log
pid-file = /data/3306/mysql.pid
log-bin = /data/3306/mysql-bin
relay-log = /data/3306/relay-bin
relay-log-info-file = /data/3306/relay-log.info
binlog_cache_size = 1M
max_binlog_cache_size = 1M
max_binlog_size = 2M
expire_logs_days = 7
key_buffer_size = 16M
read_buffer_size = 1M
read_rnd_buffer_size = 1M
bulk_insert_buffer_size = 1M
#myisam_sort_buffer_size = 1M
#myisam_max_sort_file_size = 10G
#myisam_max_extra_sort_file_size = 10G
#myisam_repair_threads = 1
#myisam_recover

lower_case_table_names = 1
skip-name-resolve
slave-skip-errors = 1032,1062
replicate-ignore-db=mysql

server-id = 1

innodb_additional_mem_pool_size = 4M
innodb_buffer_pool_size = 32M
innodb_data_file_path = ibdata1:128M:autoextend
innodb_file_io_threads = 4
innodb_thread_concurrency = 8
innodb_flush_log_at_trx_commit = 2
innodb_log_buffer_size = 2M
innodb_log_file_size = 4M
innodb_log_files_in_group = 3
innodb_max_dirty_pages_pct = 90
innodb_lock_wait_timeout = 120
innodb_file_per_table = 0
[mysqldump]
quick
max_allowed_packet = 2M

[mysqld_safe]
log-error=/data/3306/mysql_oldboy3306.err
pid-file=/data/3306/mysqld.pid
用这个！
[root@localhost 3307]# cat  my.cnf 
[client]
port            = 3307
socket          = /data/3307/mysql.sock

[mysql]
no-auto-rehash

[mysqld]
user    = mysql
port    = 3307
socket  = /data/3307/mysql.sock
basedir = /application/mysql
datadir = /data/3307/data
open_files_limit    = 1024
back_log = 600
max_connections = 800
max_connect_errors = 3000
table_cache = 614
external-locking = FALSE
max_allowed_packet =8M
sort_buffer_size = 1M
join_buffer_size = 1M
thread_cache_size = 100
thread_concurrency = 2
query_cache_size = 2M
query_cache_limit = 1M
query_cache_min_res_unit = 2k
#default_table_type = InnoDB
thread_stack = 192K
#transaction_isolation = READ-COMMITTED
tmp_table_size = 2M
max_heap_table_size = 2M
#long_query_time = 1
#log_long_format
#log-error = /data/3307/error.log
#log-slow-queries = /data/3307/slow.log
pid-file = /data/3307/mysql.pid
#log-bin = /data/3307/mysql-bin
relay-log = /data/3307/relay-bin
relay-log-info-file = /data/3307/relay-log.info
binlog_cache_size = 1M
max_binlog_cache_size = 1M
max_binlog_size = 2M
expire_logs_days = 7
key_buffer_size = 16M
read_buffer_size = 1M
read_rnd_buffer_size = 1M
bulk_insert_buffer_size = 1M
#myisam_sort_buffer_size = 1M
#myisam_max_sort_file_size = 10G
#myisam_max_extra_sort_file_size = 10G
#myisam_repair_threads = 1
#myisam_recover

lower_case_table_names = 1
skip-name-resolve
slave-skip-errors = 1032,1062
replicate-ignore-db=mysql

server-id = 3

innodb_additional_mem_pool_size = 4M
innodb_buffer_pool_size = 32M
innodb_data_file_path = ibdata1:128M:autoextend
innodb_file_io_threads = 4
innodb_thread_concurrency = 8
innodb_flush_log_at_trx_commit = 2
innodb_log_buffer_size = 2M
innodb_log_file_size = 4M
innodb_log_files_in_group = 3
innodb_max_dirty_pages_pct = 90
innodb_lock_wait_timeout = 120
innodb_file_per_table = 0
[mysqldump]
quick
max_allowed_packet = 2M

[mysqld_safe]
log-error=/data/3307/mysql_oldboy3307.err
pid-file=/data/3307/mysqld.pid

```
一个3306
一个3307
往往(846262263)  17:09:40
直接用生产环境
多实例
三目童子(1606942546)  17:11:08
@北京-悠久之翼 李导麻烦把勘误链接发到公告中。
《跟老男孩学linux运维：Web集群》勘误发布地址：
http://oldboy.blog.51cto.com/2561410/1713128
方便大家，查看，提示出勘误。