# Ex.No:4(B)  IMPLEMENT SOLID PRINCIPLES IN JAVA PROGRAM 

## QUESTION:
Write a Java program to implement the Observer Design Pattern for a smart city air quality monitoring system, where different controllers respond to AQI readings based on predefined ranges.

## AIM:
To implement the Observer Design Pattern in Java by creating a SensorNetwork as the subject and multiple SmartControllers as observers that react to AQI readings based on specific conditions.

## ALGORITHM :
1.	Start the program.
2.	Create an Observer interface and implement it using GreenZoneController, AlertZoneController, and DangerZoneController classes.
3.	Create a SensorNetwork class that maintains a list of observers and notifies them when AQI data is received.
4.	Read sensor details and AQI values, notify the observers, and display the appropriate actions taken by the relevant controllers.
5.	End the program.
   
## PROGRAM:
 ```
/*
Program to implement a SOLID Principles in Java Program
Developed by: NITHYA D
RegisterNumber: 212223240110 
*/
```

## SOURCE CODE:
```
import java.util.*;

interface Observer {
    void check(int aqi, String sensorId);
}

class GreenZoneController implements Observer {
    public void check(int aqi, String sensorId) {
        if (aqi < 100) {
            System.out.println("[GreenZoneController]: AQI is good at Sensor " + sensorId + ". No action needed.");
        }
    }
}

class AlertZoneController implements Observer {
    public void check(int aqi, String sensorId) {
        if (aqi >= 100 && aqi <= 200) {
            System.out.println("[AlertZoneController]: Moderate AQI at Sensor " + sensorId + ". Send public health alert.");
        }
    }
}

class DangerZoneController implements Observer {
    public void check(int aqi, String sensorId) {
        if (aqi > 200) {
            System.out.println("[DangerZoneController]: Critical AQI at Sensor " + sensorId + "! Trigger lockdown protocol.");
        }
    }
}

class SensorNetwork {
    private List<Observer> observers = new ArrayList<>();

    public void register(Observer o) {
        observers.add(o);
    }

    public void receiveData(String sensorId, int aqi) {
        System.out.println("Sensor " + sensorId + " reports AQI: " + aqi);
        for (Observer o : observers) {
            o.check(aqi, sensorId);
        }
    }
}

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        SensorNetwork network = new SensorNetwork();

        network.register(new GreenZoneController());
        network.register(new AlertZoneController());
        network.register(new DangerZoneController());

        int n = sc.nextInt();
        sc.nextLine();

        for (int i = 0; i < n; i++) {
            String[] parts = sc.nextLine().split(" ");
            String id = parts[0];
            int aqi = Integer.parseInt(parts[1]);
            network.receiveData(id, aqi);
        }
    }
}
```

## OUTPUT:
<img width="1230" height="276" alt="image" src="https://github.com/user-attachments/assets/f7e592ab-21c7-4509-9384-9de9d9204edb" />

## RESULT:
Thus, the Java program to demonstrate the Observer Design Pattern using a smart city air quality monitoring system was implemented successfully and the output was verified.
