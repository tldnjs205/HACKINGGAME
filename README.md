Finger Print Hacking Game
Read the license before redistributing this software.

made by utku#9999

I created this mini game for my upcoming casino heist script which will be very similar to GTA:Online Diamond Casino Heist, with all of the setups and main missions.

I also created the other hacking mini game which is this one: https://www.youtube.com/watch?v=iIVddIUm8Zg&t=349s

My Discord: https://discord.gg/yqHmvcr

English
Installation
Very simple. Open Finger-Print-Hacking-Game-master and move the folders inside it (utk_hackdependency and utk_fingerprint) to your resources folder.

in server.cfg add this:

start utk_hackdependency
start utk_fingerprint
Why hack dependency is a different script?

Because it is a shared dependency for my other hacking mini game.

Usage
To start hacking game from other scripts add this to your code:

TriggerEvent("utk_fingerprint:Start", levels, lifes, time, callback)

-- levels is how many levels you want. Max is 4, Min is 1
-- lifes is how many life player has, Max is 6, Min is 1
-- time is how much time player has in minutes, Max is 9, min is 1 (I highly recommend to set it between 3-1)
-- callback is the callback function to catch the outcome
Here is an example:

TriggerEvent("utk_fingerprint:Start", 4, 6, 2, function(outcome, reason)
    if outcome == true then -- reason will be nil if outcome is true
        print("Succeed")
    elseif outcome == false then
        print("Failed. Reason: "..reason)
    end
end)
