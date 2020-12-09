From this tutorial I learned some additional concepts of the Kaa platform and discover how to:

1. execute commands on your device
2. view command execution history on the Kaa UI

########Terms and Concepts in KAA

##Command
Command is a short-lived message sent to a connected endpoint from the Kaa platform. With the commands, you can toggle the lights on/off, open a car trunk, or request an immediate endpoint state report.

Any commands may be in either pending or executed state. Pending state means that the command was invoked but no execution result for that command is known yet. Executed state is assigned to the command that has gotten an endpoint response, meaning an endpoint received the command, executed it, and sent the execution result back to the platform.

#####Consider the following example.

Let’s assume you just sent a command to your Tesla car to park itself in a parking slot. The platform immediately assigns pending to that command, while your Tesla receives the command and starts parking. After finishing with the task, the car reports the execution result of that command back to the platform and Kaa assigns executed to that command.

Every command has an execution status code and reason phrase that endpoints can specify at the moment of reporting the execution result back to the platform. If, for example, your Tesla couldn’t finish the parking because it was taken by another vehicle, it may report the execution result specifying 409 status code and some meaningful reason phrase, which will be displayed for you in the Kaa UI.

Command type
Command type represents the type of command that you want to execute on an endpoint e.g. reboot, close-door, switch-light, or in the case of Tesla—park. An endpoint can handle as many command types as you define in its firmware.
