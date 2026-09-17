# 2026-7-15
## things done
* UI design idea
```text
1.account log in does not mean device online, need to remind user to connect device by phone App
2.design log out allow logging out current account to log in another account
```
* test if developers can get device id from firebase through user account and password, the result is cannot
## things need to do
### factors need to consider
* continue test the way to get device id through user account and password
# 2026-7-16
## things done
* UI design idea
```text
1. account logging in does not mean device online, need to remind user to connect device by phone App
2. design log out allow logging out current account to log in another account
3. need to get neurosity button of artificialintelligence page same to readbrain page
4. reminder of `Device already bound to another account.`
5. show the user all available device name when log in
```
* find ways to get device id by email and password, user doesn't need to enter a very long device id when log in
## things need to do
* understand the data flow when log in
* finish code and code
# 2026-7-17
## things done
* figure out where to put the function log out
```text
using message box:
when user already log in, click neurosity button will show the information and log out option
when user has not log in, click neurosity button will remind user entering the information of account and password
```
* Add login(), logout(), get_devices(), and select_device(); remove _load_env(); update initial variables accordingly
## things need to do
* headset selection backend need to modify to comply with the login func, click neurosity button will show up a message box which remind user log in
* UI part code finish
# 2026-7-18
## things done
* Designed the data flow and reduced the responsibilities of the QML layer.
* Added new backend functions to support the updated architecture.
## things need to do
* Continue refining the data flow between the frontend and backend.
* Implement the remaining backend and QML logic.
# 2026-8-4
## things done
* Solve the issue where a function defined in `NeurosityDataProcessor` is being called through the `BrainwavesBackend` class in QML.
## things need to do
* library conflicts in qml
* how to switch device when already login one device
# 2026-8-5
## things done
* Solve the issue library conflicts in qml
* solve the issue `auth.sign_in()` didn't work, substitute it with `auth.sign_in_with_email_and_password()`
## things need to do
* state conflict in device select dialog and neurosity button
* how to switch device when already login one device
# 2026-8-6
## things done
* Solve the issue state conflict in device select dialog and neurosity button
```text
no return value from func `selectNeurosityDevice()` in file `GUI5.py`, but in `ReadBrain.qml` dialog of devicedialog there is statement like `var state = backend.selectNeurosityDevice()` waiting for the return value from `selectNeurosityDevice()`
```
* reinitial object of neurosityprocessor problem, caused by the missing statement `self.neurosity_connected = True`
* device switch can be realized by click button Neurosity
## things need to do
* test when there are several devices online if user can switch
* record the test video
# 2026-8-7
## things done
* tested when there are several devices online if user can switch
* Solved the issue when switch the device no new client is created which lead to the incorrect state display: modified the func `select_device()` in file `neurosityprocessor.py`
## things need to do
* record the test video
# 2026-8-11
## things done
* record the test video
## things need to be done
* allow account switch without exit the app
# 2026-9-17
## things done
* Added `neurosityLogout()` func in `GUI5.py`
* Added `Sign Out`, `Close` buttons on loginDialog, allow switch account
* Added `Back` button on deviceDialog
## things need to be done
* Record the demo video again
* Restore the yeallow circle around the neurosity button after switch
