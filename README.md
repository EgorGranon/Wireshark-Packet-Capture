# Wireshark-Packet-Capture
|     | Description |
|-----|-------------|
| 1-  | Install and set up Wireshark on Ubuntu |
| 2-  | Start a packet capture on an ethernet port and save it to a file |
| 3-  | Use a display filter to detect HTTPS packets |
| 4-  | Visit a web page and detect its IP address using a display filter |
| 5-  | Locate all HTTPS packets from a capture not containing a certain IP address |

## 1- Install and set up Wireshark on Ubuntu

1- To install wireshark on Ubuntu type the following into your Terminal:

![](https://imgur.com/cClHrDK.png)

2- We then need to add the user to the wireshark group: 

![](https://imgur.com/5ts0F3d.png)

3- Lastly, log out and then log back in to the linux system so the user becomes a part of the group.

## 2- Start a packet capture on an ethernet port and save it to a file

1- Select the interface you would like to capture packets from (In this scenario we will capture from ens5):

![](https://imgur.com/NC1p79X.png)

2- Click on the blue shark fin on the top left to begin to capture the packets.

![](https://imgur.com/SsgUOZ0.png)

3- Click on the red square by the shark fin to stop the packets capture. You can only save the packet capture to a file when it has been stopped.

![](https://imgur.com/gWqvIUP.png)

## 3- Use a display filter to detect HTTPS packets

1- Start a packet capture

![](https://imgur.com/zJqOmR0.png)

2- Load a website using a web browser

![](https://imgur.com/LRD9vWx.png)

3- Go back to wireshark and stop the packet capture before saving it to a file (in this case task3):

![](https://imgur.com/NqMFigG.png)

4- Use the display filter to display only HTTPS traffic

![](https://imgur.com/DAtG4P3.png)

5- We can see the destination ip address which corresponds to the website being visited:

![](https://imgur.com/mnGeQHH.png)

## 4- Visit a web page and detect its IP address using a display filter

1- Start a packet capture

2- Go to google.com

3- Stop the packet capture and display only the https traffic

![](https://imgur.com/0i6XeDB.png)

4- View the first step of the TLS handshake. This filter will display only the Client Hello's:

![](https://imgur.com/CRhEzSF.png)

5- To filter by IP address do the following:

![](https://imgur.com/gwTcDP6.png)

6- To filter by IP source:

![](https://imgur.com/JBPCBJY.png)

7- To filter by IP destination:

![](https://imgur.com/cwZOPux.png)

## 5- Locate all HTTPS packets from a capture not containing a certain IP address

1- Start a packet capture and then visit two seperate websites and then stop the capture. Add a filter to view all packets containing client hello tls handshake.

![](https://imgur.com/9Npfc59.png)

2- Add filter to view only packets of first ip destination address discovered

![](https://imgur.com/NeRydcP.png)

3- Add an extra filter to the previous one to also display all HTTPS traffic

![](https://imgur.com/aYij1Rl.png)

4- Get rid of a specific Ip address but give all traffic from HTTPS and HTTP ports

![](https://imgur.com/r1hIxgW.png)
