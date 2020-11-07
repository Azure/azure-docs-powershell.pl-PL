---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/new-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: ac9d9423bf0098f0f6cf7abba958eb2b08404778
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705549"
---
# <span data-ttu-id="e453a-101">New-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="e453a-101">New-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="e453a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e453a-102">SYNOPSIS</span></span>
<span data-ttu-id="e453a-103">Tworzenie usługi dostarczania urządzeń centrum usług Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="e453a-103">Create an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="e453a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e453a-104">SYNTAX</span></span>

```
New-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-Location <String>]
 [-AllocationPolicy <String>] [-SkuName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e453a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e453a-105">DESCRIPTION</span></span>
<span data-ttu-id="e453a-106">Aby uzyskać wprowadzenie do usługi dostarczania urządzeń centrum usług Azure IoT, zobacz https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="e453a-106">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="e453a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e453a-107">EXAMPLES</span></span>

### <span data-ttu-id="e453a-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e453a-108">Example 1</span></span>
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

<span data-ttu-id="e453a-109">Utwórz usługę inicjowania obsługi urządzenia centrum usług Azure IoT z standardową warstwą cenową S1 w regionie grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e453a-109">Create an Azure IoT Hub device provisioning service with the standard pricing tier S1, in the region of the resource group.</span></span>

### <span data-ttu-id="e453a-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="e453a-110">Example 2</span></span>
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

<span data-ttu-id="e453a-111">Utwórz usługę inicjowania obsługi urządzenia centrum usług Azure IoT z standardową warstwą cenową S1 w regionie "Wschód".</span><span class="sxs-lookup"><span data-stu-id="e453a-111">Create an Azure IoT Hub device provisioning service with the standard pricing tier S1, in the 'eastus' region.</span></span>

## <span data-ttu-id="e453a-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e453a-112">PARAMETERS</span></span>

### <span data-ttu-id="e453a-113">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="e453a-113">-AllocationPolicy</span></span>
<span data-ttu-id="e453a-114">Zasady alokacji usług dla urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="e453a-114">IoT Device Provisioning Service Allocation policy</span></span>

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

### <span data-ttu-id="e453a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e453a-115">-DefaultProfile</span></span>
<span data-ttu-id="e453a-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e453a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e453a-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="e453a-117">-Location</span></span>
<span data-ttu-id="e453a-118">Pozycję</span><span class="sxs-lookup"><span data-stu-id="e453a-118">Location</span></span>

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

### <span data-ttu-id="e453a-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e453a-119">-Name</span></span>
<span data-ttu-id="e453a-120">Nazwa usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="e453a-120">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="e453a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e453a-121">-ResourceGroupName</span></span>
<span data-ttu-id="e453a-122">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="e453a-122">Name of the Resource Group</span></span>

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

### <span data-ttu-id="e453a-123">-SkuName</span><span class="sxs-lookup"><span data-stu-id="e453a-123">-SkuName</span></span>
<span data-ttu-id="e453a-124">Zapas</span><span class="sxs-lookup"><span data-stu-id="e453a-124">Sku</span></span>

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

### <span data-ttu-id="e453a-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e453a-125">-Confirm</span></span>
<span data-ttu-id="e453a-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e453a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e453a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e453a-127">-WhatIf</span></span>
<span data-ttu-id="e453a-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e453a-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e453a-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e453a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e453a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e453a-130">CommonParameters</span></span>
<span data-ttu-id="e453a-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e453a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e453a-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e453a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e453a-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e453a-133">INPUTS</span></span>

### <span data-ttu-id="e453a-134">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="e453a-134">None</span></span>

## <span data-ttu-id="e453a-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e453a-135">OUTPUTS</span></span>

### <span data-ttu-id="e453a-136">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="e453a-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="e453a-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e453a-137">NOTES</span></span>

## <span data-ttu-id="e453a-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e453a-138">RELATED LINKS</span></span>
