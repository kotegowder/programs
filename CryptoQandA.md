Some of the crypto items 

1.	What is Digital Signature?

	<details><summary>Click for answer!</summary>

	~~~
	a.	Person A has been given two keys. One of A's keys is called a Public Key, the other is called a Private Key.

	b.	A's Co-workers B, C and D.

	c.	A's Public Key is available to anyone who needs it, but he keeps his Private Key to himself.

	d.	Keys are used to encrypt information. Encrypting information means "scrambling it up", so that only a person with the 
		appropriate key can make it readble again. Either one of A's two keys can encrypt data, and the other key can decrypt
		that data.

	e.	Person D can encrypt a message using A's Public Key. A uses his Private Key to decrypt the message.
		Any A's coworkers might have access to the message person D encrypted, but without A's Private Key, the data is worthless.

	f.	With his Private Key and right software, person A can put digital signature on documents and other data.

		A digital signature is a stamp person A places on the data which is unique to him, and is very difficult to 
		forge. In addition, the signature assures that any changes made to the data that has been signed can not go 
		undetected.

	g.	To sign a document, person A's software will crunch down the data into just a few lines by a process called **hashing**.
		These few lines are called a **message digest**. Note that it is not possible to change a message digest back into the 
		original data from which it was created.

	h.	Person A's software then encrypts the message digest with his private key. The result is the **digital signature**.

	i.	Finally, person A's software appends the digital signature to document. All of the data that was hashed has been signed.

	j.	Person A now passes the document on to person B.

	k.	First, person B's software decrypts the signature (using person A's Public Key) changing it back into a message digest.
		If this worked, then it proves that person A signed the document, because only person A has his Private Key. 

		Person B's software then hashes the document data into a message digest. If the message digest is same as the
		message digest created when the signature was decrypted, then person B knows that the signed data has not been changed.

	l.	Person C (dissatisfied employee) wished to deceive person B. Person C makes sure that person B receives a signed message 
		and a Public Key that appears to belong to person A. Without person B knowledge, person C deceitfully send a key pair he 
		created using person A's name. Short of receiving person A's public key from him in person, how can person B be sure that 
		person A's publick key is authentic?

	m.	It just so happens that person D works at the company's certificate authority center. Person D can create a digital signature 
		for person A simply by signing person A's public key as well as some information about person A.

	n.	Now person A's co-workers can check A's trusted certificate to make sure that his Public Key truly belongs to him. 
		In fact, no one at A's company accepts a signature for which there does not exist a certificate generated by perosn D. 
		This gives person D the power to revoke signatures if private keys are compramised, or no longer needed. There are even more
		widely accepted certifcate authorities that certify person D.

	o.	Let's say that person A sends a signed document to person B.
		To certify the signature on the document, person B's software first uses person D's (the certificate authorities) public 
		key to check the signature on perons A's certificate. Successfull decryption of the certificate proves that person D created it.

		After the certificate is decrypted, person B's software can check if person A is in good standing with the 
		certificate authority and that all of the certificate information concerning A's identity has not been altered.

		Person B's software then takes A's public key from the certificate and uses it to check A's signature. 
		If A's public key decrypts the signature successfully, then person B is assured that the signature was 
		created using A's private key, for person D has certified the matching public key. And of course, if the 
		signature is valid, then we know that person C didn't try to change the signed content.
	~~~

	</details/
