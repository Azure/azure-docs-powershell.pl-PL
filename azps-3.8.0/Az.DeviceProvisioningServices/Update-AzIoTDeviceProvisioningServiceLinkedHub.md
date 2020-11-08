---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/update-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: cc8d2ec0602213bdbfd50ac89e5199952cea424c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051308"
---
# <span data-ttu-id="0e8e3-101">Update-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="0e8e3-101">Update-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="0e8e3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0e8e3-102">SYNOPSIS</span></span>
<span data-ttu-id="0e8e3-103">Aktualizowanie połączonego Centrum IoT w usłudze dostarczania urządzeń centrum usług Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="0e8e3-103">Update a linked IoT hub in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="0e8e3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0e8e3-104">SYNTAX</span></span>

### <span data-ttu-id="0e8e3-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0e8e3-105">ResourceSet (Default)</span></span>
```
Update-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName] <String> [-AllocationWeight <Int32>] [-ApplyAllocationPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e8e3-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="0e8e3-106">InputObjectSet</span></span>
```
Update-AzIoTDeviceProvisioningServiceLinkedHub [-InputObject] <PSIotHubDefinitionDescription>
 [-AllocationWeight <Int32>] [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e8e3-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="0e8e3-107">ResourceIdSet</span></span>
```
Update-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName] <String>
 [-AllocationWeight <Int32>] [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e8e3-108">Opis</span><span class="sxs-lookup"><span data-stu-id="0e8e3-108">DESCRIPTION</span></span>
<span data-ttu-id="0e8e3-109">Aby uzyskać wprowadzenie do usługi dostarczania urządzeń centrum usług Azure IoT, zobacz https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="0e8e3-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="0e8e3-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0e8e3-110">EXAMPLES</span></span>

### <span data-ttu-id="0e8e3-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0e8e3-111">Example 1</span></span>
```
PS C:\> Update-AzIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub" -AllocationWeight 10 -ApplyAllocationPolicy $true

ResourceGroupName     : myresourcegroup
Name                  : myiotdps
LinkedHubName         : myiothub.azure-devices.net
ConnectionString      : HostName=myiothub.azure-devices.net;SharedAccessKeyName=iothubowner;SharedAccessKey=****
AllocationWeight      : 10
ApplyAllocationPolicy : True
Location              : eastus
```

<span data-ttu-id="0e8e3-112">Aktualizowanie połączonego Centrum IoT "myiothub.azure-devices.net" w usłudze dostarczania urządzeń centrum usług Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="0e8e3-112">Update linked IoT hub "myiothub.azure-devices.net" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="0e8e3-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0e8e3-113">PARAMETERS</span></span>

### <span data-ttu-id="0e8e3-114">-AllocationWeight</span><span class="sxs-lookup"><span data-stu-id="0e8e3-114">-AllocationWeight</span></span>
<span data-ttu-id="0e8e3-115">Waga przydziału Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="0e8e3-115">Allocation weight of the IoT Hub</span></span>

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

### <span data-ttu-id="0e8e3-116">-ApplyAllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="0e8e3-116">-ApplyAllocationPolicy</span></span>
<span data-ttu-id="0e8e3-117">Stosowanie zasad alokacji do centrum IoT</span><span class="sxs-lookup"><span data-stu-id="0e8e3-117">Apply allocation policy to the IoT Hub</span></span>

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

### <span data-ttu-id="0e8e3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e8e3-118">-DefaultProfile</span></span>
<span data-ttu-id="0e8e3-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0e8e3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e8e3-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0e8e3-120">-InputObject</span></span>
<span data-ttu-id="0e8e3-121">Obiekt usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="0e8e3-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="0e8e3-122">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="0e8e3-122">-LinkedHubName</span></span>
<span data-ttu-id="0e8e3-123">Nazwa hosta połączonego Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="0e8e3-123">Host name of linked IoT Hub</span></span>

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

### <span data-ttu-id="0e8e3-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0e8e3-124">-Name</span></span>
<span data-ttu-id="0e8e3-125">Nazwa usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="0e8e3-125">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="0e8e3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e8e3-126">-ResourceGroupName</span></span>
<span data-ttu-id="0e8e3-127">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="0e8e3-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="0e8e3-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0e8e3-128">-ResourceId</span></span>
<span data-ttu-id="0e8e3-129">Identyfikator zasobu usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="0e8e3-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="0e8e3-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0e8e3-130">-Confirm</span></span>
<span data-ttu-id="0e8e3-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0e8e3-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e8e3-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e8e3-132">-WhatIf</span></span>
<span data-ttu-id="0e8e3-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0e8e3-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e8e3-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0e8e3-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e8e3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e8e3-135">CommonParameters</span></span>
<span data-ttu-id="0e8e3-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e8e3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e8e3-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e8e3-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e8e3-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0e8e3-138">INPUTS</span></span>

### <span data-ttu-id="0e8e3-139">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="0e8e3-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="0e8e3-140">System. String</span><span class="sxs-lookup"><span data-stu-id="0e8e3-140">System.String</span></span>

## <span data-ttu-id="0e8e3-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0e8e3-141">OUTPUTS</span></span>

### <span data-ttu-id="0e8e3-142">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="0e8e3-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

## <span data-ttu-id="0e8e3-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0e8e3-143">NOTES</span></span>

## <span data-ttu-id="0e8e3-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0e8e3-144">RELATED LINKS</span></span>
