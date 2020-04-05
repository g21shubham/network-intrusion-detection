# network-intrusion-detection

This is the data set used for The Third International Knowledge Discovery and Data Mining Tools Competition, which was held in conjunction with KDD-99 The Fifth International Conference on Knowledge Discovery and Data Mining. The competition task was to build a network intrusion detector, a predictive model capable of distinguishing between bad connections, called intrusions or attacks, and good normal connections. This database contains a standard set of data to be audited, which includes a wide variety of intrusions simulated in a military network environment.

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
|Num_failed_logins| Count of failed login attempts 
|Logged_in_Login Status| 1 if successfully logged in; 0 otherwise 
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

**TIME RELATED TRAFFIC FEATURES OF EACH NETWORK CONNECTION VECTOR**

|Variable|Description
|--------|-----------
|Count| Number of connections to the same destination host as the current connection in the past two seconds 
|Srv_count| Number of connections to the same service (port number) as the current connection in the past two seconds 
|Serror_rate| The percentage of connections that have activated the flag (4) s0, s1, s2 or s3, among the connections aggregated in count (23) 
|Srv_serror_rate| The percentage of connections that have activated the flag (4) s0, s1, s2 or s3, among the connections aggregated in srv_count (24) 
|Rerror_rate| The percentage of connections that have activated the flag (4) REJ, among the connections aggregated in count (23) 
|Srv_rerror_rate| The percentage of connections that have activated the flag (4) REJ, among the connections aggregated in srv_count (24) 
|Same_srv_rate| The percentage of connections that were to the same service, among the connections aggregated in count (23) 
|Diff_srv_rate| The percentage of connections that were to different services, among the connections aggregated in count (23)
|Srv_diff_host_rate| The percentage of connections that were to different destination machines among the connections aggregated in srv_count (24)

**HOST BASED TRAFFIC FEATURES IN A NETWORK CONNECTION VECTOR** 

|Variable|Description
|--------|-----------
|Dst_host_count| Number of connections having the same destination host IP address 
|Dst_host_srv_count| Number of connections having the same port number 
|Dst_host_same_srv_rate| The percentage of connections that were to the same service, among the connections aggregated in dst_host_count (32) 
|Dst_host_diff_ srv_rate| The percentage of connections that were to different services, among the connections aggregated in dst_host_count (32) 
|Dst_host_same_src_port_rate| The percentage of connections that were to the same source port, among the connections aggregated in dst_host_srv_c ount (33) 
|Dst_host_srv_diff_host_rate| The percentage of connections that were to different destination machines, among the connections aggregated in dst_host_srv_count (33) 
|Dst_host_serror_rate| The percentage of connections that have activated the flag (4) s0, s1, s2 or s3, among the connections aggregated in dst_host_count (32) 
|Dst_host_srv_serror_rate| The percent of connections that have activated the flag (4) s0, s1, s2 or s3, among the connections aggregated in dst_host_srv_count (33) 
|Dst_host_rerror_rate| The percentage of connections that have activated the flag (4) REJ, among the connections aggregated in dst_host_count (32) 
|Dst_host_srv_rerror_rate| The percentage of connections that have activated the flag (4) REJ, among the connections aggregated in dst_host_srv_count (33)

**ATTACK CLASS**

1. DOS: Denial of service is an attack category, which depletes the victim‟s resources thereby making it unable to handle legitimate requests – e.g. syn flooding. Relevant features: “source bytes” and “percentage of packets with errors” 

2. Probing: Surveillance and other probing attack‟s objective is to gain information about the remote victim e.g. port scanning. Relevant features: “duration of connection” and “source bytes” 

3. U2R: unauthorized access to local super user (root) privileges is an attack type, by which an attacker uses a normal account to login into a victim system and tries to gain root/administrator privileges by exploiting some vulnerability in the victim e.g. buffer overflow attacks. Relevant features: “number of file creations” and “number of shell prompts invoked,” 

4. R2L: unauthorized access from a remote machine, the attacker intrudes into a remote machine and gains local access of the victim machine. E.g. password guessing Relevant features: Network level features – “duration of connection” and “service requested” and host level features - “number of failed login attempts”

|Attack Class|Attack Type
|--------|-----------
|DOS| back, land, neptune, pod, smurf, teardrop, apache2, udpstorm, processtable, worm(10)
|Probe| satan, ipsweep, nmap, portsweep, mscan, saint(6)
|R2L| guess_password, ftp_write, imap, phf, multihop, warezmaster, warezclient, spy, xlock, xsnoop, snmpguess, snmpgetattack, httptunnel, sendmail, named(16)
|U2R| buffer_overflow, loadmodule, rootkit, perl, sqlattack, xterm, ps(7)
