---
layout: page
title: Add Your GitHub Repository Name to DataHerb
permalink: /add/link-repo-with-dataherb
exclude: true
comments: true
---

> * Overview: [List Your Dataset on DataHerb]({{site.base_url}}/add)
> * Prevous step: [Create a GitHub Repository to Host a Dataset]({{site.base_url}}/add/create-repo)

> Before adding your github repository to DataHerb, we reqire a `.dataherb` folder and a `metadata.yml` file in your `.dataherb` folder. Please read [this tutorial: Create a GitHub Repository to Host a Dataset]({{site.base_url}}/add/create-repo).

## Add your GitHub repository name to DataHerb

1. Go to [DataHerb/dataherb-flora](https://github.com/DataHerb/dataherb-flora).
2. Create a new file inside the folder `flora`: [Use this link and click on the *Create new file* button](https://github.com/DataHerb/dataherb-flora/tree/master/flora).

   The file name should be descriptive. Do not use spaces in the file name. The file should contain

   ```
   - name: Name of the dataset
     repository: repository_owner/repository_name
     tags:
       - A tag your data
       - Another tag for your data
   ```

   For example, the dataset [InterImm/dataset-planets-in-solar-system](https://github.com/InterImm/dataset-planets-in-solar-system) is represented in the flora as [planets_in_solar_system.yml](https://github.com/DataHerb/dataherb-flora/blob/master/flora/planets_in_solar_system.yml) with the following content.

   ```
   - name: Planets in the Solar System
     repository: InterImm/dataset-planets-in-solar-system
     tags:
       - Astronomy
   ```

3. Create a new Pull Request and tell us what you have added.

   <figure>
      <div>
         <img src="{{site.base_url}}/assets/videos/dataherb-ufo-create-new-pr.gif" type="video/gif" />
      </div>
   </figure>

> We do not take your data. The data page will link to your GitHub repository and the corresponding data files.


