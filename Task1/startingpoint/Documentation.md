### Group
Mikko Rinta-Homi
Heikki Ahonen
Outi Jussila

## Implementation

We implemented the state chart in *solution.des* with following states:

```
STATECHART:
    Time [CS] [DS]
        Tick [DS]
        Stop
    Refresh [CS] [DS]
        Time [DS]
        Chrono
        Alarm
    Light [CS] [DS]
        On
        AlmostOff
        Off [DS]
    Chrono [CS] [DS]
        Off [DS]
        On
    EditTime [CS] [DS]
        Off [DS]
        OffDelay
        On
        OnDelay
    Alarm
        Off [DS]
        OffDelay
        On
        OnDelay
```

As can be seen from the states, we have made advancement of time, screen refreshing, light handling, editing and alarm parallel, and given them all substates. 

In our solution, we have implemented functions for
- Default display of time and date
- Time advancement
- Changing display to Chrono and back
- Chrono advancement
- Chrono stop
- Changind display to Alarm and back

Features yet to be implemented are
- Ajustement of time
- Adjustement of alarm
- Alarm going off

The task was found quite difficult and time consuming, where learning the SVM proved to be the most challenging part.