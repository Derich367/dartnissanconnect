# dartnissanconnect
This is a fork of Tobiaswks dartnissanconnect lib for the NissanConnect API.

A Dart client library for the NissanConnect API for vehicles produced after May 2019.

Through the NissanConnect API you can ask your vehicle for the latest data, see current battery and charging statuses, see the current climate control state, start or stop climate control remotely, remotely start charging, and retrieve the last known location of the vehicle.

Though this library is called dartnissanconnect it refers to the Kamereon platform used for connected cars from the Renault-Nissan-Mitsubishi Alliance from 2019 onwards.

## Usage

A simple usage example:

    import 'package:dartnissanconnect/dartnissanconnect.dart';

    main() {
      NissanConnectSession session = new NissanConnectSession(debug: true);

      session.login(username: "username", password: "password").then((vehicle) {
        print(vehicle.vin);
        print(vehicle.modelYear);
        print(vehicle.nickname);
      });
    }
