---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/powershell/module/az.signalr/set-azsignalrupstream
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Set-AzSignalRUpstream.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Set-AzSignalRUpstream.md
ms.openlocfilehash: 7fde7a8f40efaee9cbf3011e844ee8a48e3949a4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955370"
---
# <span data-ttu-id="cef09-101">Set-AzSignalRUpstream</span><span class="sxs-lookup"><span data-stu-id="cef09-101">Set-AzSignalRUpstream</span></span>

## <span data-ttu-id="cef09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cef09-102">SYNOPSIS</span></span>
<span data-ttu-id="cef09-103">Konfigurowanie ustawień nadrzędnych usługi SignalR.</span><span class="sxs-lookup"><span data-stu-id="cef09-103">Set the upstream settings of a SignalR service.</span></span>

## <span data-ttu-id="cef09-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="cef09-104">SYNTAX</span></span>

### <span data-ttu-id="cef09-105">ResourceGroupParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="cef09-105">ResourceGroupParameterSet (Default)</span></span>
```
Set-AzSignalRUpstream [-ResourceGroupName <String>] [-Name] <String> [-AsJob]
 [-Template <PSUpstreamTemplate[]>] [-Clear] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cef09-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cef09-106">ResourceIdParameterSet</span></span>
```
Set-AzSignalRUpstream -ResourceId <String> [-AsJob] [-Template <PSUpstreamTemplate[]>] [-Clear]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cef09-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cef09-107">InputObjectParameterSet</span></span>
```
Set-AzSignalRUpstream -InputObject <PSSignalRResource> [-AsJob] [-Template <PSUpstreamTemplate[]>] [-Clear]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cef09-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="cef09-108">DESCRIPTION</span></span>
<span data-ttu-id="cef09-109">Konfigurowanie ustawień nadrzędnych usługi SignalR.</span><span class="sxs-lookup"><span data-stu-id="cef09-109">Set the upstream settings of a SignalR service.</span></span>

## <span data-ttu-id="cef09-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="cef09-110">EXAMPLES</span></span>

### <span data-ttu-id="cef09-111">Ustawianie dwóch uporządkowanych szablonów nadrzędnych</span><span class="sxs-lookup"><span data-stu-id="cef09-111">Set two ordered upstream templates</span></span>
```powershell
PS C:\>  Set-AzSignalRUpstream -name pssignalr -ResourceGroupName test_resource_group -Template @{UrlTemplate='http://host-connections1.com'; HubPattern='chat';EventPattern='broadcast' }, @{UrlTemplate='http://host-connections2.com'}

