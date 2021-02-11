---
layout: workshop      # DON'T CHANGE THIS.
# More detailed instructions (including how to fill these variables for an
# online workshop) are available at
# https://carpentries.github.io/workshop-template/customization/index.html
venue: "Somewhere"        # brief name of the institution that hosts the workshop without address (e.g., "Euphoric State University")
address: "online"      # full street address of workshop (e.g., "Room A, 123 Forth Street, Blimingen, Euphoria"), videoconferencing URL, or 'online'
country: "GB"      # lowercase two-letter ISO country code such as "fr" (see https://en.wikipedia.org/wiki/ISO_3166-1#Current_codes) for the institution that hosts the workshop
language: "en"     # lowercase two-letter ISO language code such as "fr" (see https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) for the
latitude: "45"        # decimal latitude of workshop venue (use https://www.latlong.net/)
longitude: "-1"       # decimal longitude of the workshop venue (use https://www.latlong.net)
humandate: "Sep 15-16, 2021"    # human-readable dates for the workshop (e.g., "Feb 17-18, 2020")
humantime: "10:00 - 16:30"    # human-readable times for the workshop (e.g., "9:00 am - 4:30 pm")
startdate: 2021-09-15      # machine-readable start date for the workshop in YYYY-MM-DD format like 2015-01-01
enddate: 2021-09-16        # machine-readable end date for the workshop in YYYY-MM-DD format like 2015-01-02
instructor: ["Joe Bloggs", "A.N Other"] # boxed, comma-separated list of instructors' names as strings, like ["Kay McNulty", "Betty Jennings", "Betty Snyder"]
helper: ["Jimmy Gill", "Saul Goodman"]     # boxed, comma-separated list of helpers' names, like ["Marlyn Wescoff", "Fran Bilas", "Ruth Lichterman"]
email: ["rsg@info.soton.ac.uk"]    # boxed, comma-separated list of contact email addresses for the host, lead instructor, or whoever else is handling questions, like ["marlyn.wescoff@example.org", "fran.bilas@example.org", "ruth.lichterman@example.org"]
preworkshop_survey: "http://bit.ly/2020-5-21-before" # optional: URL for the workshop survey, usually a pre-generated bitlink to a Google Form created for the workshop from a template
collaborative_notes:  # optional: URL for the workshop collaborative notes, e.g. an Etherpad or Google Docs document (e.g., https://pad.carpentries.org/2015-01-01-euphoria)
eventbrite:          # optional: alphanumeric key for Eventbrite registration, e.g., "1234567890AB" (if Eventbrite is being used)
---

<!--------------- Editing the header above ------------------------------------>
{% comment %}
Edit the values in the block above to be appropriate for your workshop.
If the value is not 'true', 'false', 'null', or a number, please use
double quotation marks around the value, unless specified otherwise.
And run 'make workshop-check' *before* committing to make sure that changes are good.
{% endcomment %}


<!--------------- General Workshop Information -------------------------------------------------->

## General Information

