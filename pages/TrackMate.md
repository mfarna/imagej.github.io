---
autogenerated: true
title: TrackMate
breadcrumb: TrackMate
layout: page
author: test author
categories: Segmentation,Tracking,Tutorials,Plugins,Citable
description: test description
---

![TrackMate-Logo85x50-color-300p.png](TrackMate-Logo85x50-color-300p.png
"TrackMate-Logo85x50-color-300p.png") 

## Citation

Please note that TrackMate is available through Fiji, and is based on a
publication. If you use it successfully for your research **please be so
kind to cite our work**:

{% capture includecontent %} TrackMate {% endcapture %}

{% include publication content=includecontent %}

## Presentation

*TrackMate is your buddy for your everyday tracking .*

### Examples

![TrackMate\_Celegans\_devel.gif](TrackMate_Celegans_devel.gif
"TrackMate_Celegans_devel.gif")

The first 2 hours of a *C.elegans* embryo development, followed in 3D
over time using TrackMate (strain:
[AZ212](http://www.wormbase.org/db/gene/strain?name=AZ212;class=Strain))

![TrackMate\_Celegans\_lineage\_detail.png](TrackMate_Celegans_lineage_detail.png
"TrackMate_Celegans_lineage_detail.png")

A detail of the corresponding unannotated lineage visualized in
TrackScheme. The full lineage of this one hour of imaging is
[there](:Image:TrackMate_Celegans_lineage.pdf "wikilink").

![TrackMate\_Split\_Merge\_Gapclosing.gif](TrackMate_Split_Merge_Gapclosing.gif
"TrackMate_Split_Merge_Gapclosing.gif")

TrackMate can be set to detect and deal with gap-closing events,
splitting events and merging events.

![TrackMate Celegans
CellDiameter.png](TrackMate_Celegans_CellDiameter.png
"TrackMate Celegans CellDiameter.png")

TrackMate can also be used for basic track analysis. Here is plotted the
estimated diameter of a *C.elegans* cell as it divides over time.

![TrackMate\_CelegansCellFollowed.gif](TrackMate_CelegansCellFollowed.gif
"TrackMate_CelegansCellFollowed.gif")

A movie following one cell of a *C.elegans* embryo tracked over 3 hours,
as it divides. The track follows the lineage from cell AB to ABaraapap.

%Replace% Clear %Replace%

### Single Particle Tracking

TrackMate provides the tools to perform single particle tracking (SPT).
SPT is an image analysis challenge where the goal is to segment and
follow over time some labelled, spot-like structures. Each spot is
segmented in multiple frames and its trajectory is reconstructed by
assigning it an identity over these frames, in the shape of a track.
These tracks can then be either visualized or yield further analysis
results such as velocity, total displacement, diffusion characteristics,
division events, etc...

TrackMate can deal with single particles, or spot-like objects. They are
bright objects over a dark background for which the object contour shape
is not important, but for which the main information can be extracted
from the X,Y,Z coordinates over time. Examples include sub-resolution
fluorescent spots, labelled traffic vesicles, nuclei or cells imaged at
low resolution.

Though these objects are solely represented by a X,Y,Z,T coordinates
array, TrackMate can compute numerical features for each spot, given its
coordinates and a radius. For instance, the mean, max, min and median
intensity will be computed, as well as the estimated radius and
orientation for each spot, allowing to follow how these feature evolves
over time for one object.

### TrackMate goals

Its development focuses on achieving two concomitant goals:

#### For users

TrackMate aims at offering a generic solution that works out of the box,
through a simple and sensible user interface.

The tracking process is divided in a series of steps, through which you
will be guided thanks to a wizard-like GUI. It privileges tracking
schemes where the segmentation step is decoupled from the
particle-linking step.

The segmentation / filtering / particle-linking processes and results
are visualized immediately in 2D or 3D, allowing to judge their
efficiency and adjust their control parameters. The visualization tools
are the one shipped with Fiji and interact nicely with others plugin.

Several automated segmentation and linking algorithms are provided. But
you are also offered to edit the results manually, or even to completely
skip the automatic steps, and perform fully manual segmentation and/or
linking.

Some tools for track and spot analysis are included. Various plots can
be made directly from the plugin and for instance used to derive
numerical results from the tracks. If they are not enough, functions are
provided to export the whole results to other analysis software such as
[MATLAB](MATLAB "wikilink").

TrackMate relies on several different libraries and plugins for data
manipulation, analysis and visualization. This can be a pitfall when
distributing a complex plugin, but this is where the Fiji magic comes
into play. All dependencies are dealt with by through the Fiji updater.
Installing TrackMate is easy as calling the [Fiji
Updater](Fiji_Updater "wikilink"), and the plugin must work out of the
box. If this does not work for you, then it is a bug and we commit to
fix it.

A strong emphasis is made on performance, and TrackMate will take
advantage of multi-cores hardware.

#### For developers

Have you ever wanted to develop your own segmentation and/or
particle-linking algorithm, but wanted to avoid the painful burden to
also write a GUI, several visualization tools, analysis tools and
exporting facilities? Then TrackMate is for you.

We spent a considerable amount of time making TrackMate extensible in
every aspect. It has a very modular design, that makes it easy to
extend. You can for instance develop your own segmentation algorithm,
extend TrackMate to include it, and benefit from the visualization tools
and the GUI already there. Here is a list of the components you can
extend and customize:

  - detection algorithms
  - particle-linking algorithms
  - numerical features for spots (such as mean intensity, etc..)
  - numerical features for links (such as velocity, orientation, etc..)
  - numerical features for tracks (total displacement, length, etc...)
  - visualization tools
  - post-processing actions (exporting, data massaging, etc...)

You can even modify the GUI, and remove, edit or insert new steps in the
wizard. This can be useful for instance if you want to implement a
tracking scheme that solves simultaneously the segmentation part and the
particle linking part, but still want to take advantage of TrackMate
components.

Do you want to make your new algorithms usable by the reviewers of your
submitted paper? Upload your extended version of TrackMate to a private
update site, as [explained
here](How_to_set_up_and_populate_an_update_site "wikilink"), then send
the link to the reviewers. Now that the paper has been accepted
(congratulations), you want to make it accessible to anyone? Just put
the link to the update site in the article. All of this can happen
without us even noticing.

TrackMate was developed to serve as a tool for Life-Science image
analysis community, so that new tracking tools can be developed more
easily and quickly, and so that end-users can use them to perform their
own research. We will support you if need help to reuse it.

## Documentation and tutorials

The [TrackMate
paper](http://www.sciencedirect.com/science/article/pii/S1046202316303346)
contains a polished, pdf version of the documentation below. But we host
it here:

![TrackMate-manual.pdf](TrackMate-manual.pdf "TrackMate-manual.pdf") 14
MB

  - TrackMate version history: Please look at the gihub page for
    TrackMate releases:

https://github.com/fiji/TrackMate/releases

  - [TrackMate FAQ](TrackMate_FAQ "wikilink")

### For users

  - [Getting started with
    TrackMate](Getting_started_with_TrackMate "wikilink") is a basic
    tutorial that explains how TrackMate works on an easy image. You
    should start here.
  - [TrackScheme](TrackScheme "wikilink"): the tool for the
    visualization, editing and analysis of tracks.
  - [Manual tracking with
    TrackMate](Manual_tracking_with_TrackMate "wikilink")
  - [Manual editing of tracks using
    TrackMate](Manual_editing_of_tracks_using_TrackMate "wikilink")
    shows how to manually curate and edit tracking results.
  - [Track analysis using
    TrackMate](Track_analysis_using_TrackMate "wikilink")
  - [TrackMate Algorithms](TrackMate_Algorithms "wikilink") details and
    documents the automated segmentation algorithms, particle-linking
    algorithms, etc.. currently implemented in TrackMate.
  - [Using TrackMate with
    MATLAB](Using_TrackMate_with_MATLAB "wikilink") documents the
    [MATLAB](MATLAB "wikilink") functions shipped with Fiji that allows
    importing data generated with TrackMate into
    [MATLAB](MATLAB "wikilink").
  - [TrackMate Performance](TrackMate_Performance "wikilink") reports
    various measures of the performance of its components. Performance
    reports include execution time and memory usage.
  - [TrackMate Accuracy](TrackMate_Accuracy "wikilink") reports various
    measures of the accuracy of its components. Accuracy reports how
    well TrackMate can generate scientifically correct results, and
    compare its output to known ground truth.
  - Various very useful tips and tricks contributed by users:
      - Dave Mason on using pivot tables to get track statistics based
        on spot features:
        [1](https://forum.image.sc/t/mean-intensity-of-tracks-using-trackmate/11848/5)

### For developers

  - [Scripting TrackMate](Scripting_TrackMate "wikilink") shows how to
    do tracking using a scripting language, *e.g.* from the Fiji [Script
    Editor](Script_Editor "wikilink"). These example scripts will show
    you how to use TrackMate as a library and familiarize yourself with
    the API.
  - [Using TrackMate from
    MATLAB](Using_TrackMate_from_MATLAB "wikilink") shows how to use
    [MATLAB](MATLAB "wikilink") as a scripting language for TrackMate,
    and benefit from [MATLAB](MATLAB "wikilink") facilities.

But the really interesting part for developers is the ability to extend
TrackMate.

Do you have a tracking or a detection algorithm you want to implement?
Of course you can write a whole software from scratch. But at some point
you will have to design a model to hold the data, to write code that can
load and save the results, visualize them, have even a minimalistic GUI,
and allow to manually correct the outcome of your algorithm. This can be
long, tedious and boring, while the part that interests you is just the
core algorithm.

We propose you to use TrackMate as a home for your algorithm. The
framework is already there; it might not be perfect but can get your
algorithm integrated very quickly. And then you can benefit from the
other modules.

The subject of extending TrackMate is not completely trivial. However,
recent advances in the [SciJava package](http://www.scijava.org/),
brewed by the Fiji and ImageJ2 teams considerably simplified the task.
It should be of no difficulty for an average Java developer.

The following tutorials show how to integrate a module of each kind in
TrackMate. They are listed by increasing complexity, and it is a good
idea to practice them in this order.

  - [How to write your own edge feature analyzer algorithm for
    TrackMate](How_to_write_your_own_edge_feature_analyzer_algorithm_for_TrackMate "wikilink")
  - [How to write your own track feature analyzer algorithm for
    TrackMate](How_to_write_your_own_track_feature_analyzer_algorithm_for_TrackMate "wikilink")
  - [How to write your own spot feature analyzer algorithm for
    TrackMate](How_to_write_your_own_spot_feature_analyzer_algorithm_for_TrackMate "wikilink")
  - [How to write your own viewer for
    TrackMate](How_to_write_your_own_viewer_for_TrackMate "wikilink")
  - [How to write custom actions for
    TrackMate](How_to_write_custom_actions_for_TrackMate "wikilink")
  - [How to write your own detection algorithm for
    TrackMate](How_to_write_your_own_detection_algorithm_for_TrackMate "wikilink")
  - [How to write your own particle-linking algorithm for
    TrackMate](How_to_write_your_own_particle-linking_algorithm_for_TrackMate "wikilink")

## Known problems

TrackMate LoG detector will crash if you have the {% include
list-of-update-sites content='Mosaic suite update site' %} activated.
Apparently they ship something that interferes with the FFT code used by
the LoG detector. The bug report can be read [on
BugZilla](https://fiji.sc/bugzilla/show_bug.cgi?id=806).

## Extensions

Please tell us if you have one that you want to advertise here\!

### Downloadable jars

Thanks to Travis, the extension we are aware of are built automatically
and can be downloaded following the links below. They point to a simple
.jar file that you just have to drop in your *Fiji.app/jars* folder.
TrackMate will recognise the extra modules it ships and will integrate
them in the plugin.

<table>
<thead>
<tr class="header">
<th><p>Extension name</p></th>
<th><p>Content</p></th>
<th><p>Authors</p></th>
<th><p>Link to jar file</p></th>
<th><p>Source code</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>TrackMate-extras</p></td>
<td><p>Various small additions to TrackMate:</p>
<ul>
<li>Multi-channel spot mean intensity analyzer: Computes the mean intensity of spots in up to 10 channels.</li>
<li>Multi-channel track mean intensity analyzer: Computes the track mean intensity of its spots in up to 10 channels.</li>
<li>ROI exporter: Exports spots as ImageJ ROIs.</li>
</ul></td>
<td><p>Benoit Lombardo &amp; Jean-Yves Tinevez</p></td>
<td><p><a href="http://maven.imagej.net/service/local/repositories/releases/content/org/scijava/TrackMate_extras/0.0.4/TrackMate_extras-0.0.4.jar">on ImageJ maven Nexus</a></p></td>
<td><p><a href="https://github.com/tinevez/TrackMate-extras">on Github</a></p></td>
</tr>
<tr class="even">
<td><p><a href="Find_maxima_(Trackmate_module)" title="wikilink">Find maxima (Trackmate module)</a></p></td>
<td><p>This plugin implements the find maxima detection algorithm for TrackMateas in the <i>Process -&gt; Find Maxima...</i> command. The results are almost the same. Subpixel accuracy is activated by default.</p></td>
<td><p>Thorsten Wagner</p></td>
<td><p><a href="https://github.com/thorstenwagner/ij-trackmate-findmaxima/releases/latest">on Github</a></p></td>
<td><p><a href="https://github.com/thorstenwagner/ij-trackmate-findmaxima">on Github</a></p></td>
</tr>
<tr class="odd">
<td><p>Track analysis</p></td>
<td><p>This extension ships several track analyzers that yield more statistics on tracks. Such as:</p>
<ul>
<li>TOTAL_DISTANCE_TRAVELED</li>
<li>MAX_DISTANCE_TRAVELED</li>
<li>TRACK_CONFINMENT_RATIO</li>
<li>MEAN_STRAIGHT_LINE_SPEED</li>
<li>LINEARITY_OF_FORWARD_PROGRESSION</li>
<li>MEAN_DIRECTIONAL_CHANGE_RATE</li>
</ul></td>
<td><p>Jean-Yves Tinevez</p></td>
<td><p><a href="http://maven.imagej.net/content/repositories/snapshots/sc/fiji/TrackMate_trackanalysis/0.0.1-SNAPSHOT/TrackMate_trackanalysis-0.0.1-20170614.171211-1.jar">on ImageJ maven Nexus</a></p></td>
<td><p><a href="https://github.com/tinevez/TrackMate-TrackAnalysis">on Github</a></p></td>
</tr>
<tr class="even">
<td><p>TrackMate -&gt; Spot-On connector</p></td>
<td><p>This extension adds an action allowing to automatically transfer a tracking analysis performed in TrackMate to <a href="https://spoton.berkeley.edu">Spot-On</a>, without having to export the tracks and reimport them. Spot-On is a web-interface designed for the analysis of single-molecule tracking experiments.</p></td>
<td><p>Maxime Woringer</p></td>
<td><p><a href="https://gitlab.com/tjian-darzacq-lab/Spot-On-TrackMate/tags">on Gitlab</a></p></td>
<td><p><a href="https://gitlab.com/tjian-darzacq-lab/Spot-On-TrackMate">on Gitlab</a></p></td>
</tr>
</tbody>
</table>

### Extra source code

[Ronny Sczech TrackMate
repository](https://github.com/chicoronny/RonnyTrackMate) contains the
source code to various TrackMate enhancements, in Java and macros:

  - Linear Tracker for TrackMate.

Principle:

  -   - Link and set a flag for all objects that are sticking more than
        80% of the time lapse movie, i.e not moving within a preset
        radius (Stick radius)
      - Establish a first possible link from an object from the first
        frame with an object in the second frame within an initial
        radius
      - Estimate the position of the object in the next frame (3rd) with
        the obtained vector
      - Link to an object near to this estimated position within a
        succeeding radius
      - Go on to the next frame until the last is reached

<!-- end list -->

  - Batch Mode Plugin to run TrackMate headless from a configuration
    file (example:Trackmate.properties) which has to placed in the
    parent folder of the processed files.

<!-- end list -->

  - Binary Detector to detect objects from a binary image using the
    ParticleAnalyzer class from ImageJ.

<!-- end list -->

  - Export tracks to SQLite.

<!-- end list -->

  - Export tracks to CSV files.

### Documentation

  - [Find maxima detector](Find_maxima_\(Trackmate_module\) "wikilink")
    from Thorsten Wagner.

## Who uses TrackMate

It turns out that TrackMate has a decent user base, as exemplified by a
crude search on [Google
Scholar](https://scholar.google.fr/scholar?q=trackmate+fiji). These
citations accumulated before the TrackMate paper was out.

## TrackMate components

TrackMate actually depends on many other Fiji plugins or libraries. The
[Fiji Build System](Fiji_Build_System "wikilink") system and the [Fiji
Updater](Fiji_Updater "wikilink") ensures that these dependencies will
not bother you. We list them here, with their author when they are not
obviously linked:

  - [ImgLib2](ImgLib2 "wikilink") is used everywhere we need dealing
    with pixels. Relying on imglib made it trivial to have a plugin that
    deals indifferently with 2D or 3D images. In particular, we use code
    from Stephan Preibisch, {% include person content='Saalfeld' %},
    Larry Lindsey and Lee Kamentsky.
  - [ImageJA](ImageJA "wikilink") is of course the entry point for the
    plugin. We use it display the images as 2D slices and in the
    HyperStack displayer.
  - The [3D Viewer](3D_Viewer "wikilink") is used for 3D display.
  - Internally, the tracks are represented by a mathematical
    [graph](wikipedia:Graph_%28mathematics%29 "wikilink"). To manipulate
    it, we take advantage of the excellent
    [JGraphT](http://www.jgrapht.org/) library.
  - TrackScheme, the TrackMate component that is used to visualize and
    edit tracks uses [JGraphX](http://www.jgraph.com/jgraph.html) for
    its UI.
  - To display plots and histograms we use
    [JFreeChart](http://www.jfree.org/jfreechart/).
  - Some algorithm in TrackMate rely on the
    [JAMA](http://math.nist.gov/javanumerics/jama/) matrix package.
  - Exporting visualizations and analysis results to SVG, PDF and other
    formats are made through the
    [Batik](http://xmlgraphics.apache.org/batik/) and
    [iText](http://itextpdf.com/) libraries.
  - The TrackMate file format is plain XML, and is generated or loaded
    using the [JDom](http://www.jdom.org/) library.
  - For the icons, as almost every ImageJ plugin with a GUI, we used the
    [silk icon set](http://www.famfamfam.com/lab/icons/silk/), by Mark
    James. But we are also very lucky to have icons and logos designed
    specifically for TrackMate by
    [IlluScienta](http://www.illuscientia.com/).

## Acknowledgements

We are extremely thankful for the support of [Khuloud
Jaqaman](http://www.utsouthwestern.edu/labs/jaqaman/) while we were
implementing in Java a stripped down version of her work on robust LAP
tracker, following her seminal paper published in the Danuser
group\[1\].

JYT acknowledges funding from the European commission FP7 ICT ([project
“MEMI”](http://www.memi-fp7.org)) at the beginning of this project. NP
was a visiting student thanks to funds provisioned by the Stanford
University. JS acknowledges funding from the Laboratory for Optical and
Computational Instrumentation at the UW-Madison and National Science
Foundation award \#1121998.

<references/>

[Category:Segmentation](Category:Segmentation "wikilink")
[Category:Tracking](Category:Tracking "wikilink")
[Category:Tutorials](Category:Tutorials "wikilink")
[Category:Plugins](Category:Plugins "wikilink")
[Category:Citable](Category:Citable "wikilink")

1.  Jaqaman et al. *Robust single-particle tracking in live-cell
    time-lapse sequences*. **Nat Methods** (2008) vol. 5 (8) pp. 695-702