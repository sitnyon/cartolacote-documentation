API
===

Exemples
--------

.. raw:: html

	<p>Voir la <a href="https://map.cartolacote.ch/apihelp/index.html" target=_blank>documentation</a></li>

.. raw:: html

   <script type="text/javascript">

   function init() {
    $.getJSON( "https://map.cartolacote.ch/layer_interface?interface=api", function( data ) {
      var layersApi = data.layers;
	  var counter = 1;
	  var newInner = "<br><table border=\"0\">";
      for (var i=0; i < layersApi.length; i++) {
	      if (layersApi[i].treegroup == 'background') {
		     var link = "https://map.cartolacote.ch/theme/plan_ville?lang=fr&baselayer_ref=" + layersApi[i].layer;
		  } else {
		     var link = "https://map.cartolacote.ch/theme/plan_ville?lang=fr&baselayer_ref=plan_ville&tree_groups=" + layersApi[i].treegroup + "&tree_group_layers_" + layersApi[i].treegroup + "=" + layersApi[i].layer;
		  }
          newInner += '<tr><td>' + counter + '</td><td>' + layersApi[i].layer + '&nbsp(<a href="' + link + '" target="_blank">' + layersApi[i].translate_name + '</a>)</td></tr>';
          counter++;
      }
	  document.getElementById('apiLayers').innerHTML = newInner;
    });
   }

   </script>
   
   <body onload="init();">
   </body>

Liste des couches disponibles 
-----------------------------

.. raw:: html   

   <body>
     <div id="apiLayers" style="margin-left:10px;margin-bottom:24px;"></div> 
   </body>
   
   
