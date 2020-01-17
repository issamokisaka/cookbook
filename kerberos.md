krb5.conf #############################################################################################

# Configuration snippets may be placed in this directory as well
includedir /etc/krb5.conf.d/

[logging]
 default = FILE:/var/kerberos/krb5kdc/kdc.log
 kdc = FILE:/var/kerberos/krb5kdc/kdc.log
 admin_server = FILE:/var/log/kadmind.log

[libdefaults]
 default_realm = HADOOPNEW.COM
 dns_lookup_kdc = false
 dns_lookup_realm = false
 ticket_lifetime = 86400
 renew_lifetime = 604800
 default_tgs_enctypes = arcfour-hmac
 default_tkt_enctypes = arcfour-hmac
 permitted_enctypes = arcfour-hmac 
 forwardable = true
 allow_weak_crypto = true
 udp_preference_limit = 1
 kdc_timeout = 3000

[realms]
 HADOOPNEW.COM = {
  kdc = dxl1big00024.dispositivos.bb.com.br:88
  admin_server = dxl1big00024.dispositivos.bb.com.br:749
  default_domain = HADOOPNEW.COM
 }

 HADOOP.COM = {
  kdc = dxl1big00001.dispositivos.bb.com.br:88
  admin_server = dxl1big00001.dispositivos.bb.com.br:749
  default_domain = HADOOP.COM
 }

[domain_realm]
 dxl1big00024.dispositivos.bb.com.br = HADOOPNEW.COM
 dxl1big00001.dispositivos.bb.com.br = HADOOP.COM
 .hadoopnew.com = HADOOPNEW.COM
 hadoopnew.com = HADOOPNEW.COM
 .hadoop.com = HADOOP.COM
 hadoop.com = HADOOP.COM



kdc.conf #########################################################################################################

[kdcdefaults]
 kdc_ports = 88
 kdc_tcp_ports = 88

[realms]
 HADOOPNEW.COM = {
   #master_key_type = aes256-cts
   acl_file = /var/kerberos/krb5kdc/kadm5.acl
   dict_file = /usr/share/dict/words
   admin_keytab = /var/kerberos/krb5kdc/kadm5.keytab
   supported_enctypes = aes128-cts:normal des3-hmac-sha1:normal arcfour-hmac:normal des-hmac-sha1:normal des-cbc-md5:normal des-cbc-crc:normal
   max_life = 1d
   max_renewable_life = 7d
 }




kadm5.acl #########################################################################################################

*/admin@HADOOPNEW.COM *
cloudera-scm@HADOOPNEW.COM * flume/*@HADOOPNEW.COM
cloudera-scm@HADOOPNEW.COM * hbase/*@HADOOPNEW.COM
cloudera-scm@HADOOPNEW.COM * hdfs/*@HADOOPNEW.COM
cloudera-scm@HADOOPNEW.COM * hive/*@HADOOPNEW.COM
cloudera-scm@HADOOPNEW.COM * httpfs/*@HADOOPNEW.COM
cloudera-scm@HADOOPNEW.COM * HTTP/*@HADOOPNEW.COM
cloudera-scm@HADOOPNEW.COM * hue/*@HADOOPNEW.COM
cloudera-scm@HADOOPNEW.COM * impala/*@HADOOPNEW.COM
cloudera-scm@HADOOPNEW.COM * mapred/*@HADOOPNEW.COM
cloudera-scm@HADOOPNEW.COM * oozie/*@HADOOPNEW.COM
cloudera-scm@HADOOPNEW.COM * solr/*@HADOOPNEW.COM
cloudera-scm@HADOOPNEW.COM * sqoop/*@HADOOPNEW.COM
cloudera-scm@HADOOPNEW.COM * yarn/*@HADOOPNEW.COM
cloudera-scm@HADOOPNEW.COM * zookeeper/*@HADOOPNEW.COM
cloudera-scm@HADOOPNEW.COM * big/*@HADOOPNEW.COM

