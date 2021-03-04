---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/powershell/module/az.signalr/update-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalR.md
ms.openlocfilehash: d02db6e59c688a79b0088c3b3b42fde0cbc13bb8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955354"
---
# <span data-ttu-id="4ecc3-101">Update-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="4ecc3-101">Update-AzSignalR</span></span>

## <span data-ttu-id="4ecc3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ecc3-102">SYNOPSIS</span></span>
<span data-ttu-id="4ecc3-103">Zaktualizuj usługę SignalR.</span><span class="sxs-lookup"><span data-stu-id="4ecc3-103">Update a SignalR service.</span></span>

## <span data-ttu-id="4ecc3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4ecc3-104">SYNTAX</span></span>

### <span data-ttu-id="4ecc3-105">ResourceGroupParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="4ecc3-105">ResourceGroupParameterSet (Default)</span></span>
```
Update-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-Sku <String>] [-UnitCount <Int32>]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-ServiceMode <String>]
 [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4ecc3-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4ecc3-106">ResourceIdParameterSet</span></span>
```
Update-AzSignalR -ResourceId <String> [-Sku <String>] [-UnitCount <Int32>]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-ServiceMode <String>]
 [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4ecc3-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4ecc3-107">InputObjectParameterSet</span></span>
```
Update-AzSignalR -InputObject <PSSignalRResource> [-Sku <String>] [-UnitCount <Int32>]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-ServiceMode <String>]
 [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4ecc3-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="4ecc3-108">DESCRIPTION</span></span>
<span data-ttu-id="4ecc3-109">Zaktualizuj usługę SignalR.</span><span class="sxs-lookup"><span data-stu-id="4ecc3-109">Update a SignalR service.</span></span>
<span data-ttu-id="4ecc3-110">W przypadku parametrów zostaną użyte następujące wartości, jeśli nie zostaną określone:</span><span class="sxs-lookup"><span data-stu-id="4ecc3-110">The following values will be used for the parameters if not specified:</span></span>
* <span data-ttu-id="4ecc3-111">`ResourceGroupName`: domyślna grupa zasobów ustawiona `Set-AzDefault -ResourceGroupName` przez.</span><span class="sxs-lookup"><span data-stu-id="4ecc3-111">`ResourceGroupName`: the default resource group set by `Set-AzDefault -ResourceGroupName`.</span></span>
* <span data-ttu-id="4ecc3-112">`Sku`: `Standard_S1`</span><span class="sxs-lookup"><span data-stu-id="4ecc3-112">`Sku`: `Standard_S1`</span></span>

## <span data-ttu-id="4ecc3-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4ecc3-113">EXAMPLES</span></span>

### <span data-ttu-id="4ecc3-114">Aktualizowanie określonej usługi SignalR.</span><span class="sxs-lookup"><span data-stu-id="4ecc3-114">Update a specific SignalR service.</span></span>
```powershell
PS C:\> Update-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -UnitCount 5

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 5         Succeeded         1.0
```

### <span data-ttu-id="4ecc3-115">Określanie wartości ServiceMode i AllowedOrigin</span><span class="sxs-lookup"><span data-stu-id="4ecc3-115">Specify ServiceMode and AllowedOrigin</span></span>
```powershell
PS C:\> Update-AzSignalR -ResourceGroupName myResourceGroup1 -Name mysignalr2 -ServiceMode Serverless -AllowedOrigin http://example1.com:12345, https://example2.cn

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 1         Succeeded         1.0
```

## <span data-ttu-id="4ecc3-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4ecc3-116">PARAMETERS</span></span>

### <span data-ttu-id="4ecc3-117">-AllowedOrigin</span><span class="sxs-lookup"><span data-stu-id="4ecc3-117">-AllowedOrigin</span></span>
<span data-ttu-id="4ecc3-118">Dozwolone pochodzenie dla usługi SignalR.</span><span class="sxs-lookup"><span data-stu-id="4ecc3-118">The allowed origins for the SignalR service.</span></span> <span data-ttu-id="4ecc3-119">Aby zezwolić wszystkim, użyj "\*" i usuń wszystkie pozostałe pochodzenie z listy.</span><span class="sxs-lookup"><span data-stu-id="4ecc3-119">To allow all, use "\*" and remove all other origins from the list.</span></span> <span data-ttu-id="4ecc3-120">Ukośniki nie są dozwolone jako część domeny lub po TLD</span><span class="sxs-lookup"><span data-stu-id="4ecc3-120">Slashes are not allowed as part of domain or after TLD</span></span>

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

### <span data-ttu-id="4ecc3-121">— AsJob</span><span class="sxs-lookup"><span data-stu-id="4ecc3-121">-AsJob</span></span>
<span data-ttu-id="4ecc3-122">Uruchom polecenie cmdlet w zadaniu w tle.</span><span class="sxs-lookup"><span data-stu-id="4ecc3-122">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="4ecc3-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ecc3-123">-DefaultProfile</span></span>
<span data-ttu-id="4ecc3-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4ecc3-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ecc3-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4ecc3-125">-InputObject</span></span>
<span data-ttu-id="4ecc3-126">Obiekt zasobu SignalR.</span><span class="sxs-lookup"><span data-stu-id="4ecc3-126">The SignalR resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ecc3-127">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="4ecc3-127">-Name</span></span>
<span data-ttu-id="4ecc3-128">Nazwa usługi SignalR.</span><span class="sxs-lookup"><span data-stu-id="4ecc3-128">The SignalR service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ecc3-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ecc3-129">-ResourceGroupName</span></span>
<span data-ttu-id="4ecc3-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4ecc3-130">The resource group name.</span></span>
<span data-ttu-id="4ecc3-131">Ustawienie domyślne będzie używane, jeśli nie zostanie określone.</span><span class="sxs-lookup"><span data-stu-id="4ecc3-131">The default one will be used if not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ecc3-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4ecc3-132">-ResourceId</span></span>
<span data-ttu-id="4ecc3-133">Identyfikator zasobu usługi SignalR.</span><span class="sxs-lookup"><span data-stu-id="4ecc3-133">The SignalR service resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ecc3-134">-ServiceMode</span><span class="sxs-lookup"><span data-stu-id="4ecc3-134">-ServiceMode</span></span>
<span data-ttu-id="4ecc3-135">Tryb usługi dla usługi SignalR.</span><span class="sxs-lookup"><span data-stu-id="4ecc3-135">The service mode for the SignalR service.</span></span>

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

### <span data-ttu-id="4ecc3-136">- SKU</span><span class="sxs-lookup"><span data-stu-id="4ecc3-136">-Sku</span></span>
<span data-ttu-id="4ecc3-137">SKU usługi SignalR.</span><span class="sxs-lookup"><span data-stu-id="4ecc3-137">The SignalR service SKU.</span></span>
<span data-ttu-id="4ecc3-138">Wartość domyślna to "Standard_S1".</span><span class="sxs-lookup"><span data-stu-id="4ecc3-138">Default to "Standard_S1".</span></span>

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

### <span data-ttu-id="4ecc3-139">— Tag</span><span class="sxs-lookup"><span data-stu-id="4ecc3-139">-Tag</span></span>
<span data-ttu-id="4ecc3-140">Tagi dla usługi SignalR.</span><span class="sxs-lookup"><span data-stu-id="4ecc3-140">The tags for the SignalR service.</span></span>

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

### <span data-ttu-id="4ecc3-141">-UnitCount</span><span class="sxs-lookup"><span data-stu-id="4ecc3-141">-UnitCount</span></span>
<span data-ttu-id="4ecc3-142">Liczba jednostek usługi SignalR, wartość tylko z {1, 2, 5, 10, 20, 50, 100}.</span><span class="sxs-lookup"><span data-stu-id="4ecc3-142">The SignalR service unit count, value only from {1, 2, 5, 10, 20, 50, 100}.</span></span>
<span data-ttu-id="4ecc3-143">Wartość domyślna to 1.</span><span class="sxs-lookup"><span data-stu-id="4ecc3-143">Default to 1.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ecc3-144">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4ecc3-144">-Confirm</span></span>
<span data-ttu-id="4ecc3-145">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4ecc3-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ecc3-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ecc3-146">-WhatIf</span></span>
<span data-ttu-id="4ecc3-147">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ecc3-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ecc3-148">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="4ecc3-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ecc3-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ecc3-149">CommonParameters</span></span>
<span data-ttu-id="4ecc3-150">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ecc3-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ecc3-151">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4ecc3-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ecc3-152">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4ecc3-152">INPUTS</span></span>

### <span data-ttu-id="4ecc3-153">System.String</span><span class="sxs-lookup"><span data-stu-id="4ecc3-153">System.String</span></span>

### <span data-ttu-id="4ecc3-154">Microsoft.Azure.Commands.Signalr.Models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="4ecc3-154">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="4ecc3-155">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4ecc3-155">OUTPUTS</span></span>

### <span data-ttu-id="4ecc3-156">Microsoft.Azure.Commands.Signalr.Models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="4ecc3-156">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="4ecc3-157">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4ecc3-157">NOTES</span></span>

## <span data-ttu-id="4ecc3-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4ecc3-158">RELATED LINKS</span></span>
