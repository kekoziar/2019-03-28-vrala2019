---
layout: workshop      # DON'T CHANGE THIS.
carpentry: "lc"    # what kind of Carpentry (must be either "lc" or "dc" or "swc")
title: "Practical Coding for Visual Resources: Python & Version Control"
venue: "Visual Resources Association<br> Annual Conference 2019<br>held at <br>DoubleTree by Hilton,<br>Los Angeles Downtown"        # brief name of host site without address (e.g., "Euphoric State University")
address: "120 South Los Angeles Street, Los Angeles, CA 90012"  # full street address of workshop (e.g., "Room A, 123 Forth Street, Blimingen, Euphoria")
country: "us"      # lowercase two-letter ISO country code such as "fr" (see https://en.wikipedia.org/wiki/ISO_3166-1)
language: "en"     # lowercase two-letter ISO language code such as "fr" (see https://en.wikipedia.org/wiki/ISO_639-1)
latlng: "34.050491, -118.242752"       # decimal latitude and longitude of workshop venue (e.g., "41.7901128,-87.6007318" - use http://www.latlong.net/)
humandate: "March 29, 2019"    # human-readable dates for the workshop (e.g., "Feb 17-18, 2020")
humantime: "8:00 AM - 5:00 PM"    # human-readable times for the workshop (e.g., "9:00 am - 4:30 pm")
startdate: 2019-03-29      # machine-readable start d"ate for the workshop in YYYY-MM-DD format like 2015-01-01
enddate: 2019-03-29        # machine-readable end date for the workshop in YYYY-MM-DD format like 2015-01-02
instructor: ["Noah Geraci", "Kat Koziar"] # boxed, comma-separated list of instructors' names as strings, like ["Kay McNulty", "Betty Jennings", "Betty Snyder"]
helper: ["Krystal Boehlert"]     # boxed, comma-separated list of helpers' names, like ["Marlyn Wescoff", "Fran Bilas", "Ruth Lichterman"]
email: ["katherine.koziar@ucr.edu"]    # boxed, comma-separated list of contact email addresses for the host, lead instructor, or whoever else is handling questions, like ["marlyn.wescoff@example.org", "fran.bilas@example.org", "ruth.lichterman@example.org"]
collaborative_notes:             # optional: URL for the workshop collaborative notes, e.g. an Etherpad or Google Docs document
eventbrite: # optional: alphanumeric key for Eventbrite registration, e.g., "1234567890AB" (if Eventbrite is being used)
---


{% comment %} See instructions in the comments below for how to edit specific sections of this workshop template. {% endcomment %}

{% comment %}
  HEADER

  Edit the values in the block above to be appropriate for your workshop.
  If the value is not 'true', 'false', 'null', or a number, please use
  double quotation marks around the value, unless specified otherwise.
  And run 'bin/workshop_check.py' *before* committing to make sure that changes are good.
{% endcomment %}

<h2 id="general">General Information</h2>
{% include lc/intro.html %}
{% include lc/who.html %}
<p id="requirements">
  <strong>Requirements:</strong> Participants must bring a laptop with a Windows, Mac, or Linux operating system (not a tablet, Chromebook, etc.) that they have the ability to install software on.
 They should come prepared with a few specific software packages installed (listed
  <a href="#setup">below</a>).
</p>

{% comment %}
  ACCESSIBILITY

  Modify the block below if there are any barriers to accessibility or
  special instructions.
{% endcomment %}
<p id="accessibility">
  <strong>Accessibility:</strong> We are committed to making this workshop
  accessible to everybody. For specific accessibility information about the venue, see the <a href="https://doubletree3.hilton.com/en/hotels/california/doubletree-by-hilton-hotel-los-angeles-downtown-LAXDTDT/about/amenities.html">DoubleTree by Hilton Los Angeles Downtown website</a>.
<p>
  Printed materials will be provided at the workshop and
  large-print handouts are available if needed by notifying the
  organizers in advance.  If there's anything else we can do to
  make it possible for you to participate, please get in touch (using contact details below)
  and we will attempt to provide it.
