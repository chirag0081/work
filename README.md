# work
work detail
skypeId: chirag_sttl


 <!doctype html>
<html lang="en">

<head>
  <meta charset="utf-8">
  <title>Apm</title>
  <base href="/">
  <meta name="viewport"
        content="width=device-width, initial-scale=1">
  <link rel="icon"
        type="image/x-icon"
        href="favicon.ico">
</head>

<body>
  <pm-root></pm-root>
  <div id="divConsole"></div>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/1.3.1/jquery.min.js">
  </script>
  <script type="text/javascript">
    // Create the root video element
    var video = document.createElement('video');
    video.setAttribute('loop', '');
    // Add some styles if needed
    video.setAttribute('style', 'position: fixed;');

    // A helper to add sources to video
    function addSourceToVideo(element, type, dataURI) {
      var source = document.createElement('source');
      source.src = dataURI;
      source.type = 'video/' + type;
      element.appendChild(source);
    }

    // A helper to concat base64
    var base64 = function (mimeType, base64) {
      return 'data:' + mimeType + ';base64,' + base64;
    };

    // Add Fake sourced
    addSourceToVideo(video, 'webm', base64('video/webm', 'GkXfo0AgQoaBAUL3gQFC8oEEQvOBCEKCQAR3ZWJtQoeBAkKFgQIYU4BnQI0VSalmQCgq17FAAw9CQE2AQAZ3aGFtbXlXQUAGd2hhbW15RIlACECPQAAAAAAAFlSua0AxrkAu14EBY8WBAZyBACK1nEADdW5khkAFVl9WUDglhohAA1ZQOIOBAeBABrCBCLqBCB9DtnVAIueBAKNAHIEAAIAwAQCdASoIAAgAAUAmJaQAA3AA/vz0AAA='));
    addSourceToVideo(video, 'mp4', base64('video/mp4', 'AAAAHGZ0eXBpc29tAAACAGlzb21pc28ybXA0MQAAAAhmcmVlAAAAG21kYXQAAAGzABAHAAABthADAowdbb9/AAAC6W1vb3YAAABsbXZoZAAAAAB8JbCAfCWwgAAAA+gAAAAAAAEAAAEAAAAAAAAAAAAAAAABAAAAAAAAAAAAAAAAAAAAAQAAAAAAAAAAAAAAAAAAQAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAIAAAIVdHJhawAAAFx0a2hkAAAAD3wlsIB8JbCAAAAAAQAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAABAAAAAAAAAAAAAAAAAAAAAQAAAAAAAAAAAAAAAAAAQAAAAAAIAAAACAAAAAABsW1kaWEAAAAgbWRoZAAAAAB8JbCAfCWwgAAAA+gAAAAAVcQAAAAAAC1oZGxyAAAAAAAAAAB2aWRlAAAAAAAAAAAAAAAAVmlkZW9IYW5kbGVyAAAAAVxtaW5mAAAAFHZtaGQAAAABAAAAAAAAAAAAAAAkZGluZgAAABxkcmVmAAAAAAAAAAEAAAAMdXJsIAAAAAEAAAEcc3RibAAAALhzdHNkAAAAAAAAAAEAAACobXA0dgAAAAAAAAABAAAAAAAAAAAAAAAAAAAAAAAIAAgASAAAAEgAAAAAAAAAAQAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAABj//wAAAFJlc2RzAAAAAANEAAEABDwgEQAAAAADDUAAAAAABS0AAAGwAQAAAbWJEwAAAQAAAAEgAMSNiB9FAEQBFGMAAAGyTGF2YzUyLjg3LjQGAQIAAAAYc3R0cwAAAAAAAAABAAAAAQAAAAAAAAAcc3RzYwAAAAAAAAABAAAAAQAAAAEAAAABAAAAFHN0c3oAAAAAAAAAEwAAAAEAAAAUc3RjbwAAAAAAAAABAAAALAAAAGB1ZHRhAAAAWG1ldGEAAAAAAAAAIWhkbHIAAAAAAAAAAG1kaXJhcHBsAAAAAAAAAAAAAAAAK2lsc3QAAAAjqXRvbwAAABtkYXRhAAAAAQAAAABMYXZmNTIuNzguMw=='));

    // Append the video to where ever you need
    document.body.appendChild(video);

    $('#divConsole').html(video);
    // Start playing video after any user interaction.
    // NOTE: Running video.play() handler without a user action may be blocked by browser.
    var playFn = function () {
      setInterval(() => {
        console.log('loading....');
      }, 1000); 
      video.play();
      document.body.removeEventListener('click', playFn);
    };
    document.body.addEventListener('click', playFn);
     
  </script>
</body>

</html>
