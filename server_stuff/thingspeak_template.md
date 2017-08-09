
## You can use an exmple from ESP8266 Core with two changes.
1. edit ssid and password for your WiFi AP.
2. use your url with no "secure" feature

## You can find an example from Arduino Sketcher.

File>Examples>ESP8266HTTPClient>BasicHttpClient

``` C++
WiFiMulti.addAP("SSID", "PASSWORD");
...

http.begin("url for calling thing speak with your own API key and field value(s)");
```
It would look like as follows:
``` C++
int v = 55;
http.begin("http://api.thingspeak.com/update?api_key=8XMMGUN78YZ6BG6W&field1="+ String(v));

```
