########################################################################
Node Definiiton 

var graphNodes = {
     [node_name]: {
      data: "[php library name] - [funcion name]\n" +
      	"[line number]  [code]\n" +
      	...
      	"[line number]  [code]",
      description: "[description]",
      style: "[node css style like fill: #FFFFF]"
      },

      .
      .
      .

     [node_name]: {
      data: "[php library name] - [funcion name]\n" +
      	"[line number]  [code]\n" +
      	...
      	"[line number]  [code]",
      description: "[description]",
      style: "[node css style like fill: #FFFFF]"
      }
  }

########################################################################
* node_name:		esme e node ke tooye tooltip miyad (abi rang hastesh)
* data:			matne e node ke tooye graph neshon dade mishe
** description:		tooltip e node vaghti mouse mire roosh
** style:		style e node vase graph i kardan graph, masalan range dakhele node chi bashe
----------------------
* nesseccary field (can't be empty)
** optional field (can be empty)
########################################################################









########################################################################
Block Definition:
	age bekhay code e ye class ro grpah koni behtare estefade koni, chon vozohe graph bishtar mishe, nakoni darham o barham mishe
vali age class nabashe niyazi nist azash estefade koni
Solution:
age bekhay block define koni avval bayad ye node vasash define koni(block dar vaghe ye node e). too var graphNodes e bala inkaro bekon.
badesh vas inke begi che node i to che block i hast ino bayad khoroji bedi
g.setParent('[block memeber]', '[block name]);

########################################################################
bana bar in vaghti ye tarif mikoni 4ta field behesh midi
*-node name: ke mishe block name
**-data: empty
**-description: empty
***-style: this is block style for example color and ...
----------------------
*: nesseccary field (can't be empty)
**: should be EMPTY
***: optional










########################################################################
Edge definition:
har edge i ye node e start date ye node end date. intori ham neveshte mishe:
g.setEdge("[start node name]",     "[end node name]",     { label: "", style: ""});

########################################################################
* start node name: jaei ke edge shoro mishe
* end node name: jaei ke edge tamom mishe
** label: should be empty (khodet gofti edge ha label nemikhan)
*style: 3 halat vase style darim
	|- age edge natije ye jump e mamoli hast (masalan function call) eyne in style insert beshe (edge e abi)
	|	style: "stroke: #0074D9; stroke-width: 2px;", arrowheadStyle: "fill: #0074D9"
	|
	|- age edge vase bakhshe true e yek conditional jump hast eyne in style insert beshe (edge e sabz)
	|	style: "stroke: #2ECC40; stroke-width: 2px;", arrowheadStyle: "fill: #2ECC40"
	|
	|-age edge vase bakhshe false e yek conditional jump hast eyne in style insert beshe (edge e ghermez)
	|	style: "stroke: #FF4136; stroke-width: 2px;", arrowheadStyle: "fill: #FF4136"
----------------------
*: nesseccary field (can't be empty)
**: should be EMPTY














note: age to text " dari hatman ghablesh \ bezan ke dorost neshon dade beshe yani: (")  ->  (\")
in vase kolle code ke feed mikoni bayad havaset bashe

mishe to bakhsh haye data, label kode html zad. masalan vase edge sample e html to lalbel intori mishe
//g.setEdge("N0",     "N1",     { labelType:"html", label:"A <span style='font-size:32px'>Big</span> <span style='color:red;'>HTML</span> Source!"});
