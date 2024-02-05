# kindle_clippings
Jupyter notebooks to make your Kindle clippings txt file more useful.

# getting started
1. copy the `Kindle_my_clippings_reader.ipynb` notebook to Colab by pressing the `Open in Colab` button.
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
2. search for words in specific sources or all sources, with detailed references as to when it was clipped and where. You can use two search terms. `Tesla | China` searches for Tesla **or** China while `Tesla .* China` searches for Tesla **and** China.
3. get an idea as to the distribution of your clipping lengths
4. get an overview of the topics covered and key words from your clippings

# addition of Kindle Scribe
The file structure for the Kindle Scribe adds an additional line in one of the fields, thus rendering the original clipping notebook inapplicable. The new notebook is designed specifically to handle the irregular line lengths found in the Kindle Scribe clippings text.

In addition, I experimented with a convenient LLM found in OpenVINO and was able to use the clippings dataframe as a local source for the language model. The OpenVINO performance was surprisingly good but the end results, while curious, are not production ready as they are basic at best. Still, the idea of tuning a LLM on local source text is interesting:
1. automatically gather text clippings while using the Kindle Scribe normally
2. process the clippings using `Kindle_scribe_my_clippings_reader_polars_cupy.ipynb` to automatically create and save a dataframe
3. load up a LLM notebook and use the dataframe columns (source and quotation) as local source text for fine tuning the LLM

With better and better LLM models, the performance of this workflow should improve. I describe a sample notebook modified from the OpenVINO example in the `local_llm_processing.ipynb` notebook as a first try in exploring the use of LLM in local source text processing.
