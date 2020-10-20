# Wifi-Jammer



wifijammer
==========

Continuously jam all wifi clients and access points within range. The effectiveness of this script is constrained by your wireless card. Alfa cards seem to effectively jam within about a block radius with heavy access point saturation. Granularity is given in the options for more effective targeting. 


Requires:.

1.python 3

2.python-scapy 

3. A wireless card capable of injection


### Advanced
```shell
python wifijammer.py -c 1 -p 5 -t .00001 -s DL:3D:8D:JJ:39:52 -d --world
```

* `-c`, Set the monitor mode interface to only listen and deauth clients or APs on channel 1

* `-p`, Send 5 packets to the client from the AP and 5 packets to the AP from the client along with 5 packets to the broadcast address of the AP

* `-t`, Set a time interval of .00001 seconds between sending each deauth (try this if you get a scapy error like 'no buffer space')

* `-s`, Do not deauth the MAC DL:3D:8D:JJ:39:52. Ignoring a certain MAC address is handy in case you want to tempt people to join your access point in cases of wanting to use LANs.py or a Pineapple on them.

* `-d`, Do not send deauths to access points' broadcast address; this will speed up the deauths to the clients that are found

* `--world`, Set the max channel to 13. In N. America the max channel standard is 11, but the rest of the world uses 13 channels so use this option if you're not in N. America

Technical breakdown
-------
[How to kick everyone around you off wifi with python](http://danmcinerney.org/how-to-kick-everyone-around-you-off-wifi-with-python/)


THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND
ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED
WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE
DISCLAIMED. IN NO EVENT SHALL <COPYRIGHT HOLDER> BE LIABLE FOR ANY
DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES
(INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES;
LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND
ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT
(INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS
SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
