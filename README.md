# angle_between_hour_minute

double angleClock(int hour, int minutes){
    
    if(hour<1 ||hour>12 || minutes<1 ||minutes>60){
        printf("invalid");
    }
    if(hour==12)
        hour=0;
    if(minutes==60){
        minutes=0;
        hour += 1;
        if(hour>12)
            hour=hour-12;
    }
    
    double h = (hour*30.0) + (minutes*0.5);
    double m = minutes*6.0;
    double angle = fabs(m-h);
    if(angle>180){
        angle = 360-angle;
    }
    return angle;
    
    

}
