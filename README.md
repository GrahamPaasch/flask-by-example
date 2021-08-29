This is what I had to do to get step 2 to work:
1. name my database after my linux account name
2. == NOT === for Flask-SQLAlchemy
3. Don’t forget a “python -m pip install –upgrade pip” before downloading the requirements
4. Only define specific version for these requirements: Flask==1.1.2, Flask-Migrate==2.5.2, Flask-Script==2.0.6, Flask-SQLAlchemy==2.4.1, psycopg2==2.8.4 Allow all other requires to download any version.
5. If you ever have to delete the migrations or version folder, you ALSO have to update or delete the psql table, or else the folders will auto-generate with mismatched values
6. Add this code to your config.py file so that the database url is modified to be in a compatible syntax with the code: .replace("://", "ql://", 1) or 'sqlite:///myDB.db'
