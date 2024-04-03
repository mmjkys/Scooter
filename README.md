#ask user miles or kilometers
unit = input("Do you want to enter distance as miles or kilometers (type m or k):")
#ask user how long the trip is
if unit == 'm':
	tripLength = float(input("How many miles would you like to scooter?"))
	otherLength = tripLength * 1.60934
	print("That is",otherLength, "Kilometers")
	hours = tripLength / 15
elif unit == 'k':
	tripLength = float(input("How many kilometers would you like to scooter?"))
	otherLength = tripLength * 0.621371
	print("That is",otherLength, "Miles")
	hours = tripLength / 24.1402
else:
	quit = True
#print opposite unit
#calculate and print how long the trip will take
	#15 miles an hour
minutes = hours*60
if hours < 1:
   print("Total time in minutes: ",minutes)
else:
	print("Total time in hours: ", hours)

costs = {"company A":0.1,"company B":0.1,"company C":0.1}
costs["company A"] = 1 + (0.15*minutes)
costs["company B"] = 2.5 + (0.12*(minutes-5))
costs["company C"] = 5 + (0.06*minutes)
sortedCosts = sorted(costs.values())
print("You should use",list(costs.keys())[list(costs.values()).index(sortedCosts[0])], ". It will cost $",sortedCosts[0])
	# costs.append("company A": 1 + (0.15*minutes)) 
	# costs.append("company B": 2.5 + (0.12*(minutes-5))) 
	# costs.append("company C": 5 + (0.06*minutes)) 
