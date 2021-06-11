# Jekyll-Conference-Template

An academic conference website template built using Jekyll.

## Features

- A data file (`_data/conference.yml`) to configure all conference information.
    - `full_title`: conference fullname e.g., First xxx conference on xxxx, 2017.
    - `short_title`: conference shortname e.g., xxxx2017
    - `descriptioin`: short description about the conference (< 160 char)
    - `location`: conference location
    - `logo_path`: conference logo
    - `slideshow`: images slideshow
    - `navbar`: navigation menu.
    - `news`: news section.
    - `sponsors`: sponsor section.
    - `deadlines`: important dates of deadlines, pass-due date will be automatically printed with del line.
    - `social_media`: social media on the navbar. (current support facebook and twitter.)
    - `organizing_committees`: organzizing committees
    - `steering_committees`: steering committees - Renamed to Local Host
    - `program_committees`: program committees
    - more configuratioins to come.
- Google Analytics: in `_config.yml`
- Font-awesome
- Bootstrap v4.

Reference
Based on @yishanhe's [jekyll-conference-template](https://github.com/yishanhe/jekyll-conference-template).

## Usage

### Conference details

The text about the conference for the main page is directly in index.html file. 
The bulk of the details about the conference are held in the _data/conference.yml file. E.g. the title, dates, organisers names, image locations for slideshow, and sponsors.
NB - the images for the carousel should be approx 16:9 ratio, 


### Schedule

The schedule is stored in the file _data/schedule.yml
To update the schedule, committ the updated schedule.yml file to the repository, the website will automatically update within a few minutes.
The layout of the schedule.ylm file is by date, and time slots, added chronologically in the file e.g.

 - date: "2021-11-10"
   dateReadable: "2021-Nov-10"
   timeslots:
   - startTime: "8:50"
     endTime: "9:00"
	 title: "Opening remarks"
  - startTime: "9:00"
    endTime: "10:00"
    title: "Keynote: Personalized Medicine"
    speaker: "Leslie Biesecker (NIH/NHGRI)"
    abstract: "Personalized medicine is the way forward, discuss..."
    chair: "Lynn Schriml"
etc...

you can add a type to any time slot to change the way its presented, e.g. type: "presentation" allows you to nest time slots into a session, or type:"service" changes the colour to display e.g. for lunched and coffee breaks.



