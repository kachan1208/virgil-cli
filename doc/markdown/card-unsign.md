NAME
====

**card-unsign** -- remove a signature from a Card

SYNOPSIS
========

**virgil card-unsign** -s *file* -z *file* -k *file* \[--\]
\[--version\] \[-h\]

DESCRIPTION
===========

Remove a signature from an already signed Card

OPTIONS
=======

    -s *file*,  --signer *file*
     (required)  Signer's Card

    -z *file*,  --signed *file*
     (required)  Signed Card

    -k *file*,  --key *file*
     (required)  Signer's Private key

    --,  --ignore_rest
     Ignores the rest of the labeled arguments following this flag

    --version
     Displays version information and exits

    -h,  --help
     Displays usage information and exits

EXAMPLES
========

1.  Alice unsigns Bob's Card:

        virgil card-unsign -s alice.vcard -z bob.vcard -k alice/private.vkey

SEE ALSO
========

[`virgil(1)`]()  
[`card-sign(1)`]()