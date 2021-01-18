---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/update-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalR.md
ms.openlocfilehash: 632f271a085df8384a100392e8ed74ad7b5d0762
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98498394"
---
# <span data-ttu-id="6c78b-101">Update-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="6c78b-101">Update-AzSignalR</span></span>

## <span data-ttu-id="6c78b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6c78b-102">SYNOPSIS</span></span>
<span data-ttu-id="6c78b-103">Aktualizowanie usługi sygnalizującej.</span><span class="sxs-lookup"><span data-stu-id="6c78b-103">Update a SignalR service.</span></span>

## <span data-ttu-id="6c78b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6c78b-104">SYNTAX</span></span>

### <span data-ttu-id="6c78b-105">ResourceGroupParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6c78b-105">ResourceGroupParameterSet (Default)</span></span>
```
Update-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-Sku <String>] [-UnitCount <Int32>]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-ServiceMode <String>]
 [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6c78b-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c78b-106">ResourceIdParameterSet</span></span>
```
Update-AzSignalR -ResourceId <String> [-Sku <String>] [-UnitCount <Int32>]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-ServiceMode <String>]
 [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6c78b-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c78b-107">InputObjectParameterSet</span></span>
```
Update-AzSignalR -InputObject <PSSignalRResource> [-Sku <String>] [-UnitCount <Int32>]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-ServiceMode <String>]
 [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6c78b-108">Opis</span><span class="sxs-lookup"><span data-stu-id="6c78b-108">DESCRIPTION</span></span>
<span data-ttu-id="6c78b-109">Aktualizowanie usługi sygnalizującej.</span><span class="sxs-lookup"><span data-stu-id="6c78b-109">Update a SignalR service.</span></span>
<span data-ttu-id="6c78b-110">Następujące wartości zostaną użyte jako parametry, jeśli nie zostały określone:</span><span class="sxs-lookup"><span data-stu-id="6c78b-110">The following values will be used for the parameters if not specified:</span></span>
* <span data-ttu-id="6c78b-111">`ResourceGroupName`: domyślna grupa zasobów ustawiona przez `Set-AzDefault -ResourceGroupName` .</span><span class="sxs-lookup"><span data-stu-id="6c78b-111">`ResourceGroupName`: the default resource group set by `Set-AzDefault -ResourceGroupName`.</span></span>
* <span data-ttu-id="6c78b-112">`Sku`: `Standard_S1`</span><span class="sxs-lookup"><span data-stu-id="6c78b-112">`Sku`: `Standard_S1`</span></span>

## <span data-ttu-id="6c78b-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6c78b-113">EXAMPLES</span></span>

### <span data-ttu-id="6c78b-114">Zaktualizuj określoną usługę sygnalizującą.</span><span class="sxs-lookup"><span data-stu-id="6c78b-114">Update a specific SignalR service.</span></span>
```powershell
PS C:\> Update-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -UnitCount 5

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 5         Succeeded         1.0
```

### <span data-ttu-id="6c78b-115">Określ usługę Servicemode i AllowedOrigin</span><span class="sxs-lookup"><span data-stu-id="6c78b-115">Specify ServiceMode and AllowedOrigin</span></span>
```powershell
PS C:\> Update-AzSignalR -ResourceGroupName myResourceGroup1 -Name mysignalr2 -ServiceMode Serverless -AllowedOrigin http://example1.com:12345, https://example2.cn

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 1         Succeeded         1.0
```

## <span data-ttu-id="6c78b-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6c78b-116">PARAMETERS</span></span>

### <span data-ttu-id="6c78b-117">-AllowedOrigin</span><span class="sxs-lookup"><span data-stu-id="6c78b-117">-AllowedOrigin</span></span>
<span data-ttu-id="6c78b-118">Dozwolone źródła dla usługi sygnalizującego.</span><span class="sxs-lookup"><span data-stu-id="6c78b-118">The allowed origins for the SignalR service.</span></span> <span data-ttu-id="6c78b-119">Aby zezwolić na wszystkie, użyj "\*" i Usuń wszystkie inne źródła z listy.</span><span class="sxs-lookup"><span data-stu-id="6c78b-119">To allow all, use "\*" and remove all other origins from the list.</span></span> <span data-ttu-id="6c78b-120">Nie można używać ukośników jako części domeny lub po domenie TLD</span><span class="sxs-lookup"><span data-stu-id="6c78b-120">Slashes are not allowed as part of domain or after TLD</span></span>

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

### <span data-ttu-id="6c78b-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6c78b-121">-AsJob</span></span>
<span data-ttu-id="6c78b-122">Uruchom polecenie cmdlet w zadaniu w tle.</span><span class="sxs-lookup"><span data-stu-id="6c78b-122">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="6c78b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c78b-123">-DefaultProfile</span></span>
<span data-ttu-id="6c78b-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6c78b-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c78b-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6c78b-125">-InputObject</span></span>
<span data-ttu-id="6c78b-126">Obiekt zasobu sygnalizującego.</span><span class="sxs-lookup"><span data-stu-id="6c78b-126">The SignalR resource object.</span></span>

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

### <span data-ttu-id="6c78b-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6c78b-127">-Name</span></span>
<span data-ttu-id="6c78b-128">Nazwa usługi sygnalizującego.</span><span class="sxs-lookup"><span data-stu-id="6c78b-128">The SignalR service name.</span></span>

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

### <span data-ttu-id="6c78b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c78b-129">-ResourceGroupName</span></span>
<span data-ttu-id="6c78b-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6c78b-130">The resource group name.</span></span>
<span data-ttu-id="6c78b-131">Jeśli nie podano, zostanie użyte ustawienie domyślne.</span><span class="sxs-lookup"><span data-stu-id="6c78b-131">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="6c78b-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6c78b-132">-ResourceId</span></span>
<span data-ttu-id="6c78b-133">Identyfikator zasobu usługi sygnalizującego.</span><span class="sxs-lookup"><span data-stu-id="6c78b-133">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="6c78b-134">-Servicemode</span><span class="sxs-lookup"><span data-stu-id="6c78b-134">-ServiceMode</span></span>
<span data-ttu-id="6c78b-135">Tryb usługi dla usługi sygnalizującego.</span><span class="sxs-lookup"><span data-stu-id="6c78b-135">The service mode for the SignalR service.</span></span>

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

### <span data-ttu-id="6c78b-136">-SKU</span><span class="sxs-lookup"><span data-stu-id="6c78b-136">-Sku</span></span>
<span data-ttu-id="6c78b-137">Jednostka SKU usługi sygnalizacji.</span><span class="sxs-lookup"><span data-stu-id="6c78b-137">The SignalR service SKU.</span></span>
<span data-ttu-id="6c78b-138">Domyślnie: "Standard_S1".</span><span class="sxs-lookup"><span data-stu-id="6c78b-138">Default to "Standard_S1".</span></span>

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

### <span data-ttu-id="6c78b-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="6c78b-139">-Tag</span></span>
<span data-ttu-id="6c78b-140">Znaczniki usługi sygnalizującego.</span><span class="sxs-lookup"><span data-stu-id="6c78b-140">The tags for the SignalR service.</span></span>

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

### <span data-ttu-id="6c78b-141">-UnitCount</span><span class="sxs-lookup"><span data-stu-id="6c78b-141">-UnitCount</span></span>
<span data-ttu-id="6c78b-142">Zliczanie jednostek usługi sygnalizującego, wartość tylko z {1, 2, 5, 10, 20, 50, 100}.</span><span class="sxs-lookup"><span data-stu-id="6c78b-142">The SignalR service unit count, value only from {1, 2, 5, 10, 20, 50, 100}.</span></span>
<span data-ttu-id="6c78b-143">Domyślnie: 1.</span><span class="sxs-lookup"><span data-stu-id="6c78b-143">Default to 1.</span></span>

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

### <span data-ttu-id="6c78b-144">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6c78b-144">-Confirm</span></span>
<span data-ttu-id="6c78b-145">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c78b-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c78b-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c78b-146">-WhatIf</span></span>
<span data-ttu-id="6c78b-147">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c78b-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c78b-148">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6c78b-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c78b-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c78b-149">CommonParameters</span></span>
<span data-ttu-id="6c78b-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c78b-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c78b-151">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6c78b-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c78b-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6c78b-152">INPUTS</span></span>

### <span data-ttu-id="6c78b-153">System. String</span><span class="sxs-lookup"><span data-stu-id="6c78b-153">System.String</span></span>

### <span data-ttu-id="6c78b-154">Microsoft. Azure. Commands. Signals. modele. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="6c78b-154">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="6c78b-155">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6c78b-155">OUTPUTS</span></span>

### <span data-ttu-id="6c78b-156">Microsoft. Azure. Commands. Signals. modele. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="6c78b-156">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="6c78b-157">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6c78b-157">NOTES</span></span>

## <span data-ttu-id="6c78b-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6c78b-158">RELATED LINKS</span></span>
