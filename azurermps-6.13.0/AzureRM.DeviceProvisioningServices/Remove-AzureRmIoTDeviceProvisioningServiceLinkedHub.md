---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Remove-AzureRmIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Remove-AzureRmIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: f50c0955d56b42c341b6a1a6b64b1993ee66175e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719129"
---
# <span data-ttu-id="6ad32-101">Remove-AzureRmIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="6ad32-101">Remove-AzureRmIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="6ad32-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6ad32-102">SYNOPSIS</span></span>
<span data-ttu-id="6ad32-103">Usuwanie połączonego Centrum IoT w usłudze dostarczania urządzeń centrum usług Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="6ad32-103">Delete a linked IoT hub in an Azure IoT Hub device provisioning service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ad32-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6ad32-104">SYNTAX</span></span>

### <span data-ttu-id="6ad32-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6ad32-105">ResourceSet (Default)</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6ad32-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="6ad32-106">InputObjectSet</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceLinkedHub [-InputObject] <PSIotHubDefinitionDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ad32-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="6ad32-107">ResourceIdSet</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ad32-108">Opis</span><span class="sxs-lookup"><span data-stu-id="6ad32-108">DESCRIPTION</span></span>
<span data-ttu-id="6ad32-109">Aby uzyskać wprowadzenie do usługi dostarczania urządzeń centrum usług Azure IoT, zobacz https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="6ad32-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="6ad32-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6ad32-110">EXAMPLES</span></span>

### <span data-ttu-id="6ad32-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6ad32-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub" -PassThru

True
```

<span data-ttu-id="6ad32-112">Usuń połączone centrum IoT "myiothub" w usłudze dostarczania urządzeń centrum usług Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="6ad32-112">Delete linked IoT hub "myiothub" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="6ad32-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="6ad32-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIoTDpsHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub" | Remove-AzureRmIoTDpsHub
```

<span data-ttu-id="6ad32-114">Usuń połączone centrum IoT "myiothub" w usłudze dostarczania urządzeń centrum usług Azure IoT za pomocą potoku.</span><span class="sxs-lookup"><span data-stu-id="6ad32-114">Delete linked IoT hub "myiothub" in an Azure IoT Hub device provisioning service using pipeline.</span></span>

## <span data-ttu-id="6ad32-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6ad32-115">PARAMETERS</span></span>

### <span data-ttu-id="6ad32-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ad32-116">-DefaultProfile</span></span>
<span data-ttu-id="6ad32-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6ad32-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ad32-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6ad32-118">-InputObject</span></span>
<span data-ttu-id="6ad32-119">Obiekt usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="6ad32-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="6ad32-120">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="6ad32-120">-LinkedHubName</span></span>
<span data-ttu-id="6ad32-121">Nazwa hosta połączonego Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="6ad32-121">Host name of linked IoT Hub</span></span>

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

### <span data-ttu-id="6ad32-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6ad32-122">-Name</span></span>
<span data-ttu-id="6ad32-123">Nazwa usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="6ad32-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="6ad32-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6ad32-124">-PassThru</span></span>
<span data-ttu-id="6ad32-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="6ad32-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="6ad32-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ad32-126">-ResourceGroupName</span></span>
<span data-ttu-id="6ad32-127">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="6ad32-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="6ad32-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6ad32-128">-ResourceId</span></span>
<span data-ttu-id="6ad32-129">Identyfikator zasobu usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="6ad32-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="6ad32-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6ad32-130">-Confirm</span></span>
<span data-ttu-id="6ad32-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ad32-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ad32-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ad32-132">-WhatIf</span></span>
<span data-ttu-id="6ad32-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ad32-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ad32-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6ad32-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ad32-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ad32-135">CommonParameters</span></span>
<span data-ttu-id="6ad32-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ad32-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ad32-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ad32-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ad32-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6ad32-138">INPUTS</span></span>

### <span data-ttu-id="6ad32-139">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="6ad32-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>
<span data-ttu-id="6ad32-140">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6ad32-140">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="6ad32-141">System. String</span><span class="sxs-lookup"><span data-stu-id="6ad32-141">System.String</span></span>

## <span data-ttu-id="6ad32-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6ad32-142">OUTPUTS</span></span>

### <span data-ttu-id="6ad32-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6ad32-143">System.Boolean</span></span>

## <span data-ttu-id="6ad32-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6ad32-144">NOTES</span></span>

## <span data-ttu-id="6ad32-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6ad32-145">RELATED LINKS</span></span>
