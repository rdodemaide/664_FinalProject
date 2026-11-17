Project Title: Diablo IV Build Guides

Project Description: explains what the project does.  For this project, I am scraping the Icy Veins Diablo IV build guide website.  I am scraping the information to compare different builds and determine how similar different builds are, and if certain classes have more overlap between builds than others.

Rationale Statement: expresses the motivations behind the project.  Diablo IV builds are very complex, and without a build guide it takes many hours of work to determine the best combinations of gear, skills, and other items.  As a seasonal player, I need a new build every ~90 days, so prefer to use a build guide rather than figuring all of this out from scratch each season.  Build guide websites don't provide ways to compare guides, however, so I would like to create a way to compare builds.  

Workflow: identifies libraries used and explains the important steps being taken in the code.  I have used BeautifulSoup4 to scrape data from Icy Veins, beginning with the main page listing all build guides. From this page, I searched by html attributes to retrieve the URL for each individual build, along with each build’s Tier ranking, class, and build name. Then, using the URLs retrieved, I created empty lists and searched each individual build page to retrieve the 6 associated skills by searching by class, as well as any mythic gear needed by searching each page for the associated attribute. For both skills and mythic gear I joined the retrieved data into strings so that the data would be compatible with creating a dataframe in Pandas.  I have exported the dataframe created by Pandas into a csv, and will next clean up the data in OpenRefine.  To determine the most popular skills and gear items for each class, I will create a new
dataframe for each class in Python using Pandas, then use value_count for the skills and gear columns to get totals for each skill and gear item. Using Pandas I will also create a bar graph to show the number of builds in each Tier ranking per class, which will help determine if certain classes are performing better overall in the current season.

Further Uses: in what ways might someone build on this work or re-use your code.

Files List: (a list of files relevant to the project (python notebooks, csv files, etc) and a brief description of what each file contains)
