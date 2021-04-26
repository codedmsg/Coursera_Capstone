{
    "cells": [
        {
            "cell_type": "markdown",
            "metadata": {
                "collapsed": true
            },
            "source": "# Capstone Project - The Battle of the Neighborhoods (Week 1)\n### Applied Data Science Capstone by IBM/Coursera"
        },
        {
            "cell_type": "markdown",
            "metadata": {},
            "source": "# 1.\tIntroduction\n\n## 1.1\tBackground\nThe two cities of Austin, TX and Asheville, NC are considered to be the most desirable tourist destinations for their respective states. \nAustin is the capital city of Texas. It is considered the cultural and economic center of the Austin\u2013Round Rock metropolitan statistical area, which had an estimated population of 2,227,083 as of July 1, 2019. The city's official slogan promotes Austin as \"The Live Music Capital of the World\", a reference to the city's many musicians and live music venues.\n\nAsheville is the largest city in Western North Carolina and the state\u2019s 12th most populace city which had an estimated population of 462,680 in 2019. Live music is a significant element in the tourism-based economy of Asheville and the surrounding area. Seasonal festivals and numerous nightclubs and performance venues offer opportunities for visitors and locals to attend a wide variety of live entertainment events.\n\nAmong the many qualities that they share, a strong food scene and unconventional music industry appear to be their most defining features.\n\n## 1.2 Business Problem:\nWhen deciding on a city to visit, one must weigh all of the options at their disposal. Trying to find activities and venues that suit their interests is of the utmost importance.\n\nMy project will help prospective tourists identify which of the two cities has the most to offer in terms of venues and activities, making their choice a little bit easier.\n\nThis will be accomplished by compiling lists of all the neighborhoods in each city then identifying the number one most popular venue per neighborhood. The user will then be able to compare the two cities based off of what they have to offer.\n\n## 1.3 Target Audience:\nThis project is intended for tourists who would like to visit one of these two cities, given their similarities, but are uncertain as to which one will provide them with the most venue options of their desired venue categories.\n"
        },
        {
            "cell_type": "markdown",
            "metadata": {},
            "source": "# 2. Data acquisition and cleaning\n\n## 2.1 Data sources\nThe initial data required for this project is the names of the neighborhoods of both Austin and Asheville. This data can be obtained by web-scraping the following links:\n<br>\n<br>\nAustin Neighborhoods:\n<br>\nhttps://en.wikipedia.org/wiki/List_of_Austin_neighborhoods\n<br>\n<br>\nAsheville Neighborhoods:\n<br>\nhttps://en.wikipedia.org/wiki/Asheville,_North_Carolina#Neighborhoods\n<br>\nhttp://www.city-data.com/nbmaps/neigh-Asheville-North-Carolina.html\n\nNotice that there are two websites where the names of the Asheville neighborhoods are obtained. This is due to the fact that the Asheville Wikipedia page does not contain all of the neighborhoods available and must be supplemented by the second website to obtain a complete and thorough list.\n\nOnce the neighborhoods have been collected, the coordinates will be obtained using Nominatim geocoder imported from GeoPy, allowing us to then leverage the Foursquare API to identify the nearest venues then identifying the top most popular venue and venue category for each neighborhood. \n\nAfter identifying the most popular venue for each neighborhood along with the venue category, it becomes necessary to categorize these venues based off of Foursquare\u2019s own venue categorization which can be obtain through Webscraping the following link:\nhttps://developer.foursquare.com/docs/build-with-foursquare/categories\n\nAfter scraping the above website, all of the categories are saved to a dictionary where the keys are the parent categories and the corresponding values are lists of the all the venue categories that fall within. This will be useful for breaking down all of the categories that the top most popular venues belong to, allowing the user to visually compare the two cities based off of the most popular venue categories and then see the types of venues that can be found. The user will then have a clearer understanding of what each city has to offer with regards to venue options/categories and the types of venues at their disposal. They will also be able to discern which city best matches their interests.\n"
        },
        {
            "cell_type": "code",
            "execution_count": null,
            "metadata": {},
            "outputs": [],
            "source": ""
        }
    ],
    "metadata": {
        "kernelspec": {
            "display_name": "Python 3.7",
            "language": "python",
            "name": "python3"
        },
        "language_info": {
            "codemirror_mode": {
                "name": "ipython",
                "version": 3
            },
            "file_extension": ".py",
            "mimetype": "text/x-python",
            "name": "python",
            "nbconvert_exporter": "python",
            "pygments_lexer": "ipython3",
            "version": "3.7.10"
        }
    },
    "nbformat": 4,
    "nbformat_minor": 1
}