---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/set-azsignalrupstream
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Set-AzSignalRUpstream.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Set-AzSignalRUpstream.md
ms.openlocfilehash: e04e87067f86f529117512e7443118f308b20547
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98498397"
---
# <span data-ttu-id="2cfaf-101">Set-AzSignalRUpstream</span><span class="sxs-lookup"><span data-stu-id="2cfaf-101">Set-AzSignalRUpstream</span></span>

## <span data-ttu-id="2cfaf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2cfaf-102">SYNOPSIS</span></span>
<span data-ttu-id="2cfaf-103">Ustawianie ustawień przechodzących przez usługę sygnalizującą.</span><span class="sxs-lookup"><span data-stu-id="2cfaf-103">Set the upstream settings of a SignalR service.</span></span>

## <span data-ttu-id="2cfaf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2cfaf-104">SYNTAX</span></span>

### <span data-ttu-id="2cfaf-105">ResourceGroupParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2cfaf-105">ResourceGroupParameterSet (Default)</span></span>
```
Set-AzSignalRUpstream [-ResourceGroupName <String>] [-Name] <String> [-AsJob]
 [-Template <PSUpstreamTemplate[]>] [-Clear] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2cfaf-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2cfaf-106">ResourceIdParameterSet</span></span>
```
Set-AzSignalRUpstream -ResourceId <String> [-AsJob] [-Template <PSUpstreamTemplate[]>] [-Clear]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2cfaf-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2cfaf-107">InputObjectParameterSet</span></span>
```
Set-AzSignalRUpstream -InputObject <PSSignalRResource> [-AsJob] [-Template <PSUpstreamTemplate[]>] [-Clear]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2cfaf-108">Opis</span><span class="sxs-lookup"><span data-stu-id="2cfaf-108">DESCRIPTION</span></span>
<span data-ttu-id="2cfaf-109">Ustawianie ustawień przechodzących przez usługę sygnalizującą.</span><span class="sxs-lookup"><span data-stu-id="2cfaf-109">Set the upstream settings of a SignalR service.</span></span>

## <span data-ttu-id="2cfaf-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2cfaf-110">EXAMPLES</span></span>

### <span data-ttu-id="2cfaf-111">Ustawianie dwóch uporządkowanych szablonów przestrumienia</span><span class="sxs-lookup"><span data-stu-id="2cfaf-111">Set two ordered upstream templates</span></span>
```powershell
PS C:\>  Set-AzSignalRUpstream -name pssignalr -ResourceGroupName test_resource_group -Template @{UrlTemplate='http://host-connections1.com'; HubPattern='chat';EventPattern='broadcast' }, @{UrlTemplate='http://host-connections2.com'}

