---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/new-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: 3102cafabecb5df8daea15a40eb179405c6c0ea8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062243"
---
# <span data-ttu-id="93396-101">New-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="93396-101">New-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="93396-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="93396-102">SYNOPSIS</span></span>
<span data-ttu-id="93396-103">Tworzenie usługi dostarczania urządzeń centrum usług Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="93396-103">Create an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="93396-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="93396-104">SYNTAX</span></span>

```
New-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-Location <String>]
 [-AllocationPolicy <String>] [-SkuName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93396-105">Opis</span><span class="sxs-lookup"><span data-stu-id="93396-105">DESCRIPTION</span></span>
<span data-ttu-id="93396-106">Aby uzyskać wprowadzenie do usługi dostarczania urządzeń centrum usług Azure IoT, zobacz https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="93396-106">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="93396-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="93396-107">EXAMPLES</span></span>

### <span data-ttu-id="93396-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="93396-108">Example 1</span></span>
```
PS C:\> New-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps"

ResourceGroupName           : myresourcegroup
Name                        : myiotdps
Location                    : westus
Type                        : Microsoft.Devices/provisioningServices
ServiceOperationsHostName   : myiotdps.azure-devices-provisioning.net
IotHubs                     : 0
State                       : Active
AllocationPolicy            : Hashed
Tags                        : {}
SkuName                     : S1
SkuTier                     : Standard
Etag                        : AAAAAAAT52k=
```

<span data-ttu-id="93396-109">Utwórz usługę inicjowania obsługi urządzenia centrum usług Azure IoT z standardową warstwą cenową S1 w regionie grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="93396-109">Create an Azure IoT Hub device provisioning service with the standard pricing tier S1, in the region of the resource group.</span></span>

### <span data-ttu-id="93396-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="93396-110">Example 2</span></span>
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

<span data-ttu-id="93396-111">Utwórz usługę inicjowania obsługi urządzenia centrum usług Azure IoT z standardową warstwą cenową S1 w regionie "Wschód".</span><span class="sxs-lookup"><span data-stu-id="93396-111">Create an Azure IoT Hub device provisioning service with the standard pricing tier S1, in the 'eastus' region.</span></span>

## <span data-ttu-id="93396-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="93396-112">PARAMETERS</span></span>

### <span data-ttu-id="93396-113">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="93396-113">-AllocationPolicy</span></span>
<span data-ttu-id="93396-114">Zasady alokacji usług dla urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="93396-114">IoT Device Provisioning Service Allocation policy</span></span>

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

### <span data-ttu-id="93396-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93396-115">-DefaultProfile</span></span>
<span data-ttu-id="93396-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="93396-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93396-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="93396-117">-Location</span></span>
<span data-ttu-id="93396-118">Pozycję</span><span class="sxs-lookup"><span data-stu-id="93396-118">Location</span></span>

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

### <span data-ttu-id="93396-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="93396-119">-Name</span></span>
<span data-ttu-id="93396-120">Nazwa usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="93396-120">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="93396-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93396-121">-ResourceGroupName</span></span>
<span data-ttu-id="93396-122">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="93396-122">Name of the Resource Group</span></span>

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

### <span data-ttu-id="93396-123">-SkuName</span><span class="sxs-lookup"><span data-stu-id="93396-123">-SkuName</span></span>
<span data-ttu-id="93396-124">Zapas</span><span class="sxs-lookup"><span data-stu-id="93396-124">Sku</span></span>

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

### <span data-ttu-id="93396-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="93396-125">-Confirm</span></span>
<span data-ttu-id="93396-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93396-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93396-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93396-127">-WhatIf</span></span>
<span data-ttu-id="93396-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93396-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93396-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="93396-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93396-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93396-130">CommonParameters</span></span>
<span data-ttu-id="93396-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93396-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93396-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93396-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93396-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="93396-133">INPUTS</span></span>

### <span data-ttu-id="93396-134">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="93396-134">None</span></span>

## <span data-ttu-id="93396-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="93396-135">OUTPUTS</span></span>

### <span data-ttu-id="93396-136">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="93396-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="93396-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="93396-137">NOTES</span></span>

## <span data-ttu-id="93396-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="93396-138">RELATED LINKS</span></span>
