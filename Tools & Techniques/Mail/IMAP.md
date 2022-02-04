# Useful IMAP commands

## Logging in

```bash
a LOGIN <user> <password>
```

## Accessing mailboxes and mail

```bash
# IMAP seems to either need 1 or 2 character preceeding commands

# List mailboxes
01 LIST "" *

# Select a mailbox (Inbox in this case).  Can also use "EXAMINE" if just want to view info
02 SELECT Inbox

# View header information of an email (Email #1)
03 FETCH 1 (FLAGS BODY[HEADER.FIELDS (DATE FROM SUBJECT)]) 

# Retrieve text of an email (Email #1)
04 FETCH 1 (BODY[TEXT])
```

