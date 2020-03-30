## Domain Name Service Server
DNS resolves an IP address to a hostname through the process called name resolution.

* An **A record** resolves hostnames to IP addresses.
* A **PTR record** resolves an IP address to the hostname. They reside in a reverse lookup zone/table in the server.
* The **MX record** translates mail records. The MX record points to the mail exchanger for a particulr host. Mail exchangers are listed in order in the record, with a priority code that indicates the order in which they should be accessed by other mail-delivery systems.

If the first priority mail exchanger doesn't respond in a given amount of time, the mail delivery system tries the second one..etc.
* hostname.company.com  IN     MX     10 mail.company.com.
* hostname.company.com  IN     MX     20 mail2.company.com.
* hostname.company.com  IN     MX     30 mail3.company.com.

The **CNAME - canonical name (CNAME) record** allows hosts to have multiple names. Suppose yoour webserver hast the hostname www and you want that machine to also have the name ftp so that users can FTP to your system. A CNAME record allows this.

* www.company.com       IN     A       204.176.47.2
* ftp.company.com       IN     CNAME   www.company.com.  

Organizing these record types together in a zone file or DNS table....

* mail.company.com.     IN     A       204.176.47.9
* mail2.company.com.    IN     A       204.176.47.21
* mail3.company.com.    IN     A       204.176.47.89
* yourhost.company.com. IN     MX      10 mail.company.com.
* yourhost.company.com. IN     MX      20 mail2.company.com.
* yourhost.company.com. IN     MX      30 mail3.company.com.
* www.company.com.      IN     A       204.176.47.2
* ftp.company.com.      IN     CNAME   www.company.com.
