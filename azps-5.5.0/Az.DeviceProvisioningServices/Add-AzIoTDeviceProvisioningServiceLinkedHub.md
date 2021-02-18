---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: 30bcf61f309a400270e9cca378fce6d1149cf66a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200434"
---
# <span data-ttu-id="5879e-101">Add-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="5879e-101">Add-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="5879e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5879e-102">SYNOPSIS</span></span>
<span data-ttu-id="5879e-103">Połączone centrum IoT z usługą inicjowania obsługi urządzeń w centrum Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="5879e-103">Linked IoT hub to an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="5879e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5879e-104">SYNTAX</span></span>

### <span data-ttu-id="5879e-105">ResourceSet (Default)</span><span class="sxs-lookup"><span data-stu-id="5879e-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-IotHubConnectionString] <String> [-IotHubLocation] <String> [-AllocationWeight <Int32>]
 [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5879e-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5879e-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceLinkedHub [-DpsObject] <PSProvisioningServiceDescription>
 [-IotHubConnectionString] <String> [-IotHubLocation] <String> [-AllocationWeight <Int32>]
 [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5879e-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="5879e-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-IotHubConnectionString] <String>
 [-IotHubLocation] <String> [-AllocationWeight <Int32>] [-ApplyAllocationPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5879e-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="5879e-108">DESCRIPTION</span></span>
<span data-ttu-id="5879e-109">Aby uzyskać wprowadzenie do usługi inicjowania obsługi urządzeń w centrum IoT Azure, https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps zobacz.</span><span class="sxs-lookup"><span data-stu-id="5879e-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="5879e-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5879e-110">EXAMPLES</span></span>

### <span data-ttu-id="5879e-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5879e-111">Example 1</span></span>
```
PS C:\> Add-AzIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -IotHubConnectionString $hubConnectionString -IotHubLocation "eastus"

ResourceGroupName     : myresourcegroup
Name                  : myiotdps
LinkedHubName         : myiothub.azure-devices.net
ConnectionString      : HostName=myiothub.azure-devices.net;SharedAccessKeyName=iothubowner;SharedAccessKey=****
AllocationWeight      : 
ApplyAllocationPolicy : 
Location              : eastus
```

<span data-ttu-id="5879e-112">Połączone centrum IoT z usługą inicjowania obsługi urządzeń w centrum Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="5879e-112">Linked IoT hub to an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="5879e-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="5879e-113">Example 2</span></span>
```
PS C:\> Add-AzIoTDpsHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -IotHubConnectionString $hubConnectionString -IotHubLocation "eastus" -AllocationWeight 10 -ApplyAllocationPolicy $false

LinkedHubName                   Location    AllocationWeight    ApplyAllocationPolicy
-------------                   --------    ----------------    ---------------------
myiothub1.azure-devices.net     eastus      2                   true
myiothub2.azure-devices.net     westus2     10                  false
```

<span data-ttu-id="5879e-114">Połączone centrum IoT z usługą inicjowania obsługi urządzeń w centrum Azure IoT Hub za pomocą funkcji AllocationWeight i ApplyAllocationPolicy.</span><span class="sxs-lookup"><span data-stu-id="5879e-114">Linked IoT hub to an Azure IoT Hub device provisioning service with AllocationWeight and ApplyAllocationPolicy.</span></span>

## <span data-ttu-id="5879e-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5879e-115">PARAMETERS</span></span>

### <span data-ttu-id="5879e-116">- AllocationWeight</span><span class="sxs-lookup"><span data-stu-id="5879e-116">-AllocationWeight</span></span>
<span data-ttu-id="5879e-117">Waga alokacji centrum IoT</span><span class="sxs-lookup"><span data-stu-id="5879e-117">Allocation weight of the IoT Hub</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5879e-118">-ApplyAllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="5879e-118">-ApplyAllocationPolicy</span></span>
<span data-ttu-id="5879e-119">Wartość logiczna wskazująca, czy mają być stosowane zasady alokacji do Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="5879e-119">A boolean indicating whether to apply allocation policy to the IoT Hub</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5879e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5879e-120">-DefaultProfile</span></span>
<span data-ttu-id="5879e-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5879e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5879e-122">- DpsObject</span><span class="sxs-lookup"><span data-stu-id="5879e-122">-DpsObject</span></span>
<span data-ttu-id="5879e-123">Obiekt usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="5879e-123">IoT Device Provisioning Service Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5879e-124">-IotHubConnectionString</span><span class="sxs-lookup"><span data-stu-id="5879e-124">-IotHubConnectionString</span></span>
<span data-ttu-id="5879e-125">Connection String of the Iot Hub resource.</span><span class="sxs-lookup"><span data-stu-id="5879e-125">Connection String of the Iot Hub resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5879e-126">-IotHubLocation</span><span class="sxs-lookup"><span data-stu-id="5879e-126">-IotHubLocation</span></span>
<span data-ttu-id="5879e-127">Lokalizacja Centrum Iot</span><span class="sxs-lookup"><span data-stu-id="5879e-127">Location of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5879e-128">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="5879e-128">-Name</span></span>
<span data-ttu-id="5879e-129">Nazwa usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="5879e-129">Name of the IoT Device Provisioning Service</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5879e-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5879e-130">-ResourceGroupName</span></span>
<span data-ttu-id="5879e-131">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="5879e-131">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5879e-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5879e-132">-ResourceId</span></span>
<span data-ttu-id="5879e-133">Identyfikator zasobu usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="5879e-133">IoT Device Provisioning Service Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5879e-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5879e-134">-Confirm</span></span>
<span data-ttu-id="5879e-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5879e-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5879e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5879e-136">-WhatIf</span></span>
<span data-ttu-id="5879e-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5879e-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5879e-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="5879e-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5879e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5879e-139">CommonParameters</span></span>
<span data-ttu-id="5879e-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5879e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5879e-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5879e-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5879e-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5879e-142">INPUTS</span></span>

### <span data-ttu-id="5879e-143">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="5879e-143">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="5879e-144">System.String</span><span class="sxs-lookup"><span data-stu-id="5879e-144">System.String</span></span>

## <span data-ttu-id="5879e-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5879e-145">OUTPUTS</span></span>

### <span data-ttu-id="5879e-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="5879e-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="5879e-147">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitions</span><span class="sxs-lookup"><span data-stu-id="5879e-147">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitions</span></span>

## <span data-ttu-id="5879e-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5879e-148">NOTES</span></span>

## <span data-ttu-id="5879e-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5879e-149">RELATED LINKS</span></span>
