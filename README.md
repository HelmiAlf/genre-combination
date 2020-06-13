<html>
  <head>
  	<meta http-equiv="Content-Type" content="text/html;charset=utf-8"/>
    <title>Chord Diagram</title>
    <!-- Google Fonts -->
    <script src="https://d3js.org/d3.v5.min.js"></script>
    <link
      href="https://fonts.googleapis.com/css?family=Lato:400,900"
      rel="stylesheet"
      type="text/css"
    />

    <style>
      .tippy-content {
        font-family: "Verdana", sans-serif;
      }

      #chart-5d7dd0c6 {

        font-size: ;
        font-family: "Verdana", sans-serif;
        text-align: center;
        fill: #454545;
      }

      #chart-5d7dd0c6 svg {
        max-width: px;
      }

      @media (min-width: 600px) {
				#chart-5d7dd0c6{
					font-size: ;
				}
			}
    </style>
  </head>
  <body>
    <div id="chart-5d7dd0c6" class="chord">
    </div>
    <script src="https://unpkg.com/@popperjs/core@2"></script>
    <script src="https://unpkg.com/tippy.js@6"></script>
    <script>
      var script = document.createElement("script");
      script.type = "text/javascript";
      script.src = "https://d3js.org/d3.v5.min.js";

      script.onload = function () {

        var script2 = document.createElement("script");
        script2.type = "text/javascript";
        script2.src = "https://shahinrostami.com/assets/chord/script.js";
        script2.onload = function () {
          margin = {
          left: 0,
          top: 15,
          right: 0,
          bottom: 0
        };
        width = Math.min(window.innerWidth, ) - margin.left - margin.right;
        height = Math.min(window.innerHeight, ) - margin.top - margin.bottom;
        innerRadius = Math.min(width, height) * 0.39;
        outerRadius = innerRadius * 1.1;

      tag_id = "chart-5d7dd0c6";
      padding = 0.01;
      Names = ['Action', 'Adventure', 'Crime', 'Drama', 'Romance', 'Thriller', 'War', 'Biography', 'Comedy', 'Family', 'Fantasy', 'History', 'Western', 'Music', 'Musical', 'Sport', 'Mystery', 'Film-Noir'];
      colors = ['#bcc9ea', '#FF0000', '#C0C0C0', '#446cd4', '#800000', '#ffe90e', '#008000', '#ffb400', '#000080', '#ff6700', '#808080', '#5a1016', '#8A2BE2', '#430c10', '#D2691E', '#3f3359', '#708090'];
      opacityDefault = 0.8;
      matrix = [[0, 1, 1, 2, 1, 1, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], [1, 0, 0, 5, 3, 1, 2, 2, 2, 1, 2, 4, 1, 0, 0, 0, 0, 0], [1, 0, 0, 10, 1, 7, 0, 1, 2, 0, 0, 0, 0, 0, 2, 0, 1, 0], [2, 5, 10, 0, 28, 12, 14, 16, 8, 5, 2, 11, 3, 2, 7, 3, 2, 2], [1, 3, 1, 28, 0, 2, 8, 4, 8, 4, 1, 3, 0, 0, 7, 0, 1, 0], [1, 1, 7, 12, 2, 0, 1, 1, 1, 0, 1, 0, 0, 0, 0, 0, 2, 0], [1, 2, 0, 14, 8, 1, 0, 3, 0, 0, 0, 3, 0, 0, 0, 0, 0, 0], [0, 2, 1, 16, 4, 1, 3, 0, 1, 1, 0, 10, 0, 2, 2, 1, 0, 0], [0, 2, 2, 8, 8, 1, 0, 1, 0, 1, 0, 2, 0, 2, 2, 0, 0, 0], [0, 1, 0, 5, 4, 0, 0, 1, 1, 0, 0, 0, 0, 0, 3, 0, 0, 0], [0, 2, 0, 2, 1, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], [0, 4, 0, 11, 3, 0, 3, 10, 2, 0, 0, 0, 0, 1, 0, 0, 0, 0], [0, 1, 0, 3, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], [0, 0, 0, 2, 0, 0, 0, 2, 2, 0, 0, 1, 0, 0, 0, 0, 0, 0], [0, 0, 2, 7, 7, 0, 0, 2, 2, 3, 0, 0, 0, 0, 0, 0, 0, 0], [0, 0, 0, 3, 0, 0, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], [0, 0, 1, 2, 1, 2, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], [0, 0, 0, 2, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0]];
      wrap_labels = false;

      winner_matrix = [
      [ 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0],
      [ 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0],
      [ 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0],
      [ 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0],
      [ 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0],
      [ 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0],
      [ 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0],
      [ 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0],
      [ 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0],
      [ 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0],
      [ 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0],
      [ 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0],
      [ 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0],
      [ 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0],
      [ 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0],
      [ 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0],
      [ 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0],
      [ 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0]
      ]



      
      ////////////////////////////////////////////////////////////
      /////////// Create scale and layout functions //////////////
      ////////////////////////////////////////////////////////////

      var colors = d3
        .scaleOrdinal()
        .domain(d3.range(Names.length))
        .range(colors);

      //A "custom" d3 chord function that automatically sorts the order of the chords in such a manner to reduce overlap
      var chord = customChordLayout()
        .padding(padding)
        .sortChords(d3.descending) //which chord should be shown on top when chords cross. Now the biggest chord is at the bottom
        .matrix(matrix);

      var arc = d3
        .arc()
        .innerRadius(innerRadius * 1.01)
        .outerRadius(outerRadius);

      var path = d3.ribbon().radius(innerRadius);

      ////////////////////////////////////////////////////////////
      ////////////////////// Create SVG //////////////////////////
      ///////////////////////////////////////////////////////////

      var svg = d3
        .select("#" + tag_id)
        .append("svg")
        .attr(
          "viewBox",
          "0 0 " +
            (width + margin.left + margin.right) +
          " " +
          (height + margin.top + margin.bottom)
        )
        .attr("preserveAspectRatio", "xMinYMin meet")
        .append("g")
        .attr(
          "transform",
          "translate(" +
            (width / 2 + margin.left) +
            "," +
            (height / 2 + margin.top) +
            ")"
        );

      d3.select("#" + tag_id)
        .append("span")
        .style("display", "block")
        .style("font-size", "16px")
        .style("text-align", "right")
        .style("font-family", '"Arial", sans-serif')
        .html(
          'made with <a href="https://github.com/shahinrostami/chord">chord</a></span>'
        );

      ////////////////////////////////////////////////////////////
      /////////////// Create the gradient fills //////////////////
      ////////////////////////////////////////////////////////////

      //Function to create the id for each chord gradient
      function getGradID(d) {
        return (
          "linkGrad-" + tag_id + "-" + d.source.index + "-" + d.target.index
        );
      }




      //Create the gradients definitions for each chord
      var grads = svg
        .append("defs")
        .selectAll("linearGradient")
        .data(chord.chords())
        .enter()
        .append("linearGradient")
        .attr("id", getGradID)
        .attr("gradientUnits", "userSpaceOnUse")
        .attr("x1", function (d, i) {
          return (
            innerRadius *
            Math.cos(
              (d.source.endAngle - d.source.startAngle) / 2 +
                d.source.startAngle -
                Math.PI / 2
            )
          );
        })
        .attr("y1", function (d, i) {
          return (
            innerRadius *
            Math.sin(
              (d.source.endAngle - d.source.startAngle) / 2 +
                d.source.startAngle -
                Math.PI / 2
            )
          );
        })
        .attr("x2", function (d, i) {
          return (
            innerRadius *
            Math.cos(
              (d.target.endAngle - d.target.startAngle) / 2 +
                d.target.startAngle -
                Math.PI / 2
            )
          );
        })
        .attr("y2", function (d, i) {
          return (
            innerRadius *
            Math.sin(
              (d.target.endAngle - d.target.startAngle) / 2 +
                d.target.startAngle -
                Math.PI / 2
            )
          );
        });

      //Set the starting color (at 0%)
      grads
        .append("stop")
        .attr("offset", "0%")
        .attr("stop-color", function (d) {
          return colors(d.source.index);
        });

      //Set the ending color (at 100%)
      grads
        .append("stop")
        .attr("offset", "100%")
        .attr("stop-color", function (d) {
          return colors(d.target.index);
        });

      ////////////////////////////////////////////////////////////
      ////////////////// Draw outer Arcs /////////////////////////
      ////////////////////////////////////////////////////////////

      var outerArcs = svg
        .selectAll("g.group")
        .data(chord.groups)
        .enter()
        .append("g")
        .attr("class", "group")
        .on("mouseover", fade(0.1, 1))
        .on("mouseout", fade(opacityDefault, opacityDefault));

      outerArcs
        .append("path")
        .style("fill", function (d) {
          return colors(d.index);
        })
        .attr("d", arc)
        .each(function (d, i) {
          //Search pattern for everything between the start and the first capital L
          var firstArcSection = /(^.+?)L/;

          //Grab everything up to the first Line statement
          var newArc = firstArcSection.exec(d3.select(this).attr("d"))[1];
          //Replace all the comma's so that IE can handle it
          newArc = newArc.replace(/,/g, " ");

          //If the end angle lies beyond a quarter of a circle (90 degrees or pi/2)
          //flip the end and start position
          if (
            (d.endAngle > (90 * Math.PI) / 180) &
            (d.startAngle < (270 * Math.PI) / 180)
          ) {
            var startLoc = /M(.*?)A/, //Everything between the first capital M and first capital A
              middleLoc = /A(.*?)0 0 1/, //Everything between the first capital A and 0 0 1
              endLoc = /0 0 1 (.*?)$/; //Everything between the first 0 0 1 and the end of the string (denoted by $)
            //Flip the direction of the arc by switching the start en end point (and sweep flag)
            //of those elements that are below the horizontal line
            var newStart = endLoc.exec(newArc)[1];
            var newEnd = startLoc.exec(newArc)[1];
            var middleSec = middleLoc.exec(newArc)[1];

            //Build up the new arc notation, set the sweep-flag to 0
            newArc = "M" + newStart + "A" + middleSec + "0 0 0 " + newEnd;
          } //if

          //Create a new invisible arc that the text can flow along
          svg
            .append("path")
            .attr("class", "hiddenArcs")
            .attr("id", "arc-" + tag_id + "-" + i)
            .attr("d", newArc)
            .style("fill", "none");

          ////////////////////////////////////////////////////////////
          ////////////////// Append Names ////////////////////////////
          ////////////////////////////////////////////////////////////

          //Append the label names on the outside

          if (wrap_labels) {
            outerArcs
              .append("text")
              .attr("class", "titles")
              .attr("dy", function (d, i) {
                return (d.endAngle > (90 * Math.PI) / 180) &
                  (d.startAngle < (270 * Math.PI) / 180)
                  ? 25
                  : -16;
              })
              .append("textPath")
              .attr("startOffset", "50%")
              .style("text-anchor", "middle")
              .attr("xlink:href", function (d, i) {
                return "#arc-" + tag_id + "-" + i;
              })
              .text(function (d, i) {
                return Names[i];
              });
          } else {
            //Append the label names on the outside
            outerArcs
              .append("text")
              .each(function (d) {
                d.angle = (d.startAngle + d.endAngle) / 2;
              })
              .attr("dy", ".35em")
              .attr("class", "titles")
              .attr("text-anchor", function (d) {
                return d.angle > Math.PI ? "end" : null;
              })
              .attr("transform", function (d) {
                return (
                  "rotate(" +
                  ((d.angle * 180) / Math.PI - 90) +
                  ")" +
                  "translate(" +
                  (outerRadius + 10) +
                  ")" +
                  (d.angle > Math.PI ? "rotate(180)" : "")
                );
              })
              .text(function (d, i) {
                return Names[i];
              });
          }

          ////////////////////////////////////////////////////////////
          ////////////////// Draw inner chords ///////////////////////
          ////////////////////////////////////////////////////////////

          svg
            .selectAll("path.chord")
            .data(chord.chords)
            .enter()
            .append("path")
            .attr("class", "chord")
            .style("fill", function (d) {
              return "url(#" + getGradID(d) + ")";
            })
            .style("opacity", opacityDefault)
            .attr("d", path)
            .on("mouseover", mouseoverChord())
            .on("mouseout", mouseoutChord(opacityDefault, opacityDefault));
        });
      ////////////////////////////////////////////////////////////
      ////////////////// Extra Functions /////////////////////////
      ////////////////////////////////////////////////////////////

      //Returns an event handler for fading a given chord group.
      function fade(opacityIn, opacityOut) {
        return function (d, i) {
          d3.select(this.ownerSVGElement)
            .selectAll("path.chord")
            .filter(function (d) {
              return d.source.index !== i && d.target.index !== i;
            })
            .transition()
            .style("opacity", opacityIn);

          d3.select(this.ownerSVGElement)
            .selectAll("path.chord")
            .filter(function (d) {
              return d.source.index == i || d.target.index == i;
            })
            .transition()
            .style("opacity", opacityOut);

            
        };
      } //fade

      //Highlight hovered over chord
      function mouseoverChord() {
        return function (d, i) {

        d3.select(this.ownerSVGElement)
          .selectAll("path.chord")
          .transition()
          .style("opacity", 0.1);
        //Show hovered over chord with full opacity
        d3.select(this).transition().style("opacity", 1);

        console.log("src "+d.source.index+" target "+d.target.index)
        tippy_content = "<div style='width:200%'><span style='font-weight:900'>" +
            Names[d.source.index] +
            "</span> and <span style='font-weight:900'>" +
            Names[d.target.index] +
            "</span><br>occur together in <span style='font-weight:900'>" +
            d.source.value +
            "</span> instances<br>" +
            "<ul><li> Parasite (2019) </li><li> 12 Angry Men (2019) </li><li> Rocky (2019) </li>"

            ;

        

        

        
        tippy(this, {
          allowHTML: true,
          followCursor: true,
          content: tippy_content,
          size: "large",
          arrow: true,
        });

      /*d3.select("#list")
        .html(
          details[d.source.index][d.target.index]
        );*/
      

        };
        
      } //fade

      //Bring all chords back to default opacity
      function mouseoutChord(opacityIn, opacityOut) {
        return function (d, i) {
        d3.select(this.ownerSVGElement)
          .selectAll("path.chord")
          .transition()
          .style("opacity", opacityOut);
        };
        //Set opacity back to default for all
      } //function mouseoutChord


        };
        document.body.appendChild(script2);
      };

      document.body.appendChild(script);
    </script>
    <script></script>
  </body>
</html>
