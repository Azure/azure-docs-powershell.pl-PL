---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/new-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalR.md
ms.openlocfilehash: 8c8240ed1df30dface1bdb2ce0b649bacf17d08a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708059"
---
# <span data-ttu-id="66a92-101">New-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="66a92-101">New-AzSignalR</span></span>

## <span data-ttu-id="66a92-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="66a92-102">SYNOPSIS</span></span>
<span data-ttu-id="66a92-103">Tworzenie usługi sygnalizacji.</span><span class="sxs-lookup"><span data-stu-id="66a92-103">Create a SignalR service.</span></span>

## <span data-ttu-id="66a92-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="66a92-104">SYNTAX</span></span>

```
New-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-Location <String>] [-Sku <String>]
 [-UnitCount <Int32>] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66a92-105">Opis</span><span class="sxs-lookup"><span data-stu-id="66a92-105">DESCRIPTION</span></span>
<span data-ttu-id="66a92-106">Tworzenie usługi sygnalizacji.</span><span class="sxs-lookup"><span data-stu-id="66a92-106">Create a SignalR service.</span></span>
<span data-ttu-id="66a92-107">Następujące wartości zostaną użyte jako parametry, jeśli nie zostały określone:</span><span class="sxs-lookup"><span data-stu-id="66a92-107">The following values will be used for the parameters if not specified:</span></span>
* <span data-ttu-id="66a92-108">`ResourceGroupName`: domyślna grupa zasobów ustawiona przez `Set-AzDefault -ResourceGroupName` .</span><span class="sxs-lookup"><span data-stu-id="66a92-108">`ResourceGroupName`: the default resource group set by `Set-AzDefault -ResourceGroupName`.</span></span>
* <span data-ttu-id="66a92-109">`Location`: Lokalizacja grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="66a92-109">`Location`: the location of the resource group</span></span>
* <span data-ttu-id="66a92-110">`Sku`: `Standard_S1`</span><span class="sxs-lookup"><span data-stu-id="66a92-110">`Sku`: `Standard_S1`</span></span>

## <span data-ttu-id="66a92-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="66a92-111">EXAMPLES</span></span>

### <span data-ttu-id="66a92-112">Tworzenie serivcea sygnału</span><span class="sxs-lookup"><span data-stu-id="66a92-112">Create a SignalR serivce</span></span>
```powershell
PS C:\> New-AzSignalR -ResourceGroupName myResourceGroup1 -Name mysignalr1 -Location eastus -Sku Standard_S1

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0-preview
```

## <span data-ttu-id="66a92-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="66a92-113">PARAMETERS</span></span>

### <span data-ttu-id="66a92-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="66a92-114">-AsJob</span></span>
<span data-ttu-id="66a92-115">Uruchom polecenie cmdlet w zadaniu w tle.</span><span class="sxs-lookup"><span data-stu-id="66a92-115">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="66a92-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66a92-116">-DefaultProfile</span></span>
<span data-ttu-id="66a92-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="66a92-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66a92-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="66a92-118">-Location</span></span>
<span data-ttu-id="66a92-119">Lokalizacja usługi sygnalizacji.</span><span class="sxs-lookup"><span data-stu-id="66a92-119">The SignalR service location.</span></span> <span data-ttu-id="66a92-120">Jeśli nie podano, zostanie wykorzystana lokalizacja grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="66a92-120">The resource group location will be used if not specified.</span></span>

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

### <span data-ttu-id="66a92-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="66a92-121">-Name</span></span>
<span data-ttu-id="66a92-122">Nazwa usługi sygnalizującego.</span><span class="sxs-lookup"><span data-stu-id="66a92-122">The SignalR service name.</span></span>

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

### <span data-ttu-id="66a92-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66a92-123">-ResourceGroupName</span></span>
<span data-ttu-id="66a92-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="66a92-124">The resource group name.</span></span> <span data-ttu-id="66a92-125">Jeśli nie podano, zostanie użyte ustawienie domyślne.</span><span class="sxs-lookup"><span data-stu-id="66a92-125">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="66a92-126">-SKU</span><span class="sxs-lookup"><span data-stu-id="66a92-126">-Sku</span></span>
<span data-ttu-id="66a92-127">Jednostka SKU usługi sygnalizacji.</span><span class="sxs-lookup"><span data-stu-id="66a92-127">The SignalR service SKU.</span></span>

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

### <span data-ttu-id="66a92-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="66a92-128">-Tag</span></span>
<span data-ttu-id="66a92-129">Znaczniki usługi sygnalizującego.</span><span class="sxs-lookup"><span data-stu-id="66a92-129">The tags for the SignalR service.</span></span>

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

### <span data-ttu-id="66a92-130">-UnitCount</span><span class="sxs-lookup"><span data-stu-id="66a92-130">-UnitCount</span></span>
<span data-ttu-id="66a92-131">Liczba jednostek usługi sygnalizującego — od 1 do 10.</span><span class="sxs-lookup"><span data-stu-id="66a92-131">The SignalR service unit count, from 1 to 10.</span></span> <span data-ttu-id="66a92-132">Domyślnie: 1.</span><span class="sxs-lookup"><span data-stu-id="66a92-132">Default to 1.</span></span>

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

### <span data-ttu-id="66a92-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="66a92-133">-Confirm</span></span>
<span data-ttu-id="66a92-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66a92-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66a92-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66a92-135">-WhatIf</span></span>
<span data-ttu-id="66a92-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66a92-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66a92-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="66a92-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66a92-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66a92-138">CommonParameters</span></span>
<span data-ttu-id="66a92-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66a92-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66a92-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66a92-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66a92-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="66a92-141">INPUTS</span></span>

### <span data-ttu-id="66a92-142">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="66a92-142">None</span></span>

## <span data-ttu-id="66a92-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="66a92-143">OUTPUTS</span></span>

### <span data-ttu-id="66a92-144">Microsoft. Azure. Commands. Signals. modele. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="66a92-144">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="66a92-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="66a92-145">NOTES</span></span>

## <span data-ttu-id="66a92-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="66a92-146">RELATED LINKS</span></span>
