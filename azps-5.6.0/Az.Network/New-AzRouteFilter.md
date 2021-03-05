---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilter.md
ms.openlocfilehash: 9a262bd5680a9d5cd89d5ec32e3a57edbdaf60f4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982337"
---
# <span data-ttu-id="bbeb2-101">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="bbeb2-101">New-AzRouteFilter</span></span>

## <span data-ttu-id="bbeb2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bbeb2-102">SYNOPSIS</span></span>
<span data-ttu-id="bbeb2-103">Tworzy filtr trasy.</span><span class="sxs-lookup"><span data-stu-id="bbeb2-103">Creates a route filter.</span></span>

## <span data-ttu-id="bbeb2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bbeb2-104">SYNTAX</span></span>

```
New-AzRouteFilter -Name <String> -ResourceGroupName <String> -Location <String> [-Rule <PSRouteFilterRule[]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bbeb2-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="bbeb2-105">DESCRIPTION</span></span>
<span data-ttu-id="bbeb2-106">Polecenie New-AzRouteFilter cmdlet tworzy filtr trasy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="bbeb2-106">The New-AzRouteFilter cmdlet creates an Azure route filter.</span></span>

## <span data-ttu-id="bbeb2-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bbeb2-107">EXAMPLES</span></span>

### <span data-ttu-id="bbeb2-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bbeb2-108">Example 1</span></span>
```powershell
PS C:\> New-AzRouteFilter -Name "MyRouteFilter" -ResourceGroupName "MyResourceGroup" -Location "West US"
```

<span data-ttu-id="bbeb2-109">Polecenie tworzy nowy filtr trasy.</span><span class="sxs-lookup"><span data-stu-id="bbeb2-109">The command creates a new route filter.</span></span>

## <span data-ttu-id="bbeb2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bbeb2-110">PARAMETERS</span></span>

### <span data-ttu-id="bbeb2-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="bbeb2-111">-AsJob</span></span>
<span data-ttu-id="bbeb2-112">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="bbeb2-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bbeb2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbeb2-113">-DefaultProfile</span></span>
<span data-ttu-id="bbeb2-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="bbeb2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bbeb2-115">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="bbeb2-115">-Force</span></span>
<span data-ttu-id="bbeb2-116">Wskazuje, że to polecenie cmdlet tworzy tabelę trasy, nawet jeśli istnieje filtr trasy o takiej samej nazwie.</span><span class="sxs-lookup"><span data-stu-id="bbeb2-116">Indicates that this cmdlet creates a route table even if a route filter that has the same name already exists.</span></span>

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

### <span data-ttu-id="bbeb2-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="bbeb2-117">-Location</span></span>
<span data-ttu-id="bbeb2-118">Określa region platformy Azure, w którym to polecenie cmdlet tworzy filtr trasy.</span><span class="sxs-lookup"><span data-stu-id="bbeb2-118">Specifies the Azure region in which this cmdlet creates a route filter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbeb2-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="bbeb2-119">-Name</span></span>
<span data-ttu-id="bbeb2-120">Określa nazwę filtru trasy.</span><span class="sxs-lookup"><span data-stu-id="bbeb2-120">Specifies a name for the route filter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbeb2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbeb2-121">-ResourceGroupName</span></span>
<span data-ttu-id="bbeb2-122">Określa nazwę grupy zasobów, w której to polecenie cmdlet tworzy filtr trasy.</span><span class="sxs-lookup"><span data-stu-id="bbeb2-122">Specifies the name of the resource group in which this cmdlet creates a route filter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbeb2-123">— reguła</span><span class="sxs-lookup"><span data-stu-id="bbeb2-123">-Rule</span></span>
<span data-ttu-id="bbeb2-124">Określa tablicę obiektów reguły filtrowania trasy do skojarzenia z filtrem trasy.</span><span class="sxs-lookup"><span data-stu-id="bbeb2-124">Specifies an array of Route Filter Rule objects to associate with the route filter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbeb2-125">— Tag</span><span class="sxs-lookup"><span data-stu-id="bbeb2-125">-Tag</span></span>
<span data-ttu-id="bbeb2-126">Pary klucz-wartość w postaci tabeli skrótu.</span><span class="sxs-lookup"><span data-stu-id="bbeb2-126">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="bbeb2-127">Na przykład: @{key0="value0";key1=$null;key2="wartość2"}</span><span class="sxs-lookup"><span data-stu-id="bbeb2-127">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbeb2-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bbeb2-128">-Confirm</span></span>
<span data-ttu-id="bbeb2-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="bbeb2-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bbeb2-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbeb2-130">-WhatIf</span></span>
<span data-ttu-id="bbeb2-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bbeb2-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bbeb2-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="bbeb2-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bbeb2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbeb2-133">CommonParameters</span></span>
<span data-ttu-id="bbeb2-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbeb2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbeb2-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbeb2-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbeb2-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bbeb2-136">INPUTS</span></span>

### <span data-ttu-id="bbeb2-137">System.String</span><span class="sxs-lookup"><span data-stu-id="bbeb2-137">System.String</span></span>

### <span data-ttu-id="bbeb2-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule[]</span><span class="sxs-lookup"><span data-stu-id="bbeb2-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule[]</span></span>

### <span data-ttu-id="bbeb2-139">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="bbeb2-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="bbeb2-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bbeb2-140">OUTPUTS</span></span>

### <span data-ttu-id="bbeb2-141">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="bbeb2-141">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="bbeb2-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bbeb2-142">NOTES</span></span>
<span data-ttu-id="bbeb2-143">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="bbeb2-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="bbeb2-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bbeb2-144">RELATED LINKS</span></span>

[<span data-ttu-id="bbeb2-145">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="bbeb2-145">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="bbeb2-146">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="bbeb2-146">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="bbeb2-147">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="bbeb2-147">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)

[<span data-ttu-id="bbeb2-148">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bbeb2-148">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="bbeb2-149">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bbeb2-149">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="bbeb2-150">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bbeb2-150">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="bbeb2-151">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bbeb2-151">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="bbeb2-152">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bbeb2-152">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
