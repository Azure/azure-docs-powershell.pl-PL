---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubdevicemethod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeviceMethod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeviceMethod.md
ms.openlocfilehash: 78247b26d2f8e6618d3999389efa509e3f8854b9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052782"
---
# <span data-ttu-id="45785-101">Invoke-AzIotHubDeviceMethod</span><span class="sxs-lookup"><span data-stu-id="45785-101">Invoke-AzIotHubDeviceMethod</span></span>

## <span data-ttu-id="45785-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="45785-102">SYNOPSIS</span></span>
<span data-ttu-id="45785-103">Wywołaj metodę bezpośrednią na urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="45785-103">Invoke a direct method on a device.</span></span>

## <span data-ttu-id="45785-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="45785-104">SYNTAX</span></span>

### <span data-ttu-id="45785-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="45785-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubDeviceMethod [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 -Name <String> [-Payload <String>] [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45785-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="45785-106">InputObjectSet</span></span>
```
Invoke-AzIotHubDeviceMethod [-InputObject] <PSIotHub> [-DeviceId] <String> -Name <String> [-Payload <String>]
 [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45785-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="45785-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubDeviceMethod [-ResourceId] <String> [-DeviceId] <String> -Name <String> [-Payload <String>]
 [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45785-108">Opis</span><span class="sxs-lookup"><span data-stu-id="45785-108">DESCRIPTION</span></span>
<span data-ttu-id="45785-109">Wywołaj metodę bezpośrednią na urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="45785-109">Invoke a direct method on a device.</span></span> <span data-ttu-id="45785-110"> https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methodsAby uzyskać więcej informacji, zobacz.</span><span class="sxs-lookup"><span data-stu-id="45785-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods for more information.</span></span>

## <span data-ttu-id="45785-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="45785-111">EXAMPLES</span></span>

### <span data-ttu-id="45785-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="45785-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubDeviceMethod -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Name "methodName" -ResponseTimeOut 20 -ConnectionTimeOut 15
```

<span data-ttu-id="45785-113">Wywoływanie metody urządzenia.</span><span class="sxs-lookup"><span data-stu-id="45785-113">Invoke a device method.</span></span>

## <span data-ttu-id="45785-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="45785-114">PARAMETERS</span></span>

### <span data-ttu-id="45785-115">-ConnectionTimeOut</span><span class="sxs-lookup"><span data-stu-id="45785-115">-ConnectionTimeOut</span></span>
<span data-ttu-id="45785-116">Liczba sekund określająca czas oczekiwania na pomyślną nawiązaniu połączenia.</span><span class="sxs-lookup"><span data-stu-id="45785-116">Number of seconds to wait until a connection is successfully made.</span></span>
<span data-ttu-id="45785-117">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="45785-117">Default is 10.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45785-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45785-118">-DefaultProfile</span></span>
<span data-ttu-id="45785-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="45785-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45785-120">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="45785-120">-DeviceId</span></span>
<span data-ttu-id="45785-121">Identyfikator urządzenia docelowego.</span><span class="sxs-lookup"><span data-stu-id="45785-121">Target Device Id.</span></span>

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

### <span data-ttu-id="45785-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="45785-122">-InputObject</span></span>
<span data-ttu-id="45785-123">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="45785-123">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="45785-124">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="45785-124">-IotHubName</span></span>
<span data-ttu-id="45785-125">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="45785-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="45785-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="45785-126">-Name</span></span>
<span data-ttu-id="45785-127">Nazwa metody do wywołania na tym urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="45785-127">The name of the method to invoke on this device.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45785-128">-Ładunek</span><span class="sxs-lookup"><span data-stu-id="45785-128">-Payload</span></span>
<span data-ttu-id="45785-129">Ładunek metody wywoływania na tym urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="45785-129">The payload for the method to invoke on this device.</span></span>

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

### <span data-ttu-id="45785-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45785-130">-ResourceGroupName</span></span>
<span data-ttu-id="45785-131">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="45785-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="45785-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="45785-132">-ResourceId</span></span>
<span data-ttu-id="45785-133">Identyfikator zasobu IotHub</span><span class="sxs-lookup"><span data-stu-id="45785-133">IotHub Resource Id</span></span>

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

### <span data-ttu-id="45785-134">-ResponseTimeOut</span><span class="sxs-lookup"><span data-stu-id="45785-134">-ResponseTimeOut</span></span>
<span data-ttu-id="45785-135">Liczba sekund określająca czas oczekiwania na otrzymanie wyniku z metody bezpośredniej.</span><span class="sxs-lookup"><span data-stu-id="45785-135">Number of seconds to wait until a result is received from the direct method.</span></span>
<span data-ttu-id="45785-136">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="45785-136">Default is 10.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45785-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="45785-137">-Confirm</span></span>
<span data-ttu-id="45785-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45785-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45785-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45785-139">-WhatIf</span></span>
<span data-ttu-id="45785-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45785-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45785-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="45785-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45785-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45785-142">CommonParameters</span></span>
<span data-ttu-id="45785-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45785-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45785-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45785-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45785-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="45785-145">INPUTS</span></span>

### <span data-ttu-id="45785-146">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="45785-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="45785-147">System. String</span><span class="sxs-lookup"><span data-stu-id="45785-147">System.String</span></span>

## <span data-ttu-id="45785-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="45785-148">OUTPUTS</span></span>

### <span data-ttu-id="45785-149">Microsoft. Azure. Commands. Management. IotHub. models. PSCloudToDeviceMethodResult</span><span class="sxs-lookup"><span data-stu-id="45785-149">Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceMethodResult</span></span>

## <span data-ttu-id="45785-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="45785-150">NOTES</span></span>

## <span data-ttu-id="45785-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="45785-151">RELATED LINKS</span></span>
