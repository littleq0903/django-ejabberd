django-ejabberd
===============

Ejabberd copy for extending functions of Django binding.ejabberd - High-Performance Enterprise Instant Messaging Server 

Quickstart guide


0. Requirements

To compile ejabberd you need:
 - GNU Make
 - GCC
 - Erlang/OTP R12B-5 or higher. Recommended: R12B-5, R13B04 and R14B01.
   Avoid R14A and R14B.
 - exmpp 0.9.6 or higher
 - OpenSSL 0.9.8 or higher, for STARTTLS, SASL and SSL encryption.
 - Erlang mysql library. Optional. MySQL authentication/storage.
 - Erlang pgsql library. Optional. PostgreSQL authentication/storage.
 - PAM library. Optional. For Pluggable Authentication Modules (PAM).
 - ESASL library. Optional. For SASL GSSAPI authentication.
 - ImageMagick's Convert program. Optional. For CAPTCHA challenges.


1. Compile and install on *nix systems

To compile ejabberd, go to the directory src/ and execute the commands:
  ./configure
  make

If you get an error like:
  ./configure: No such file or directory
the solution is to first execute:
  aclocal
  autoconf

To install ejabberd, run this command with system administrator rights
(root user):

  sudo make install

These commands will:
 - Install the configuration files in /etc/ejabberd/
 - Install ejabberd binary, header and runtime files in /lib/ejabberd/
 - Install the administration script: /sbin/ejabberdctl
 - Install ejabberd documentation in /share/doc/ejabberd/
 - Create a spool directory: /var/lib/ejabberd/
 - Create a directory for log files: /var/log/ejabberd/


2. Start ejabberd

You can use the ejabberdctl command line administration script to
start and stop ejabberd. For example:
  ejabberdctl start


For detailed information please refer to the
ejabberd Installation and Operation Guide
