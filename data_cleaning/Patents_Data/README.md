Below are order of methodology in collecting and processing the patent data reproducibly:

1) Run Get_patents_data.ipynb to Pull patent data from the PatentsView API and return a .csv for each year called

2) Run Clean_and_agg_patent_data.ipynb to clean all the .csv's returned from initial API pull

3) Run Create_index.ipynb to creates patent scores. This creates the scores that help determine 'Score_invented' and 'Score_assigned'
