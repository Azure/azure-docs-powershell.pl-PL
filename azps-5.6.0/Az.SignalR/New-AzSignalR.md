---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/powershell/module/az.signalr/new-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalR.md
ms.openlocfilehash: 62beafd5546a52bd8e9cc61fae8ff90f7cd2ed1c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955482"
---
# <span data-ttu-id="857b8-101">New-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="857b8-101">New-AzSignalR</span></span>

## <span data-ttu-id="857b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="857b8-102">SYNOPSIS</span></span>
<span data-ttu-id="857b8-103">Utwórz usługę SignalR.</span><span class="sxs-lookup"><span data-stu-id="857b8-103">Create a SignalR service.</span></span>

## <span data-ttu-id="857b8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="857b8-104">SYNTAX</span></span>

```
New-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-Location <String>] [-Sku <String>]
 [-UnitCount <Int32>] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-ServiceMode <String>] [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="857b8-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="857b8-105">DESCRIPTION</span></span>
<span data-ttu-id="857b8-106">Utwórz usługę SignalR.</span><span class="sxs-lookup"><span data-stu-id="857b8-106">Create a SignalR service.</span></span>
<span data-ttu-id="857b8-107">W przypadku parametrów zostaną użyte następujące wartości, jeśli nie zostaną określone:</span><span class="sxs-lookup"><span data-stu-id="857b8-107">The following values will be used for the parameters if not specified:</span></span>
* <span data-ttu-id="857b8-108">`ResourceGroupName`: domyślna grupa zasobów ustawiona `Set-AzDefault -ResourceGroupName` przez.</span><span class="sxs-lookup"><span data-stu-id="857b8-108">`ResourceGroupName`: the default resource group set by `Set-AzDefault -ResourceGroupName`.</span></span>
* <span data-ttu-id="857b8-109">`Location`: lokalizacja grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="857b8-109">`Location`: the location of the resource group</span></span>
* <span data-ttu-id="857b8-110">`Sku`: `Standard_S1`</span><span class="sxs-lookup"><span data-stu-id="857b8-110">`Sku`: `Standard_S1`</span></span>

## <span data-ttu-id="857b8-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="857b8-111">EXAMPLES</span></span>

### <span data-ttu-id="857b8-112">Tworzenie usługi SignalR</span><span class="sxs-lookup"><span data-stu-id="857b8-112">Create a SignalR service</span></span>
```powershell
PS C:\> New-AzSignalR -ResourceGroupName myResourceGroup1 -Name mysignalr1 -Location eastus -Sku Standard_S1 -UnitCount 5

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 5         Succeeded         1.0
```

### <span data-ttu-id="857b8-113">Określanie wartości ServiceMode i AllowedOrigin</span><span class="sxs-lookup"><span data-stu-id="857b8-113">Specify ServiceMode and AllowedOrigin</span></span>
```powershell
PS C:\> New-AzSignalR -ResourceGroupName myResourceGroup1 -Name mysignalr2 -Location eastus -ServiceMode Serverless -AllowedOrigin http://example1.com:12345, https://example2.cn

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 1         Succeeded         1.0
```

## <span data-ttu-id="857b8-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="857b8-114">PARAMETERS</span></span>

### <span data-ttu-id="857b8-115">-AllowedOrigin</span><span class="sxs-lookup"><span data-stu-id="857b8-115">-AllowedOrigin</span></span>
<span data-ttu-id="857b8-116">Dozwolone pochodzenie dla usługi SignalR.</span><span class="sxs-lookup"><span data-stu-id="857b8-116">The allowed origins for the SignalR service.</span></span> <span data-ttu-id="857b8-117">Aby zezwolić wszystkim, użyj "\*" i usuń wszystkie pozostałe pochodzenie z listy.</span><span class="sxs-lookup"><span data-stu-id="857b8-117">To allow all, use "\*" and remove all other origins from the list.</span></span> <span data-ttu-id="857b8-118">Ukośniki nie są dozwolone jako część domeny lub po TLD</span><span class="sxs-lookup"><span data-stu-id="857b8-118">Slashes are not allowed as part of domain or after TLD</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="857b8-119">— AsJob</span><span class="sxs-lookup"><span data-stu-id="857b8-119">-AsJob</span></span>
<span data-ttu-id="857b8-120">Uruchom polecenie cmdlet w zadaniu w tle.</span><span class="sxs-lookup"><span data-stu-id="857b8-120">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="857b8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="857b8-121">-DefaultProfile</span></span>
<span data-ttu-id="857b8-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="857b8-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="857b8-123">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="857b8-123">-Location</span></span>
<span data-ttu-id="857b8-124">Lokalizacja usługi SignalR.</span><span class="sxs-lookup"><span data-stu-id="857b8-124">The SignalR service location.</span></span> <span data-ttu-id="857b8-125">Lokalizacja grupy zasobów będzie używana, jeśli nie zostanie określona.</span><span class="sxs-lookup"><span data-stu-id="857b8-125">The resource group location will be used if not specified.</span></span>

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

### <span data-ttu-id="857b8-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="857b8-126">-Name</span></span>
<span data-ttu-id="857b8-127">Nazwa usługi SignalR.</span><span class="sxs-lookup"><span data-stu-id="857b8-127">The SignalR service name.</span></span>

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

### <span data-ttu-id="857b8-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="857b8-128">-ResourceGroupName</span></span>
<span data-ttu-id="857b8-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="857b8-129">The resource group name.</span></span> <span data-ttu-id="857b8-130">Ustawienie domyślne będzie używane, jeśli nie zostanie określone.</span><span class="sxs-lookup"><span data-stu-id="857b8-130">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="857b8-131">-ServiceMode</span><span class="sxs-lookup"><span data-stu-id="857b8-131">-ServiceMode</span></span>
<span data-ttu-id="857b8-132">Tryb usługi dla usługi SignalR.</span><span class="sxs-lookup"><span data-stu-id="857b8-132">The service mode for the SignalR service.</span></span>

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

### <span data-ttu-id="857b8-133">- SKU</span><span class="sxs-lookup"><span data-stu-id="857b8-133">-Sku</span></span>
<span data-ttu-id="857b8-134">SKU usługi SignalR.</span><span class="sxs-lookup"><span data-stu-id="857b8-134">The SignalR service SKU.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Standard_S1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="857b8-135">— Tag</span><span class="sxs-lookup"><span data-stu-id="857b8-135">-Tag</span></span>
<span data-ttu-id="857b8-136">Tagi dla usługi SignalR.</span><span class="sxs-lookup"><span data-stu-id="857b8-136">The tags for the SignalR service.</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="857b8-137">-UnitCount</span><span class="sxs-lookup"><span data-stu-id="857b8-137">-UnitCount</span></span>
<span data-ttu-id="857b8-138">Liczba jednostek usługi SignalR z 1 do 10.</span><span class="sxs-lookup"><span data-stu-id="857b8-138">The SignalR service unit count, from 1 to 10.</span></span> <span data-ttu-id="857b8-139">Wartość domyślna to 1.</span><span class="sxs-lookup"><span data-stu-id="857b8-139">Default to 1.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="857b8-140">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="857b8-140">-Confirm</span></span>
<span data-ttu-id="857b8-141">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="857b8-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="857b8-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="857b8-142">-WhatIf</span></span>
<span data-ttu-id="857b8-143">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="857b8-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="857b8-144">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="857b8-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="857b8-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="857b8-145">CommonParameters</span></span>
<span data-ttu-id="857b8-146">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="857b8-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="857b8-147">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="857b8-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="857b8-148">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="857b8-148">INPUTS</span></span>

### <span data-ttu-id="857b8-149">System.String</span><span class="sxs-lookup"><span data-stu-id="857b8-149">System.String</span></span>

## <span data-ttu-id="857b8-150">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="857b8-150">OUTPUTS</span></span>

### <span data-ttu-id="857b8-151">Microsoft.Azure.Commands.Signalr.Models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="857b8-151">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="857b8-152">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="857b8-152">NOTES</span></span>

## <span data-ttu-id="857b8-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="857b8-153">RELATED LINKS</span></span>
