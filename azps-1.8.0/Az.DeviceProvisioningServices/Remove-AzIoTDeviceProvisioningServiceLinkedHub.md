---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: ae7335c6430001affa76894dac6334036d1f04d4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709877"
---
# <span data-ttu-id="db920-101">Remove-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="db920-101">Remove-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="db920-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="db920-102">SYNOPSIS</span></span>
<span data-ttu-id="db920-103">Usuwanie połączonego Centrum IoT w usłudze dostarczania urządzeń centrum usług Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="db920-103">Delete a linked IoT hub in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="db920-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="db920-104">SYNTAX</span></span>

### <span data-ttu-id="db920-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="db920-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="db920-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="db920-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceLinkedHub [-InputObject] <PSIotHubDefinitionDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db920-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="db920-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db920-108">Opis</span><span class="sxs-lookup"><span data-stu-id="db920-108">DESCRIPTION</span></span>
<span data-ttu-id="db920-109">Aby uzyskać wprowadzenie do usługi dostarczania urządzeń centrum usług Azure IoT, zobacz https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="db920-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="db920-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="db920-110">EXAMPLES</span></span>

### <span data-ttu-id="db920-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="db920-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub" -PassThru

True
```

<span data-ttu-id="db920-112">Usuń połączone centrum IoT "myiothub" w usłudze dostarczania urządzeń centrum usług Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="db920-112">Delete linked IoT hub "myiothub" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="db920-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="db920-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDpsHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub" | Remove-AzIoTDpsHub
```

<span data-ttu-id="db920-114">Usuń połączone centrum IoT "myiothub" w usłudze dostarczania urządzeń centrum usług Azure IoT za pomocą potoku.</span><span class="sxs-lookup"><span data-stu-id="db920-114">Delete linked IoT hub "myiothub" in an Azure IoT Hub device provisioning service using pipeline.</span></span>

## <span data-ttu-id="db920-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="db920-115">PARAMETERS</span></span>

### <span data-ttu-id="db920-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db920-116">-DefaultProfile</span></span>
<span data-ttu-id="db920-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="db920-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db920-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="db920-118">-InputObject</span></span>
<span data-ttu-id="db920-119">Obiekt usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="db920-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="db920-120">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="db920-120">-LinkedHubName</span></span>
<span data-ttu-id="db920-121">Nazwa hosta połączonego Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="db920-121">Host name of linked IoT Hub</span></span>

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

### <span data-ttu-id="db920-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="db920-122">-Name</span></span>
<span data-ttu-id="db920-123">Nazwa usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="db920-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="db920-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="db920-124">-PassThru</span></span>
<span data-ttu-id="db920-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="db920-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="db920-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db920-126">-ResourceGroupName</span></span>
<span data-ttu-id="db920-127">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="db920-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="db920-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="db920-128">-ResourceId</span></span>
<span data-ttu-id="db920-129">Identyfikator zasobu usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="db920-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="db920-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="db920-130">-Confirm</span></span>
<span data-ttu-id="db920-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db920-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db920-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db920-132">-WhatIf</span></span>
<span data-ttu-id="db920-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db920-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db920-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="db920-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db920-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db920-135">CommonParameters</span></span>
<span data-ttu-id="db920-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db920-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db920-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db920-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db920-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="db920-138">INPUTS</span></span>

### <span data-ttu-id="db920-139">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="db920-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="db920-140">System. String</span><span class="sxs-lookup"><span data-stu-id="db920-140">System.String</span></span>

## <span data-ttu-id="db920-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="db920-141">OUTPUTS</span></span>

### <span data-ttu-id="db920-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="db920-142">System.Boolean</span></span>

## <span data-ttu-id="db920-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="db920-143">NOTES</span></span>

## <span data-ttu-id="db920-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="db920-144">RELATED LINKS</span></span>
