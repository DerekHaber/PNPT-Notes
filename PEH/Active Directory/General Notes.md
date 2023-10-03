
Active Directory is a Microsoft identity management service

At least 95% of Fortune 1000 companies use AD

AD can be exploited without ever attacking patchable exploits.
>Instead, we abuse features, trusts, components, and more


Physical components:
>Domain controllers -
>	Hosts the AD directory store
>	Provides authentication and authorization
>	Replicate updates to other domain controllers in the domain and forest
>	Allow administrative access to manage user accounts and network resources
>AD DS Directory Store
>	Consists of the Ntds.dit file
>	Default stored in %SystemRoot%\NTDS folder on DC
>	Only accessible through DC processes and protocols
>Global catalog server
>Read-Only

Logical components:
>Schema
>	Defines objects and enforces object rules
>	Class object - user, computer, printer
>	Attribute - Display name
>Domain
>	Boundary for applying policies to groups of objects
>	replication boundary for replicating data between DCs
>	Auth boundary to limit scope of access to resources
>Tree:
>	Hierarchy of domains with parent and child domains
>	Defaults two-way transitive trust
>Forest:
>	Share commen schema
>	share partition
>	global catalog shared
>	trust between all domains
>	share Enterprise Admins and Schema Admins
>Trusts:
>	Directional - trusts from domain to domain
>	Transitive - includes other domains trusted by the original domain (within forests)

