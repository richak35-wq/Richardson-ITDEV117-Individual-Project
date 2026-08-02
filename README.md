# Richardson-ITDEV117-Individual-Project
Summer 2026
Application name: Traffic Reroute Decision Diagram (concept)

Problem it solves: Helps drivers make better route choices when conditions change—balancing delay, safety, and preferences—by deciding whether to reroute or stay on course.

Who it’s for: Drivers using navigation; also teams designing/operating the reroute logic.

Main features (including traffic lights):

Traffic conditions: congestion level, speed drop, incident reports
Traffic signals: signal density on candidate routes, expected red-light delay, corridor signal timing patterns (where available)
Road constraints: closures, restrictions
Route options comparison: ETA difference, distance, turn count/complexity, tolls
User preferences: avoid tolls/highways, arrive-by time (and optionally “avoid many stops/lights”)
Safety/context: hands-free mode, distraction sensitivity, confidence level
Decision logic: compute a benefit score vs. threshold to recommend reroute, keep route, or require reroute for closures
Learning loop: uses accept/decline feedback to tune thresholds and preference weighting over time
How the app works (short): The app continuously estimates travel time on the current route and alternatives using live traffic, constraints, and expected signal delay from traffic lights (which can materially affect ETAs on arterial routes). It then scores the net benefit of switching routes (time saved vs. added complexity like extra turns/stops/lights, toll cost, and confidence), recommends a change only when the benefit clears a threshold, forces reroutes for closures, and learns from what the driver accepts or declines.
