Lets take a real example of crowdstrike and see how one routine content update for a security sensor led to the downtime of millions of windows PC's globally. 

Consider in Crowdstrike there was an individual who wants to make a routine content update to a security sensor. In this case the individual who wants to make the change is considered as the ==🟠owner== in this process.

The ==🟠owner== typically will not perform the actual change and will instead fill out the form to make the change and will only be kept in the loop as more steps are completed and decisions are taken regarding the requested change.

After the owners come the ==🟠stakeholders==, these are the ones who will be impacted by this change, this could be one person or the entire organization who will face the effects of this change. The IT team will have to research and document each system and individual who will be affected by this change. In case of the content update, this would be both crowdstrike and the clients using crowdstrike on their machines. Unfortunately in this case the clients were not informed of the update and due to an internal error millions of Windows machines got the blue screen of death error making business operations unable to proceed.

The next step in the process is to conduct ==🟠impact analysis== for the process. This involves determining a risk value associated with the change typically ==🟡'high', 'medium' or 'low'.== These risks could be that the fix would not fix anything, the risk could break something else which in the case of crowdstrike it did etc. However the flip side of the coin must also be considered what are the risks of not making the changes. These may include a security vulnerability due to an old version, unexpected downtime on other services or even application unavailability.

Considering the risks you may not want to directly implement the fix to the production system but instead first test it on a [[Sandbox]] environment where the risk would be minimal. Even after confirming that there is no risk after applying the fix it is always good to have a backup plan in case the fix breaks something else in production so that you can always rollback to the previous working version as and when required. 

Even after taking every necessary precaution it is always good practice to have a ==🟠backout plan== as some changes are difficult to revert. This backout plans consists of having the entire system backed up in a safe location so that it easy to restart services again from the backup taken and to ensure there is minimal business impact.

Finally we have the ==🟠Maintenance Window==, getting approval for the change is usually an easy task which may or may not take a lot of time. The task that typically takes the most amount of time is deciding on when to implement the update. This is because we do not want to implement the update during business hours as it could damage business operations and as such they have to done during off hours. This could be worse for retails businesses that have are busiest during holiday season as they typically have policies stating no updates can be made to system during the holiday months. 

The change approval process is a vital aspect of organizations due to this reason and are well documented as SOP's in each organization due to the reasons above.

# Previous Topic
[[Change Approval Process]]

# Next Section
[[Technical Change Management]]

