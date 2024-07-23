---
layout: workshop      # DON'T CHANGE THIS.
# More detailed instructions (including how to fill these variables for an
# online workshop) are available at
# https://carpentries.github.io/workshop-template/customization/index.html
venue: "FIXME"        # brief name of the institution that hosts the workshop without address (e.g., "Euphoric State University")
address: "FIXME"      # full street address of workshop (e.g., "Room A, 123 Forth Street, Blimingen, Euphoria"), videoconferencing URL, or 'online'
country: "FIXME"      # lowercase two-letter ISO country code such as "fr" (see https://en.wikipedia.org/wiki/ISO_3166-1#Current_codes) for the institution that hosts the workshop
language: "FIXME"     # lowercase two-letter ISO language code such as "fr" (see https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) for the workshop
latitude: "45"        # decimal latitude of workshop venue (use https://www.latlong.net/)
longitude: "-1"       # decimal longitude of the workshop venue (use https://www.latlong.net)
mazemaps_url:         # Mazemaps URL (use https://properties.curtin.edu.au/visit-curtin/campus-maps/ click your building, then click the share button, e.g. https://link.mazemap.com/kBQQTJKo)
humandate: "FIXME"    # human-readable dates for the workshop (e.g., "Feb 17-18, 2020")
humantime: "FIXME"    # human-readable times for the workshop e.g., "9:00 am - 4:30 pm CEST (7:00 am - 2:30 pm UTC)"
startdate: FIXME      # machine-readable start date for the workshop in YYYY-MM-DD format like 2015-01-01
enddate: FIXME        # machine-readable end date for the workshop in YYYY-MM-DD format like 2015-01-02
instructor: ["instructor one", "instructor two"] # boxed, comma-separated list of instructors' names as strings, like ["Kay McNulty", "Betty Jennings", "Betty Snyder"]
helper: ["helper one", "helper two"]     # boxed, comma-separated list of helpers' names, like ["Marlyn Wescoff", "Fran Bilas", "Ruth Lichterman"]
email: ["curtinids@curtin.edu.au"]    # boxed, comma-separated list of contact email addresses for the host, lead instructor, or whoever else is handling questions, like ["marlyn.wescoff@example.org", "fran.bilas@example.org", "ruth.lichterman@example.org"]
collaborative_notes:  # optional: URL for the workshop collaborative notes, e.g. an Etherpad or Google Docs document (e.g., https://pad.carpentries.org/2015-01-01-euphoria)
eventbrite:           # optional: alphanumeric key for Eventbrite registration, e.g., "1234567890AB" (if Eventbrite is being used)
---





{% comment %}
8< ============= For a workshop delete from here =============
For a workshop please delete the following block until the next dashed-line. This is just a check to make sure you're paying attention.
Altneratively delete everything include the {% comment %} and {% endcomment %}
{% endcomment %}


<div class="alert alert-danger">
This is the workshop template. Delete these lines and use it to customize
your own website. You will need to edit the header of this file (`index.md`), and ensure both `_includes/schedule.html` and `setup/index.md` are accurate.  For `_includes/schedule.html`, you should be able to copy-paste lines as needed.
</div>

{% comment %}
8< ============================= until here ==================
{% endcomment %} 






{% comment %}
EVENTBRITE

This block includes the Eventbrite registration widget if
'eventbrite' has been set in the header.  You can delete it if you
are not using Eventbrite, or leave it in, since it will not be
displayed if the 'eventbrite' field in the header is not set.
{% endcomment %}
{% if page.eventbrite %}
<strong>Some adblockers block the registration window. If you do not see the
  registration box below, please check your adblocker settings.</strong>
<iframe
  src="https://www.eventbrite.com/tickets-external?eid={{page.eventbrite}}&ref=etckt"
  frameborder="0"
  width="100%"
  height="280px"
  scrolling="auto">
</iframe>
{% endif %}




<h2 id="general">General Information</h2>

<p>
<strong><a href="https://carpentries.org">The Carpentries</a></strong> project comprises the <a
href="{{site.swc_site}}">Software Carpentry</a>, <a href="{{site.dc_site}}">Data Carpentry</a>, and
<a href="{{site.lc_site}}">Library Carpentry</a> communities of Instructors, Trainers, Maintainers,
helpers, and supporters who share a mission to teach foundational computational and data science
skills to researchers. This workshop is a 2-day blend of both Software Carpentries and Data caprnetires.



<p>
  <a href="{{site.swc_site}}">Software Carpentry</a>
  aims to help researchers get their work done
  in less time and with less pain
  by teaching them basic research computing skills.
  This hands-on workshop will cover basic concepts and tools,
  including program design, version control, data management,
  and task automation.
  Participants will be encouraged to help one another
  and to apply what they have learned to their own research problems.
</p>



<p>
  <a href="{{site.dc_site}}">Data Carpentry</a> develops and teaches workshops on the fundamental data skills needed to conduct
  research. Its target audience is researchers who have little to no prior computational experience,
  and its lessons are domain specific, building on learners' existing knowledge to enable them to quickly
  apply skills learned to their own research.
  Participants will be encouraged to help one another
  and to apply what they have learned to their own research problems.
</p>
<p align="center">
  <em>
    For more information on what we teach and why,
    please see our papers
    "<a href="https://doi.org/10.1371/journal.pcbi.1005510">Good Enough Practices for Scientific Computing</a>" and "<a href="https://doi.org/10.1371/journal.pbio.1001745">Best Practices for Scientific Computing</a>".
  </em>
</p>

<p id="who"> 
  <strong>Who:</strong> <br>
  The course is aimed at graduate students and other researchers.
  <strong>
    You don't need to have any previous knowledge of the tools
    that will be presented at the workshop.
  </strong>
