# Sending Telemetry

The sample portal site is ready to accept data.  Send telemetry data to the sample portal site through IoT Hub.

If you do not have a real/physical device, you can still send telemetry using a simulator.

## Raspberry Pi Online Simulator

Raspberry Pi Online Simulator is an online tool you can send simulated temperature and humidity telemetry to IoT Hub.

1. Open a new browser window then navigate to <https://azure-samples.github.io/raspberry-pi-web-simulator/>

    ![Simulator 01](media/Simulator01.png)

1. Go back to Azure Portal browser window, then click the new IoT device just created

    > [!TIP]  
    > If you do not see the device, click `Refresh` button

    ![Azure Portal 11](media/Portal11.png)

1. Copy `Primary Connection String` in Azure Portal window

    ![Azure Portal 12](media/Portal12.png)

1. Replace line #15 with the connection string

    Example : 

    ```shell
        :
    const connectionString = '[Your IoT hub device connection string]';
        :
    ```

    to

    ```shell
        :
    const connectionString = 'HostName=Hub-ki323.azure-devices.net;DeviceId=MyFirstDevice;SharedAccessKey=testtesttestetest=';
        :
    ```

    ![Simulator 02](media/Simulator02.png)

## Sending Telemetry to IoT Hub

1. Click `Run` to start sending messages

    ![Simulator 03](media/Simulator03.png)

1. Telemetry data should be sent to the Portal Web site in real time

    > [!TIP]  
    > The initial connection may take time to initialize Azure Functions

    ![Web App 03](media/WebApp03.png)

## Next Step

Completed!

- [Project 15 from Microsoft](../README.md)