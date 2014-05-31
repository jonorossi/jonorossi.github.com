---
layout: page
title: "Castle Visual Studio Integration"
comments: false
sharing: false
footer: false
---

{% img right /projects/cvsi/cvsi_logo.png %}

Castle Visual Studio Integration (CVSI) provides Microsoft Visual Studio integration for the Castle Project.
Currently it only contains a colorizer and IntelliSense for the NVelocity language.

__New Project Wizard:__ If you are looking for the New Project wizard you will need the official Visual Studio integration.
See the [Castle Project web site][1] for more details.

### Releases
* __0.5.0:__ (25 May 2014, [2b91889][5])
  * __VS2013:__ <a href="cvsi-0.5.0-vs2013.vsix">cvsi-0.5.0-vs2013.vsix</a>
  * __VS2012:__ <a href="cvsi-0.5.0-vs2012.vsix">cvsi-0.5.0-vs2012.vsix</a>
  * __VS2005/2008/2010:__ No changes from 0.4.0
  * __Note:__ I haven't been able to work out how to have a single vsix on the Visual Studio Gallery for all Visual Studio versions so 2012 and 2013 will be here for now.
* __0.4.0:__ (07 Mar 2011, c6cbce9)
  * __VS2010:__ See the [Visual Studio Gallery][2]</a> (or search for 'castle' in the Visual Studio Extension Manager)
  * __VS2005/2008:__ No changes from 0.3.2
* __0.3.2:__ <a href="CVSI-0.3.2.msi">CVSI-0.3.2.msi</a> (1.26 MB, 30 Sep 2008, r625, VS2005/2008)
* __0.3.1:__ <a href="CVSI-0.3.1.msi">CVSI-0.3.1.msi</a> (1.26 MB, 15 Aug 2008, r616, VS2005/2008)
* __0.3.0:__ <a href="CVSI-0.3.0.msi">CVSI-0.3.0.msi</a> (1.26 MB, 29 Jun 2008, r576, VS2005/2008)
* __0.2.1:__ <a href="CVSI-0.2.1.zip">CVSI-0.2.1.zip</a> (178 KB, 29 Oct 2007, r339, VS2005)
* __0.2.0:__ <a href="CVSI-0.2.0-Alpha.zip">CVSI-0.2.0-Alpha.zip</a> (177 KB, 09 Oct 2007, r317, VS2005)
* __0.1.3:__ <a href="CVSI-0.1.3-Preview1Update.zip">CVSI-0.1.3-Preview1Update.zip</a> (23 KB, 27 Jul 2007, r257, VS2005)
* __0.1.2:__ <a href="CVSI-0.1.2-Preview1Update.zip">CVSI-0.1.2-Preview1Update.zip</a> (22 KB, 13 Jul 2007, r253, VS2005)
* __0.1.1:__ <a href="CVSI-0.1.1-Preview1Update.zip">CVSI-0.1.1-Preview1Update.zip</a> (22 KB, 12 Jul 2007, r252, VS2005)
* __0.1.0:__ <a href="CVSI-0.1-Preview1.msi">CVSI-0.1-Preview1.msi</a> (636 KB, 01 Jul 2007, r245, VS2005)

### Source Code & License
<p style="float: right;">
  <script type="text/javascript" src="http://www.ohloh.net/p/6484/widgets/project_partner_badge.js"></script>
</p>

* __Source Code:__ [https://github.com/jonorossi/cvsi][3]
* __Change Log:__ See [Changes.txt][4] for full details of the changes.
* __License:__ Apache License Version 2.0

### Having trouble with syntax hightlighting not working?
Visual Studio (especially 2012+) seems to aggressively cache its fonts and colours cache.
You'll need to manually reset the cache by deleting the Cache key in the registry:

    HKEY_CURRENT_USER\Software\Microsoft\VisualStudio\xx.0\FontAndColors\Cache

### Screenshots
[{% img /projects/cvsi/screenshots/colorizer_large.png %}](/projects/cvsi/screenshots/colorizer_large.png)

#### Directives
{% img /projects/cvsi/screenshots/directives.png %}
    
#### Helpers
{% img /projects/cvsi/screenshots/helpers.png %}
{% img /projects/cvsi/screenshots/helper-methods.png %}
{% img /projects/cvsi/screenshots/helper-method-overloads.png %}

#### View Components
{% img /projects/cvsi/screenshots/viewcomponents.png %}

[1]: http://www.castleproject.org/castle/vsintegration.html
[2]: http://visualstudiogallery.msdn.microsoft.com/5f5f4523-95f6-4277-b499-959950368a4d
[3]: https://github.com/jonorossi/cvsi
[4]: https://github.com/jonorossi/cvsi/blob/master/doc/Changes.txt
[5]: https://github.com/jonorossi/cvsi/commit/2b91889acb7430c6f6893f1321c3c151ccecaca8
