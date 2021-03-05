---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/new-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: bb6094644b9f2cbd831aa8d64a142d5888a5bcc4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013649"
---
# <span data-ttu-id="b0aa1-101">New-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="b0aa1-101">New-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="b0aa1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0aa1-102">SYNOPSIS</span></span>
<span data-ttu-id="b0aa1-103">Utwórz usługę inicjowania obsługi urządzeń w Centrum IoT Azure.</span><span class="sxs-lookup"><span data-stu-id="b0aa1-103">Create an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="b0aa1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b0aa1-104">SYNTAX</span></span>

```
New-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-Location <String>]
 [-AllocationPolicy <String>] [-SkuName <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0aa1-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="b0aa1-105">DESCRIPTION</span></span>
<span data-ttu-id="b0aa1-106">Aby uzyskać wprowadzenie do usługi inicjowania obsługi urządzeń w centrum IoT Azure, https://docs.microsoft.com/azure/iot-dps/about-iot-dps zobacz.</span><span class="sxs-lookup"><span data-stu-id="b0aa1-106">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="b0aa1-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b0aa1-107">EXAMPLES</span></span>

### <span data-ttu-id="b0aa1-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b0aa1-108">Example 1</span></span>
```
PS C:\> $tags = @{}
PS C:\> $tags.Add('key1','value1')
PS C:\> New-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -Tag $tags

ResourceGroupName           : myresourcegroup
Name                        : myiotdps
Location                    : westus
Type                        : Microsoft.Devices/provisioningServices
ServiceOperationsHostName   : myiotdps.azure-devices-provisioning.net
IotHubs                     : 0
State                       : Active
AllocationPolicy            : Hashed
Tags                        : {[key1, value1]}
SkuName                     : S1
SkuTier                     : Standard
Etag                        : AAAAAAAT52k=
```

<span data-ttu-id="b0aa1-109">Utwórz usługę obsługi administracyjnej urządzeń centrum IoT Azure przy użyciu standardowej warstwy cenowej S1 i tagów w regionie grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b0aa1-109">Create an Azure IoT Hub device provisioning service with the standard pricing tier S1 and tags, in the region of the resource group.</span></span>

### <span data-ttu-id="b0aa1-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="b0aa1-110">Example 2</span></span>
```
PS C:\> New-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -Location "eastus"

ResourceGroupName           : myresourcegroup
Name                        : myiotdps
Location                    : eastus
Type                        : Microsoft.Devices/provisioningServices
ServiceOperationsHostName   : myiotdps.azure-devices-provisioning.net
IotHubs                     : 0
State                       : Active
AllocationPolicy            : Hashed
Tags                        : {}
SkuName                     : S1
SkuTier                     : Standard
Etag                        : AAAAAAAPoOk=
```

<span data-ttu-id="b0aa1-111">Utwórz usługę inicjowania obsługi urządzeń w centrum IoT Azure za pomocą standardowej warstwy cenowej S1 w regionie "eastus".</span><span class="sxs-lookup"><span data-stu-id="b0aa1-111">Create an Azure IoT Hub device provisioning service with the standard pricing tier S1, in the 'eastus' region.</span></span>

## <span data-ttu-id="b0aa1-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b0aa1-112">PARAMETERS</span></span>

### <span data-ttu-id="b0aa1-113">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="b0aa1-113">-AllocationPolicy</span></span>
<span data-ttu-id="b0aa1-114">Zasady alokacji usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="b0aa1-114">IoT Device Provisioning Service Allocation policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Hashed, GeoLatency, Static

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0aa1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0aa1-115">-DefaultProfile</span></span>
<span data-ttu-id="b0aa1-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b0aa1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0aa1-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="b0aa1-117">-Location</span></span>
<span data-ttu-id="b0aa1-118">Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="b0aa1-118">Location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0aa1-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b0aa1-119">-Name</span></span>
<span data-ttu-id="b0aa1-120">Nazwa usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="b0aa1-120">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="b0aa1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0aa1-121">-ResourceGroupName</span></span>
<span data-ttu-id="b0aa1-122">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="b0aa1-122">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0aa1-123">-SKUName</span><span class="sxs-lookup"><span data-stu-id="b0aa1-123">-SkuName</span></span>
<span data-ttu-id="b0aa1-124">SKU</span><span class="sxs-lookup"><span data-stu-id="b0aa1-124">Sku</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: S1

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0aa1-125">— Tag</span><span class="sxs-lookup"><span data-stu-id="b0aa1-125">-Tag</span></span>
<span data-ttu-id="b0aa1-126">Tagi wystąpienia usługi inicjowania obsługi urządzeń IoT.</span><span class="sxs-lookup"><span data-stu-id="b0aa1-126">IoT Device Provisioning Service instance tags.</span></span> <span data-ttu-id="b0aa1-127">Work property bag in key-value pairs in the form of a hash table.</span><span class="sxs-lookup"><span data-stu-id="b0aa1-127">Property bag in key-value pairs in the form of a hash table.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0aa1-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b0aa1-128">-Confirm</span></span>
<span data-ttu-id="b0aa1-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b0aa1-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0aa1-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0aa1-130">-WhatIf</span></span>
<span data-ttu-id="b0aa1-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0aa1-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0aa1-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b0aa1-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0aa1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0aa1-133">CommonParameters</span></span>
<span data-ttu-id="b0aa1-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0aa1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0aa1-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0aa1-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0aa1-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b0aa1-136">INPUTS</span></span>

### <span data-ttu-id="b0aa1-137">Brak</span><span class="sxs-lookup"><span data-stu-id="b0aa1-137">None</span></span>

## <span data-ttu-id="b0aa1-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b0aa1-138">OUTPUTS</span></span>

### <span data-ttu-id="b0aa1-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="b0aa1-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="b0aa1-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b0aa1-140">NOTES</span></span>

## <span data-ttu-id="b0aa1-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b0aa1-141">RELATED LINKS</span></span>
