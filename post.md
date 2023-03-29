![image|601x500](upload://4jhNZfj8eVolw98ufjXMbkmPYfm.jpeg)

Hello, I'm failing to properly automate my ventilation system and I keep shorting relays. Attached a diagram of what I try to do, I'm trying to put the relay in the Switch 2 which currently is a two gangs controlling the ensuite lights and the ventilation speed.

The ventilation system I have is the MrBox ECO 2 from Nuaire: 
https://info.nuaire.co.uk/catalogue/MRXBOX-ECO2.pdf

It has a maximum power consumption of 155Watts according to the PDF, however, the label on the product states 152W

![image|690x422](upload://yfVDcN57E3B8eXKxATiQKGaInIM.jpeg)

I originally got a 2 gang smart click relay:
https://www.directelectrical.co.uk/products/Home+Automation/Click+Scolmore+Home+Automation/White+2+Gang+Zigbee+2+x+100W+LED+Smart+Switch+Module%2C+IP20/2497932556



I can now see that they are 100W per output... so that is not ideal, but even before getting there... I blew the first one because I wired it wrongly putting live in one of the switch terminals on the relay (ooops)

Then for the second one I wired it "properly" but... toggling the relay was causing the RCD1 or RCD2 to trip... I believe because the relay has only one Live input, so if I put the MrCOM in the relay, when I switch the lights the RCD1 trip, if I put the L(ights) COM in the relay, the RCD2 trip when switching the lights.

I have then gave up on the idea of retaining the two gangs and tried to use the smart relay only to automate the ventialtion based on humidity, so I've removed switch inputs on the relay and just had the MrCOM in the line input and the MrL1 in the output. 
I've then used a dumb switch for the lights, this worked, I could toggle the ventilation via HomeAssistant without tripping, however, the morning after it the smart relay was completely dead (although was not operated during the night)

I've then got a zigbee mini from SONOFF planning to use the Neutrals.
https://sonoff.tech/wp-content/uploads/2021/08/%E4%BA%A7%E5%93%81%E5%8F%82%E6%95%B0%E8%A1%A8-ZBMINI-20210811.pdf

This is rated for 2200W so I thought I was golden... I wired all N1, 2, 3, 4 together and used a jumper cable to the Nin of the Sonoff, then used the MrCOM and MrL1 for line input and output...

This tripped bot RCD1 and RCD2... I now undertand that this is because the Neutrals of for the lights only? So the sonoff is dead again.

I then understand that I cannot use a relay that require a Neutral because I cannot "cross" the circuits... I'm ok as said to automate only the MrBox... would it be ok then to get this one:
https://www.directelectrical.co.uk/products/Home+Automation/Click+Scolmore+Home+Automation/White+1+Gang+Zigbee+250W+LED+Smart+Switch+Module%2C+IP20/1325174863

I have disconnected the terminals on Switch1 for the MrBox and replaced that switch with one gang for the lights only.

All works without trips with dumb switches on Switch 2

Any help appreciated!
