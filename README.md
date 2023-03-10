# kindle_clippings
Jupyter notebooks to make your Kindle clippings txt file more useful.

# getting started
1. copy the Jupyter notebook to Colab.
2. connect your Kindle to your PC and navigate to your `/documents` folder. Copy the `My_Clippings.txt` file to your Colab default directory.
3. copy the `blank.csv` file to the default Colab directory
4. run the notebook

# when you already have vocabulary words and definitions
Save them to a csv file called `2DoList.csv` with the csv format. Duplicate the csv format found in `Kindle_vocab.csv` (essentially WORD and DEFINITION) for your own vocabulary file. When re-running the Jupyter notebook you should then have your old words plus the new words from the Kindle clipping text file.

Note that the `Kindle_vocab_updated.csv` file will be the reference vocabulary file going forward. You can save this file or load it in other applications.

# oxford dictionary lookup.ipynb
Uses the Oxford Dictionary API to automatically lookup definitions for words saved in the Kindle vocabulary file. You will need to register for your free API key. Note that Oxford also imposes traffic limits on the number of definitions it can lookup in the free tier.

# suggested uses
Beside providing an automated method of updating your vocabulary database (with definitions using the `oxford dictionary lookup.ipyb` notebook), the Kindle clippings reader notebook provides an easy way to extract information from the Kindle clippings text file.
1. list all the books, pdfs and other sources you clipped from
2. search for words in specific sources or all sources, with detailed references as to when it was clipped and where. You can use two search terms. `Tesla | China` searches for Tesla or China while `Tesla .* China` searches for Tesla and China.
3. get an idea as to the distribution of your clipping lengths
4. get an overview of the topics covered and key words from your clippings