</p>




{% assign begin_address = page.address | slice: 0, 4 | downcase  %}


<p id="where">
  <strong>Where:</strong> <br>
  {{page.address}}.
  Get directions with
  <a href="//www.openstreetmap.org/?mlat={{page.latitude}}&mlon={{page.longitude}}&zoom=16">OpenStreetMap</a>
  or
  <a href="//maps.google.com/maps?q={{page.latitude}},{{page.longitude}}">Google Maps</a>,
  or
  <a href="{{page.mazemaps_url}}">Curtin Mazemaps</a>.
</p>



<p id="when">
  <strong>When:</strong> <br>
  {{page.humandate}}; {{page.humantime}}
  {% include workshop_calendar.html %}
</p>




<p id="requirements">
  <strong>Requirements:</strong> <br>
    Participants must bring a laptop with a
    Mac, Linux, or Windows operating system (not a tablet, Chromebook, etc.) that they have administrative privileges on.  <br>

    They should have a few specific software packages installed (listed <a href="#setup">below</a>).
</p>


<p id="accessibility">
  <strong>Accessibility:</strong> <br>
  We are committed to making this workshop
  accessible to everybody. 
  The workshop organizers have checked that:
<p>
  <ul>
    <li>The room is wheelchair / scooter accessible.</li>
    <li>Accessible restrooms are available.</li>
  </ul>
</p>
Materials will be provided in advance of the workshop and large-print handouts are available if needed by notifying the organizers in advance. If we can help making learning easier for you (e.g. sign-language interpreters, lactation facilities) please get in touch (using contact details below) and we will attempt to provide them. 

 <br>  <br>



{% comment %}
CONTACT EMAIL ADDRESS

Display the contact email address set in the configuration file by looping through all emails.
{% endcomment %}
<p id="contact">
  <strong>Contact:</strong> <br>
  Please email
  {% if page.email %}
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
  {% else %}
  to-be-announced
  {% endif %}
  for more information.
</p>

<p id="roles">
  <strong>Roles:</strong> <br>
  To learn more about the roles at the workshop (who will be doing what),
  refer to <a href="https://carpentries.org/workshop_faq/#what-are-the-roles-of-everyone-participating-in-a-workshop">our Workshop FAQ</a>.
</p>


<p id="who-can-attend">
    <strong>Who can attend?</strong> <br>
    This workshop is open to Curtin University researchers and HDR students.
</p>

<p id="before-attending">
<strong>What do I need to do before attending?</strong> <br>
  Before attending please ensure you've followed the <a href="{{ relative_root_path }}/setup">setup</a> . This means you should have:  
  <ol>
    <li> Installed VSCode </li>
    <li> Installed the python enviornment </li>
    <li> Can run the confirmation script and get the required output </li>
  </ol>
  You can email <a href="mailto:curtinids@curtin.edu.au">curtinids@curtin.edu.au</a> if you need help. There will also be a short half-hour before the workshop for any serious issues.
</p>
{% comment%}
CODE OF CONDUCT
{% endcomment %}

<hr/>
<h2 id="code-of-conduct">Code of Conduct</h2>

<p>
Everyone who participates in Carpentries activities is required to conform to the <a href="https://docs.carpentries.org/topic_folders/policies/code-of-conduct.html">Code of Conduct</a>. This document also outlines how to report an incident if needed.
</p>

<p class="text-center">
  <a href="https://goo.gl/forms/KoUfO53Za3apOuOK2">
    <button type="button" class="btn btn-info">Report a Code of Conduct Incident</button>
  </a>
</p>
<hr/>


{% comment %}
Collaborative Notes

If you want to use an Etherpad, go to

https://pad.carpentries.org/YYYY-MM-DD-site

where 'YYYY-MM-DD-site' is the identifier for your workshop,
e.g., '2015-06-10-esu'.

Note we also have a CodiMD (the open-source version of HackMD)
available at https://codimd.carpentries.org

Alternatively just link a google doc
{% endcomment %}
{% if page.collaborative_notes %}
<h2 id="collaborative_notes">Collaborative Notes</h2>

<p>
We will use this <a href="{{ page.collaborative_notes }}">collaborative document</a> for chatting, taking notes, and sharing URLs and bits of code.
</p>
<hr/>
{% endif %}


{% comment %}
SURVEYS -These will automatically link to the carpentries surveys. .
{% endcomment %}
<h2 id="surveys">Surveys</h2>
<p>Please be sure to complete these surveys before and after the workshop.</p>
<p><a href="{{ site.pre_survey }}{{ site.github.project_title }}">Pre-workshop Survey</a></p>
<p><a href="{{ site.post_survey }}{{ site.github.project_title }}">Post-workshop Survey</a></p>

<hr/>



<h2 id="schedule">Schedule</h2>

{% include schedule.html %}


<hr/>



<h2 id="setup">Setup</h2>

<p>
  To participate in this workshop,
  you <b><u>will</u></b> need to follow the instructions on the <a href="{{ relative_root_path }}/setup">setup page</a> <br>
  In addition, you will need an up-to-date web browser.
</p>


<p>
  The Carpentries maintain a list of common issues that occur during installation as a reference for instructors
  that may be useful on the
  <a href = "{{site.swc_github}}/workshop-template/wiki/Configuration-Problems-and-Solutions">Configuration Problems and Solutions wiki page</a>.
</p>

<p>
  <a href="https://glosario.carpentries.org/">Glosario</a> is a multilingual glossary 
  for computing and data science terms. The glossary helps 
  learners who attend workshops and use our lessons to make sense of computational and programming jargon written in English by offering it 
  in their native language. This glossary may be useful for looking up unknown terms while following the setup.
</p>

