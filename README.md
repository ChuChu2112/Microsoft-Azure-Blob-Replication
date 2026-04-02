Imagine you are the Cloud Engineer for a company with global presence, with customers in North Europe and East US. This is totally hypothetical.
Your primary read/write storage account is in North Europe, but you want your customers in the US to have access to your data, but closer to them.
With blob object replication in Azure, you can transfer your data from your primary region to a secondary of your choice.
This is different from the redundancy/backup that Azure geo region redundancy offers. GRS services replicate your data to a secondary region at Microsoft's discretion.
Usually, this every region has a region pair. This is by Microsoft's design. Therefore, your data is only replicated to the region pair for your primary region.
The region paired to your primary region may not be of buisness sense to you.
That is where utilizing object replication is helpful.
For object replication to work, blob versioning must be configured in both storage accounts.

Please note that the json files and pictures have been uploaded in the order that reflects the way object replication should be configured.
# az104publicaccessacct2 was deployed using a modified 'az104publicaccessaccount.json' ARM template
