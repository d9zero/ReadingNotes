# Day Fourteen Notes

# Topic: CSS Transforms, Transitions, and Animations


## Table of Contents

- [Day 1](class-01.md)
- [Day 2](class-02.md)
- [Day 3](class-03.md)
- [Day 4](class-04.md)
- [Day 5](class-05.md)
- [Day 6](class-06.md)
- [Day 7](class-07.md)
- [Day 8](class-08.md)
- [Day 9](class-09.md)
- [Day 10](class-10.md)
- [Day 11](class-11.md)
- [Day 12](class-12.md)
- [Day 13](class-13.md)
- [Day 14](class-14.md), [Day 14 (Extended)](class-14b.md)
- [Day 15](class-15.md)
- [Day 16](class-16.md)
- [Day 17](class-17.md)
- [Day 18](class-18.md)
- [Day 19](class-19.md)
- [Day 20](class-20.md)






# Day Fourteen Reading:

Readings
Below you will find some reading material, code samples, and some additional resources that support today’s topic and the upcoming lecture.

Review the Submission Instructions for guidance on completing and submitting this assignment.

Reading
The following reading is required for psychological safety talk:

[What Google Learned From Its Quest to Build the Perfect Team](https://www.google.com/amp/mobile.nytimes.com/2016/02/28/magazine/what-google-learned-from-its-quest-to-build-the-perfect-team.amp.html)

Read the following articles and/or review the following examples on CSS animations:

[Read this article on CSS Transforms](http://learn.shayhowe.com/advanced-html-css/css-transforms/)

[Read this article on CSS Transitions & Animations](http://learn.shayhowe.com/advanced-html-css/transitions-animations/)

[8 simple CSS3 transitions that will wow your users](http://www.webdesignerdepot.com/2014/05/8-simple-css3-transitions-that-will-wow-your-users)

[6 Buttons animated](http://codepen.io/retyui/pen/ByoaXV)

[CSS3 Animations: Keyframes](http://codepen.io/akshaychauhan/pen/oAfae)

[404](http://codepen.io/kieranfivestars/pen/MYdQxX)

[Pure CSS Bounce Animation](http://codepen.io/dp_lewis/pen/gCfBv)



![teams](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Ftse2.mm.bing.net%2Fth%3Fid%3DOIP.qhr0XlDToyinEBD8-igU_AHaE8%26pid%3DApi&f=1)


# What Google Learned From Its Quest to Build the Perfect Team

          "No matter how researchers arranged the data, though, it was almost impossible to find patterns — or any evidence that the composition of a team made any difference. ‘‘We looked at 180 teams from all over the company,’’ Dubey said. ‘‘We had lots of data, but there was nothing showing that a mix of specific personality types or skills or backgrounds made any difference. The ‘who’ part of the equation didn’t seem to matter.’’

          Some groups that were ranked among Google’s most effective teams, for instance, were composed of friends who socialized outside work. Others were made up of people who were basically strangers away from the conference room. Some groups sought strong managers. Others preferred a less hierarchical structure. Most confounding of all, two teams might have nearly identical makeups, with overlapping memberships, but radically different levels of effectiveness. ‘‘At Google, we’re good at finding patterns,’’ Dubey said. ‘‘There weren’t strong patterns here.’’"

First, on the good teams, members spoke in roughly the same proportion, a phenomenon the researchers referred to as ‘‘equality in distribution of conversational turn-taking.’’

Second, the good teams all had high ‘‘average social sensitivity’’ — a fancy way of saying they were skilled at intuiting how others felt based on their tone of voice, their expressions and other nonverbal cues.



![advCss](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fi.ytimg.com%2Fvi%2FnwmlSPaz4d4%2Fmaxresdefault.jpg&f=1&nofb=1)


# Transforms

The transform property comes in two different settings, two-dimensional and three-dimensional. Each of these come with their own individual properties and values.

      div {
        -webkit-transform: scale(1.5);
          -moz-transform: scale(1.5);
            -o-transform: scale(1.5);
                transform: scale(1.5);
      }


      HTML
      1
      2
      3
      <figure class="box-1">Box 1</figure>
      <figure class="box-2">Box 2</figure>

                    
      CSS
      1
      2
      3
      4
      5
      6
      7
      .box-1 {
        transform: rotate(20deg);
      }
      .box-2 {
        transform: rotate(-55deg);
      }

2D Scale
Using the scale value within the transform property allows you to change the appeared size of an element. The default scale value is 1, therefore any value between .99 and .01 makes an element appear smaller while any value greater than or equal to 1.01 makes an element appear larger.

            HTML
            1
            2
            3
            <figure class="box-1">Box 1</figure>
            <figure class="box-2">Box 2</figure>

                          
            CSS
            1
            2
            3
            4
            5
            6
            7
            .box-1 {
              transform: scale(.75);
            }
            .box-2 {
              transform: scale(1.25);
            }

      HTML
      1
      2
      3
      4
      <figure class="box-1">Box 1</figure>
      <figure class="box-2">Box 2</figure>
      <figure class="box-3">Box 3</figure>

                    
      CSS
      1
      2
      3
      4
      5
      6
      7
      8
      9
      10
      .box-1 {
        transform: scaleX(.5);
      }
      .box-2 {
        transform: scaleY(1.15);
      }
      .box-3 {
        transform: scale(.5, 1.15);
      }
