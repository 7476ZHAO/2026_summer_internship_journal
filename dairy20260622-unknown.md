#  2026-6-22
* fix the UI bug, the headset selection row outside the darkbox, caused by the headset selection codes put outside the rectangle brace
* check neurosity pipeline repo, find that the random forest pytorch and tensorflow didn't use feature extraction, maybe crown can be improved in this aspect
* check the neurosity SDK, 
* remind classmates update branch and resubmit
#  2026-7-6
## things done
* begin working on issue 39
* figure out how to develop scripts based on unmerged PR
* set the venv
* compare different ways to indicate the status of device Crown: final case: add a button next to headset selection button
* correct the location of the headset selection button
## things need to do and check
* left bottom connect button, related to func setDataMode( ), looks like the neurosity is not related to this button, consider after issue 39 finished
* add a button next to headset selection button
* add a func in neurosityprocessor.py file checking the status of Crown device
#  2026-7-7
## things done
* test if there is state in dict status of neurosity SDK
* update PR of adding missing dependencies in requirements.txt
* add call back func for subscribing to the status, (line 50-56) Subscribe to status() during initialization, cache the current state, and use that cached state everywhere.
* learn __name__ built-in value in python
## things need to do and check
* understand the Callback mechanism
* finish the backend part of issue 39: add state check in func get_neurosity_brainwave_data(self), add state change func connect to UI
* finish the ui part of issue 39: 
* test
#  2026-7-8
## things done
* understand callback mechanism
* add status check in func get_tensor()
* add state check in func get_neurosity_brainwave_data()
* test func get_tensor() and get_device_state ()
## things need to do and check
* online offline status indicate cannot stop the live data streaming
* submit PR to Neurosity about the device offline indicator problem, modify func stream_metric() and brainwaves_raw():
```text
When the device goes offline during an active brainwaves_raw subscription, the SDK continues to deliver buffered/database data without any indication that the device is no longer connected. This makes it difficult to determine whether EEG acquisition is truly live. It would be helpful if the SDK could notify subscribers (e.g., via an error, stream termination, or offline callback) when the device disconnects.
```
* state cannot update in realtime, need to continue test
* finish the ui part of issue 39
