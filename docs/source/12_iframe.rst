Iframe
======

Intégrer une carte
------------------

Voir la :ref:`documentation<integrer_la_carte>`

.. raw:: html

   <script type="text/javascript">

   function init() {
    $.getJSON( "https://map.cartolacote.ch/layer_interface?interface=iframe", function( data ) {
      var layersIframe = data.layers;
	  var counter = 1;
	  var newInner = "<br><table border=\"0\">";
      for (var i=0; i < layersIframe.length; i++) {
	      if (layersIframe[i].treegroup == 'background') {
		     var link = "https://map.cartolacote.ch/theme/plan_ville?lang=fr&baselayer_ref=" + layersIframe[i].layer;
		  } else {
		     var link = "https://map.cartolacote.ch/theme/plan_ville?lang=fr&baselayer_ref=plan_ville&tree_groups=" + layersIframe[i].treegroup + "&tree_group_layers_" + layersIframe[i].treegroup + "=" + layersIframe[i].layer;
		  }
          newInner += '<tr><td>' + counter + '</td><td>' + layersIframe[i].layer + '&nbsp(<a href="' + link + '" target="_blank">' + layersIframe[i].translate_name + '</a>)</td></tr>';
          counter++;
      }
	  document.getElementById('iframeLayers').innerHTML = newInner;
    });
   }

   </script>
   
   <body onload="init();">
   </body>

Liste des couches disponibles 
-----------------------------

.. raw:: html   

   <body>
     <div id="iframeLayers" style="margin-left:10px;margin-bottom:24px;"></div> 
   </body>
   
   
