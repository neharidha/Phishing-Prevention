# Phishing-Prevention
Phishing Prevention | TryHackMe | Solution

What is the Sender Policy Framework (SPF)?

Per dmarcian, "Sender Policy Framework (SPF) is used to authenticate the sender of an email. With an SPF record in place, Internet Service Providers can verify that a mail server is authorized to send email for a specific domain. An SPF record is a DNS TXT record containing a list of the IP addresses that are allowed to send email on behalf of your domain."

What is DKIM?

Per dmarcian, "DKIM stands for DomainKeys Identified Mail and is used for the authentication of an email that’s being sent. Like SPF, DKIM is an open standard for email authentication that is used for DMARC alignment. A DKIM record exists in the DNS, but it is a bit more complicated than SPF. DKIM’s advantage is that it can survive forwarding, which makes it superior to SPF and a foundation for securing your email."
What is DMARC?

Per dmarcian, "DMARC, (Domain-based  Message Authentication Reporting, & Conformance) an open source standard, uses a concept called alignment to tie the result of two other open source standards, SPF (a published list of servers that are authorized to send email on behalf of a domain) and DKIM (a tamper-evident domain seal associated with a piece of email), to the content of an email. If not already deployed, putting a DMARC record into place for your domain will give you feedback that will allow you to troubleshoot your SPF and DKIM configurations if needed."
What is S/MIME?

Per Microsoft, "S/MIME (Secure/Multipurpose internet Mail Extensions) is a widely accepted protocol for sending digitally signed and encrypted messages."

As you can tell from the definition above, the 2 main ingredients for S/MIME are:

Digital Signatures
Encryption

— — — — — — — — — — — — — — — — — — — — — — — — — — — — — — — —

Phishing Prevention

Learn how to defend against phishing emails.

Task1:

After visiting the link in the task, what is the MITRE ID for the “Software Configuration” mitigation technique?

Correct Answer: M1054

— — — — — — — — — — — — — — — — — — — — — — — — — — — — — — — —

Task2:

Referencing the dmarcian SPF syntax table, what prefix character can be added to the “all” mechanism to ensure a “softfail” result?

Correct Answer: ~

What is the meaning of the -all tag?

Correct Answer: fail

— — — — — — — — — — — — — — — — — — — — — — — — — — — — — — — —

Task3:

Which email header shows the status of whether DKIM passed or failed?

Correct Answer: Authentication-Results

— — — — — — — — — — — — — — — — — — — — — — — — — — — — — — — —

Task4:

Which DMARC policy would you use not to accept an email if the message fails the DMARC check?

Correct Answer: p=reject

— — — — — — — — — — — — — — — — — — — — — — — — — — — — — — — —

Task5:

What is nonrepudiation? (The answer is a full sentence, including the “.”)

Correct Answer: The uniqueness of a signature prevents the owner of the signature from disowning the signature.

— — — — — — — — — — — — — — — — — — — — — — — — — — — — — — — —

Task6:

What Wireshark filter can you use to narrow down the packet output using SMTP status codes?

Correct Answer: smtp.response.code

Per the network traffic, what was the message for status code 220? (Do not include the status code (220) in the answer)

Correct Answer: <domain> service ready

One packet shows a response that an email was blocked using spamhaus.org. What were the packet number and status code? (no spaces in your answer)

Correct Answer: 156,553

Based on the packet from the previous question, what was the message regarding the mailbox?

Correct Answer: mailbox name not allowed

What is the status code that will typically precede a SMTP DATA command?

Correct Answer: 354

— — — — — — — — — — — — — — — — — — — — — — — — — — — — — — — —

Task7:

What port is the SMTP traffic using?

Correct Answer: 25

How many packets are specifically SMTP?

Correct Answer: 512

What is the source IP address for all the SMTP traffic?

Correct Answer: 10.12.19.101

What is the filename of the third file attachment?

Correct Answer: attachment.scr

How about the last file attachment?

Correct Answer: .zip

— — — — — — — — — — — — — — — — — — — — — — — — — — — — — — — —

Task8:

Per MITRE ATT&CK, which software is associated with using SMTP and POP3 for C2 communications?

Correct Answer: Zebrocy

— — — — — — — — — — — — — — — — — — — — — — — — — — — — — — — —

Task9:

Per the playbook, what framework was used for the IR process?

Correct Answer:nist

— — — — — — — — — — — — — — — — — — — — — — — — — — — — — — — —
