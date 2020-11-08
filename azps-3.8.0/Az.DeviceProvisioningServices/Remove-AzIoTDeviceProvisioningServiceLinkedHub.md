---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: b4ff0c778eb5185623160f977cdbecbaa0d85994
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050876"
---
# <span data-ttu-id="b6d2f-101">Remove-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="b6d2f-101">Remove-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="b6d2f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b6d2f-102">SYNOPSIS</span></span>
<span data-ttu-id="b6d2f-103">Usuwanie połączonego Centrum IoT w usłudze dostarczania urządzeń centrum usług Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-103">Delete a linked IoT hub in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="b6d2f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b6d2f-104">SYNTAX</span></span>

### <span data-ttu-id="b6d2f-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b6d2f-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b6d2f-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b6d2f-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceLinkedHub [-InputObject] <PSIotHubDefinitionDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6d2f-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b6d2f-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6d2f-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b6d2f-108">DESCRIPTION</span></span>
<span data-ttu-id="b6d2f-109">Aby uzyskać wprowadzenie do usługi dostarczania urządzeń centrum usług Azure IoT, zobacz https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="b6d2f-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="b6d2f-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b6d2f-110">EXAMPLES</span></span>

### <span data-ttu-id="b6d2f-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b6d2f-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub" -PassThru

True
```

<span data-ttu-id="b6d2f-112">Usuń połączone centrum IoT "myiothub" w usłudze dostarczania urządzeń centrum usług Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-112">Delete linked IoT hub "myiothub" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="b6d2f-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="b6d2f-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDpsHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub" | Remove-AzIoTDpsHub
```

<span data-ttu-id="b6d2f-114">Usuń połączone centrum IoT "myiothub" w usłudze dostarczania urządzeń centrum usług Azure IoT za pomocą potoku.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-114">Delete linked IoT hub "myiothub" in an Azure IoT Hub device provisioning service using pipeline.</span></span>

## <span data-ttu-id="b6d2f-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b6d2f-115">PARAMETERS</span></span>

### <span data-ttu-id="b6d2f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6d2f-116">-DefaultProfile</span></span>
<span data-ttu-id="b6d2f-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6d2f-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b6d2f-118">-InputObject</span></span>
<span data-ttu-id="b6d2f-119">Obiekt usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="b6d2f-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="b6d2f-120">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="b6d2f-120">-LinkedHubName</span></span>
<span data-ttu-id="b6d2f-121">Nazwa hosta połączonego Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="b6d2f-121">Host name of linked IoT Hub</span></span>

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

### <span data-ttu-id="b6d2f-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b6d2f-122">-Name</span></span>
<span data-ttu-id="b6d2f-123">Nazwa usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="b6d2f-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="b6d2f-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b6d2f-124">-PassThru</span></span>
<span data-ttu-id="b6d2f-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="b6d2f-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="b6d2f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6d2f-126">-ResourceGroupName</span></span>
<span data-ttu-id="b6d2f-127">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="b6d2f-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="b6d2f-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b6d2f-128">-ResourceId</span></span>
<span data-ttu-id="b6d2f-129">Identyfikator zasobu usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="b6d2f-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="b6d2f-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b6d2f-130">-Confirm</span></span>
<span data-ttu-id="b6d2f-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6d2f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6d2f-132">-WhatIf</span></span>
<span data-ttu-id="b6d2f-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6d2f-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6d2f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6d2f-135">CommonParameters</span></span>
<span data-ttu-id="b6d2f-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6d2f-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6d2f-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6d2f-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b6d2f-138">INPUTS</span></span>

### <span data-ttu-id="b6d2f-139">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="b6d2f-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="b6d2f-140">System. String</span><span class="sxs-lookup"><span data-stu-id="b6d2f-140">System.String</span></span>

## <span data-ttu-id="b6d2f-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b6d2f-141">OUTPUTS</span></span>

### <span data-ttu-id="b6d2f-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b6d2f-142">System.Boolean</span></span>

## <span data-ttu-id="b6d2f-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b6d2f-143">NOTES</span></span>

## <span data-ttu-id="b6d2f-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b6d2f-144">RELATED LINKS</span></span>
