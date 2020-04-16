Buttons, spinners, bootstrap
============================

.. image:: /images/buttons.jpg
  :align: center

I wanted a way to iniatiate an upload and also show its progress. The image above shows the result as three buttons but, in real life, this would
all be done with just one button.

.. code-block::

  <!-- html part, uses bootstrap -->
  <div class="mx-auto button-block">
    <button class="btn btn-secondary" id="btnUpload1">Upload</button>
    <button class="btn btn-secondary" id="btnUpload2">Upload</button>
    <button class="btn btn-secondary" id="btnUpload3">Upload</button>
  </div>

  <!-- javascript part, also uses bootstrap -->
  <script>
    $(function(){
    	$("#btnUpload2")
    	  .html(
          '<span class="spinner-border spinner-border-sm" role="status"></span>\n' +
          '<span class="sr-only"></span>\n' +
          'Uploading...')
        .toggleClass('btn-secondary btn-primary');

      $("#btnUpload3")
        .html('Thank you, upload complete')
        .toggleClass('btn-success');
    })
  </script>

