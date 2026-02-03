# **tle uncertainity modelling**

## Theory 1
through the code we try to estimate how much a position propagated from an older TLE is likely to disagree with a position propagated from a newer TLE, as a function of time and orbital characteristics.


firstly the problem lies not in tracking, but the root itself, the tle data.

satellites move in space, so humans cannot see them directly most of the time. so humans invented a compact way to summarize what we currently believe about a satellite's orbit.
This summary is called TLE (two-line-element)

a tle is not reality, it is belief encoded in numbers. 

CelesTrak publishes these publicly

## Theory 2

when someone uses a TLE, they download a tle at time t0, use orbital math (sgp4 engine) to compute where the satellite should be at time t0 + delta(t). the data would show that position is reasonable.
this is how tracking, collision avoidance, and planning acutally work.

**but the truth bends here**
the extrapolation gets worse as time passes. not because the math is bad - but because the tle gets stale.
factors like atmospheric drag, solar activity, and sattelites' maneuverability changes. FREQUENTLY. 

**core problem**
people are using TLEs without knowing how much to trust them, 
they might ask: 
    Is this TLE still relevant?
    For how many hours/days/months/years?
    Is this satellite more upredictable than others?

tle data might not answer this, but it gives a position only, not confidence.

## Theory 3
**what im doing and what im not**

i am not finding the true satellite position, correcting orbital mechanics, replaceing the sgp4 engine, or trying to track satellites better than space agencies (it'd be so cool if i did).

i am trying to find a way to estimate how unreliable the predicted position is likely to be for a given tle and a future time.


## Work 1
right now i have said that tle based predictions degrade in a measurable, structure way.

so i will do this:
    i will pick 5-10 satellites (mix of both high and low altitude) and i will build a timeline of to collect historical tles over a period
    of 1 week. 




