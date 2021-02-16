---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: 4701070ae7810b86ff7567f73b39606909d7fa10
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243738"
---
# <span data-ttu-id="d14dc-101">Remove-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="d14dc-101">Remove-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="d14dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d14dc-102">SYNOPSIS</span></span>
<span data-ttu-id="d14dc-103">Usuń usługę inicjowania obsługi urządzeń w centrum Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="d14dc-103">Delete an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="d14dc-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d14dc-104">SYNTAX</span></span>

### <span data-ttu-id="d14dc-105">ResourceSet (Default)</span><span class="sxs-lookup"><span data-stu-id="d14dc-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d14dc-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d14dc-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d14dc-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d14dc-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningService [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d14dc-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="d14dc-108">DESCRIPTION</span></span>
<span data-ttu-id="d14dc-109">Aby uzyskać wprowadzenie do usługi inicjowania obsługi urządzeń w centrum IoT Azure, https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps zobacz.</span><span class="sxs-lookup"><span data-stu-id="d14dc-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="d14dc-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d14dc-110">EXAMPLES</span></span>

### <span data-ttu-id="d14dc-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d14dc-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -PassThru

True
```

<span data-ttu-id="d14dc-112">Usuń usługę inicjowania obsługi urządzeń w centrum IoT Hub Azure , "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="d14dc-112">Delete an Azure IoT Hub device provisioning service 'myiotdps'.</span></span>

### <span data-ttu-id="d14dc-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="d14dc-113">Example 2</span></span>
```
PS C:\> Get-AzIotDps -ResourceGroupName "myresourcegroup" -Name "myiotdps" | Remove-AzIotDps
```

<span data-ttu-id="d14dc-114">Usuń "mojeiotdps" usługi inicjowania obsługi urządzeń w centrum Azure IoT Hub przy użyciu potoku.</span><span class="sxs-lookup"><span data-stu-id="d14dc-114">Delete an Azure IoT Hub device provisioning service 'myiotdps' using pipeline.</span></span>

## <span data-ttu-id="d14dc-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d14dc-115">PARAMETERS</span></span>

### <span data-ttu-id="d14dc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d14dc-116">-DefaultProfile</span></span>
<span data-ttu-id="d14dc-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d14dc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d14dc-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d14dc-118">-InputObject</span></span>
<span data-ttu-id="d14dc-119">Obiekt usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="d14dc-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="d14dc-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d14dc-120">-Name</span></span>
<span data-ttu-id="d14dc-121">Nazwa usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="d14dc-121">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="d14dc-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d14dc-122">-PassThru</span></span>
<span data-ttu-id="d14dc-123">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="d14dc-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="d14dc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d14dc-124">-ResourceGroupName</span></span>
<span data-ttu-id="d14dc-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="d14dc-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="d14dc-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d14dc-126">-ResourceId</span></span>
<span data-ttu-id="d14dc-127">Identyfikator zasobu usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="d14dc-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="d14dc-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d14dc-128">-Confirm</span></span>
<span data-ttu-id="d14dc-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d14dc-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d14dc-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d14dc-130">-WhatIf</span></span>
<span data-ttu-id="d14dc-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d14dc-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d14dc-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d14dc-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d14dc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d14dc-133">CommonParameters</span></span>
<span data-ttu-id="d14dc-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d14dc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d14dc-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d14dc-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d14dc-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d14dc-136">INPUTS</span></span>

### <span data-ttu-id="d14dc-137">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="d14dc-137">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="d14dc-138">System.String</span><span class="sxs-lookup"><span data-stu-id="d14dc-138">System.String</span></span>

## <span data-ttu-id="d14dc-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d14dc-139">OUTPUTS</span></span>

### <span data-ttu-id="d14dc-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d14dc-140">System.Boolean</span></span>

## <span data-ttu-id="d14dc-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d14dc-141">NOTES</span></span>

## <span data-ttu-id="d14dc-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d14dc-142">RELATED LINKS</span></span>
