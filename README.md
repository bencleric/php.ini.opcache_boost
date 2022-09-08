# php.ini.opcache_boost
Change your INI to boost the performance of your website (tested in IONOS and CPANEL)

zend_extension=opcache.so;
magic_quotes_gpc = Off;
register_globals = Off;
default_charset = UTF-8;
memory_limit = 1024M;
max_execution_time = 36000;
upload_max_filesize = 999M;
allow_furl_open =On;
safe_mode=false;
display_errors =Off;
error_reporting =Off;
mysql.connect_timeout = 20;
session.auto_start = Off;
session.use_only_cookies = On;
session.use_cookies = On;
session.use_trans_sid = Off;
session.cookie_httponly = On;op
session.gc_maxlifetime = 3600;
display_startup_errors =Off;
expose_php= off;
post_max_size=256M;
max_input_vars =5000;
max_input_time =-1;
zlib.output_compression=1;
zlib.output_compression_level=9
opcache.enable=1;
opcache.memory_consumption=128;
opcache.interned_strings_buffer=8;
opcache.max_accelerated_files=10000; 
opcache.max_wasted_percentage=5;
opcache.use_cwd=1;
opcache.validate_timestamps=1;
opcache.revalidate_freq=2;
opcache.revalidate_path=0; 
opcache.save_comments=1;	 
opcache.fast_shutdown=0;
opcache.enable_file_override=0; 
opcache.optimization_level=0x7FFEBFFF;
opcache.inherited_hack=1;
opcache.dups_fix=0; 
opcache.blacklist_filename="" 
opcache.max_file_size=0; 
opcache.consistency_checks=0; 
opcache.force_restart_timeout=180; 
opcache.error_log="";
opcache.log_verbosity_level=1;	 
opcache.record_warnings=0;
opcache.preferred_memory_model=""; 
opcache.protect_memory=0;
opcache.mmap_base=NULL
opcache.restrict_api="";
opcache.file_update_protection=2;
opcache.huge_code_pages=0; 
opcache.lockfile_path=/tmp; 
opcache.opt_debug_level=0;
opcache.file_cache=NULL;
opcache.file_cache_only=0; 
opcache.file_cache_consistency_checks=1; 
opcache.file_cache_fallback=1;
opcache.validate_permission=0;
opcache.preload="";
opcache.preload_user="";
opcache.cache_id="";
opcache.jit=tracing;
opcache.jit_buffer_size=0;
opcache.jit_debug=0;
opcache.jit_bisect_limit=0;
opcache.jit_prof_threshold=0.005;
opcache.jit_max_root_traces=1024;
opcache.jit_max_side_traces=128;
opcache.jit_max_exit_counters=8192;
opcache.jit_hot_loop=64;
opcache.jit_hot_func=127;
opcache.jit_hot_return=8;
opcache.jit_hot_side_exit=8;
opcache.jit_blacklist_root_trace=16;
opcache.jit_blacklist_side_trace=8;
opcache.jit_max_loop_unrolls=8;
opcache.jit_max_recursive_calls=2
opcache.jit_max_recursive_returns=2;
opcache.jit_max_polymorphic_calls=2;
opcache.enable_cli=1;
opcache.file_cache=/kunden/homepages/12/yourfolderb/htdocs/yourfoldername.opcache;




in opcache.file_cache = you can find this one in your DOCUMENT_ROOT then just add on the last part .opcache;






if you want to use the OPCACHE only just copy the code below 

zend_extension=opcache.so;
opcache.enable=1;
opcache.memory_consumption=128;
opcache.interned_strings_buffer=8;
opcache.max_accelerated_files=10000; 
opcache.max_wasted_percentage=5;
opcache.use_cwd=1;
opcache.validate_timestamps=1;
opcache.revalidate_freq=2;
opcache.revalidate_path=0; 
opcache.save_comments=1;	 
opcache.fast_shutdown=0;
opcache.enable_file_override=0; 
opcache.optimization_level=0x7FFEBFFF;
opcache.inherited_hack=1;
opcache.dups_fix=0; 
opcache.blacklist_filename="" 
opcache.max_file_size=0; 
opcache.consistency_checks=0; 
opcache.force_restart_timeout=180; 
opcache.error_log="";
opcache.log_verbosity_level=1;	 
opcache.record_warnings=0;
opcache.preferred_memory_model=""; 
opcache.protect_memory=0;
opcache.mmap_base=NULL
opcache.restrict_api="";
opcache.file_update_protection=2;
opcache.huge_code_pages=0; 
opcache.lockfile_path=/tmp; 
opcache.opt_debug_level=0;
opcache.file_cache=NULL;
opcache.file_cache_only=0; 
opcache.file_cache_consistency_checks=1; 
opcache.file_cache_fallback=1;
opcache.validate_permission=0;
opcache.preload="";
opcache.preload_user="";
opcache.cache_id="";
opcache.jit=tracing;
opcache.jit_buffer_size=0;
opcache.jit_debug=0;
opcache.jit_bisect_limit=0;
opcache.jit_prof_threshold=0.005;
opcache.jit_max_root_traces=1024;
opcache.jit_max_side_traces=128;
opcache.jit_max_exit_counters=8192;
opcache.jit_hot_loop=64;
opcache.jit_hot_func=127;
opcache.jit_hot_return=8;
opcache.jit_hot_side_exit=8;
opcache.jit_blacklist_root_trace=16;
opcache.jit_blacklist_side_trace=8;
opcache.jit_max_loop_unrolls=8;
opcache.jit_max_recursive_calls=2
opcache.jit_max_recursive_returns=2;
opcache.jit_max_polymorphic_calls=2;
opcache.enable_cli=1;
opcache.file_cache=/kunden/homepages/12/yourfolderb/htdocs/yourfoldername.opcache;





remember to use the zend engine to enable the opcache | for CPANEL, you need to enable the DSO as your PHP compiler. Be aware, enabling the DSO as your compiler in Cpanel, you wont be able to have a multiple PHP version. in other words. you can only use 1 version.
