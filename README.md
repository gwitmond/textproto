# textproto
A copy of the Golang Authors net/textproto package with a small change to make it work for Tor Control socket data

Tor Control sockets use a slightly different layout for multiline responses.
Instead of:
    250-bla/bla
    line 1
    line 2
    .
    250 OK

they use:

    250+bla/bla
    enz.

The minus sign is replaces with a plus sign. So far for compatibility.
This package adds the plus sign as a valid multiline indicator.

Please fork this repository before using. I won't accept pull requests.
