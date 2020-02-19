# ARSCADA-1.5
ARSCADA 1.5
This version fixes some bugs and enhances some of the modules as follows:
1. The communication module embedarscada modified to include a request/response based communication between client and server.
2. The tour.html files in the tours folder modified to load the tour.xml files after the initial handshake between client and server.
3. The rws.html and rws1.html files in rws folder modified to take into account the request/response architecture of the communication module. Basically two functions added, one for requesting data from server and the other in called when response is received. You have to call the request function from your timer loop to request data from server and call your update module to refresh your screen. The two functions are as follows:
  function request_scan(){
    request("SCAN");
    ttime+=ctime;
  }
  function response(){
    update_display();
    //console.log("length=",dbobj.TAGDB.length);
  }
4. The latest version 1.20.4 (build 2020-02-04) of krpano included.
5. To install this version, 
5.1 rename C:\ARS folder if you have installed the previous version,
5.2 down load this ARS.zip file and extract it to C:\ARS folder
5.3 rest of the procedure reamins same as the previous version.
