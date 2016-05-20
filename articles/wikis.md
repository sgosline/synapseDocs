---
title: "Synapse Wikis"
layout: article
---

##Synapse Wikis

Wikis are available to:
  * Describe a project
  * Update results
  * Share results

###Editing Wiki in Synpase
A wiki is created by default for every project, folder and file. For folders and files, the wikis are not visible until there is content. 

{% tabs %} {% tab Command %}

{% highlight bash %} 
The command line client does not support the creation of wiki content. We suggest using (to get to the webpage of the project) synapse onweb syn### where syn### is the Synapse Id of your created project. Then editing the wiki using the web client. {% endhighlight %} {% endtab %}

{% tab Python %} {% highlight python %}
projWiki = Wiki(title='Data Summary', owner = myProj ) markdown = '''* Cell growth look normally distributed
There is evidence of inverse growth between these two cell lines ''' projWiki['markdown'] = markdown projWiki = syn.store(projWiki) 
{% endhighlight %} {% endtab %}

{% tab R %} {% highlight r %} library(synapseClient); 
placeholderText <- "* Cell growth look normally distributed\n* There is evidence of inverse growth between these two cell lines." wiki <- WikiPage(owner=myProject, title="Analysis summary", markdown=placeholderText) wiki <- synStore(wiki) 
{%endhighlight %} {% endtab %}

{% tab Web %} Select **Tools** then select **Edit Project/Folder/File wiki** {% endtab %}

{% endtabs %}

###Editing the Wiki

The easiest way to edit the wiki is through the web interface, though the Python and R clients can also be used. Each client requires formatting the text using the Wiki Markdown langage.  

####Markdown langauge
Wiki markdown language has many capabilities to customize the layout and text of the wiki. For full capabilities of the markdown language see the [help document](https://www.synapse.org/#!Wiki:syn2467792/ENTITY).

###Synapse Widgets
In addition to textual descriptions of a project Synapse also provides the ability to customize a wiki with specific widgets.  

 * Table of contents
To summarize the contents of a wiki.

 * Table Widgets
 There are many ways to add tabular data to the wiki.
  * Paste tabular data
  The easiest way.
  * Query on Synapse table
  More detail, link to Synapse table.
  * Query on files/folers
  Even more complex.

 * Genome Browser 
 Genome browser data can also be added.
 
 * File Preview
 To preview a file, use this.
 
 * User
 To link to a specific user. 
 * Provenance graph

 * Button Link

 * Entity List

####Challenge-specific widgets
Sage is involved in many DREAM challenges that require specific functionality built into the Synapse Wiki. 
  * Join Team
  * Submit for Evaluation
  * Team Badge

