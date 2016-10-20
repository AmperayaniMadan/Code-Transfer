# Code-Transfer
To get the code to the Android machine

Find your code here dude.


        protected BluetoothManager _manager;
        protected BluetoothAdapter _adapter;
        
        public void PermissionChecks()
        {
            throw new NotImplementedException();

            //Lets turn on the BT adapter here...ok.
            var appContext = Android.App.Application.Context;
            _manager = (BluetoothManager)appContext.GetSystemService("bluetooth");
            _adapter = _manager.Adapter;

            if (_adapter == null || !_adapter.IsEnabled)
            {
                Intent enableBT_intent = new Intent(BluetoothAdapter.ActionRequestEnable);
                StartActivityForResult(enableBT_intent, 1);
            }
        }
