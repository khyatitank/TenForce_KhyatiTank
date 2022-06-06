# TenForce_KhyatiTank

**Steps**

1. Get "MeanRadius" value while reading planet.moons data (Class name : MoonDto)
[JsonProperty("meanRadius")] public float MeanRadius { get; set; }

2. Calculate "Gravity" of each moon by using formula g = GM / r2 (Class name : Moon) 
Gravity = G * (moonDto.MassValue / (moonDto.MeanRadius * moonDto.MeanRadius));

3. Writting average "Gravity" based on each planet in ScreenOutputService file
var avgMoonGravity = planet.Moons?.Select(data => data.Gravity).Average() ?? 0;
