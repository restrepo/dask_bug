# Dask bug 
Real json data from http://lens.org. The original data with exactly the same `ValueError` to be shown below, is for some specific set of 50,000 records in a file of 150MB. Other similar sets do not show the error and load smootly. Here one small extract of 191 records displaying exactly the same error. 

The error appears when trying to load a json file into a Dask DataFrame with the `blocksize` option with some specific number of records, in this example: 191 records. The error seem to not depend on some specific record, e.g the first one or the last one, or any subset as illustrated in [dfdask.ipynb](./dfdask.ipynb)
