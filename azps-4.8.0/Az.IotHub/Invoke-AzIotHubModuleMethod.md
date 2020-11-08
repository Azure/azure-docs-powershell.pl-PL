---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubmodulemethod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubModuleMethod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubModuleMethod.md
ms.openlocfilehash: e9faa07f4addabcb556819e1d45b63a0dec0f6b3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223881"
---
# <span data-ttu-id="62107-101">Invoke-AzIotHubModuleMethod</span><span class="sxs-lookup"><span data-stu-id="62107-101">Invoke-AzIotHubModuleMethod</span></span>

## <span data-ttu-id="62107-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="62107-102">SYNOPSIS</span></span>
<span data-ttu-id="62107-103">Wywoływanie metody modułu Edge.</span><span class="sxs-lookup"><span data-stu-id="62107-103">Invoke an Edge module method.</span></span>

## <span data-ttu-id="62107-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="62107-104">SYNTAX</span></span>

### <span data-ttu-id="62107-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="62107-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubModuleMethod [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId] <String> -Name <String> [-Payload <String>] [-ResponseTimeOut <Int32>]
 [-ConnectionTimeOut <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="62107-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="62107-106">InputObjectSet</span></span>
```
Invoke-AzIotHubModuleMethod [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId] <String> -Name <String>
 [-Payload <String>] [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62107-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="62107-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubModuleMethod [-ResourceId] <String> [-DeviceId] <String> [-ModuleId] <String> -Name <String>
 [-Payload <String>] [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62107-108">Opis</span><span class="sxs-lookup"><span data-stu-id="62107-108">DESCRIPTION</span></span>
<span data-ttu-id="62107-109">Wywoływanie metody modułu Edge.</span><span class="sxs-lookup"><span data-stu-id="62107-109">Invoke an Edge module method.</span></span> <span data-ttu-id="62107-110"> https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methodsAby uzyskać więcej informacji, zobacz.</span><span class="sxs-lookup"><span data-stu-id="62107-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods for more information.</span></span>

## <span data-ttu-id="62107-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="62107-111">EXAMPLES</span></span>

### <span data-ttu-id="62107-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="62107-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubModuleMethod -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Name "methodName" -Payload "method-input" -ResponseTimeOut 20 -ConnectionTimeOut 15
```

<span data-ttu-id="62107-113">Wywoływanie metody modułu Edge.</span><span class="sxs-lookup"><span data-stu-id="62107-113">Invoke an Edge module method.</span></span>

## <span data-ttu-id="62107-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="62107-114">PARAMETERS</span></span>

### <span data-ttu-id="62107-115">-ConnectionTimeOut</span><span class="sxs-lookup"><span data-stu-id="62107-115">-ConnectionTimeOut</span></span>
<span data-ttu-id="62107-116">Liczba sekund określająca czas oczekiwania na pomyślną nawiązaniu połączenia.</span><span class="sxs-lookup"><span data-stu-id="62107-116">Number of seconds to wait until a connection is successfully made.</span></span>
<span data-ttu-id="62107-117">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="62107-117">Default is 10.</span></span>

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

### <span data-ttu-id="62107-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62107-118">-DefaultProfile</span></span>
<span data-ttu-id="62107-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="62107-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62107-120">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="62107-120">-DeviceId</span></span>
<span data-ttu-id="62107-121">Identyfikator urządzenia docelowego.</span><span class="sxs-lookup"><span data-stu-id="62107-121">Target Device Id.</span></span>

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

### <span data-ttu-id="62107-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="62107-122">-InputObject</span></span>
<span data-ttu-id="62107-123">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="62107-123">IotHub object</span></span>

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

### <span data-ttu-id="62107-124">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="62107-124">-IotHubName</span></span>
<span data-ttu-id="62107-125">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="62107-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="62107-126">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="62107-126">-ModuleId</span></span>
<span data-ttu-id="62107-127">Identyfikator modułu urządzenia docelowego.</span><span class="sxs-lookup"><span data-stu-id="62107-127">Target device's module id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62107-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="62107-128">-Name</span></span>
<span data-ttu-id="62107-129">Nazwa metody, którą należy wywołać w tym module urządzenia.</span><span class="sxs-lookup"><span data-stu-id="62107-129">The name of the method to invoke on this device module.</span></span>

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

### <span data-ttu-id="62107-130">-Ładunek</span><span class="sxs-lookup"><span data-stu-id="62107-130">-Payload</span></span>
<span data-ttu-id="62107-131">Ładunek metody wywoływania w tym module urządzenia.</span><span class="sxs-lookup"><span data-stu-id="62107-131">The payload for the method to invoke on this device module.</span></span>

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

### <span data-ttu-id="62107-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62107-132">-ResourceGroupName</span></span>
<span data-ttu-id="62107-133">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="62107-133">Name of the Resource Group</span></span>

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

### <span data-ttu-id="62107-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="62107-134">-ResourceId</span></span>
<span data-ttu-id="62107-135">Identyfikator zasobu IotHub</span><span class="sxs-lookup"><span data-stu-id="62107-135">IotHub Resource Id</span></span>

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

### <span data-ttu-id="62107-136">-ResponseTimeOut</span><span class="sxs-lookup"><span data-stu-id="62107-136">-ResponseTimeOut</span></span>
<span data-ttu-id="62107-137">Liczba sekund określająca czas oczekiwania na otrzymanie wyniku z metody bezpośredniej.</span><span class="sxs-lookup"><span data-stu-id="62107-137">Number of seconds to wait until a result is received from the direct method.</span></span>
<span data-ttu-id="62107-138">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="62107-138">Default is 10.</span></span>

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

### <span data-ttu-id="62107-139">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="62107-139">-Confirm</span></span>
<span data-ttu-id="62107-140">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62107-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62107-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62107-141">-WhatIf</span></span>
<span data-ttu-id="62107-142">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62107-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62107-143">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="62107-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62107-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62107-144">CommonParameters</span></span>
<span data-ttu-id="62107-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62107-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62107-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62107-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62107-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="62107-147">INPUTS</span></span>

### <span data-ttu-id="62107-148">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="62107-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="62107-149">System. String</span><span class="sxs-lookup"><span data-stu-id="62107-149">System.String</span></span>

## <span data-ttu-id="62107-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="62107-150">OUTPUTS</span></span>

### <span data-ttu-id="62107-151">Microsoft. Azure. Commands. Management. IotHub. models. PSCloudToDeviceMethodResult</span><span class="sxs-lookup"><span data-stu-id="62107-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceMethodResult</span></span>

## <span data-ttu-id="62107-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="62107-152">NOTES</span></span>

## <span data-ttu-id="62107-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="62107-153">RELATED LINKS</span></span>
