---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/New-AzureRmIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/New-AzureRmIoTDeviceProvisioningService.md
ms.openlocfilehash: 9665b0ae486c12aec350db572aee6fc4f718ed43
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543852"
---
# <span data-ttu-id="36845-101">New-AzureRmIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="36845-101">New-AzureRmIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="36845-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="36845-102">SYNOPSIS</span></span>
<span data-ttu-id="36845-103">Tworzenie usługi dostarczania urządzeń centrum usług Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="36845-103">Create an Azure IoT Hub device provisioning service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36845-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="36845-104">SYNTAX</span></span>

```
New-AzureRmIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-Location <String>]
 [-AllocationPolicy <String>] [-SkuName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36845-105">Opis</span><span class="sxs-lookup"><span data-stu-id="36845-105">DESCRIPTION</span></span>
<span data-ttu-id="36845-106">Aby uzyskać wprowadzenie do usługi dostarczania urządzeń centrum usług Azure IoT, zobacz https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="36845-106">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="36845-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="36845-107">EXAMPLES</span></span>

### <span data-ttu-id="36845-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="36845-108">Example 1</span></span>
```
PS C:\> New-AzureRmIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps"

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

<span data-ttu-id="36845-109">Utwórz usługę inicjowania obsługi urządzenia centrum usług Azure IoT z standardową warstwą cenową S1 w regionie grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="36845-109">Create an Azure IoT Hub device provisioning service with the standard pricing tier S1, in the region of the resource group.</span></span>

### <span data-ttu-id="36845-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="36845-110">Example 2</span></span>
```
PS C:\> New-AzureRmIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -Location "eastus"

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

<span data-ttu-id="36845-111">Utwórz usługę inicjowania obsługi urządzenia centrum usług Azure IoT z standardową warstwą cenową S1 w regionie "Wschód".</span><span class="sxs-lookup"><span data-stu-id="36845-111">Create an Azure IoT Hub device provisioning service with the standard pricing tier S1, in the 'eastus' region.</span></span>

## <span data-ttu-id="36845-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="36845-112">PARAMETERS</span></span>

### <span data-ttu-id="36845-113">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="36845-113">-AllocationPolicy</span></span>
<span data-ttu-id="36845-114">Zasady alokacji usług dla urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="36845-114">IoT Device Provisioning Service Allocation policy</span></span>

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

### <span data-ttu-id="36845-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36845-115">-DefaultProfile</span></span>
<span data-ttu-id="36845-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="36845-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36845-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="36845-117">-Location</span></span>
<span data-ttu-id="36845-118">Pozycję</span><span class="sxs-lookup"><span data-stu-id="36845-118">Location</span></span>

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

### <span data-ttu-id="36845-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="36845-119">-Name</span></span>
<span data-ttu-id="36845-120">Nazwa usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="36845-120">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="36845-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36845-121">-ResourceGroupName</span></span>
<span data-ttu-id="36845-122">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="36845-122">Name of the Resource Group</span></span>

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

### <span data-ttu-id="36845-123">-SkuName</span><span class="sxs-lookup"><span data-stu-id="36845-123">-SkuName</span></span>
<span data-ttu-id="36845-124">Zapas</span><span class="sxs-lookup"><span data-stu-id="36845-124">Sku</span></span>

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

### <span data-ttu-id="36845-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="36845-125">-Confirm</span></span>
<span data-ttu-id="36845-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36845-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36845-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36845-127">-WhatIf</span></span>
<span data-ttu-id="36845-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36845-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36845-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="36845-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36845-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36845-130">CommonParameters</span></span>
<span data-ttu-id="36845-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36845-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36845-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36845-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36845-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="36845-133">INPUTS</span></span>

### <span data-ttu-id="36845-134">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="36845-134">None</span></span>

## <span data-ttu-id="36845-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="36845-135">OUTPUTS</span></span>

### <span data-ttu-id="36845-136">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="36845-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="36845-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="36845-137">NOTES</span></span>

## <span data-ttu-id="36845-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="36845-138">RELATED LINKS</span></span>
