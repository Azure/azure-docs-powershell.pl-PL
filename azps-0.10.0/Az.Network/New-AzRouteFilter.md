---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzRouteFilter.md
ms.openlocfilehash: 0b02c1bfbeee6fa3a628ea6ffacd04c15e96a440
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890434"
---
# <span data-ttu-id="7f1f9-101">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="7f1f9-101">New-AzRouteFilter</span></span>

## <span data-ttu-id="7f1f9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7f1f9-102">SYNOPSIS</span></span>
<span data-ttu-id="7f1f9-103">Tworzy filtr trasy.</span><span class="sxs-lookup"><span data-stu-id="7f1f9-103">Creates a route filter.</span></span>

## <span data-ttu-id="7f1f9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7f1f9-104">SYNTAX</span></span>

```
New-AzRouteFilter -Name <String> -ResourceGroupName <String> -Location <String>
 [-Rule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7f1f9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7f1f9-105">DESCRIPTION</span></span>
<span data-ttu-id="7f1f9-106">Polecenie cmdlet New-AzRouteFilter powoduje utworzenie filtru tras platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7f1f9-106">The New-AzRouteFilter cmdlet creates an Azure route filter.</span></span>

## <span data-ttu-id="7f1f9-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7f1f9-107">EXAMPLES</span></span>

### <span data-ttu-id="7f1f9-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7f1f9-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

 
<span data-ttu-id="7f1f9-109">{{Dodaj opis przykładu}}</span><span class="sxs-lookup"><span data-stu-id="7f1f9-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="7f1f9-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7f1f9-110">PARAMETERS</span></span>

### <span data-ttu-id="7f1f9-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7f1f9-111">-AsJob</span></span>
<span data-ttu-id="7f1f9-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="7f1f9-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f1f9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f1f9-113">-DefaultProfile</span></span>
<span data-ttu-id="7f1f9-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7f1f9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f1f9-115">-Force</span><span class="sxs-lookup"><span data-stu-id="7f1f9-115">-Force</span></span>
<span data-ttu-id="7f1f9-116">Wskazuje, że to polecenie cmdlet tworzy tabelę tras, nawet jeśli filtr trasy o takiej samej nazwie już istnieje.</span><span class="sxs-lookup"><span data-stu-id="7f1f9-116">Indicates that this cmdlet creates a route table even if a route filter that has the same name already exists.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f1f9-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="7f1f9-117">-Location</span></span>
<span data-ttu-id="7f1f9-118">Określa obszar Azure, w którym to polecenie cmdlet tworzy filtr trasy.</span><span class="sxs-lookup"><span data-stu-id="7f1f9-118">Specifies the Azure region in which this cmdlet creates a route filter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f1f9-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7f1f9-119">-Name</span></span>
<span data-ttu-id="7f1f9-120">Określa nazwę filtru tras.</span><span class="sxs-lookup"><span data-stu-id="7f1f9-120">Specifies a name for the route filter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f1f9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f1f9-121">-ResourceGroupName</span></span>
<span data-ttu-id="7f1f9-122">Określa nazwę grupy zasobów, w której to polecenie cmdlet tworzy filtr trasy.</span><span class="sxs-lookup"><span data-stu-id="7f1f9-122">Specifies the name of the resource group in which this cmdlet creates a route filter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f1f9-123">— Reguła</span><span class="sxs-lookup"><span data-stu-id="7f1f9-123">-Rule</span></span>
<span data-ttu-id="7f1f9-124">Określa tablicę obiektów reguł filtrowania tras, które mają zostać skojarzone z filtrem tras.</span><span class="sxs-lookup"><span data-stu-id="7f1f9-124">Specifies an array of Route Filter Rule objects to associate with the route filter.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f1f9-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="7f1f9-125">-Tag</span></span>
<span data-ttu-id="7f1f9-126">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="7f1f9-126">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="7f1f9-127">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="7f1f9-127">For example:</span></span>

<span data-ttu-id="7f1f9-128">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="7f1f9-128">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f1f9-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7f1f9-129">-Confirm</span></span>
<span data-ttu-id="7f1f9-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f1f9-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f1f9-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f1f9-131">-WhatIf</span></span>
<span data-ttu-id="7f1f9-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f1f9-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7f1f9-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7f1f9-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f1f9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f1f9-134">CommonParameters</span></span>
<span data-ttu-id="7f1f9-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f1f9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f1f9-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f1f9-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f1f9-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7f1f9-137">INPUTS</span></span>

## <span data-ttu-id="7f1f9-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7f1f9-138">OUTPUTS</span></span>

### <span data-ttu-id="7f1f9-139">Microsoft. Azure. Commands. Network. models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="7f1f9-139">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="7f1f9-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7f1f9-140">NOTES</span></span>
<span data-ttu-id="7f1f9-141">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking</span><span class="sxs-lookup"><span data-stu-id="7f1f9-141">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="7f1f9-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7f1f9-142">RELATED LINKS</span></span>

[<span data-ttu-id="7f1f9-143">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="7f1f9-143">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="7f1f9-144">Nowe — AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7f1f9-144">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="7f1f9-145">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="7f1f9-145">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="7f1f9-146">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="7f1f9-146">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
