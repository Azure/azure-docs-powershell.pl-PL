---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/update-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: cc8d2ec0602213bdbfd50ac89e5199952cea424c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194451"
---
# <span data-ttu-id="634c4-101">Update-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="634c4-101">Update-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="634c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="634c4-102">SYNOPSIS</span></span>
<span data-ttu-id="634c4-103">Zaktualizuj połączone centrum IoT w usłudze inicjowania obsługi administracyjnej urządzeń w centrum Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="634c4-103">Update a linked IoT hub in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="634c4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="634c4-104">SYNTAX</span></span>

### <span data-ttu-id="634c4-105">Zestaw zasobów (domyślny)</span><span class="sxs-lookup"><span data-stu-id="634c4-105">ResourceSet (Default)</span></span>
```
Update-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName] <String> [-AllocationWeight <Int32>] [-ApplyAllocationPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="634c4-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="634c4-106">InputObjectSet</span></span>
```
Update-AzIoTDeviceProvisioningServiceLinkedHub [-InputObject] <PSIotHubDefinitionDescription>
 [-AllocationWeight <Int32>] [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="634c4-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="634c4-107">ResourceIdSet</span></span>
```
Update-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName] <String>
 [-AllocationWeight <Int32>] [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="634c4-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="634c4-108">DESCRIPTION</span></span>
<span data-ttu-id="634c4-109">Aby uzyskać wprowadzenie do usługi inicjowania obsługi urządzeń w centrum IoT Azure, zobacz https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="634c4-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="634c4-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="634c4-110">EXAMPLES</span></span>

### <span data-ttu-id="634c4-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="634c4-111">Example 1</span></span>
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

<span data-ttu-id="634c4-112">Zaktualizuj połączone centrum IoT "myiothub.azure-devices.net" w usłudze inicjowania obsługi urządzeń w Centrum IoT Azure.</span><span class="sxs-lookup"><span data-stu-id="634c4-112">Update linked IoT hub "myiothub.azure-devices.net" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="634c4-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="634c4-113">PARAMETERS</span></span>

### <span data-ttu-id="634c4-114">- AllocationWeight</span><span class="sxs-lookup"><span data-stu-id="634c4-114">-AllocationWeight</span></span>
<span data-ttu-id="634c4-115">Waga alokacji Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="634c4-115">Allocation weight of the IoT Hub</span></span>

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

### <span data-ttu-id="634c4-116">-ApplyAllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="634c4-116">-ApplyAllocationPolicy</span></span>
<span data-ttu-id="634c4-117">Stosowanie zasad alokacji do Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="634c4-117">Apply allocation policy to the IoT Hub</span></span>

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

### <span data-ttu-id="634c4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="634c4-118">-DefaultProfile</span></span>
<span data-ttu-id="634c4-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="634c4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="634c4-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="634c4-120">-InputObject</span></span>
<span data-ttu-id="634c4-121">Obiekt usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="634c4-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="634c4-122">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="634c4-122">-LinkedHubName</span></span>
<span data-ttu-id="634c4-123">Nazwa hosta połączonego centrum IoT</span><span class="sxs-lookup"><span data-stu-id="634c4-123">Host name of linked IoT Hub</span></span>

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

### <span data-ttu-id="634c4-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="634c4-124">-Name</span></span>
<span data-ttu-id="634c4-125">Nazwa usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="634c4-125">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="634c4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="634c4-126">-ResourceGroupName</span></span>
<span data-ttu-id="634c4-127">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="634c4-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="634c4-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="634c4-128">-ResourceId</span></span>
<span data-ttu-id="634c4-129">Identyfikator zasobu usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="634c4-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="634c4-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="634c4-130">-Confirm</span></span>
<span data-ttu-id="634c4-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="634c4-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="634c4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="634c4-132">-WhatIf</span></span>
<span data-ttu-id="634c4-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="634c4-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="634c4-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="634c4-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="634c4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="634c4-135">CommonParameters</span></span>
<span data-ttu-id="634c4-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="634c4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="634c4-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="634c4-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="634c4-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="634c4-138">INPUTS</span></span>

### <span data-ttu-id="634c4-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="634c4-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="634c4-140">System.String</span><span class="sxs-lookup"><span data-stu-id="634c4-140">System.String</span></span>

## <span data-ttu-id="634c4-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="634c4-141">OUTPUTS</span></span>

### <span data-ttu-id="634c4-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="634c4-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

## <span data-ttu-id="634c4-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="634c4-143">NOTES</span></span>

## <span data-ttu-id="634c4-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="634c4-144">RELATED LINKS</span></span>
