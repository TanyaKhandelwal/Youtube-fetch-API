# Youtube Fetch Api
An API to fetch latest videos from youtube sorted in reverse chronological order of their publishing date-time from YouTube for a given tag/search query in a paginated response.

The server fetches latest videos async after every 10 minutes and saves it to the db.

It is completely based on Django.

## Method Used

Used Cron Jobs [django_cron](https://django-cron.readthedocs.io/en/latest/introduction.html) to fetch videos after every 10 minutes using [Youtube Data Api](https://developers.google.com/youtube/v3/docs/search/list) and save it to the db

## Setup Guide

- As this project is based on Django, your system need to have proper python setup, refer [this](https://www.python.org/downloads/)
- Go the project through the terminal and install all dependencies by using typing `pip install -r requirements.txt` in the terminal
- Inside the `setting.py` file, fill the variable `GOOGLE_API_KEYS` with all the API Keys available, the list should be filled as `['API_KEY_1','API_KEY_2',...]`
- For getting an API key follow [this](https://developers.google.com/youtube/v3/getting-started)
- Setup crontab to run Job, Follow [this](https://django-cron.readthedocs.io/en/latest/installation.html)
- Run the server using `python mange.py runserver`
- Copy the server from the output of above code and run it in browser.
- Click on filters button and type the keyword for search in the text box and click on search and see the results

