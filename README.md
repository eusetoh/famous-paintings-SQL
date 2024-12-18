Basic SQL script doing two things: (1) generate list of the average price of a painting by artist, and (2) generate list of museums that are open on both monday and sunday.

Task 1: Generate list of the average price of a painting by artist

    Step 1: Create new temporary table using columns sale_price and work_id from product_size table, and columns artist_id from work table, and full_name from artist table
            a: Left join the work table to product_size table using the work.id column
            b: Left join the artist table to the product_size table in (a) using artist_id column 
    Step 2: Use new table to find the average price of artworks grouped by artist
            a: Remove the missing values for cleaner output

Task 2: Generate list of museums that are open on both monday and sunday

    Step 1: Create temporary table for all museums open on Monday by joining musesum_id column from museum_hours table and museum table
    Step 2: Create temporary table for all museums open on Sunday by joining musesum_id column from museum_hours table and museum table
    Step 3: Inner join the first table onto the second table (only museums open on both days will appear in this final table)

Data taken from: https://www.kaggle.com/datasets/mexwell/famous-paintings
