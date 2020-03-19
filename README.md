// Created on Thu March 19 2020
//variables//
int l_motor = 0;
int r_motor = 2;
int lb = 8;
int rb = 9;
int go = 75;
int back = -75;
int pause = 2000;




int main()
{
	while(1){ //as long as the log test is true...
     straight();
        	if(digital(lb)==1){ //if it hits something turn right
        		right();
            }
        	if(digital(rb)==1){ //if it hits something stop
                msleep(pause);
				ao();
            }
		}
	
	printf("Hello, World!\n");
	return 0;
	
}

//functions//
void straight(){
    motor(l_motor,go);
    motor(r_motor,go);
}
void reverse(){
 	motor(l_motor,back);
    motor(r_motor,back);
    msleep(pause);
    ao();
}
void right(){
 	motor(l_motor,go);
    msleep(pause);
    ao();
}
void left(){
    motor(r_motor,go);
    msleep(pause);
    ao();
}

