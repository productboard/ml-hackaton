# Productboard ML hackaton data


This github repository contains data for Productboard ML hackaton.


## Data schema

The data are saved in JSON Line format (http://jsonlines.org/). Each line of the file contains JSON for one specific idea.

Data can be found in data folder of this repository. They are separated to multiple files. Each file represent specific application.

* delve
* fasttrack
* general
* microsoft-connections-email-marketing
* microsoft-invoicing
* microsoft-listings-online-presence
* office-365-admin
* office-365-admin-mobile
* office-365-business-center
* office-365-groups
* office-365-security-compliance
* office-com-home-page

### Data structure

* url -> Link to original post
* header -> Idea title
* idea_text -> Idea text
* author -> Numerical ID of idea author
* created_at -> Timestamp when idea was created (YYYY-MM-DD)
* votes -> Number of votes that this idea received
* reaction -> List containing all official reactions to this idea 
    * status -> Status of idea consideration  
    * author -> Numerical ID of reaction author
    * created_at -> Timestamp when reaction was added (YYYY-MM-DD)
    * note -> Text of the reaction
* comments -> List containing all public reactions to this idea
    * author -> Numerical ID of comment author
    * created_at -> Timestamp when comment was added (YYYY-MM-DD)
    * text -> Text of the comment


### Example

```json
{ 
   "url":"https://office365.uservoice.com/forums/273493-office-365-admin/suggestions/7771980-provide-a-powershell-interface-from-admin-area-s",
   "header":"Provide a powershell interface from admin area - so you can use powershell directly from the portal page.",
   "idea_text":"Having this ability to run PowerShell directly will remove the need to connect from on-premises to perform PowerShell tasks. This will also help 100% Mac shops - which cannot run PowerShell at all.",
   "author":"74217705",
   "created_at":"2015-04-30",
   "votes":1255,
   "reaction":[ 
      {
         "status": "thinking about it",
         "author": "168490332",
         "created_at": "2017-02-16",
         "note": "Thanks for your feedback! We’re reviewing your suggestion. Remember, the more votes a suggestion gets, the more likely it is that we’ll do it.",
      }
   ],
   "comments":[ 
      { 
         "author":"919176934",
         "created_at":"2019-09-09",
         "text":"For anyone still looking for a PS interface for SharePoint from Mac\\Linux, check the Office 365 CLI from the PnP team . It's a community effort to fill the gap - and impressively doing very well at that. You can also head to  to report any issues, make suggestions and (if you feel like making a dent in the world) submit PRs with cool new features as well."
      },
      { 
         "author":"152007912",
         "created_at":"2019-06-10",
         "text":"An interesting article here regarding how to achieve similar using the Azure cloud Shell:\n"
      },
      { 
         "author":"896471458",
         "created_at":"2019-04-24",
         "text":"It's not a full answer to this ask, but note that Connect-ExoPSSession is now available in Azure Cloud Shell."
      }
   ]
}
``` 
