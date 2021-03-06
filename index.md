---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: splash
title: PyBpod
excerpt: Real-time behaviour measurement software
header:
    overlay_color: "#333"
    overlay_image: /assets/images/pybpod2.png
    actions:
    - label: "Documentation"
      url: "https://pybpod.readthedocs.io"
    - label: "Source code"
      url: "https://github.com/pybpod/pybpod"

feature_row_code:
  - image_path: /assets/images/github_logo.png
    alt: "Github logo"
    title: "Open source"
    excerpt: |
      PyBpod's related code is hosted in several repositories on GitHub.

    url: "https://github.com/pybpod/"
    btn_label: "PyBpod on GitHub"
    btn_class: "btn--inverse"
feature_row_pypi:
  - image_path: /assets/images/pypi.png
    alt: "PyPI logo"
    title: "Available in PyPI"
    excerpt: |
      Available through Python Package Index (PyPI) with  
      ``` pip install pybpod ```  

      More detailed installation instructions on the [Installing and updating](https://pybpod.readthedocs.io/en/v1.7.8/getting-started/install.html){:target="_blank"} <i class="fas fa-external-link-alt fa-xs"/> section of the documentation.
    url: "https://pypi.org/project/pybpod/"
    btn_label: "PyBpod on PyPI"
    btn_class: "btn--inverse"
feature_row_rtd:
  - image_path: /assets/images/rtd-logo-wordmark-dark.svg
    alt: "Read the docs wordmark logo"
    title: "Documentation"
    excerpt: |
      Extensive documentation available online and hosted on Read the Docs.


    url: "https://pybpod.readthedocs.io"
    btn_label: "PyBpod on Read the Docs"
    btn_class: "btn--inverse"
feature_row_plugins:
  - image_path: /assets/images/puzzle-team.svg
    title: "Extensible"
    excerpt: "PyBpod was designed from the start with extensibility in mind.You can use the plugins already developed to extend PyBpod's functionality or develop your own to fit your needs."
    url: "/plugins"
    btn_label: "See available plugins"
    btn_class: "btn--inverse"
---
{% capture notice-text %}
* [Bpod device](https://sanworks.io/shop/viewproduct?productID=1024){% include external-link.html %}
* [Bpod on Github](https://github.com/sanworks/Bpod){% include external-link.html %}
* [Bpod Wiki](https://sites.google.com/site/bpoddocumentation/){% include external-link.html %}
* [BControl project](http://brodywiki.princeton.edu/bcontrol/index.php/Main_Page/){% include external-link.html %}
{% endcapture %}

![bpod state machine](/assets/images/bpod.jpg){: .align-right}
# Bpod #
Bpod is a system from [Sanworks](https://sanworks.io){% include external-link.html %} for precise measurement of small animal behaviour. It is a family of open source hardware devices which includes also software and firmware to control these devices. The Bpod State Machine can connect to different modules
such as a Valve Driver, Analog Input, Analog Output, an Optical Lickmeter, among others. More information regarding available modules can be found at [Sanworks Store website](https://sanworks.io/shop/products.php?productFamily=bpod){% include external-link.html %}.

The software was originally developed in MATLAB providing retro-compatibility with the BControl system.

<div class="notice--info">
  <h4>For further information on Bpod please check the following links</h4>
  {{ notice-text | markdownify }}
</div>

{% include feature_row id="intro" type="center" %}

# PyBpod #
PyBpod is a Python port of the [Bpod Matlab project](https://github.com/sanworks/Bpod>){% include external-link.html %}. It is a GUI application that enables interaction with the latest [Bpod devices](https://sanworks.io/shop/products.php?productFamily=bpod){% include external-link.html %}.

This project is maintained by a team of software developers at the [Champalimaud Foundation](http://research.fchampalimaud.org){% include external-link.html %}.

{% include feature_row id="intro" type="center" %}

{% include feature_row id="feature_row_code" type="left" %}

{% include feature_row id="feature_row_rtd" type="right" %}

{% include feature_row id="feature_row_pypi" type="left" %}

{% include feature_row id="feature_row_plugins" type="right" %}


<!-- 
{% highlight python linenos %}
def my_softcode_handler(data):
    global start, soundStream, timeit, cam, camOK
    print(data)
    if data == 55:
        print("----PLAY-----")
        soundStream.playSound()
        start = timeit.default_timer()
        if not camOK:
            cam.record()
            camOK = True
    elif data == 66:
        soundStream.stopSound()
        print(':::::::::Time to stop:::::::::', timeit.default_timer() - start)
#=> prints 'Hi, Tom' to STDOUT.
{% endhighlight %} -->