</p>
<p id="contact">
  <strong>Contact</strong>:
  For registration questions or general workshop logistics, contact the moderator
  <a href="mailto:krystal.boehlert@ucr.edu">krystal.boehlert@ucr.edu</a>. For questions about workshop content or software installation,
  contact <a href="mailto:katherine.koziar@ucr.edu">katherine.koziar@ucr.edu</a>.
</p>

<p id="survey">
	<strong>Survey</strong>:
	{% comment %} DO NOT EDIT SURVEY LINKS {% endcomment %}
	{% if page.carpentry == "swc" %}
	<p>Please be sure to complete these surveys before and after the workshop.</p>
	<p><a href="{{ site.swc_pre_survey }}{{ site.github.project_title }}">Pre-workshop Survey</a></p>
	<p><a href="{{ site.swc_post_survey }}{{ site.github.project_title }}">Post-workshop Survey</a></p>
	{% elsif page.carpentry == "dc" %}
  	<p>Please be sure to complete these surveys before and after the workshop.</p>
	<p><a href="{{ site.dc_pre_survey }}{{ site.github.project_title }}">Pre-workshop Survey</a></p>
	<p><a href="{{ site.dc_post_survey }}{{ site.github.project_title }}">Post-workshop Survey</a></p>
	{% elsif page.carpentry == "lc" %}
	The <a href="{{ site.vra_pre_survey }}">pre-workshop survey</a> is a quick, optional survey to help the instructor learn more 	about participants' interests and backgrounds, and better tailor the workshop to your needs.
	{% endif %}
</p >

<p>
	<strong>Other Resources</strong>:
	The <a href="https://goo.gl/6So6D5" target="_blank">workshop slide deck</a> includes next steps and a small resources
	list.
</p>

<hr/>

{% comment %}
  SCHEDULE

  Show the workshop's schedule.  Edit the items and times in the table
  to match your plans.  You may also want to change 'Day 1' and 'Day
  2' to be actual dates or days of the week.
{% endcomment %}
<h2 id="schedule">Schedule</h2>
{% include lc/schedule.html %}

<!-- <hr/>-->
<!-- {% comment %}
  SYLLABUS

  Show what topics will be covered.

  1. If your workshop is R rather than Python, remove the comment
     around that section and put a comment around the Python section.
  2. Some workshops will delete SQL.
  3. Please make sure the list of topics is synchronized with what you
     intend to teach.
  4. You may need to move the div's with class="col-md-6" around inside
     the div's with class="row" to balance the multi-column layout.

  This is one of the places where people frequently make mistakes, so
  please preview your site before committing, and make sure to run
  'tools/check' as well.
{% endcomment %}
<h2 id="syllabus">Syllabus</h2>

{% if page.carpentry == "swc" %}
  {% include sc/syllabus.html %}
{% elsif page.carpentry == "dc" %}
  {% include dc/syllabus.html %}
{% elsif page.carpentry == "lc" %}
  {% include lc/syllabus.html %}
{% endif %} -->

<hr/>

{% comment %}
  SETUP

  Delete irrelevant sections from the setup instructions.  Each
  section is inside a 'div' without any classes to make the beginning
  and end easier to find.

  This is the other place where people frequently make mistakes, so
  please preview your site before committing, and make sure to run
  'tools/check' as well.
{% endcomment %}

<h2 id="setup">Setup</h2>

<p>
  To participate in the workshop, you will need access to the software described below.
  In addition, you will need an up-to-date web browser.
</p>

