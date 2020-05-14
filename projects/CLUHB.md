---
layout: project
type: project
image: images/cl-uh-b-logo.png
title: CLUHB
permalink: projects/CLUHB
# All dates must be YYYY-MM-DD format!
date: 2020-05-14
labels:
  - UH Manoa Clubs
  - React
  - Meteor
  - MongoDB
summary: My team developed a website to allow students at UH Manoa to easily browse clubs offered.
---

<img class="ui image" src="{{ site.baseurl }}/images/browse.png">

CL-UH-B is a web application developer by 4 developers, [Julian Kim](https://github.com/julianki-cs), [Anh Le](https://github.com/lekanh), [Tiffany Williams](https://github.com/tiffanywilliams), and myself. Over the course a month we were given the project of developing this web application for students at UH Manoa to browse clubs at our campus. Our goal was to make it a simple UI as the main feature is browsing the clubs but also to be aesthetically pleasing to the eyes. This was so students can find a club and not have an eye sore while using our app. Above this paragraph is the page where the main feature happens of browsing and where I believe I contributed most of my time developing.

This application is built in JavaScript using React, Meteor, and MongoDB. Where these 3 features come in for this specific browsing page is for one, checking to make sure the user is logged in using Meteor, finding all the clubs and interest using MongoDB, and finally putting all that together in the frontend using React so that the students can easily interact with the website. The issues on this page were to first load all the clubs from the database to display it in a nice view. Then from there, to implement a search and interest filter feature to narrow down the results, and then finally to paginate it so that the student would not have to scroll through nearly 300 clubs. If you want to check out how the code is done, you may go to our [ListClubs.jsx](https://github.com/cl-uh-b/cl-uh-b/blob/master/app/imports/ui/pages/ListClubs.jsx) to see all of it. The issue I do want to talk about is how I implemented the search and filter feature together. Originially, I believed the issue would be simple (how optimistic I was) but then ran into many issues, one specifically being where searching would ignore whatever interest is selected. To fix this, I had to pass the club data through both of them and ended up causing my interest filter to be a lot longer than anticipated. Here is the simplest version I could come up with:
```js
    /** Filter to selected interest */
    if (this.state.value === '' || this.state.value.length === 0) {
      clubsOnPage = this.props.clubs;
    } else {
      let filteredResults = [];
      for (let i = 0; i < this.state.value.length; i++) {
        const temp = this.props.clubs.filter((club) => 
            club.interest.includes(this.state.value[i]));
        filteredResults = _.union(filteredResults, temp);
      }
      clubsOnPage = filteredResults;
    }

    /** Filter to search results */
    clubsOnPage = clubsOnPage.filter(
      (club) =>
        club.clubName.toLowerCase().indexOf(this.state.search.toLowerCase()) !== -1,
    );
```
To expain this a bit more, in the interest filter, I check to see if the select interest dropdown is empty, and if it is, it just displays all the clubs. If this was not the case, I created an empty array to store the clubs with the selected interest, went through all the clubs and filtered it down to the clubs that had the same interest. From there, it reassigns the clubs to display to those filters. That was the trickiest part as clearing the interest always seemed to remove all clubs from the page in general. The easy part came with the searching as it was able to work on what was displayed with all the clubs or with a filtered list. It went through the clubs and filtered it down to the clubs that included the key word that the student types in. This allows students to find the clubs contact information if they know what they were looking for. For anyone that has faced a problem for hours on end, I am sure you can relate to the satisfaction of finally coming to a working product.

Source: <a href="https://github.com/cl-uh-b/cl-uh-b"><i class="large github icon"></i>"cl-uh-b/cl-uh-b"</a>
