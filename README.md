# esp32_cam

This code is based on using the AI Thinker ESP32-CAM.

## Setup
Using Arduino IDE 2:
- Add ESP boards package: [Guide](https://randomnerdtutorials.com/installing-the-esp32-board-in-arduino-ide-windows-instructions/)
- Select 'AI Thinker ESP32-CAM'  

### Properties
Create file called 'props.h' (right click on the ellipses on the far right, and select 'New Tab')

populate as such:
```
const char* ssid = "YOUR_SSID";
const char* password = "YOUR_PASSWORD";
IPAddress local_IP(192, 168, 1, 147); // The required IP of the camera
IPAddress gateway(192, 168, 1, 254); // The IP of your gateway/router (normally 192.168.1.1 or 192.168.1.254)
IPAddress subnet(255, 255, 255, 0);
```

## Debug
To debug, plug into computer, using Arduino IDE 2, open serial montior and select baud rate of 115200, reset the board and you should see errors pop up (if there are any!). You might get an error similar to `E (495) esp_core_dump_flash: No core dump partition found!`, this can safely be ignored, provided it then connects succesfully.