<div id="shell"> {% comment %} Start of 'shell' section. {% endcomment %}
  <h3>Bash Shell</h3>

  <p>
    Bash is a commonly-used shell that gives you the power to do simple
    tasks more quickly.
  </p>

  <div class="row">
    <div class="col-md-4">
      <h4 id="shell-windows">Windows</h4>
      <a href="https://www.youtube.com/watch?v=339AEqk9c-8">Video Tutorial</a>
      <ol>
        <li>Download the Git for Windows <a href="https://git-for-windows.github.io/">installer</a>.</li>
        <li>Run the installer and follow the steps bellow:
          <ol>
            {% comment %} Git 2.8.2 Setup {% endcomment %}
            {% comment %} Information {% endcomment %}
            <li>Click on "Next".</li>
            {% comment %} Select Components {% endcomment %}
            <li>Click on "Next".</li>
            {% comment %} Adjusting your PATH environment {% endcomment %}
            <li>
              <strong>
                Keep "Use Git from the Windows Command Prompt" selected and click on "Next".
              </strong>
                If you forgot to do this programs that you need for the workshop will not work properly.
                If this happens rerun the installer and select the appropriate option.
            </li>
            {% comment %} Choosing the SSH executable {% endcomment %}
            <li>Click on "Next".</li>
            {% comment %} Configuring the line ending conversions {% endcomment %}
            <li>
              <strong>
                Keep "Checkout Windows-style, commit Unix-style line endings" selected and click on "Next".
              </strong>
            </li>
            {% comment %} Configuring the terminal emulator to use with Git Bash {% endcomment %}
            <li>
              <strong>
                Keep "Use Windows' default console window" selected and click on "Next".
              </strong>
            </li>
            {% comment %} Configuring experimental performance tweaks {% endcomment %}
            <li>Click on "Install".</li>
            {% comment %} Installing {% endcomment %}
            {% comment %} Completing the Git Setup Wizard {% endcomment %}
            <li>Click on "Finish".</li>
          </ol>
        </li>
        <li>
          If your "HOME" environment variable is not set (or you don't know what this is):
          <ol>
            <li>Open command prompt (Open Start Menu then type <code>cmd</code> and press [Enter])</li>
            <li>
              Type the following line into the command prompt window exactly as shown:
              <p><code>setx HOME "%USERPROFILE%"</code></p>
            </li>
            <li>Press [Enter], you should see <code>SUCCESS: Specified value was saved.</code></li>
            <li>Quit command prompt by typing <code>exit</code> then pressing [Enter]</li>
          </ol>
        </li>
      </ol>
      <p>This will provide you with both Git and Bash in the Git Bash program.</p>
    </div>
    <div class="col-md-4">
      <h4 id="shell-macosx">macOS</h4>
      <p>
        The default shell in all versions of macOS is Bash, so no
        need to install anything.  You access Bash from the Terminal
        (found in
        <code>/Applications/Utilities</code>).
        See the Git installation <a href="https://www.youtube.com/watch?v=9LQhwETCdwY ">video tutorial</a>
        for an example on how to open the Terminal.
        You may want to keep
        Terminal in your dock for this workshop.
      </p>
    </div>
    <div class="col-md-4">
      <h4 id="shell-linux">Linux</h4>
      <p>
        The default shell is usually Bash, but if your
        machine is set up differently you can run it by opening a
        terminal and typing <code>bash</code>.  There is no need to
        install anything.
      </p>
    </div>
  </div>
</div> {% comment %} End of 'shell' section. {% endcomment %}

<div id="git"> {% comment %} Start of 'Git' section. GitHub browser compatability
           is given at https://help.github.com/articles/supported-browsers/{% endcomment %}
  <h3>Git</h3>
  <p>
    Git is a version control system that lets you track who made changes
    to what when and has options for easily updating a shared or public
    version of your code
    on <a href="https://github.com/">github.com</a>. You will need a
    <a href="https://help.github.com/articles/supported-browsers/">supported</a>
    web browser (current versions of Chrome, Firefox or Safari,
    or Internet Explorer version 9 or above).
  </p>
  <p>
    You will need an account at <a href="https://github.com/">github.com</a>
    for parts of the Git lesson. Basic GitHub accounts are free. We encourage
    you to create a GitHub account if you don't have one already.
    Please consider what personal information you'd like to reveal. For
    example, you may want to review these
    <a href="https://help.github.com/articles/keeping-your-email-address-private/">instructions
    for keeping your email address private</a> provided at GitHub.
  </p>

  <div class="row">
    <div class="col-md-4">
      <h4 id="git-windows">Windows</h4>
      <p>
        Git should be installed on your computer as part of your Bash
        install (described above).
      </p>
    </div>
    <div class="col-md-4">
      <h4 id="git-macosx">macOS</h4>
      <a href="https://www.youtube.com/watch?v=9LQhwETCdwY ">Video Tutorial</a>
      <p>
        <strong>For OS X 10.9 and higher</strong>, install Git for Mac
        by downloading and running the most recent "mavericks" installer from
        <a href="http://sourceforge.net/projects/git-osx-installer/files/">this list</a>.
        After installing Git, there will not be anything in your <code>/Applications</code> folder,
        as Git is a command line program.
        <strong>For older versions of OS X (10.5-10.8)</strong> use the
        most recent available installer labelled "snow-leopard"
        <a href="http://sourceforge.net/projects/git-osx-installer/files/">available here</a>.
      </p>
    </div>
    <div class="col-md-4">
      <h4 id="git-linux">Linux</h4>
      <p>
        If Git is not already available on your machine you can try to
        install it via your distro's package manager. For Debian/Ubuntu run
        <code>sudo apt-get install git</code> and for Fedora run
        <code>sudo dnf install git</code>.
      </p>
    </div>
  </div>
</div> {% comment %} End of 'Git' section. {% endcomment %}


<div id="editor"> {% comment %} Start of 'editor' section. {% endcomment %}
  <h3>Text Editor</h3>
  <p>
    When you're writing code, it's nice to have a text editor that is
    optimized for writing code, with features like automatic
    color-coding of key words.  The default text editor on macOS and
    Linux is usually set to Vim, which is not famous for being
    intuitive.  if you accidentally find yourself stuck in it, try
    typing the escape key, followed by <code>:q!</code> (colon, lower-case 'q',
    exclamation mark), then hitting Return to return to the shell.
  </p>

  <div class="row">
    <div class="col-md-4">
      <h4 id="editor-windows">Windows</h4>
      <a href="https://www.youtube.com/watch?v=339AEqk9c-8">Video Tutorial</a>
      <p>
        nano is a basic editor and the default the instructor will use in the workshop.
        To install it,
        download the <a href="{{site.swc_installer}}">
          {% if page.carpentry == "swc" %}
          Software Carpentry
          {% elsif page.carpentry == "dc" %}
          Data Carpentry
          {% elsif page.carpentry == "lc" %}
          Library Carpentry
          {% endif %}
          Windows installer
	</a>
        and double click on the file to run it.
        <strong>This installer requires an active internet connection.</strong>
      </p>
      <p>
        Others editors that you can use are
        <a href="http://notepad-plus-plus.org/">Notepad++</a>,
        <a href="http://www.sublimetext.com/">Sublime Text</a>, or
	<a href="https://atom.io/">Atom</a>.
        <strong>Be aware that you must
          add its installation directory to your system path.</strong>
        Please ask your instructor to help you do this.
      </p>
    </div>
    <div class="col-md-4">
      <h4 id="editor-macosx">macOS</h4>
      <p>
        nano is a basic editor and the default the instructor will use in the workshop.
        See the Git installation <a href="https://www.youtube.com/watch?v=9LQhwETCdwY ">video tutorial</a>
        for an example on how to open nano.
        It should be pre-installed.
      </p>
      <p>
        Other editors that you can use are
	 	<a href="http://www.sublimetext.com/">Sublime Text</a>,
		<a href="https://atom.io/">Atom</a>, or
        <a href="http://www.barebones.com/products/bbedit/">BBEdit (formerly Text Wrangler)</a>.
      </p>
    </div>
    <div class="col-md-4">
      <h4 id="editor-linux">Linux</h4>
      <p>
        nano is a basic editor and the default the instructor will use in the workshop.
        It should be pre-installed.
      </p>
      <p>
        Others editors that you can use are
        <a href="https://wiki.gnome.org/Apps/Gedit">Gedit</a>,
        <a href="http://kate-editor.org/">Kate</a> or
        <a href="http://www.sublimetext.com/">Sublime Text</a>.
      </p>
    </div>
  </div>
</div> {% comment %} End of 'editor' section. {% endcomment %}

<div id="python"> {% comment %} Start of 'Python' section. Remove the third paragraph if
           the workshop will teach Python using something other than
           the Jupyter notebook.
           Details at https://jupyter-notebook.readthedocs.io/en/stable/notebook.html#browser-compatibility {% endcomment %}
  <h3>Python</h3>

  <p>
    <a href="http://python.org">Python</a> is a popular language in the library and archives fields, and great for general-purpose programming as
    well. Installing all of its packages individually can be a bit of a pain, so we recommend using
    <a href="https://www.anaconda.com/distribution/">Anaconda</a>,
    an all-in-one installer.
  </p>

    <p>
      Regardless of how you choose to install it,
      <strong>please make sure you install Python version 3.x</strong>
      (e.g., 3.6 is fine).
    </p>

  <div class="row">
    <div class="col-md-4">
      <h4 id="python-windows">Windows</h4>
      <a href="https://www.youtube.com/watch?v=xxQ0mzZ8UvA">Video Tutorial</a>
      <ol>
        <li>Open <a href="https://www.anaconda.com/download/#windows">https://www.anaconda.com/download/#windows</a> with your web browser.</li>
        <li>Download the Python 3 installer for Windows.</li>
        <li>Install Python 3 using the defaults for installation, <em>except</em>:
          <ul style="list-style-type:disc">
            <li>Make sure to check <strong>Add Anaconda to my PATH environment variable</strong>, even though the installer will warn you not to.</li>
            <li>Make sure to check <strong>Make Anaconda the default Python</strong>.</li>
          </ul>
         </li>
      </ol>
    </div>
    <div class="col-md-4">
      <h4 id="python-macosx">macOS</h4>
      <a href="https://www.youtube.com/watch?v=TcSAln46u9U">Video Tutorial</a>
      <ol>
        <li>Open <a href="https://www.anaconda.com/download/#macos">https://www.anaconda.com/download/#macos</a> with your web browser.</li>
        <li>Download the Python 3 installer for OS X.</li>
        <li>Install Python 3 using all of the defaults for installation.</li>
      </ol>
    </div>
    <div class="col-md-4">
      <h4 id="python-linux">Linux</h4>
      <ol>
        <li>Open <a href="https://www.anaconda.com/download/#linux">https://www.anaconda.com/download/#linux</a> with your web browser.</li>
        <li>Download the Python 3 installer for Linux.<br>
          (The installation requires using the shell. If you aren't
           comfortable doing the installation yourself
           stop here and request help at the workshop.)
        </li>
        <li>
          Open a terminal window.
        </li>
        <li>
          Type <pre>bash Anaconda3-</pre> and then press
          tab. The name of the file you just downloaded should
          appear. If it does not, navigate to the folder where you
          downloaded the file, for example with:
          <pre>cd Downloads</pre>
          Then, try again.
        </li>
        <li>
          Press enter. You will follow the text-only prompts. To move through
          the text, press the space key. Type <code>yes</code> and
          press enter to approve the license. Press enter to approve the
          default location for the files. Type <code>yes</code> and
          press enter to prepend Anaconda to your <code>PATH</code>
          (this makes the Anaconda distribution the default Python).
        </li>
        <li>
          Close the terminal window.
        </li>
      </ol>
    </div>
  </div>
{% comment %}
  <p>
  Once you are done installing the software listed above,
  please go to <a href="setup/index.html">this page</a>,
  which has instructions on how to test that everything was installed correctly.
  </p>
{% endcomment %}
</div> {% comment %} End of 'Python' section. {% endcomment %}

<hr/>

<div>
    <h2>Attribution</h2>
    <p>
        This workshop contains material adapted and modified
        from work that is &copy; 2016-2018 <a href="http://software-carpentry.org">Software Carpentry</a>
        and made available under a <a href="https://creativecommons.org/licenses/by/4.0/">
        Creative Commons Attribution</a> license.
    </p>
</div>
