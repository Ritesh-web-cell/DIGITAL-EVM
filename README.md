# DIGITAL-EVM
School level project on digital EVM.
print("-----VOTING TO SELECT THE CARTEL LEADER-----")

candidates = ["Elchapito","Elmencho","Pabloescobar","Elchapo"]

votes = {candidates[0]:0,candidates[1]:0,candidates[2]:0,candidates[3]:0}

print("\nCANDIDATES ARE:")
for i in candidates:
    print(i)

while True:
    vote = input("ENTER THE CANDIDATES NAME (type 'stop' to end) = ").title().strip()

    if vote == 'Stop':
        break

    elif vote in votes:
        votes[vote] += 1
        print("YOU HAVE SELECTED",vote)
    else:
        print("candidate not found!")

print(votes)

winner = ""
highest_votes = 0

for vote in votes:
    if votes[vote]>highest_votes:
        highest_votes = votes[vote]
        winner = vote

print("winner = ", winner)
print("votes = ", highest_votes)
print("Thank You")
