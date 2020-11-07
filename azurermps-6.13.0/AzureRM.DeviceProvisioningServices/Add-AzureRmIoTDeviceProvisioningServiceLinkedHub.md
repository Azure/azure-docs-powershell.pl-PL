---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Add-AzureRmIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Add-AzureRmIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: ca32f2d0436ea16d8897f279239ce4de079d1550
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717419"
---
# <span data-ttu-id="68562-101">Add-AzureRmIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="68562-101">Add-AzureRmIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="68562-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="68562-102">SYNOPSIS</span></span>
<span data-ttu-id="68562-103">Połączony Centrum IoT z usługą dostarczania urządzeń centrum usługi Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="68562-103">Linked IoT hub to an Azure IoT Hub device provisioning service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68562-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="68562-104">SYNTAX</span></span>

### <span data-ttu-id="68562-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="68562-105">ResourceSet (Default)</span></span>
```
Add-AzureRmIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-IotHubConnectionString] <String> [-IotHubLocation] <String> [-AllocationWeight <Int32>]
 [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68562-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="68562-106">InputObjectSet</span></span>
```
Add-AzureRmIoTDeviceProvisioningServiceLinkedHub [-DpsObject] <PSProvisioningServiceDescription>
 [-IotHubConnectionString] <String> [-IotHubLocation] <String> [-AllocationWeight <Int32>]
 [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68562-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="68562-107">ResourceIdSet</span></span>
```
Add-AzureRmIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-IotHubConnectionString] <String>
 [-IotHubLocation] <String> [-AllocationWeight <Int32>] [-ApplyAllocationPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68562-108">Opis</span><span class="sxs-lookup"><span data-stu-id="68562-108">DESCRIPTION</span></span>
<span data-ttu-id="68562-109">Aby uzyskać wprowadzenie do usługi dostarczania urządzeń centrum usług Azure IoT, zobacz https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="68562-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="68562-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="68562-110">EXAMPLES</span></span>

### <span data-ttu-id="68562-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="68562-111">Example 1</span></span>
```
PS C:\> Add-AzureRmIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -IotHubConnectionString $hubConnectionString -IotHubLocation "eastus"

ResourceGroupName     : myresourcegroup
Name                  : myiotdps
LinkedHubName         : myiothub.azure-devices.net
ConnectionString      : HostName=myiothub.azure-devices.net;SharedAccessKeyName=iothubowner;SharedAccessKey=****
AllocationWeight      : 
ApplyAllocationPolicy : 
Location              : eastus
```

<span data-ttu-id="68562-112">Połączony Centrum IoT z usługą dostarczania urządzeń centrum usługi Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="68562-112">Linked IoT hub to an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="68562-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="68562-113">Example 2</span></span>
```
PS C:\> Add-AzureRmIoTDpsHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -IotHubConnectionString $hubConnectionString -IotHubLocation "eastus" -AllocationWeight 10 -ApplyAllocationPolicy $false

LinkedHubName                   Location    AllocationWeight    ApplyAllocationPolicy
-------------                   --------    ----------------    ---------------------
myiothub1.azure-devices.net     eastus      2                   true
myiothub2.azure-devices.net     westus2     10                  false
```

<span data-ttu-id="68562-114">Połączony Centrum IoT z usługą Azure IoT Hub, usługa udostępniania połączenia z AllocationWeight i ApplyAllocationPolicy.</span><span class="sxs-lookup"><span data-stu-id="68562-114">Linked IoT hub to an Azure IoT Hub device provisioning service with AllocationWeight and ApplyAllocationPolicy.</span></span>

## <span data-ttu-id="68562-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="68562-115">PARAMETERS</span></span>

### <span data-ttu-id="68562-116">-AllocationWeight</span><span class="sxs-lookup"><span data-stu-id="68562-116">-AllocationWeight</span></span>
<span data-ttu-id="68562-117">Waga przydziału Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="68562-117">Allocation weight of the IoT Hub</span></span>

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

### <span data-ttu-id="68562-118">-ApplyAllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="68562-118">-ApplyAllocationPolicy</span></span>
<span data-ttu-id="68562-119">Wartość logiczna wskazująca, czy należy zastosować zasadę alokacji do centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="68562-119">A boolean indicating whether to apply allocation policy to the IoT Hub</span></span>

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

### <span data-ttu-id="68562-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68562-120">-DefaultProfile</span></span>
<span data-ttu-id="68562-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="68562-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68562-122">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="68562-122">-DpsObject</span></span>
<span data-ttu-id="68562-123">Obiekt usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="68562-123">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="68562-124">-IotHubConnectionString</span><span class="sxs-lookup"><span data-stu-id="68562-124">-IotHubConnectionString</span></span>
<span data-ttu-id="68562-125">Parametry połączenia z zasobem centrum usług IoT.</span><span class="sxs-lookup"><span data-stu-id="68562-125">Connection String of the Iot Hub resource.</span></span>

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

### <span data-ttu-id="68562-126">-IotHubLocation</span><span class="sxs-lookup"><span data-stu-id="68562-126">-IotHubLocation</span></span>
<span data-ttu-id="68562-127">Lokalizacja Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="68562-127">Location of the Iot Hub</span></span>

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

### <span data-ttu-id="68562-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="68562-128">-Name</span></span>
<span data-ttu-id="68562-129">Nazwa usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="68562-129">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="68562-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68562-130">-ResourceGroupName</span></span>
<span data-ttu-id="68562-131">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="68562-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="68562-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="68562-132">-ResourceId</span></span>
<span data-ttu-id="68562-133">Identyfikator zasobu usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="68562-133">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="68562-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="68562-134">-Confirm</span></span>
<span data-ttu-id="68562-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68562-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68562-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68562-136">-WhatIf</span></span>
<span data-ttu-id="68562-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68562-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68562-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="68562-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68562-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68562-139">CommonParameters</span></span>
<span data-ttu-id="68562-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68562-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68562-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68562-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68562-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="68562-142">INPUTS</span></span>

### <span data-ttu-id="68562-143">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="68562-143">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>
<span data-ttu-id="68562-144">Parametry: DpsObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="68562-144">Parameters: DpsObject (ByValue)</span></span>

### <span data-ttu-id="68562-145">System. String</span><span class="sxs-lookup"><span data-stu-id="68562-145">System.String</span></span>

## <span data-ttu-id="68562-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="68562-146">OUTPUTS</span></span>

### <span data-ttu-id="68562-147">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="68562-147">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="68562-148">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSIotHubDefinitions</span><span class="sxs-lookup"><span data-stu-id="68562-148">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitions</span></span>

## <span data-ttu-id="68562-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="68562-149">NOTES</span></span>

## <span data-ttu-id="68562-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="68562-150">RELATED LINKS</span></span>
