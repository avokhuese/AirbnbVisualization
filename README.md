# Report document

The following document explains the design of the assignment related to analysis over the Airbnb UK 2022 dataset.

# Dataset

Each row of the CSV describes a listing in Airbnb, containing various features/attributes of a listing such as number of bedrooms, rating, accomodations, price, etc.

The objective of this assignment is to familiarize with data science tools, such as `pandas` and `csv` (which we will talk more about in the next section). Also to get hands-on experience with data-visualization techniques and tools using the `matplotlib` library.

# Tooling

The environment used was Python 3.10, although any version beyond Python 3.9 will work.

A Jupyter notebook was created containing all the code for this assignment. We defined various python functions to encapsulate functionality and make it easier to work with.

For CSV parsing we used the `csv` and `pandas` module as required. `pandas` let us manipulate with ease the dataset and it includes many useful methods and functions that saves us a bunch of time when performing repetitive tools (such as calculating statistics and plotting series).

The `csv` module, on the other hand, is low-level compared with `pandas`, and it requires more work to do basic tasks. It's not as batteries-ready as `pandas`, but it's good for simple tasks (simple queries and projections).

The `matplotlib` library was used, most of the times, through `pandas` wrappers. That is, instead of running `plt.plot`, we used `pandas.dataframe.plot`. The end result is the same, and it saves a few lines for formatting-related tasks such as adding titles and labels to our plots.

The only extra library we used was `ast`, and it was needed to parse the `host_verifications` and `amenities` of a listing, since those were list of strings, and each string may have inside a comma, parsing using simple regexes or replacing might be cumbersome to have something working properly. Using `ast.literal_eval` did the trick. Another option was using `json`, but we prefer this one, since the values are not exactly in JSON format (close, but not exact).

# Results

The results of this assignment can be better seen on the notebook. To summarize, we could find interesting features about this dataset using data-visualization, and we noted the importance of doing proper cleaning, since they were a few plots with weird points, specifically called **outliers**.

We recommend to introduce data-cleaning tasks in the future after running exploration of the dataset, thus it makes the report more accurate and interesting at the end.
