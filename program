from mcpi.minecraft import Minecraft
mc=Minecraft.create()

import time



def gaugetower():
        pos=mc.player.getTilePos()
        x,y,z=pos.x,pos.y,pos.z
        blocks=[20,20,20,20,20,20,20,20,20,20]
        count=0
        mc.setBlock(x,y+count,z,blocks[count])
        length=len(blocks)-1
        guage=22
        count=0
        while count<=length:
                mc.setBlock(x,y+count,z,blocks[count])
                count=count+1
        count=0
        blocktype=input("게이지타워에 넣고 싶은 블럭코드를 입력하세요")
        blocktype = int(blocktype)
        count_gauge = 20
        while count_gauge != 0:
                while count<=length:
                        blocks=[blocktype,blocktype,blocktype,blocktype,blocktype,blocktype,blocktype,blocktype,blocktype,blocktype]
                        mc.setBlock(x,y+count,z,blocks[count])
                        count += 1
                        time.sleep(1)
                        count_gauge -= 1


                while count>0:

                        count=count-1
                        blocks[count]=20
                        mc.setBlock(x,y+count,z,blocks[count])
                        time.sleep(1)
                        count_gauge -= 1

def ChangeWoolColor():
        pos = mc.player.getTilePos()
        x,y,z=pos.x,pos.y,pos.z

        colorList = [0,1,2,3,4,5,6,7,8,9]


        time_count = 10
        while time_count != 0:
                color = colorList[time_count-1]
                mc.setBlock(x,y,z,35,color)
                time.sleep(1)
                time_count -= 1
                        
def massage():
        messagetime = input("몇번 입력하시겠습니까?:")
        messagetime = int(messagetime)
        while messagetime != 0:
                message = input("채팅할 문자를 입력하세요")
                mc.postToChat(message)
                messagetime = messagetime - 1
        

def tree():
        pos=mc.player.getTilePos()
        x,y,z=pos.x,pos.y,pos.z
        mc.setBlocks(x,y,z, x,y+4,z, 57)
        mc.setBlocks(x-2,y+5,z-2,x+2,y+5,z+2, 18)
        mc.setBlocks(x-1,y+6,z-1,x+1,y+6,z+1, 18)
        mc.setBlocks(x,y+6,z, x, y+7, z, 18)

                        
def digMan():   
        while True:     
                pos=mc.player.getTilePos()      
                x,y,z=pos.x,pos.y,pos.z         
                mc.setBlocks(x-1,y,z-1, x+1,y+1,z+1, 0) 
                block=mc.getBlock(x,y-1,z)  
                air=0   
                if block != air:        
                        mc.setBlock(x,y-1,z, 169)       
                else: 
                        break 

def fireMan():  
        while True:
                pos=mc.player.getTilePos()      
                x,y,z=pos.x,pos.y,pos.z 
                mc.setBlocks(x,y,z, x,y+2,z, 51)        
                air = 0                       
                block=mc.getBlock(x,y-1,z)      
                if block == air:
                        break
        
def playeranswer():
        if answer == ("gaugetower"):
                gaugetower()
        elif answer == ("ChangeWoolColor"):
                ChangeWoolColor()
        elif answer == ("building"):
                building()
        elif answer == ("tree"):
                tree()
        elif answer == ("message"):
                massage()
        elif answer == ("digman"):
                digMan()
        elif answer == ("fireman"):
                fireMan()
        
              
        elif answer == ("help"):
                print ("gaugetower,ChangeWoolColor,tree,message")
        else:
                print ("다시 입력하세요")
while True:
        answer = input("무슨 기능을 실행시키겠습니까?")
        playeranswer()
