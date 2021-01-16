---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: 4701070ae7810b86ff7567f73b39606909d7fa10
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376994"
---
# <span data-ttu-id="3bde7-101">Remove-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="3bde7-101">Remove-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="3bde7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3bde7-102">SYNOPSIS</span></span>
<span data-ttu-id="3bde7-103">Usuwanie usługi dostarczania urządzeń centrum usługi Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="3bde7-103">Delete an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="3bde7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3bde7-104">SYNTAX</span></span>

### <span data-ttu-id="3bde7-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3bde7-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3bde7-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3bde7-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3bde7-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="3bde7-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningService [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3bde7-108">Opis</span><span class="sxs-lookup"><span data-stu-id="3bde7-108">DESCRIPTION</span></span>
<span data-ttu-id="3bde7-109">Aby uzyskać wprowadzenie do usługi dostarczania urządzeń centrum usług Azure IoT, zobacz https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="3bde7-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="3bde7-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3bde7-110">EXAMPLES</span></span>

### <span data-ttu-id="3bde7-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3bde7-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -PassThru

True
```

<span data-ttu-id="3bde7-112">Usuń usługę "myiotdps" urządzenia centrum usług Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="3bde7-112">Delete an Azure IoT Hub device provisioning service 'myiotdps'.</span></span>

### <span data-ttu-id="3bde7-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="3bde7-113">Example 2</span></span>
```
PS C:\> Get-AzIotDps -ResourceGroupName "myresourcegroup" -Name "myiotdps" | Remove-AzIotDps
```

<span data-ttu-id="3bde7-114">Usuwanie usługi "myiotdps" urządzenia centrum usług Azure IoT Hub przy użyciu potoku.</span><span class="sxs-lookup"><span data-stu-id="3bde7-114">Delete an Azure IoT Hub device provisioning service 'myiotdps' using pipeline.</span></span>

## <span data-ttu-id="3bde7-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3bde7-115">PARAMETERS</span></span>

### <span data-ttu-id="3bde7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bde7-116">-DefaultProfile</span></span>
<span data-ttu-id="3bde7-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3bde7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3bde7-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3bde7-118">-InputObject</span></span>
<span data-ttu-id="3bde7-119">Obiekt usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="3bde7-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="3bde7-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3bde7-120">-Name</span></span>
<span data-ttu-id="3bde7-121">Nazwa usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="3bde7-121">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="3bde7-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3bde7-122">-PassThru</span></span>
<span data-ttu-id="3bde7-123">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="3bde7-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="3bde7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3bde7-124">-ResourceGroupName</span></span>
<span data-ttu-id="3bde7-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="3bde7-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="3bde7-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3bde7-126">-ResourceId</span></span>
<span data-ttu-id="3bde7-127">Identyfikator zasobu usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="3bde7-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="3bde7-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3bde7-128">-Confirm</span></span>
<span data-ttu-id="3bde7-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3bde7-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3bde7-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3bde7-130">-WhatIf</span></span>
<span data-ttu-id="3bde7-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3bde7-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3bde7-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3bde7-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3bde7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bde7-133">CommonParameters</span></span>
<span data-ttu-id="3bde7-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3bde7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bde7-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3bde7-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bde7-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3bde7-136">INPUTS</span></span>

### <span data-ttu-id="3bde7-137">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="3bde7-137">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="3bde7-138">System. String</span><span class="sxs-lookup"><span data-stu-id="3bde7-138">System.String</span></span>

## <span data-ttu-id="3bde7-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3bde7-139">OUTPUTS</span></span>

### <span data-ttu-id="3bde7-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3bde7-140">System.Boolean</span></span>

## <span data-ttu-id="3bde7-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3bde7-141">NOTES</span></span>

## <span data-ttu-id="3bde7-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3bde7-142">RELATED LINKS</span></span>
