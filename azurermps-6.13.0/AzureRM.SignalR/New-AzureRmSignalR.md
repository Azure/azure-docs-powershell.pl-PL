---
external help file: Microsoft.Azure.Commands.SignalR.dll-Help.xml
Module Name: AzureRM.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.signalr/new-azurermsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/New-AzureRmSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/New-AzureRmSignalR.md
ms.openlocfilehash: d5b7e5480ea3078dadf5280b4f683280dcd00ea4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546439"
---
# <span data-ttu-id="c2092-101">New-AzureRmSignalR</span><span class="sxs-lookup"><span data-stu-id="c2092-101">New-AzureRmSignalR</span></span>

## <span data-ttu-id="c2092-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c2092-102">SYNOPSIS</span></span>
<span data-ttu-id="c2092-103">Tworzenie usługi sygnalizacji.</span><span class="sxs-lookup"><span data-stu-id="c2092-103">Create a SignalR service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2092-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c2092-104">SYNTAX</span></span>

```
New-AzureRmSignalR [-ResourceGroupName <String>] [-Name] <String> [-Location <String>] [-Sku <String>]
 [-UnitCount <Int32>] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2092-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c2092-105">DESCRIPTION</span></span>
<span data-ttu-id="c2092-106">Tworzenie usługi sygnalizacji.</span><span class="sxs-lookup"><span data-stu-id="c2092-106">Create a SignalR service.</span></span>
<span data-ttu-id="c2092-107">Następujące wartości zostaną użyte jako parametry, jeśli nie zostały określone:</span><span class="sxs-lookup"><span data-stu-id="c2092-107">The following values will be used for the parameters if not specified:</span></span>
* <span data-ttu-id="c2092-108">`ResourceGroupName`: domyślna grupa zasobów ustawiona przez `Set-AzureRmDefault -ResourceGroupName` .</span><span class="sxs-lookup"><span data-stu-id="c2092-108">`ResourceGroupName`: the default resource group set by `Set-AzureRmDefault -ResourceGroupName`.</span></span>
* <span data-ttu-id="c2092-109">`Location`: Lokalizacja grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="c2092-109">`Location`: the location of the resource group</span></span>
* <span data-ttu-id="c2092-110">`Sku`: `Standard_S1`</span><span class="sxs-lookup"><span data-stu-id="c2092-110">`Sku`: `Standard_S1`</span></span>

## <span data-ttu-id="c2092-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c2092-111">EXAMPLES</span></span>

### <span data-ttu-id="c2092-112">Tworzenie serivcea sygnału</span><span class="sxs-lookup"><span data-stu-id="c2092-112">Create a SignalR serivce</span></span>
```powershell
PS C:\> New-AzureRmSignalR -ResourceGroupName myResourceGroup1 -Name mysignalr1 -Location eastus -Sku Standard_S1

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0-preview
```

## <span data-ttu-id="c2092-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c2092-113">PARAMETERS</span></span>

### <span data-ttu-id="c2092-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c2092-114">-AsJob</span></span>
<span data-ttu-id="c2092-115">Uruchom polecenie cmdlet w zadaniu w tle.</span><span class="sxs-lookup"><span data-stu-id="c2092-115">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="c2092-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2092-116">-DefaultProfile</span></span>
<span data-ttu-id="c2092-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c2092-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2092-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="c2092-118">-Location</span></span>
<span data-ttu-id="c2092-119">Lokalizacja usługi sygnalizacji.</span><span class="sxs-lookup"><span data-stu-id="c2092-119">The SignalR service location.</span></span> <span data-ttu-id="c2092-120">Jeśli nie podano, zostanie wykorzystana lokalizacja grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c2092-120">The resource group location will be used if not specified.</span></span>

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

### <span data-ttu-id="c2092-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c2092-121">-Name</span></span>
<span data-ttu-id="c2092-122">Nazwa usługi sygnalizującego.</span><span class="sxs-lookup"><span data-stu-id="c2092-122">The SignalR service name.</span></span>

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

### <span data-ttu-id="c2092-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2092-123">-ResourceGroupName</span></span>
<span data-ttu-id="c2092-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c2092-124">The resource group name.</span></span> <span data-ttu-id="c2092-125">Jeśli nie podano, zostanie użyte ustawienie domyślne.</span><span class="sxs-lookup"><span data-stu-id="c2092-125">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="c2092-126">-SKU</span><span class="sxs-lookup"><span data-stu-id="c2092-126">-Sku</span></span>
<span data-ttu-id="c2092-127">Jednostka SKU usługi sygnalizacji.</span><span class="sxs-lookup"><span data-stu-id="c2092-127">The SignalR service SKU.</span></span>

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

### <span data-ttu-id="c2092-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="c2092-128">-Tag</span></span>
<span data-ttu-id="c2092-129">Znaczniki usługi sygnalizującego.</span><span class="sxs-lookup"><span data-stu-id="c2092-129">The tags for the SignalR service.</span></span>

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

### <span data-ttu-id="c2092-130">-UnitCount</span><span class="sxs-lookup"><span data-stu-id="c2092-130">-UnitCount</span></span>
<span data-ttu-id="c2092-131">Liczba jednostek usługi sygnalizującego — od 1 do 10.</span><span class="sxs-lookup"><span data-stu-id="c2092-131">The SignalR service unit count, from 1 to 10.</span></span> <span data-ttu-id="c2092-132">Domyślnie: 1.</span><span class="sxs-lookup"><span data-stu-id="c2092-132">Default to 1.</span></span>

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

### <span data-ttu-id="c2092-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c2092-133">-Confirm</span></span>
<span data-ttu-id="c2092-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2092-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2092-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2092-135">-WhatIf</span></span>
<span data-ttu-id="c2092-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2092-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2092-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c2092-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2092-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2092-138">CommonParameters</span></span>
<span data-ttu-id="c2092-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2092-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2092-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2092-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2092-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c2092-141">INPUTS</span></span>

### <span data-ttu-id="c2092-142">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="c2092-142">None</span></span>

## <span data-ttu-id="c2092-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c2092-143">OUTPUTS</span></span>

### <span data-ttu-id="c2092-144">Microsoft. Azure. Commands. Signals. modele. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="c2092-144">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="c2092-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c2092-145">NOTES</span></span>

## <span data-ttu-id="c2092-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c2092-146">RELATED LINKS</span></span>
