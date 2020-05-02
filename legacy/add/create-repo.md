---
layout: page
title: Create a GitHub Repository to Host a Dataset
permalink: /add/create-repo
exclude: true
comments: true
---

> * Overview: [List Your Dataset on DataHerb]({{site.base_url}}/add)
> * Next step: [Add Your GitHub Repository Name to DataHerb]({{site.base_url}}/add/link-repo-with-dataherb)

## Create your GitHub repository to host your data

> If you have generic questions about GitHub, please [leave a comment](#comments) so we could improve this tutorial.

> If you prefer to learn from examples, simple copy everything from this repo [InterImm/dataset-planets-in-solar-system](https://github.com/InterImm/dataset-planets-in-solar-system) and adapt.

### If you prefer to use the web interface of GitHub

1. Go to [github.com and click on the + on the top right](https://github.com/new)
2. Create a repository for your data. [GitHub Help](https://help.github.com/en/github/getting-started-with-github/create-a-repo)

   <figure>
      <div>
         <img src="{{site.base_url}}/assets/videos/dataherb-demo-ufo-create-new-repo.gif" type="video/gif" />
      </div>
   </figure>

3. Create a folder to hold your data file, in this example, we will create a fold called `dataset`. Click on the `Create new file` button, and type in `dataset/.githold`. This will creae a folder called `dataset` and place a file called `.githold` inside it.
   <figure>
      <div>
         <video  style="display:block; width:100%; height:auto;" autoplay controls loop="loop">
            <source src="{{site.base_url}}/assets/videos/dataherb-demo-ufo-upload-datafile-1.mp4" type="video/mp4" />
         </video>
      </div>
   </figure>

   Upload your data file into this folder by clicking on button `Upload files`.

4. Create a `.dataherb` folder in the root of your repository. Now the folder structure should be

   ```
   .
   ├── README.md
   ├── .dataherb
   ├── dataset
       └── your_data_file
   ```

5. Create a file `metadata.yml` in the `.dataherb` with the following content:

   ```
   name: [Name of your dataset]
   description: [Describe your dataset here]
   contributors:
   - name: [Name of the the first contributor]
   data:
   - name: [name of your data file, optional]
     description: [description of your data file, optional]
     path: [path_to_your_data_file.csv]
     format: csv
     size: [size of your data file]
     fields:
     - name: [name of the first colomn]
       description: [description of the first column]
     - name: [name of the second colomn]
       description: [description of the second column]
   - name: [name of your second data file, optional]
     description: [description of your second data file, optional]
     path: [path_to_your_data_file.csv]
     format: csv
     size: [size of your data file]
     fields:
     - name: [name of the first colomn]
       description: [description of the first column]
     - name: [name of the second colomn]
       description: [description of the second column]
   license:
   - name: [Name of the license of the dataset]
     link: [Link to the license page]
   references:
   - name: [Name of the first reference]
     link: [https://link_to_your_first_reference]
   ```

   > As an example, one could use similar contents as in this demo project [InterImm/dataset-planets-in-solar-system](https://github.com/InterImm/dataset-planets-in-solar-system/blob/master/.dataherb/metadata.yml).


### If you prefer to use the command line

If you use command line for git, the precess is more or less the same. However, there is at least one advantage of using the command line. We have created a command line tool to help you generate the metadata.

1. Install the [dataherb python package](https://pypi.org/project/dataherb/): `pip install dataherb`.
2. Place the data files in a folder like `datasets`.
3. In the root folder of your repo, use the command `dataherb create` and follow the guidlines.


## Next Step

> After creating the repository, you could link your dataset with DataHerb index very easily. Please read [the Next Step: Add Your GitHub Repository Name to DataHerb]({{site.base_url}}/add/link-repo-with-dataherb).