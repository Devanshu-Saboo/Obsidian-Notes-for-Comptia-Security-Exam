Lets take a real example of CrowdStrike and see how one routine content update for a security sensor in July 2024 led to the downtime of millions of Windows PCs globally.

Consider that in CrowdStrike there was an individual who wanted to make a routine content update to a security sensor. In this case the individual who wants to make the change is considered the ==🟠owner== in this process.

The ==🟠owner== typically will not perform the actual change and will instead fill out the form to request the change, and will only be kept in the loop as more steps are completed and decisions are taken regarding the requested change.

After the owner come the ==🟠stakeholders==. These are the ones who will be impacted by this change, which could be one person or the entire organization. The IT team will have to research and document each system and individual who will be affected by the change. In the case of the content update, this would be both CrowdStrike and the clients using CrowdStrike on their machines. Unfortunately, in this case the clients were not informed of the update and, due to an internal error, millions of Windows machines got the blue screen of death, making it impossible for business operations to proceed.

The next step in the process is to conduct ==🟠impact analysis==. This involves determining a risk value associated with the change, typically ==🟡'high', 'medium' or 'low'==. These risks could be that the fix would not fix anything, or that it breaks something else, which in the case of CrowdStrike it did. However the flip side of the coin must also be considered: what are the risks of not making the change? These may include a security vulnerability due to an old version, unexpected downtime on other services or even application unavailability.

Considering the risks, you may not want to directly implement the fix on the production system and should instead first test it in a ==🟠sandbox== environment where the risk would be minimal.

Even after taking every necessary precaution, it is always good practice to have a ==🟠backout plan== as some changes are difficult to revert. The backout plan consists of having the entire system backed up in a safe location, so that it is easy to roll back to the previous working version and restart services from the backup as and when required, ensuring minimal business impact.

Finally we have the ==🟠Maintenance Window==. Getting approval for the change is usually an easy task which may or may not take a lot of time. The task that typically takes the most time is deciding when to implement the update. We do not want to implement the update during business hours as it could damage business operations, so it has to be done during off hours. This could be worse for retail businesses that are busiest during the holiday season, as they typically have policies stating no updates can be made to systems during the holiday months.

To sum up, the terms to remember from this note are ==🟠owner, stakeholders, impact analysis, sandbox, backout plan and maintenance window==. The change approval process is a vital aspect of organizations for these reasons and is well documented as SOPs in each organization.

# Previous Topic
[[Change Approval Process]]
# Previous Section
[[Change Management]]
# Next Section
[[Technical Change Management]]
