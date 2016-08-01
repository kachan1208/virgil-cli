NAME
====

**public-key-revoke** -- revoke the Card from the Public Keys Service

SYNOPSIS
========

        virgil public-key-revoke  {-f <file> ... |-d <arg> ... } -e <arg> -a <arg> -k
                          <file> [-p <arg>] [-V] [--] [--version] [-h]

DESCRIPTION
===========

Revoke a group of Cards from the Public Keys Service connected by
public-key-id + card-id of one of the Cards from the group

OPTIONS
=======

        -f <file>,  --validated-identity <file>  (accepted multiple times)
         (OR required)  ValidatedIdentity
             -- OR --
        -d <arg>,  --identity <arg>  (accepted multiple times)
         (OR required)  Identity user


        -e <arg>,  --public-key-id <arg>
         (required)  Public Key identifier


        -a <arg>,  --card-id <arg>
         (required)  virgil Card identifier

        -k <file>,  --key <file>
         (required)  Private key

        -p <arg>,  --private-key-password <arg>
         Password to be used for Private Key encryption.

        -V,  --VERBOSE
         Show detailed information

        --,  --ignore_rest
         Ignores the rest of the labeled arguments following this flag.

        --version
         Displays version information and exits.

        -h,  --help
         Displays usage information and exits.

EXAMPLES
========

1.  Revoke a chain of cards with confirmed identities connected by
    public-key-id from virgil Keys Service::

        virgil public-key-revoke -e <public_key_id> -a <card_id> -k alice/private.key -f alice/validated-identity.txt

2.  Revoke a chain of cards with unconfirmed identities connected by
    public-key-id from virgil Keys Service:

        virgil public-key-revoke -e <public_key_id> -a <card_id> -k alice/private.key -d email:user@domain.com

SEE ALSO
========

virgil(1)  
card-create-global(1)  
card-create-private(1)  
public-key-revoke(1)