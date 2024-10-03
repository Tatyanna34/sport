# sportimport random
import time

# Teams
team_1 = "Team A"
team_2 = "Team B"

# Simulation time in seconds
match_duration = 90

# Initialize scores
score_team_1 = 0
score_team_2 = 0

# Define the chances of scoring a goal (1 in 10)
goal_probability = 10

def simulate_match():
    global score_team_1, score_team_2
    
    print(f"Kick-off! {team_1} vs {team_2}")
    
    for minute in range(1, match_duration + 1):
        # Random chance to score for each team
        if random.randint(1, goal_probability) == 1:
            score_team_1 += 1
            print(f"{team_1} scored! Minute: {minute} - Score: {team_1} {score_team_1} : {team_2} {score_team_2}")
        
        if random.randint(1, goal_probability) == 1:
            score_team_2 += 1
            print(f"{team_2} scored! Minute: {minute} - Score: {team_1} {score_team_1} : {team_2} {score_team_2}")
        
        # Simulate time passing
        time.sleep(0.1)  # Delay to simulate match progression
        
    # End of match
    print(f"Full-time! Final Score: {team_1} {score_team_1} : {team_2} {score_team_2}")
    if score_team_1 > score_team_2:
        print(f"{team_1} wins!")
    elif score_team_1 < score_team_2:
        print(f"{team_2} wins!")
    else:
        print("It's a draw!")

# Run the simulation
simulate_match()
