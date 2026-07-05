# Updating WSO2 API Microgateway via U2 Update

When applying a U2 (Update 2) to WSO2 API Microgateway (MGW), you need to follow the steps below to ensure the update is applied correctly.

## Steps to follow during a U2 update

1. After updating to the new U2 level, navigate to the `<MGW_TOOLKIT_HOME>/lib/` directory and check for a folder named `platform`. If it is present, remove it.

    !!! note
        Do not remove the `platform.zip` file.

2. Navigate to `<MGW_TOOLKIT_HOME>/lib/gateway-balo/` and check for a folder named `gateway-2020r1-java8-3.2.0`. If it is present, remove it.

    !!! note
        Do not remove the `gateway-2020r1-java8-3.2.0.balo` file.

3. Create a new folder and initialize a new project using the following command.

```bash
    micro-gw init <project_name> -a <api definition path>
```

4. Build the project using the following command.

```bash
    micro-gw build <project_name>
```

5. Deploy the API by starting WSO2 API Microgateway using the following command.

```bash
    gateway <path-to-MGW-jar-file>
```