Templates
---------
{Microsoft.Azure.Commands.SignalR.Models.PSUpstreamTemplate, Microsoft.Azure.Commands.SignalR.Models.PSUpstreamTemplat…
```

<span data-ttu-id="cef09-112">Poniższy JSON reprezentuje rzeczywisty zestaw szablonów.</span><span class="sxs-lookup"><span data-stu-id="cef09-112">The following JSON represents the actual templates set.</span></span> 

 `
{
    "hubPattern": "chat",
    "eventPattern": "broadcast",
    "categoryPattern": "*",
    "urlTemplate": "http://host-connections1.com"
},
{
    "hubPattern": "*",
    "eventPattern": "*",
    "categoryPattern": "*",
    "urlTemplate": "http://host-connections2.com"
}
`

### <span data-ttu-id="cef09-113">Wyczyszczenie wszystkich ustawień nadrzędnych</span><span class="sxs-lookup"><span data-stu-id="cef09-113">Clear all the upstream settings</span></span>
```powershell
PS C:\>  Set-AzSignalRUpstream -name pssignalr -ResourceGroupName test_resource_group -Clear

Templates
---------
{}
```

## <span data-ttu-id="cef09-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cef09-114">PARAMETERS</span></span>

### <span data-ttu-id="cef09-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="cef09-115">-AsJob</span></span>
<span data-ttu-id="cef09-116">Uruchom polecenie cmdlet w zadaniu w tle.</span><span class="sxs-lookup"><span data-stu-id="cef09-116">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="cef09-117">— Wyczyść</span><span class="sxs-lookup"><span data-stu-id="cef09-117">-Clear</span></span>
<span data-ttu-id="cef09-118">Wyczyść wszystkie ustawienia nadrzędnego strumienia danych.</span><span class="sxs-lookup"><span data-stu-id="cef09-118">Clear all the upstream settings.</span></span>

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

### <span data-ttu-id="cef09-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cef09-119">-DefaultProfile</span></span>
<span data-ttu-id="cef09-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="cef09-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cef09-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cef09-121">-InputObject</span></span>
<span data-ttu-id="cef09-122">Obiekt zasobu SignalR.</span><span class="sxs-lookup"><span data-stu-id="cef09-122">The SignalR resource object.</span></span>

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

### <span data-ttu-id="cef09-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="cef09-123">-Name</span></span>
<span data-ttu-id="cef09-124">Nazwa usługi SignalR.</span><span class="sxs-lookup"><span data-stu-id="cef09-124">The SignalR service name.</span></span>

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

### <span data-ttu-id="cef09-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cef09-125">-ResourceGroupName</span></span>
<span data-ttu-id="cef09-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cef09-126">The resource group name.</span></span>
<span data-ttu-id="cef09-127">Ustawienie domyślne będzie używane, jeśli nie zostanie określone.</span><span class="sxs-lookup"><span data-stu-id="cef09-127">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="cef09-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cef09-128">-ResourceId</span></span>
<span data-ttu-id="cef09-129">Identyfikator zasobu usługi SignalR.</span><span class="sxs-lookup"><span data-stu-id="cef09-129">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="cef09-130">— Szablon</span><span class="sxs-lookup"><span data-stu-id="cef09-130">-Template</span></span>
<span data-ttu-id="cef09-131">Pozycja szablonu dla ustawień nadrzędnych.</span><span class="sxs-lookup"><span data-stu-id="cef09-131">Template item(s) for upstream settings.</span></span>
<span data-ttu-id="cef09-132">Wymagany klucz: UrlTemplate.</span><span class="sxs-lookup"><span data-stu-id="cef09-132">Required key: UrlTemplate.</span></span>
<span data-ttu-id="cef09-133">Klucze opcjonalne: HubPattern, EventPattern, CategoryPattern.</span><span class="sxs-lookup"><span data-stu-id="cef09-133">Optional keys: HubPattern, EventPattern, CategoryPattern.</span></span>
<span data-ttu-id="cef09-134">Przykład użycia składni splattingu w celu przekazania parametru szablonów: @{UrlTemplate=' http://host-connections1.com ', HubPattern= 'chat'; EventPattern='broadcast' },@{UrlTemplate=' http://host-connections2.com '}</span><span class="sxs-lookup"><span data-stu-id="cef09-134">Example using splatting syntax to pass templates parameter: @{UrlTemplate='http://host-connections1.com', HubPattern= 'chat';EventPattern='broadcast' },@{UrlTemplate='http://host-connections2.com'}</span></span>

```yaml
Type: Microsoft.Azure.Commands.SignalR.Models.PSUpstreamTemplate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cef09-135">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cef09-135">-Confirm</span></span>
<span data-ttu-id="cef09-136">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="cef09-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cef09-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cef09-137">-WhatIf</span></span>
<span data-ttu-id="cef09-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cef09-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cef09-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="cef09-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cef09-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cef09-140">CommonParameters</span></span>
<span data-ttu-id="cef09-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cef09-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cef09-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cef09-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cef09-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cef09-143">INPUTS</span></span>

### <span data-ttu-id="cef09-144">System.String</span><span class="sxs-lookup"><span data-stu-id="cef09-144">System.String</span></span>

## <span data-ttu-id="cef09-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cef09-145">OUTPUTS</span></span>

### <span data-ttu-id="cef09-146">Microsoft.Azure.Commands.SignalR.Models.PSServerlessUpstreamSettings</span><span class="sxs-lookup"><span data-stu-id="cef09-146">Microsoft.Azure.Commands.SignalR.Models.PSServerlessUpstreamSettings</span></span>

## <span data-ttu-id="cef09-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="cef09-147">NOTES</span></span>

## <span data-ttu-id="cef09-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cef09-148">RELATED LINKS</span></span>

[<span data-ttu-id="cef09-149">Jak za pomocą funkcji splatting przekazać parametry do poleceń w programie PowerShell</span><span class="sxs-lookup"><span data-stu-id="cef09-149">How to use splatting to pass parameters to commands in PowerShell</span></span>](https://docs.microsoft.com/powershell/module/microsoft.powershell.core/about/about_splatting?view=powershell-7)
