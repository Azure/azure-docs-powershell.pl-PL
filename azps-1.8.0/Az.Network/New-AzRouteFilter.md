---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilter.md
ms.openlocfilehash: b89772c1afe621e456dfb269fe869b6cd3fa8a8c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709247"
---
# <span data-ttu-id="572e7-101">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="572e7-101">New-AzRouteFilter</span></span>

## <span data-ttu-id="572e7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="572e7-102">SYNOPSIS</span></span>
<span data-ttu-id="572e7-103">Tworzy filtr trasy.</span><span class="sxs-lookup"><span data-stu-id="572e7-103">Creates a route filter.</span></span>

## <span data-ttu-id="572e7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="572e7-104">SYNTAX</span></span>

```
New-AzRouteFilter -Name <String> -ResourceGroupName <String> -Location <String> [-Rule <PSRouteFilterRule[]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="572e7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="572e7-105">DESCRIPTION</span></span>
<span data-ttu-id="572e7-106">Polecenie cmdlet New-AzRouteFilter powoduje utworzenie filtru tras platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="572e7-106">The New-AzRouteFilter cmdlet creates an Azure route filter.</span></span>

## <span data-ttu-id="572e7-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="572e7-107">EXAMPLES</span></span>

### <span data-ttu-id="572e7-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="572e7-108">Example 1</span></span>
```powershell
PS C:\> New-AzRouteFilter -Name "MyRouteFilter" -ResourceGroupName "MyResourceGroup" -Location "West US"
```

<span data-ttu-id="572e7-109">Polecenie tworzy nowy filtr tras.</span><span class="sxs-lookup"><span data-stu-id="572e7-109">The command creates a new route filter.</span></span>

## <span data-ttu-id="572e7-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="572e7-110">PARAMETERS</span></span>

### <span data-ttu-id="572e7-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="572e7-111">-AsJob</span></span>
<span data-ttu-id="572e7-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="572e7-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="572e7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="572e7-113">-DefaultProfile</span></span>
<span data-ttu-id="572e7-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="572e7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="572e7-115">-Force</span><span class="sxs-lookup"><span data-stu-id="572e7-115">-Force</span></span>
<span data-ttu-id="572e7-116">Wskazuje, że to polecenie cmdlet tworzy tabelę tras, nawet jeśli filtr trasy o takiej samej nazwie już istnieje.</span><span class="sxs-lookup"><span data-stu-id="572e7-116">Indicates that this cmdlet creates a route table even if a route filter that has the same name already exists.</span></span>

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

### <span data-ttu-id="572e7-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="572e7-117">-Location</span></span>
<span data-ttu-id="572e7-118">Określa obszar Azure, w którym to polecenie cmdlet tworzy filtr trasy.</span><span class="sxs-lookup"><span data-stu-id="572e7-118">Specifies the Azure region in which this cmdlet creates a route filter.</span></span>

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

### <span data-ttu-id="572e7-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="572e7-119">-Name</span></span>
<span data-ttu-id="572e7-120">Określa nazwę filtru tras.</span><span class="sxs-lookup"><span data-stu-id="572e7-120">Specifies a name for the route filter.</span></span>

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

### <span data-ttu-id="572e7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="572e7-121">-ResourceGroupName</span></span>
<span data-ttu-id="572e7-122">Określa nazwę grupy zasobów, w której to polecenie cmdlet tworzy filtr trasy.</span><span class="sxs-lookup"><span data-stu-id="572e7-122">Specifies the name of the resource group in which this cmdlet creates a route filter.</span></span>

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

### <span data-ttu-id="572e7-123">— Reguła</span><span class="sxs-lookup"><span data-stu-id="572e7-123">-Rule</span></span>
<span data-ttu-id="572e7-124">Określa tablicę obiektów reguł filtrowania tras, które mają zostać skojarzone z filtrem tras.</span><span class="sxs-lookup"><span data-stu-id="572e7-124">Specifies an array of Route Filter Rule objects to associate with the route filter.</span></span>

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

### <span data-ttu-id="572e7-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="572e7-125">-Tag</span></span>
<span data-ttu-id="572e7-126">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="572e7-126">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="572e7-127">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="572e7-127">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="572e7-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="572e7-128">-Confirm</span></span>
<span data-ttu-id="572e7-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="572e7-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="572e7-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="572e7-130">-WhatIf</span></span>
<span data-ttu-id="572e7-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="572e7-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="572e7-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="572e7-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="572e7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="572e7-133">CommonParameters</span></span>
<span data-ttu-id="572e7-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="572e7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="572e7-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="572e7-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="572e7-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="572e7-136">INPUTS</span></span>

### <span data-ttu-id="572e7-137">System. String</span><span class="sxs-lookup"><span data-stu-id="572e7-137">System.String</span></span>

### <span data-ttu-id="572e7-138">Microsoft. Azure. Commands. Network. models. PSRouteFilterRule []</span><span class="sxs-lookup"><span data-stu-id="572e7-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule[]</span></span>

### <span data-ttu-id="572e7-139">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="572e7-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="572e7-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="572e7-140">OUTPUTS</span></span>

### <span data-ttu-id="572e7-141">Microsoft. Azure. Commands. Network. models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="572e7-141">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="572e7-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="572e7-142">NOTES</span></span>
<span data-ttu-id="572e7-143">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking</span><span class="sxs-lookup"><span data-stu-id="572e7-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="572e7-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="572e7-144">RELATED LINKS</span></span>

[<span data-ttu-id="572e7-145">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="572e7-145">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="572e7-146">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="572e7-146">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="572e7-147">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="572e7-147">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)

[<span data-ttu-id="572e7-148">Dodaj-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="572e7-148">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="572e7-149">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="572e7-149">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="572e7-150">Nowe — AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="572e7-150">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="572e7-151">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="572e7-151">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="572e7-152">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="572e7-152">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)