Templates
---------
{Microsoft.Azure.Commands.SignalR.Models.PSUpstreamTemplate, Microsoft.Azure.Commands.SignalR.Models.PSUpstreamTemplat…
```

<span data-ttu-id="2cfaf-112">Poniższy kod JSON reprezentuje rzeczywisty zestaw szablonów.</span><span class="sxs-lookup"><span data-stu-id="2cfaf-112">The following JSON represents the actual templates set.</span></span> 

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

### <span data-ttu-id="2cfaf-113">Wyczyść wszystkie ustawienia przechodzące</span><span class="sxs-lookup"><span data-stu-id="2cfaf-113">Clear all the upstream settings</span></span>
```powershell
PS C:\>  Set-AzSignalRUpstream -name pssignalr -ResourceGroupName test_resource_group -Clear

Templates
---------
{}
```

## <span data-ttu-id="2cfaf-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2cfaf-114">PARAMETERS</span></span>

### <span data-ttu-id="2cfaf-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2cfaf-115">-AsJob</span></span>
<span data-ttu-id="2cfaf-116">Uruchom polecenie cmdlet w zadaniu w tle.</span><span class="sxs-lookup"><span data-stu-id="2cfaf-116">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="2cfaf-117">-Clear</span><span class="sxs-lookup"><span data-stu-id="2cfaf-117">-Clear</span></span>
<span data-ttu-id="2cfaf-118">Wyczyść wszystkie ustawienia ustawień nadrzędnych.</span><span class="sxs-lookup"><span data-stu-id="2cfaf-118">Clear all the upstream settings.</span></span>

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

### <span data-ttu-id="2cfaf-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cfaf-119">-DefaultProfile</span></span>
<span data-ttu-id="2cfaf-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2cfaf-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2cfaf-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2cfaf-121">-InputObject</span></span>
<span data-ttu-id="2cfaf-122">Obiekt zasobu sygnalizującego.</span><span class="sxs-lookup"><span data-stu-id="2cfaf-122">The SignalR resource object.</span></span>

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

### <span data-ttu-id="2cfaf-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2cfaf-123">-Name</span></span>
<span data-ttu-id="2cfaf-124">Nazwa usługi sygnalizującego.</span><span class="sxs-lookup"><span data-stu-id="2cfaf-124">The SignalR service name.</span></span>

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

### <span data-ttu-id="2cfaf-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cfaf-125">-ResourceGroupName</span></span>
<span data-ttu-id="2cfaf-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2cfaf-126">The resource group name.</span></span>
<span data-ttu-id="2cfaf-127">Jeśli nie podano, zostanie użyte ustawienie domyślne.</span><span class="sxs-lookup"><span data-stu-id="2cfaf-127">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="2cfaf-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2cfaf-128">-ResourceId</span></span>
<span data-ttu-id="2cfaf-129">Identyfikator zasobu usługi sygnalizującego.</span><span class="sxs-lookup"><span data-stu-id="2cfaf-129">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="2cfaf-130">— Szablon</span><span class="sxs-lookup"><span data-stu-id="2cfaf-130">-Template</span></span>
<span data-ttu-id="2cfaf-131">Elementy szablonu dla ustawień odstrumienia.</span><span class="sxs-lookup"><span data-stu-id="2cfaf-131">Template item(s) for upstream settings.</span></span>
<span data-ttu-id="2cfaf-132">Wymagany klucz: UrlTemplate.</span><span class="sxs-lookup"><span data-stu-id="2cfaf-132">Required key: UrlTemplate.</span></span>
<span data-ttu-id="2cfaf-133">Klucze opcjonalne: HubPattern, EventPattern, CategoryPattern.</span><span class="sxs-lookup"><span data-stu-id="2cfaf-133">Optional keys: HubPattern, EventPattern, CategoryPattern.</span></span>
<span data-ttu-id="2cfaf-134">Przykład użycia składni splatting, aby przejść do parametru templates: @ {UrlTemplate = ' http://host-connections1.com ', HubPattern = EventPattern = "broadcast"}, @ {UrlTemplate = ' http://host-connections2.com '}</span><span class="sxs-lookup"><span data-stu-id="2cfaf-134">Example using splatting syntax to pass templates parameter: @{UrlTemplate='http://host-connections1.com', HubPattern= 'chat';EventPattern='broadcast' },@{UrlTemplate='http://host-connections2.com'}</span></span>

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

### <span data-ttu-id="2cfaf-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2cfaf-135">-Confirm</span></span>
<span data-ttu-id="2cfaf-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2cfaf-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2cfaf-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2cfaf-137">-WhatIf</span></span>
<span data-ttu-id="2cfaf-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2cfaf-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2cfaf-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2cfaf-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2cfaf-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cfaf-140">CommonParameters</span></span>
<span data-ttu-id="2cfaf-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cfaf-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cfaf-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2cfaf-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cfaf-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2cfaf-143">INPUTS</span></span>

### <span data-ttu-id="2cfaf-144">System. String</span><span class="sxs-lookup"><span data-stu-id="2cfaf-144">System.String</span></span>

## <span data-ttu-id="2cfaf-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2cfaf-145">OUTPUTS</span></span>

### <span data-ttu-id="2cfaf-146">Microsoft. Azure. Commands. Signals. modele. PSServerlessUpstreamSettings</span><span class="sxs-lookup"><span data-stu-id="2cfaf-146">Microsoft.Azure.Commands.SignalR.Models.PSServerlessUpstreamSettings</span></span>

## <span data-ttu-id="2cfaf-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2cfaf-147">NOTES</span></span>

## <span data-ttu-id="2cfaf-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2cfaf-148">RELATED LINKS</span></span>

[<span data-ttu-id="2cfaf-149">Jak przekazywać parametry do poleceń w programie PowerShell za pomocą splatting</span><span class="sxs-lookup"><span data-stu-id="2cfaf-149">How to use splatting to pass parameters to commands in PowerShell</span></span>](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.core/about/about_splatting?view=powershell-7)
