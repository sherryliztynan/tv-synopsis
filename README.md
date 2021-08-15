# TV Synopsis

## Instructions
In the initial commit to this project, you have been provided with a data set for a TV show. Your task is to create an Express/Pug powered website that will display the information in a manner similar to the screenshots below.

### Show Info
![image](./mainpage.png)

### Single Season Info
![image](./seasonpage.png)



                        a(href=`/showtimes/${showdata.seasons.number}`)= showdata.seasons.number
                        div= showdata.seasons.number

      div(class = 'season-table-header')
                div(class = 'episode-table-header episode-number-header') No.
                div(class = 'episode-table-header episode-title-header') Title
                div(class = 'episode-table-header episode-director-header') Director
            for episode in seasons.episodes  
                div(class = 'episode')
                    div(class = 'episode-top')
                        div= episode.number 
                        div= episode.title
                        div= episode.director 
                    div(class = 'episode-bottom')
                        div= episode.synopsis