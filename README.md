##RESTfulMoviesInNode.js
RESTful movie rating service implemented in node.js, with MongoDB and Mongoose.  
Service returns Collection+JSON and was an project used to investigate implementing a Hypermedia API.

#####Sample Response
        {
          "collection": {
            "version": "1.0",
            "href": "http://iswq2014.bryanbarnard.com:1337/api/movies?offset=0&limit=5",
            "links": [
              {
                "href": "https://rawgithub.com/bryanbarnard/ISWQ2014/master/docs/movies.xml",
                "rel": "profile"
              },
              {
                "href": "https://rawgithub.com/bryanbarnard/ISWQ2014/master/docs/movies.xml#movie",
                "rel": "type"
              },
              {
                "href": "http://iswq2014.bryanbarnard.com:1337/api/movies",
                "rel": "first",
                "prompt": "first page of results"
              },
              {
                "href": "http://iswq2014.bryanbarnard.com:1337/api/movies",
                "rel": "previous",
                "prompt": "immediate previous page results"
              },
              {
                "href": "http://iswq2014.bryanbarnard.com:1337/api/movies?offset=-4&limit=5",
                "rel": "last",
                "prompt": "last page of results"
              }
            ],
            "items": [
              {
                "href": "http://iswq2014.bryanbarnard.com:1337/api/movies/157a9b89b8c049ad9ef70663de0ef68e",
                "rel": "item",
                "rt": "movie",
                "data": [
                  {
                    "name": "name",
                    "value": "So I Married An Axe Murderer 001",
                    "prompt": "title of the movie"
                  },
                  {
                    "name": "description",
                    "value": "A San Francisco poet who fears commitment has a girlfriend who he suspects may not be who she appears.",
                    "prompt": "description of movie"
                  },
                  {
                    "name": "datePublished",
                    "value": "1993-03-28T21:51:08.406Z",
                    "prompt": "date movie was published"
                  },
                  {
                    "name": "about",
                    "value": "Cult Classic Michael Myers",
                    "prompt": "short description of this item"
                  },
                  {
                    "name": "genre",
                    "value": "comedy",
                    "prompt": "movie genre"
                  },
                  {
                    "name": "version",
                    "value": "1.0",
                    "prompt": "version of this release"
                  },
                  {
                    "name": "timeRequired",
                    "value": "PT120M",
                    "prompt": "time required to view this movie, aka duration"
                  },
                  {
                    "name": "contentRating",
                    "value": "r",
                    "prompt": "rating of the movie"
                  },
                  {
                    "name": "created",
                    "value": "2014-03-17T05:02:30.338Z",
                    "prompt": "record created"
                  },
                  {
                    "name": "updated",
                    "value": "2014-03-17T05:02:30.338Z",
                    "prompt": "record last updated"
                  }
                ],
                "links": [
                  {
                    "rel": "type",
                    "href": "https://rawgithub.com/bryanbarnard/ISWQ2014/master/docs/movies.xml#movie"
                  }
                ]
              }
            ],
            "queries": [
              {
                "href": "http://iswq2014.bryanbarnard.com:1337/api//movies",
                "rel": "search",
                "rt": "movie",
                "prompt": "Movie-Search By Name",
                "name": "movie-search",
                "data": {
                  "name": "name",
                  "value": "",
                  "prompt": "Name"
                }
              }
            ],
            "template": {
              "data": [
                {
                  "name": "name",
                  "value": "",
                  "prompt": "title of movie",
                  "required": "true"
                },
                {
                  "name": "description",
                  "value": "",
                  "prompt": "description of movie",
                  "required": "true"
                },
                {
                  "name": "datePublished",
                  "value": "",
                  "prompt": "date movie was published",
                  "required": "true"
                },
                {
                  "name": "about",
                  "value": "",
                  "prompt": "short description of film",
                  "required": "true"
                },
                {
                  "name": "genre",
                  "value": "",
                  "prompt": "movie genre",
                  "required": "true"
                },
                {
                  "name": "version",
                  "value": "",
                  "prompt": "version of this release",
                  "required": "true"
                },
                {
                  "name": "timeRequired",
                  "value": "",
                  "prompt": "time required to view this movie aka duration",
                  "required": "true"
                },
                {
                  "name": "contentRating",
                  "value": "",
                  "prompt": "movie content rating",
                  "required": "true"
                }
              ]
            }
          }
        }
