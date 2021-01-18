---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/new-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: 482acd4f82320bbc14c5bf95c113304a8720019b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98499174"
---
# <span data-ttu-id="3ce77-101">New-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="3ce77-101">New-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="3ce77-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3ce77-102">SYNOPSIS</span></span>
<span data-ttu-id="3ce77-103">Tworzenie usługi dostarczania urządzeń centrum usług Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="3ce77-103">Create an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="3ce77-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3ce77-104">SYNTAX</span></span>

```
New-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-Location <String>]
 [-AllocationPolicy <String>] [-SkuName <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ce77-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3ce77-105">DESCRIPTION</span></span>
<span data-ttu-id="3ce77-106">Aby uzyskać wprowadzenie do usługi dostarczania urządzeń centrum usług Azure IoT, zobacz https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="3ce77-106">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="3ce77-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3ce77-107">EXAMPLES</span></span>

### <span data-ttu-id="3ce77-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3ce77-108">Example 1</span></span>
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

<span data-ttu-id="3ce77-109">Utwórz usługę inicjowania obsługi urządzenia centrum usług Azure IoT z standardową warstwą cenową S1 i znacznikami w regionie grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3ce77-109">Create an Azure IoT Hub device provisioning service with the standard pricing tier S1 and tags, in the region of the resource group.</span></span>

### <span data-ttu-id="3ce77-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="3ce77-110">Example 2</span></span>
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

<span data-ttu-id="3ce77-111">Utwórz usługę inicjowania obsługi urządzenia centrum usług Azure IoT z standardową warstwą cenową S1 w regionie "Wschód".</span><span class="sxs-lookup"><span data-stu-id="3ce77-111">Create an Azure IoT Hub device provisioning service with the standard pricing tier S1, in the 'eastus' region.</span></span>

## <span data-ttu-id="3ce77-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3ce77-112">PARAMETERS</span></span>

### <span data-ttu-id="3ce77-113">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="3ce77-113">-AllocationPolicy</span></span>
<span data-ttu-id="3ce77-114">Zasady alokacji usług dla urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="3ce77-114">IoT Device Provisioning Service Allocation policy</span></span>

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

### <span data-ttu-id="3ce77-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ce77-115">-DefaultProfile</span></span>
<span data-ttu-id="3ce77-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3ce77-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ce77-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="3ce77-117">-Location</span></span>
<span data-ttu-id="3ce77-118">Pozycję</span><span class="sxs-lookup"><span data-stu-id="3ce77-118">Location</span></span>

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

### <span data-ttu-id="3ce77-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3ce77-119">-Name</span></span>
<span data-ttu-id="3ce77-120">Nazwa usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="3ce77-120">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="3ce77-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ce77-121">-ResourceGroupName</span></span>
<span data-ttu-id="3ce77-122">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="3ce77-122">Name of the Resource Group</span></span>

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

### <span data-ttu-id="3ce77-123">-SkuName</span><span class="sxs-lookup"><span data-stu-id="3ce77-123">-SkuName</span></span>
<span data-ttu-id="3ce77-124">Zapas</span><span class="sxs-lookup"><span data-stu-id="3ce77-124">Sku</span></span>

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

### <span data-ttu-id="3ce77-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="3ce77-125">-Tag</span></span>
<span data-ttu-id="3ce77-126">Znaczniki wystąpienia usługi obsługi urządzeń IoT.</span><span class="sxs-lookup"><span data-stu-id="3ce77-126">IoT Device Provisioning Service instance tags.</span></span> <span data-ttu-id="3ce77-127">Zbiór właściwości w postaci par klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="3ce77-127">Property bag in key-value pairs in the form of a hash table.</span></span>

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

### <span data-ttu-id="3ce77-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3ce77-128">-Confirm</span></span>
<span data-ttu-id="3ce77-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ce77-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ce77-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ce77-130">-WhatIf</span></span>
<span data-ttu-id="3ce77-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ce77-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ce77-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3ce77-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ce77-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ce77-133">CommonParameters</span></span>
<span data-ttu-id="3ce77-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ce77-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ce77-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ce77-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ce77-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3ce77-136">INPUTS</span></span>

### <span data-ttu-id="3ce77-137">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="3ce77-137">None</span></span>

## <span data-ttu-id="3ce77-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3ce77-138">OUTPUTS</span></span>

### <span data-ttu-id="3ce77-139">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="3ce77-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="3ce77-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3ce77-140">NOTES</span></span>

## <span data-ttu-id="3ce77-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3ce77-141">RELATED LINKS</span></span>
