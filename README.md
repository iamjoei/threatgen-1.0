#
# You will need to ensure that tcpreplay is installed on the system
#
# apt-get -y install tcpreplay
#
apt-get -y install tcpreplay

#
# Get the sample threats package
#
cd /opt; git clone https://github.com/iamjoei/threatgen-1.0

#
# Make sure that the inject_pcaps.sh is executable
#
cd threatgen-1.0; mkdir pcaps; mv *.pcap ./pcaps; chmod 755 inject_pcaps.sh

#
# Run the injection script (pcaps can vary based on preference)
#
/opt/threatgen-1.0/inject_pcaps.sh 2>&1