[Software Carpentry](http://software-carpentry.org/)'s mission is to help scientists and engineers get 
more research done in less time and with less pain by teaching them basic skills for scientific computing. 
This hands-on workshop will cover basic concepts and tools, including using the command-line, building and 
designing programs in Python, and managing the development of code with version control in Git. 
Participants will be encouraged to help one another.

*For more information on what we teach and why, please see our paper 
["Best Practices for Scientific Computing"](http://journals.plos.org/plosbiology/article?id=10.1371/journal.pbio.1001745).*

**Who:** The course is aimed at postgraduate students and postdoctoral scientists who are familiar with basic programming concepts (like loops and arrays) and would like to learn best practise techniques and tools to develop their software more effectively and productively.

<!-- Uncomment for Data Carpentry-style workshop

[Data Carpentry](https://www.data-carpentry.org/) develops and teaches workshops on the fundamental data skills needed to conduct research. 
Our mission is to provide researchers high-quality, training covering the full lifecycle of data-driven research. 
Data Carpentry is a sibling organization of Software Carpentry. Where Software Carpentry teaches best practices in software development, our focus is on the introductory computational skills needed for data management and analysis in all domains of research. Our initial target audience is learners who have little to no prior computational experience. We create a friendly environment for learning to empower researchers and enable data driven discovery. Participants will be encouraged to help one another and to apply what they have learned to their own research problems.

*For more information on what we teach and why, please see our paper 
["Best Practices for Scientific Computing"](http://journals.plos.org/plosbiology/article?id=10.1371/journal.pbio.1001745).*

The course is aimed at graduate students and other researchers.
You don't need to have any previous knowledge of the tools that will be presented at the workshop.
-->

<!-- Uncomment for Computational Research Skills-style workshop

The Computational Research Skills training course helps researchers get more done, in less time, and with less pain!
It teaches the fundamental data and software skills needed for research.

Delivered online, this hands-on, self-learning workshop will cover basic concepts and tools, including data organisation and management, using the command line, 
building and designing R programs to analyse, manipulate, and visualise data, as well as providing introductions to version control and cloud computing.

**Who:** The course is aimed at postgraduate students who are familiar with basic programming concepts (like loops and arrays).
-->


<!--------------- Location ---------------------------------------------------->
{% comment %}
This block displays the address and links to maps showing directions
if the latitude and longitude of the workshop have been set.  You
can use https://itouchmap.com/latlong.html to find the lat/long of an
address.
{% endcomment %}
{% assign begin_address = page.address | slice: 0, 4 | downcase  %}
{% if page.address == "online" %}
  {% assign online = "true_private" %}
{% elsif begin_address contains "http" %}
  {% assign online = "true_public" %}
{% else %}
  {% assign online = "false" %}
{% endif %}

{% if page.latitude and page.longitude and online == "false" %}
**Where:** {{ page.address }}. Get directions with
[OpenStreetMap](https://www.openstreetmap.org/?mlat={{ page.latitude }}&mlon={{ page.longitude }}&zoom=16)
or
[Google Maps](https://maps.google.com/maps?q={{ page.latitude }},{{ page.longitude }}).
{% elsif online == "true_public" %}
**Where:** online at [{{ page.address }}]({{page.address}}). If you need a password or other information to access the training,
the instructor will pass it on to you before the workshop.
{% elsif online == "true_private" %}
**Where:** This training will take place online. The instructors will provide you with the information you will need to connect to this meeting.
{% endif %}


<!--------------- When (start date) ------------------------------------------->

{% if page.humandate %}
<p>
<strong>When:</strong> {{page.humandate}}.
{% include workshop_calendar.html %}
</p>
{% endif %}


<!--------------- Requirements ------------------------------------------------>

**Requirements:** Before attending the workshop you need to install some useful and free software.
For more information, see the [software prerequisites](prerequisites.html).

You must also abide by the Carpentry's [Code of Conduct](https://docs.carpentries.org/topic_folders/policies/code-of-conduct.html).


<!--------------- Accessibility ----------------------------------------------->

**Accessibility:** We are dedicated to providing a positive and accessible learning environment for all.

{% if online == "false" %}
The workshop organizers have checked that:

- The room is wheelchair / scooter accessible.
- Accessible restrooms are available.

Materials will be provided in advance of the workshop and
large-print handouts are available if needed by notifying the
organizers in advance.  If we can help making learning easier for
you please get in touch (using contact details below) and we will
attempt to provide them.
{% else %}
Please notify the instructors in advance of the workshop if you require any accommodations or if there is
anything we can do to make this workshop more accessible to you.
{% endif %}

<!--------------- Contact information ----------------------------------------->

**Contact:** This workshop is being organised by the University of Southampton's <a href='http://rsg.soton.ac.uk/'>Research Software Group</a>.

Our talented team of Research Software Engineers is dedicated to ensuring that software developed
for research at the University of Southampton is the best it can be.

- We offer a full range of Software Development Services, covering many different technologies and all academic disciplines.
- We provide Software Carpentry Training in good software engineering practice, for postgraduate students and
researchers at any career stage.
- We organise regular Research Software Community events for researchers who develop software.

<!-- Set within p element to remove whitespace and linespacing -->
<p>
Please email
{% for email in page.email %}
  {% if forloop.last and page.email.size > 1 %}
    or
  {% else %}
    {% unless forloop.first %}
      ,
    {% endunless %}
  {% endif %}
  <a href='mailto:{{email}}'>{{email}}</a>
{% endfor %}
for more information.
</p>
___

<!--------------- Collaborative Notes ----------------------------------------->

{% if page.collaborative_notes %}
## Collaborative Notes

We will use this [collaborative document]({{ page.collaborative_notes }}) for chatting, taking notes, and sharing URLs and bits of code.
___
{% endif %}


<!--------------- Before the Workshop ----------------------------------------->

## Before the workshop

Before attending the workshop you need to install some useful and free software. 
For more information, see the [software prerequisites](prerequisites.html).

{% if page.preworkshop_survey %}
Please also fill in the [Pre-workshop Survey]({{ page.preworkshop_survey }}).
{% endif %}

---

<!--------------- During the workshop ----------------------------------------->

## During the Workshop

We will attempt to fix any technical issues people encounter during the workshop. 
If you encounter an issue, please copy the error message you encounter and send it as a direct message to the presenter.

Some problems may be too complicated to solve during the online event. 
If that's the case, we will attempt to resolve the issue after the workshop. 
All training materials are available online through the schedule, 
so if this does occur you will be able to work through them after the workshop.

---

<!--------------- During the workshop ----------------------------------------->

## Schedule

Check the [schedule page](schedule-text.html) for details.

---

<!--------------- Register Interest ------------------------------------------>

## Register an interest in our course for possible future dates

If you're interested in our training, but can't make the date, you can 
[sign up to be notified](https://docs.google.com/forms/d/1KW8DTErxhEXUJbtbwUfVw7s6AWwHKFNZNWSsALV2E0A/viewform)
 about future events.
