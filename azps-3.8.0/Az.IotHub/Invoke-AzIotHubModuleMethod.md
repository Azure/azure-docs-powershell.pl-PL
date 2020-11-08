---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubmodulemethod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubModuleMethod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubModuleMethod.md
ms.openlocfilehash: 818e973d4d7be9fb03e23a23d7264745920f843f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052785"
---
# <span data-ttu-id="a3717-101">Invoke-AzIotHubModuleMethod</span><span class="sxs-lookup"><span data-stu-id="a3717-101">Invoke-AzIotHubModuleMethod</span></span>

## <span data-ttu-id="a3717-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a3717-102">SYNOPSIS</span></span>
<span data-ttu-id="a3717-103">Wywoływanie metody modułu Edge.</span><span class="sxs-lookup"><span data-stu-id="a3717-103">Invoke an Edge module method.</span></span>

## <span data-ttu-id="a3717-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a3717-104">SYNTAX</span></span>

### <span data-ttu-id="a3717-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a3717-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubModuleMethod [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId] <String> -Name <String> [-Payload <String>] [-ResponseTimeOut <Int32>]
 [-ConnectionTimeOut <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a3717-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a3717-106">InputObjectSet</span></span>
```
Invoke-AzIotHubModuleMethod [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId] <String> -Name <String>
 [-Payload <String>] [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3717-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a3717-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubModuleMethod [-ResourceId] <String> [-DeviceId] <String> [-ModuleId] <String> -Name <String>
 [-Payload <String>] [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3717-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a3717-108">DESCRIPTION</span></span>
<span data-ttu-id="a3717-109">Wywoływanie metody modułu Edge.</span><span class="sxs-lookup"><span data-stu-id="a3717-109">Invoke an Edge module method.</span></span> <span data-ttu-id="a3717-110"> https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methodsAby uzyskać więcej informacji, zobacz.</span><span class="sxs-lookup"><span data-stu-id="a3717-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods for more information.</span></span>

## <span data-ttu-id="a3717-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a3717-111">EXAMPLES</span></span>

### <span data-ttu-id="a3717-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a3717-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubModuleMethod -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Name "methodName" -Payload "method-input" -ResponseTimeOut 20 -ConnectionTimeOut 15
```

<span data-ttu-id="a3717-113">Wywoływanie metody modułu Edge.</span><span class="sxs-lookup"><span data-stu-id="a3717-113">Invoke an Edge module method.</span></span>

## <span data-ttu-id="a3717-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a3717-114">PARAMETERS</span></span>

### <span data-ttu-id="a3717-115">-ConnectionTimeOut</span><span class="sxs-lookup"><span data-stu-id="a3717-115">-ConnectionTimeOut</span></span>
<span data-ttu-id="a3717-116">Liczba sekund określająca czas oczekiwania na pomyślną nawiązaniu połączenia.</span><span class="sxs-lookup"><span data-stu-id="a3717-116">Number of seconds to wait until a connection is successfully made.</span></span>
<span data-ttu-id="a3717-117">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="a3717-117">Default is 10.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3717-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3717-118">-DefaultProfile</span></span>
<span data-ttu-id="a3717-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a3717-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3717-120">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="a3717-120">-DeviceId</span></span>
<span data-ttu-id="a3717-121">Identyfikator urządzenia docelowego.</span><span class="sxs-lookup"><span data-stu-id="a3717-121">Target Device Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3717-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a3717-122">-InputObject</span></span>
<span data-ttu-id="a3717-123">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="a3717-123">IotHub object</span></span>

```yaml
Type: PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3717-124">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="a3717-124">-IotHubName</span></span>
<span data-ttu-id="a3717-125">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="a3717-125">Name of the Iot Hub</span></span>

```yaml
Type: String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3717-126">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="a3717-126">-ModuleId</span></span>
<span data-ttu-id="a3717-127">Identyfikator modułu urządzenia docelowego.</span><span class="sxs-lookup"><span data-stu-id="a3717-127">Target device's module id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3717-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a3717-128">-Name</span></span>
<span data-ttu-id="a3717-129">Nazwa metody, którą należy wywołać w tym module urządzenia.</span><span class="sxs-lookup"><span data-stu-id="a3717-129">The name of the method to invoke on this device module.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3717-130">-Ładunek</span><span class="sxs-lookup"><span data-stu-id="a3717-130">-Payload</span></span>
<span data-ttu-id="a3717-131">Ładunek metody wywoływania w tym module urządzenia.</span><span class="sxs-lookup"><span data-stu-id="a3717-131">The payload for the method to invoke on this device module.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3717-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3717-132">-ResourceGroupName</span></span>
<span data-ttu-id="a3717-133">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="a3717-133">Name of the Resource Group</span></span>

```yaml
Type: String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3717-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a3717-134">-ResourceId</span></span>
<span data-ttu-id="a3717-135">Identyfikator zasobu IotHub</span><span class="sxs-lookup"><span data-stu-id="a3717-135">IotHub Resource Id</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3717-136">-ResponseTimeOut</span><span class="sxs-lookup"><span data-stu-id="a3717-136">-ResponseTimeOut</span></span>
<span data-ttu-id="a3717-137">Liczba sekund określająca czas oczekiwania na otrzymanie wyniku z metody bezpośredniej.</span><span class="sxs-lookup"><span data-stu-id="a3717-137">Number of seconds to wait until a result is received from the direct method.</span></span>
<span data-ttu-id="a3717-138">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="a3717-138">Default is 10.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3717-139">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a3717-139">-Confirm</span></span>
<span data-ttu-id="a3717-140">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3717-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3717-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3717-141">-WhatIf</span></span>
<span data-ttu-id="a3717-142">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3717-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3717-143">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a3717-143">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3717-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3717-144">CommonParameters</span></span>
<span data-ttu-id="a3717-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3717-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="a3717-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3717-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3717-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a3717-147">INPUTS</span></span>

### <span data-ttu-id="a3717-148">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="a3717-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="a3717-149">System. String</span><span class="sxs-lookup"><span data-stu-id="a3717-149">System.String</span></span>

## <span data-ttu-id="a3717-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a3717-150">OUTPUTS</span></span>

### <span data-ttu-id="a3717-151">Microsoft. Azure. Commands. Management. IotHub. models. PSCloudToDeviceMethodResult</span><span class="sxs-lookup"><span data-stu-id="a3717-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceMethodResult</span></span>

## <span data-ttu-id="a3717-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a3717-152">NOTES</span></span>

## <span data-ttu-id="a3717-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a3717-153">RELATED LINKS</span></span>
