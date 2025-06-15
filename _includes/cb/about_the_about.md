{% comment %}
    Find some sample images or use defaults for About demos
{% endcomment %}
{% assign imagesample = site.data[site.metadata] | where_exp: 'item','item.format contains "image"' | first %}
{% capture imagesampleid %}{{ imagesample.objectid | default: "https://www.lib.uidaho.edu/collectionbuilder/demo-objects/mg101_b6_photographs_01.jpg" }}{% endcapture %}
{% assign pdfsample = site.data[site.metadata] | where_exp: 'item','item.format contains "pdf"' | first %}
{% capture pdfsampleid %}{{ pdfsample.objectid | default: "https://www.lib.uidaho.edu/collectionbuilder/demo-objects/uiext21768.pdf" }}{% endcapture %}
{% assign videosample = site.data[site.metadata] | where_exp: 'item','item.format contains "video"' | first %}
{% capture videosampleid %}{{ videosample.objectid | default: "https://cdil.lib.uidaho.edu/storying-extinction/objects/trailcams/videos/ballcreek-cedarrub-birdonpath.mp4" }}{% endcapture %}
{% assign audiosample = site.data[site.metadata] | where_exp: 'item','item.format contains "audio"' | first %}
{% capture audiosampleid %}{{ audiosample.objectid | default: "https://www.lib.uidaho.edu/digital/mp3s/Clouds.mp3" }}{% endcapture %}

### GLOBALISE
GLOBALISE is a digital infrastructure project committed to enhancing the accessibility and research potential of the UNESCO Memory of the World-listed Dutch East India Company (VOC) archives. Our mission is to empower researchers and the general public to explore these archives and write new, inclusive histories.

Through this initiative, we invite researchers, citizen scientists and community partners to be involved with us co-creating new stories.

{% include feature/video.html objectid=videosampleid width="75" %}
Do you have an interesting story to share? Would you contribute to our collection?
[Get in touch with us!](https://globalise.huygens.knaw.nl/contact-us/)

For inspiration, feel free to [explore](/browse.html) stories in this website, on our [blog](https://globalise.huygens.knaw.nl/globalise-blog/), and read more about [working with us](https://globalise.huygens.knaw.nl/work-with-us/).


### Acknowledgements
[GLOBALISE](https://globalise.huygens.knaw.nl/) is a project of the Huygens Institute with the International Institute of Social History, the Digital Infrastructure Department of the KNAW Humanities Cluster, VU University, the University of Amsterdam, and the Dutch National Archives. It is funded by the Dutch Research Council (NWO), grant no. 175.2019.003.

The archival sources featured in this collection comes from the Dutch East India Company archives, 1.04.02 at [Nationaal Archief, Den Haag](https://www.nationaalarchief.nl/en/research/archive/1.04.02).

Archival transcriptions are generated through GLOBALISE's [Transcriptions Viewer](https://transcriptions.globalise.huygens.knaw.nl).


{% comment %}
The template provides includes to pull your collection objects and metadata into your interpretive page, allowing you to write with your materials directly embedded in the content.
#### Include an Image
- Image --> `{% raw %}{% include feature/image.html objectid="demo_001" width="75" %}{% endraw %}`
{% include feature/image.html objectid=imagesampleid width="75" %}
#### Include a PDF
- PDF -- > `{% raw %}{% include feature/pdf.html objectid="demo_002"  width="50" %}{% endraw %}`
{% include feature/pdf.html objectid=pdfsampleid width="50" %}
{% endcomment %}

{% comment %}
#### Include an Audio File
- Audio: `{% raw %}{% include feature/audio.html objectid="demo_003" %}{% endraw %}`
{% include feature/audio.html objectid=audiosampleid  %}
### Include Bootstrap Features
The template also provides includes to make it easier to add [Bootstrap](https://getbootstrap.com/) components to your Markdown writing.
These features allow you to better organize and highlight your content.
#### Include a Card
- Card -- > `{% raw %}{% include feature/card.html header="This is a Card" text="The card features an image from the collection as a cap" objectid="demo004" width="25" centered=true %}{% endraw %}`
{% include feature/card.html header="This is a Card" text="The card features an image from the collection as a cap" objectid=imagesampleid width="50" centered=true %}

#### Include a Button 
- Buttons -- > `{% raw %}{% include feature/button.html text="Button Link to Somewhere" link="https://collectionbuilder.github.io/" color="success" %}{% endraw %}`

{% include feature/button.html text="Button Link to Somewhere" link="https://collectionbuilder.github.io/" color="success" centered=true %}
  
#### Include an Alert
- Alerts -- > `{% raw %}{% include feature/alert.html text="this is an *alert* that 'warns' a user" color="warning" align="center" %}{% endraw %}`
{% include feature/alert.html text="This is an *alert* that 'warns' a user with centrally aligned text." color="warning" align="center"  %}

#### Include a Modal
- Modals -- > `{% raw %}{% include feature/modal.html button="This is a modal using a 'primary' colored button to invite clicking" title="when clicked:" text="A Modal will pop out a box with some more information" color="primary"  %}{% endraw %}`
{% include feature/modal.html button="This is a modal using a 'primary' colored button to invite clicking" title="When clicked:" text="A Modal will pop out a box with some more information" color="primary"  %} {% endcomment %}
