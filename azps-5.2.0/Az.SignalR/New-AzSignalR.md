---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/new-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalR.md
ms.openlocfilehash: 222a40c101d0491a6d9409a7404e6731d739a2ba
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98323190"
---
# <span data-ttu-id="ec29e-101">New-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="ec29e-101">New-AzSignalR</span></span>

## <span data-ttu-id="ec29e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ec29e-102">SYNOPSIS</span></span>
<span data-ttu-id="ec29e-103">Tworzenie usługi sygnalizacji.</span><span class="sxs-lookup"><span data-stu-id="ec29e-103">Create a SignalR service.</span></span>

## <span data-ttu-id="ec29e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ec29e-104">SYNTAX</span></span>

```
New-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-Location <String>] [-Sku <String>]
 [-UnitCount <Int32>] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-ServiceMode <String>] [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec29e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ec29e-105">DESCRIPTION</span></span>
<span data-ttu-id="ec29e-106">Tworzenie usługi sygnalizacji.</span><span class="sxs-lookup"><span data-stu-id="ec29e-106">Create a SignalR service.</span></span>
<span data-ttu-id="ec29e-107">Następujące wartości zostaną użyte jako parametry, jeśli nie zostały określone:</span><span class="sxs-lookup"><span data-stu-id="ec29e-107">The following values will be used for the parameters if not specified:</span></span>
* <span data-ttu-id="ec29e-108">`ResourceGroupName`: domyślna grupa zasobów ustawiona przez `Set-AzDefault -ResourceGroupName` .</span><span class="sxs-lookup"><span data-stu-id="ec29e-108">`ResourceGroupName`: the default resource group set by `Set-AzDefault -ResourceGroupName`.</span></span>
* <span data-ttu-id="ec29e-109">`Location`: Lokalizacja grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="ec29e-109">`Location`: the location of the resource group</span></span>
* <span data-ttu-id="ec29e-110">`Sku`: `Standard_S1`</span><span class="sxs-lookup"><span data-stu-id="ec29e-110">`Sku`: `Standard_S1`</span></span>

## <span data-ttu-id="ec29e-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ec29e-111">EXAMPLES</span></span>

### <span data-ttu-id="ec29e-112">Tworzenie usługi sygnalizacji</span><span class="sxs-lookup"><span data-stu-id="ec29e-112">Create a SignalR service</span></span>
```powershell
PS C:\> New-AzSignalR -ResourceGroupName myResourceGroup1 -Name mysignalr1 -Location eastus -Sku Standard_S1 -UnitCount 5

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 5         Succeeded         1.0
```

### <span data-ttu-id="ec29e-113">Określ usługę Servicemode i AllowedOrigin</span><span class="sxs-lookup"><span data-stu-id="ec29e-113">Specify ServiceMode and AllowedOrigin</span></span>
```powershell
PS C:\> New-AzSignalR -ResourceGroupName myResourceGroup1 -Name mysignalr2 -Location eastus -ServiceMode Serverless -AllowedOrigin http://example1.com:12345, https://example2.cn

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 1         Succeeded         1.0
```

## <span data-ttu-id="ec29e-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ec29e-114">PARAMETERS</span></span>

### <span data-ttu-id="ec29e-115">-AllowedOrigin</span><span class="sxs-lookup"><span data-stu-id="ec29e-115">-AllowedOrigin</span></span>
<span data-ttu-id="ec29e-116">Dozwolone źródła dla usługi sygnalizującego.</span><span class="sxs-lookup"><span data-stu-id="ec29e-116">The allowed origins for the SignalR service.</span></span> <span data-ttu-id="ec29e-117">Aby zezwolić na wszystkie, użyj "\*" i Usuń wszystkie inne źródła z listy.</span><span class="sxs-lookup"><span data-stu-id="ec29e-117">To allow all, use "\*" and remove all other origins from the list.</span></span> <span data-ttu-id="ec29e-118">Nie można używać ukośników jako części domeny lub po domenie TLD</span><span class="sxs-lookup"><span data-stu-id="ec29e-118">Slashes are not allowed as part of domain or after TLD</span></span>

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

### <span data-ttu-id="ec29e-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ec29e-119">-AsJob</span></span>
<span data-ttu-id="ec29e-120">Uruchom polecenie cmdlet w zadaniu w tle.</span><span class="sxs-lookup"><span data-stu-id="ec29e-120">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="ec29e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec29e-121">-DefaultProfile</span></span>
<span data-ttu-id="ec29e-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ec29e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec29e-123">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="ec29e-123">-Location</span></span>
<span data-ttu-id="ec29e-124">Lokalizacja usługi sygnalizacji.</span><span class="sxs-lookup"><span data-stu-id="ec29e-124">The SignalR service location.</span></span> <span data-ttu-id="ec29e-125">Jeśli nie podano, zostanie wykorzystana lokalizacja grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ec29e-125">The resource group location will be used if not specified.</span></span>

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

### <span data-ttu-id="ec29e-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ec29e-126">-Name</span></span>
<span data-ttu-id="ec29e-127">Nazwa usługi sygnalizującego.</span><span class="sxs-lookup"><span data-stu-id="ec29e-127">The SignalR service name.</span></span>

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

### <span data-ttu-id="ec29e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec29e-128">-ResourceGroupName</span></span>
<span data-ttu-id="ec29e-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ec29e-129">The resource group name.</span></span> <span data-ttu-id="ec29e-130">Jeśli nie podano, zostanie użyte ustawienie domyślne.</span><span class="sxs-lookup"><span data-stu-id="ec29e-130">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="ec29e-131">-Servicemode</span><span class="sxs-lookup"><span data-stu-id="ec29e-131">-ServiceMode</span></span>
<span data-ttu-id="ec29e-132">Tryb usługi dla usługi sygnalizującego.</span><span class="sxs-lookup"><span data-stu-id="ec29e-132">The service mode for the SignalR service.</span></span>

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

### <span data-ttu-id="ec29e-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="ec29e-133">-Sku</span></span>
<span data-ttu-id="ec29e-134">Jednostka SKU usługi sygnalizacji.</span><span class="sxs-lookup"><span data-stu-id="ec29e-134">The SignalR service SKU.</span></span>

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

### <span data-ttu-id="ec29e-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="ec29e-135">-Tag</span></span>
<span data-ttu-id="ec29e-136">Znaczniki usługi sygnalizującego.</span><span class="sxs-lookup"><span data-stu-id="ec29e-136">The tags for the SignalR service.</span></span>

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

### <span data-ttu-id="ec29e-137">-UnitCount</span><span class="sxs-lookup"><span data-stu-id="ec29e-137">-UnitCount</span></span>
<span data-ttu-id="ec29e-138">Liczba jednostek usługi sygnalizującego — od 1 do 10.</span><span class="sxs-lookup"><span data-stu-id="ec29e-138">The SignalR service unit count, from 1 to 10.</span></span> <span data-ttu-id="ec29e-139">Domyślnie: 1.</span><span class="sxs-lookup"><span data-stu-id="ec29e-139">Default to 1.</span></span>

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

### <span data-ttu-id="ec29e-140">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ec29e-140">-Confirm</span></span>
<span data-ttu-id="ec29e-141">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec29e-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec29e-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec29e-142">-WhatIf</span></span>
<span data-ttu-id="ec29e-143">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec29e-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec29e-144">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ec29e-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec29e-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec29e-145">CommonParameters</span></span>
<span data-ttu-id="ec29e-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec29e-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec29e-147">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ec29e-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec29e-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ec29e-148">INPUTS</span></span>

### <span data-ttu-id="ec29e-149">System. String</span><span class="sxs-lookup"><span data-stu-id="ec29e-149">System.String</span></span>

## <span data-ttu-id="ec29e-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ec29e-150">OUTPUTS</span></span>

### <span data-ttu-id="ec29e-151">Microsoft. Azure. Commands. Signals. modele. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="ec29e-151">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="ec29e-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ec29e-152">NOTES</span></span>

## <span data-ttu-id="ec29e-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ec29e-153">RELATED LINKS</span></span>
