---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: b4ff0c778eb5185623160f977cdbecbaa0d85994
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100237960"
---
# <span data-ttu-id="40eb4-101">Remove-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="40eb4-101">Remove-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="40eb4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40eb4-102">SYNOPSIS</span></span>
<span data-ttu-id="40eb4-103">Usuń połączone centrum IoT w usłudze inicjowania obsługi administracyjnej urządzeń w centrum Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="40eb4-103">Delete a linked IoT hub in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="40eb4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="40eb4-104">SYNTAX</span></span>

### <span data-ttu-id="40eb4-105">Zestaw zasobów (domyślny)</span><span class="sxs-lookup"><span data-stu-id="40eb4-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="40eb4-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="40eb4-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceLinkedHub [-InputObject] <PSIotHubDefinitionDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40eb4-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="40eb4-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40eb4-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="40eb4-108">DESCRIPTION</span></span>
<span data-ttu-id="40eb4-109">Aby uzyskać wprowadzenie do usługi inicjowania obsługi urządzeń w centrum IoT Azure, https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps zobacz.</span><span class="sxs-lookup"><span data-stu-id="40eb4-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="40eb4-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="40eb4-110">EXAMPLES</span></span>

### <span data-ttu-id="40eb4-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="40eb4-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub" -PassThru

True
```

<span data-ttu-id="40eb4-112">Usuń połączone centrum IoT "myiothub" w usłudze inicjowania obsługi urządzeń w centrum Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="40eb4-112">Delete linked IoT hub "myiothub" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="40eb4-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="40eb4-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDpsHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub" | Remove-AzIoTDpsHub
```

<span data-ttu-id="40eb4-114">Usuń połączone centrum IoT "myiothub" w usłudze inicjowania obsługi urządzeń w usłudze Azure IoT Hub przy użyciu potoku.</span><span class="sxs-lookup"><span data-stu-id="40eb4-114">Delete linked IoT hub "myiothub" in an Azure IoT Hub device provisioning service using pipeline.</span></span>

## <span data-ttu-id="40eb4-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="40eb4-115">PARAMETERS</span></span>

### <span data-ttu-id="40eb4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40eb4-116">-DefaultProfile</span></span>
<span data-ttu-id="40eb4-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="40eb4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40eb4-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="40eb4-118">-InputObject</span></span>
<span data-ttu-id="40eb4-119">Obiekt usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="40eb4-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="40eb4-120">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="40eb4-120">-LinkedHubName</span></span>
<span data-ttu-id="40eb4-121">Nazwa hosta połączonego centrum IoT</span><span class="sxs-lookup"><span data-stu-id="40eb4-121">Host name of linked IoT Hub</span></span>

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

### <span data-ttu-id="40eb4-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="40eb4-122">-Name</span></span>
<span data-ttu-id="40eb4-123">Nazwa usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="40eb4-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="40eb4-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="40eb4-124">-PassThru</span></span>
<span data-ttu-id="40eb4-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="40eb4-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="40eb4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40eb4-126">-ResourceGroupName</span></span>
<span data-ttu-id="40eb4-127">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="40eb4-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="40eb4-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="40eb4-128">-ResourceId</span></span>
<span data-ttu-id="40eb4-129">Identyfikator zasobu usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="40eb4-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="40eb4-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="40eb4-130">-Confirm</span></span>
<span data-ttu-id="40eb4-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="40eb4-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40eb4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40eb4-132">-WhatIf</span></span>
<span data-ttu-id="40eb4-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40eb4-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40eb4-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="40eb4-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40eb4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40eb4-135">CommonParameters</span></span>
<span data-ttu-id="40eb4-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40eb4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40eb4-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40eb4-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40eb4-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="40eb4-138">INPUTS</span></span>

### <span data-ttu-id="40eb4-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="40eb4-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="40eb4-140">System.String</span><span class="sxs-lookup"><span data-stu-id="40eb4-140">System.String</span></span>

## <span data-ttu-id="40eb4-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="40eb4-141">OUTPUTS</span></span>

### <span data-ttu-id="40eb4-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="40eb4-142">System.Boolean</span></span>

## <span data-ttu-id="40eb4-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="40eb4-143">NOTES</span></span>

## <span data-ttu-id="40eb4-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="40eb4-144">RELATED LINKS</span></span>
