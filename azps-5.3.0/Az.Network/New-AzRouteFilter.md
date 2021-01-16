---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilter.md
ms.openlocfilehash: 8be04cd9e483e990d73130866779710bbed879bb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490966"
---
# <span data-ttu-id="9b7c3-101">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="9b7c3-101">New-AzRouteFilter</span></span>

## <span data-ttu-id="9b7c3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9b7c3-102">SYNOPSIS</span></span>
<span data-ttu-id="9b7c3-103">Tworzy filtr trasy.</span><span class="sxs-lookup"><span data-stu-id="9b7c3-103">Creates a route filter.</span></span>

## <span data-ttu-id="9b7c3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9b7c3-104">SYNTAX</span></span>

```
New-AzRouteFilter -Name <String> -ResourceGroupName <String> -Location <String> [-Rule <PSRouteFilterRule[]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9b7c3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9b7c3-105">DESCRIPTION</span></span>
<span data-ttu-id="9b7c3-106">Polecenie cmdlet New-AzRouteFilter powoduje utworzenie filtru tras platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9b7c3-106">The New-AzRouteFilter cmdlet creates an Azure route filter.</span></span>

## <span data-ttu-id="9b7c3-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9b7c3-107">EXAMPLES</span></span>

### <span data-ttu-id="9b7c3-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9b7c3-108">Example 1</span></span>
```powershell
PS C:\> New-AzRouteFilter -Name "MyRouteFilter" -ResourceGroupName "MyResourceGroup" -Location "West US"
```

<span data-ttu-id="9b7c3-109">Polecenie tworzy nowy filtr tras.</span><span class="sxs-lookup"><span data-stu-id="9b7c3-109">The command creates a new route filter.</span></span>

## <span data-ttu-id="9b7c3-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9b7c3-110">PARAMETERS</span></span>

### <span data-ttu-id="9b7c3-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9b7c3-111">-AsJob</span></span>
<span data-ttu-id="9b7c3-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="9b7c3-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9b7c3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b7c3-113">-DefaultProfile</span></span>
<span data-ttu-id="9b7c3-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9b7c3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b7c3-115">-Force</span><span class="sxs-lookup"><span data-stu-id="9b7c3-115">-Force</span></span>
<span data-ttu-id="9b7c3-116">Wskazuje, że to polecenie cmdlet tworzy tabelę tras, nawet jeśli filtr trasy o takiej samej nazwie już istnieje.</span><span class="sxs-lookup"><span data-stu-id="9b7c3-116">Indicates that this cmdlet creates a route table even if a route filter that has the same name already exists.</span></span>

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

### <span data-ttu-id="9b7c3-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="9b7c3-117">-Location</span></span>
<span data-ttu-id="9b7c3-118">Określa obszar Azure, w którym to polecenie cmdlet tworzy filtr trasy.</span><span class="sxs-lookup"><span data-stu-id="9b7c3-118">Specifies the Azure region in which this cmdlet creates a route filter.</span></span>

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

### <span data-ttu-id="9b7c3-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9b7c3-119">-Name</span></span>
<span data-ttu-id="9b7c3-120">Określa nazwę filtru tras.</span><span class="sxs-lookup"><span data-stu-id="9b7c3-120">Specifies a name for the route filter.</span></span>

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

### <span data-ttu-id="9b7c3-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b7c3-121">-ResourceGroupName</span></span>
<span data-ttu-id="9b7c3-122">Określa nazwę grupy zasobów, w której to polecenie cmdlet tworzy filtr trasy.</span><span class="sxs-lookup"><span data-stu-id="9b7c3-122">Specifies the name of the resource group in which this cmdlet creates a route filter.</span></span>

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

### <span data-ttu-id="9b7c3-123">— Reguła</span><span class="sxs-lookup"><span data-stu-id="9b7c3-123">-Rule</span></span>
<span data-ttu-id="9b7c3-124">Określa tablicę obiektów reguł filtrowania tras, które mają zostać skojarzone z filtrem tras.</span><span class="sxs-lookup"><span data-stu-id="9b7c3-124">Specifies an array of Route Filter Rule objects to associate with the route filter.</span></span>

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

### <span data-ttu-id="9b7c3-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="9b7c3-125">-Tag</span></span>
<span data-ttu-id="9b7c3-126">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="9b7c3-126">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="9b7c3-127">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="9b7c3-127">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="9b7c3-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9b7c3-128">-Confirm</span></span>
<span data-ttu-id="9b7c3-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b7c3-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b7c3-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b7c3-130">-WhatIf</span></span>
<span data-ttu-id="9b7c3-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b7c3-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9b7c3-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9b7c3-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b7c3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b7c3-133">CommonParameters</span></span>
<span data-ttu-id="9b7c3-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b7c3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b7c3-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b7c3-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b7c3-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9b7c3-136">INPUTS</span></span>

### <span data-ttu-id="9b7c3-137">System. String</span><span class="sxs-lookup"><span data-stu-id="9b7c3-137">System.String</span></span>

### <span data-ttu-id="9b7c3-138">Microsoft. Azure. Commands. Network. models. PSRouteFilterRule []</span><span class="sxs-lookup"><span data-stu-id="9b7c3-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule[]</span></span>

### <span data-ttu-id="9b7c3-139">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="9b7c3-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="9b7c3-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9b7c3-140">OUTPUTS</span></span>

### <span data-ttu-id="9b7c3-141">Microsoft. Azure. Commands. Network. models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="9b7c3-141">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="9b7c3-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9b7c3-142">NOTES</span></span>
<span data-ttu-id="9b7c3-143">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking</span><span class="sxs-lookup"><span data-stu-id="9b7c3-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="9b7c3-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9b7c3-144">RELATED LINKS</span></span>

[<span data-ttu-id="9b7c3-145">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="9b7c3-145">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="9b7c3-146">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="9b7c3-146">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="9b7c3-147">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="9b7c3-147">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)

[<span data-ttu-id="9b7c3-148">Dodaj-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9b7c3-148">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="9b7c3-149">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9b7c3-149">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="9b7c3-150">Nowe — AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9b7c3-150">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="9b7c3-151">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9b7c3-151">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="9b7c3-152">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9b7c3-152">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
