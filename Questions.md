
### Adresses

I always had a question of what would be the relation between, IP's, email addresses and user@local_host

Tho I'm not a great fan of AI, it comes really handy when trying to answer these kind of questions.

I went ahead, made a simple search and the resume I can make of it is:

	example.com -> 190.190.00.01

	user @example.com -> user@190.190.00.01

Till here everything seems trivial, DNS just takes place and the magic happens.

My question is, why would a host name resemble so much this shape, simply lacking the domain.

It turns out there are 2 main points here that I discovered.

	MX Records
	Machine is DNS registered

**MX Records** - Mail Exchange Records:

DNS records that specify which mail servers are responsible for accepting email messages on behalf of a domain. Like a postal sorting system.

For this a `gmail.com` wont come to a `hotmail.com` account.

These take 2 parameters:

	Priority
	Mail Server Domain -> example@example.com

The *Mail Server Domain* must resolve an A or AAAA record (I didnt go further than here in this topic)


**Machine is DNS registered**

Which makes all the sense. the machine already has all the needed tools in order to be an email service provider for itself.

It has:

	ip
	ip assigned host
	user

Now my question is, what do we really want domain providers and the little *.something* for.

Is to "manage" the internet and make sure there wont be 2 times the same host assigned to one IP?

Do we really need to pay for anything if we can do all the hosting?

