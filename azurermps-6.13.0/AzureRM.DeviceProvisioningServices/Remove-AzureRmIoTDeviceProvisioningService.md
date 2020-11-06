---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Remove-AzureRmIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Remove-AzureRmIoTDeviceProvisioningService.md
ms.openlocfilehash: ecc91bb19b3d5d40f8c5aa3e4f25812a9999e45b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543848"
---
# <span data-ttu-id="f48ba-101">Remove-AzureRmIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="f48ba-101">Remove-AzureRmIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="f48ba-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f48ba-102">SYNOPSIS</span></span>
<span data-ttu-id="f48ba-103">Usuwanie usługi dostarczania urządzeń centrum usługi Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="f48ba-103">Delete an Azure IoT Hub device provisioning service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f48ba-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f48ba-104">SYNTAX</span></span>

### <span data-ttu-id="f48ba-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f48ba-105">ResourceSet (Default)</span></span>
```
Remove-AzureRmIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f48ba-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f48ba-106">InputObjectSet</span></span>
```
Remove-AzureRmIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f48ba-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f48ba-107">ResourceIdSet</span></span>
```
Remove-AzureRmIoTDeviceProvisioningService [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f48ba-108">Opis</span><span class="sxs-lookup"><span data-stu-id="f48ba-108">DESCRIPTION</span></span>
<span data-ttu-id="f48ba-109">Aby uzyskać wprowadzenie do usługi dostarczania urządzeń centrum usług Azure IoT, zobacz https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="f48ba-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="f48ba-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f48ba-110">EXAMPLES</span></span>

### <span data-ttu-id="f48ba-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f48ba-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -PassThru

True
```

<span data-ttu-id="f48ba-112">Usuń usługę "myiotdps" urządzenia centrum usług Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="f48ba-112">Delete an Azure IoT Hub device provisioning service 'myiotdps'.</span></span>

### <span data-ttu-id="f48ba-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="f48ba-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIotDps -ResourceGroupName "myresourcegroup" -Name "myiotdps" | Remove-AzureRmIotDps
```

<span data-ttu-id="f48ba-114">Usuwanie usługi "myiotdps" urządzenia centrum usług Azure IoT Hub przy użyciu potoku.</span><span class="sxs-lookup"><span data-stu-id="f48ba-114">Delete an Azure IoT Hub device provisioning service 'myiotdps' using pipeline.</span></span>

## <span data-ttu-id="f48ba-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f48ba-115">PARAMETERS</span></span>

### <span data-ttu-id="f48ba-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f48ba-116">-DefaultProfile</span></span>
<span data-ttu-id="f48ba-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f48ba-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f48ba-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f48ba-118">-InputObject</span></span>
<span data-ttu-id="f48ba-119">Obiekt usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="f48ba-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="f48ba-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f48ba-120">-Name</span></span>
<span data-ttu-id="f48ba-121">Nazwa usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="f48ba-121">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="f48ba-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f48ba-122">-PassThru</span></span>
<span data-ttu-id="f48ba-123">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="f48ba-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="f48ba-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f48ba-124">-ResourceGroupName</span></span>
<span data-ttu-id="f48ba-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="f48ba-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="f48ba-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f48ba-126">-ResourceId</span></span>
<span data-ttu-id="f48ba-127">Identyfikator zasobu usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="f48ba-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="f48ba-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f48ba-128">-Confirm</span></span>
<span data-ttu-id="f48ba-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f48ba-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f48ba-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f48ba-130">-WhatIf</span></span>
<span data-ttu-id="f48ba-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f48ba-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f48ba-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f48ba-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f48ba-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f48ba-133">CommonParameters</span></span>
<span data-ttu-id="f48ba-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f48ba-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f48ba-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f48ba-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f48ba-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f48ba-136">INPUTS</span></span>

### <span data-ttu-id="f48ba-137">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="f48ba-137">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>
<span data-ttu-id="f48ba-138">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f48ba-138">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="f48ba-139">System. String</span><span class="sxs-lookup"><span data-stu-id="f48ba-139">System.String</span></span>

## <span data-ttu-id="f48ba-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f48ba-140">OUTPUTS</span></span>

### <span data-ttu-id="f48ba-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f48ba-141">System.Boolean</span></span>

## <span data-ttu-id="f48ba-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f48ba-142">NOTES</span></span>

## <span data-ttu-id="f48ba-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f48ba-143">RELATED LINKS</span></span>
