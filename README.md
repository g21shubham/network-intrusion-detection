# network-intrusion-detection

This is the data set used for The Third International Knowledge Discovery and Data Mining Tools Competition, which was held in conjunction with KDD-99 The Fifth International Conference on Knowledge Discovery and Data Mining. The competition task was to build a network intrusion detector, a predictive model capable of distinguishing between ``bad'' connections, called intrusions or attacks, and ``good'' normal connections. This database contains a standard set of data to be audited, which includes a wide variety of intrusions simulated in a military network environment.

### Data Availability

**BASIC FEATURES OF EACH NETWORK CONNECTION VECTOR**

|Variable|Description
|--------|-----------
|Duration| Length of time duration of the connection 
|Protocol_type| Protocol used in the connection 
|Service| Destination network service used 
|Flag| Status of the connection – Normal or Error 
|Src_bytes| Number of data bytes transferred from source to destination in single connection 
|Dst_bytes| Number of data bytes transferred from destination to source in single connection 
|Land| if source and destination IP addresses and port numbers are equal then, this variable takes value 1 else 0 
|Wrong_fragment| Total number of wrong fragments in this connection 
|Urgent| Number of urgent packets in this connection. Urgent packets are packets with the urgent bit activated

**CONTENT RELATED FEATURES OF EACH NETWORK CONNECTION VECTOR** 
|Variable|Description
|--------|-----------
|Hot| Number of hot indicators in the content such as: entering a system directory, creating programs and executing programs 
|Num_failed _logins| Count of failed login attempts 
|Logged_in Login Status| 1 if successfully logged in; 0 otherwise 
|Num_compromised| Number of compromised conditions 
|Root_shell| 1 if root shell is obtained; 0 otherwise 
|Su_attempted| 1 if su root command attempted or used; 0 otherwise 
|Num_root| Number of root accesses or number of operations performed as a root in the connection 
|Num_file_creations| Number of file creation operations in the connection 
|Num_shells| Number of shell prompts 
|Num_access_files| Number of operations on access control files 
|Num_outbound_cmds| Number of outbound commands in an ftp session 
|Is_hot_login| 1 if the login belongs to the hot list i.e., root or admin; else 0 
|Is_guest_login| 1 if the login is a guest login; 0 otherwise
