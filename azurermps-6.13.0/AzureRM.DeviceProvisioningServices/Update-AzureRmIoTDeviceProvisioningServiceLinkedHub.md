---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Update-AzureRmIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Update-AzureRmIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: b3cd05b286ddfef69228b8aae12e222e5fffd4d0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545367"
---
# <span data-ttu-id="3df0b-101">Update-AzureRmIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="3df0b-101">Update-AzureRmIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="3df0b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3df0b-102">SYNOPSIS</span></span>
<span data-ttu-id="3df0b-103">Aktualizowanie połączonego Centrum IoT w usłudze dostarczania urządzeń centrum usług Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="3df0b-103">Update a linked IoT hub in an Azure IoT Hub device provisioning service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3df0b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3df0b-104">SYNTAX</span></span>

### <span data-ttu-id="3df0b-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3df0b-105">ResourceSet (Default)</span></span>
```
Update-AzureRmIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName] <String> [-AllocationWeight <Int32>] [-ApplyAllocationPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3df0b-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3df0b-106">InputObjectSet</span></span>
```
Update-AzureRmIoTDeviceProvisioningServiceLinkedHub [-InputObject] <PSIotHubDefinitionDescription>
 [-AllocationWeight <Int32>] [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3df0b-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="3df0b-107">ResourceIdSet</span></span>
```
Update-AzureRmIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName] <String>
 [-AllocationWeight <Int32>] [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3df0b-108">Opis</span><span class="sxs-lookup"><span data-stu-id="3df0b-108">DESCRIPTION</span></span>
<span data-ttu-id="3df0b-109">Aby uzyskać wprowadzenie do usługi dostarczania urządzeń centrum usług Azure IoT, zobacz https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="3df0b-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="3df0b-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3df0b-110">EXAMPLES</span></span>

### <span data-ttu-id="3df0b-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3df0b-111">Example 1</span></span>
```
PS C:\> Update-AzureRmIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub" -AllocationWeight 10 -ApplyAllocationPolicy $true

ResourceGroupName     : myresourcegroup
Name                  : myiotdps
LinkedHubName         : myiothub.azure-devices.net
ConnectionString      : HostName=myiothub.azure-devices.net;SharedAccessKeyName=iothubowner;SharedAccessKey=****
AllocationWeight      : 10
ApplyAllocationPolicy : True
Location              : eastus
```

<span data-ttu-id="3df0b-112">Aktualizowanie połączonego Centrum IoT "myiothub.azure-devices.net" w usłudze dostarczania urządzeń centrum usług Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="3df0b-112">Update linked IoT hub "myiothub.azure-devices.net" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="3df0b-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3df0b-113">PARAMETERS</span></span>

### <span data-ttu-id="3df0b-114">-AllocationWeight</span><span class="sxs-lookup"><span data-stu-id="3df0b-114">-AllocationWeight</span></span>
<span data-ttu-id="3df0b-115">Waga przydziału Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="3df0b-115">Allocation weight of the IoT Hub</span></span>

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

### <span data-ttu-id="3df0b-116">-ApplyAllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="3df0b-116">-ApplyAllocationPolicy</span></span>
<span data-ttu-id="3df0b-117">Stosowanie zasad alokacji do centrum IoT</span><span class="sxs-lookup"><span data-stu-id="3df0b-117">Apply allocation policy to the IoT Hub</span></span>

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

### <span data-ttu-id="3df0b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3df0b-118">-DefaultProfile</span></span>
<span data-ttu-id="3df0b-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3df0b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3df0b-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3df0b-120">-InputObject</span></span>
<span data-ttu-id="3df0b-121">Obiekt usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="3df0b-121">IoT Device Provisioning Service Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3df0b-122">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="3df0b-122">-LinkedHubName</span></span>
<span data-ttu-id="3df0b-123">Nazwa hosta połączonego Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="3df0b-123">Host name of linked IoT Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet, ResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3df0b-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3df0b-124">-Name</span></span>
<span data-ttu-id="3df0b-125">Nazwa usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="3df0b-125">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="3df0b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3df0b-126">-ResourceGroupName</span></span>
<span data-ttu-id="3df0b-127">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="3df0b-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="3df0b-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3df0b-128">-ResourceId</span></span>
<span data-ttu-id="3df0b-129">Identyfikator zasobu usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="3df0b-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="3df0b-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3df0b-130">-Confirm</span></span>
<span data-ttu-id="3df0b-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3df0b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3df0b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3df0b-132">-WhatIf</span></span>
<span data-ttu-id="3df0b-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3df0b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3df0b-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3df0b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3df0b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3df0b-135">CommonParameters</span></span>
<span data-ttu-id="3df0b-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3df0b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3df0b-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3df0b-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3df0b-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3df0b-138">INPUTS</span></span>

### <span data-ttu-id="3df0b-139">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="3df0b-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>
<span data-ttu-id="3df0b-140">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3df0b-140">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="3df0b-141">System. String</span><span class="sxs-lookup"><span data-stu-id="3df0b-141">System.String</span></span>

## <span data-ttu-id="3df0b-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3df0b-142">OUTPUTS</span></span>

### <span data-ttu-id="3df0b-143">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="3df0b-143">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

## <span data-ttu-id="3df0b-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3df0b-144">NOTES</span></span>

## <span data-ttu-id="3df0b-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3df0b-145">RELATED LINKS</span></span>
