---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermroutefilter
schema: 2.0.0
ms.openlocfilehash: 981ef70f711cf418a92d8fb0caaae22c114f96b9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899105"
---
# <span data-ttu-id="1ca17-101">New-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1ca17-101">New-AzureRmRouteFilter</span></span>

## <span data-ttu-id="1ca17-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1ca17-102">SYNOPSIS</span></span>
<span data-ttu-id="1ca17-103">Tworzy filtr trasy.</span><span class="sxs-lookup"><span data-stu-id="1ca17-103">Creates a route filter.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ca17-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1ca17-104">SYNTAX</span></span>

```
New-AzureRmRouteFilter -Name <String> -ResourceGroupName <String> -Location <String>
 [-Rule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1ca17-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1ca17-105">DESCRIPTION</span></span>
<span data-ttu-id="1ca17-106">Polecenie cmdlet New-AzureRmRouteFilter powoduje utworzenie filtru tras platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1ca17-106">The New-AzureRmRouteFilter cmdlet creates an Azure route filter.</span></span>

## <span data-ttu-id="1ca17-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1ca17-107">EXAMPLES</span></span>

### <span data-ttu-id="1ca17-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1ca17-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

 
<span data-ttu-id="1ca17-109">{{Dodaj opis przykładu}}</span><span class="sxs-lookup"><span data-stu-id="1ca17-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="1ca17-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1ca17-110">PARAMETERS</span></span>

### <span data-ttu-id="1ca17-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1ca17-111">-AsJob</span></span>
<span data-ttu-id="1ca17-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="1ca17-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1ca17-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ca17-113">-DefaultProfile</span></span>
<span data-ttu-id="1ca17-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1ca17-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ca17-115">-Force</span><span class="sxs-lookup"><span data-stu-id="1ca17-115">-Force</span></span>
<span data-ttu-id="1ca17-116">Wskazuje, że to polecenie cmdlet tworzy tabelę tras, nawet jeśli filtr trasy o takiej samej nazwie już istnieje.</span><span class="sxs-lookup"><span data-stu-id="1ca17-116">Indicates that this cmdlet creates a route table even if a route filter that has the same name already exists.</span></span>

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

### <span data-ttu-id="1ca17-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="1ca17-117">-Location</span></span>
<span data-ttu-id="1ca17-118">Określa obszar Azure, w którym to polecenie cmdlet tworzy filtr trasy.</span><span class="sxs-lookup"><span data-stu-id="1ca17-118">Specifies the Azure region in which this cmdlet creates a route filter.</span></span>

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

### <span data-ttu-id="1ca17-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1ca17-119">-Name</span></span>
<span data-ttu-id="1ca17-120">Określa nazwę filtru tras.</span><span class="sxs-lookup"><span data-stu-id="1ca17-120">Specifies a name for the route filter.</span></span>

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

### <span data-ttu-id="1ca17-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ca17-121">-ResourceGroupName</span></span>
<span data-ttu-id="1ca17-122">Określa nazwę grupy zasobów, w której to polecenie cmdlet tworzy filtr trasy.</span><span class="sxs-lookup"><span data-stu-id="1ca17-122">Specifies the name of the resource group in which this cmdlet creates a route filter.</span></span>

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

### <span data-ttu-id="1ca17-123">— Reguła</span><span class="sxs-lookup"><span data-stu-id="1ca17-123">-Rule</span></span>
<span data-ttu-id="1ca17-124">Określa tablicę obiektów reguł filtrowania tras, które mają zostać skojarzone z filtrem tras.</span><span class="sxs-lookup"><span data-stu-id="1ca17-124">Specifies an array of Route Filter Rule objects to associate with the route filter.</span></span>

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

### <span data-ttu-id="1ca17-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="1ca17-125">-Tag</span></span>
<span data-ttu-id="1ca17-126">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="1ca17-126">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="1ca17-127">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="1ca17-127">For example:</span></span>

<span data-ttu-id="1ca17-128">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="1ca17-128">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="1ca17-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1ca17-129">-Confirm</span></span>
<span data-ttu-id="1ca17-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ca17-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ca17-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ca17-131">-WhatIf</span></span>
<span data-ttu-id="1ca17-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ca17-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1ca17-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1ca17-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ca17-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ca17-134">CommonParameters</span></span>
<span data-ttu-id="1ca17-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ca17-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ca17-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ca17-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ca17-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1ca17-137">INPUTS</span></span>

## <span data-ttu-id="1ca17-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1ca17-138">OUTPUTS</span></span>

### <span data-ttu-id="1ca17-139">Microsoft. Azure. Commands. Network. models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1ca17-139">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="1ca17-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1ca17-140">NOTES</span></span>
<span data-ttu-id="1ca17-141">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking</span><span class="sxs-lookup"><span data-stu-id="1ca17-141">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="1ca17-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1ca17-142">RELATED LINKS</span></span>

[<span data-ttu-id="1ca17-143">Get-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1ca17-143">Get-AzureRmRouteFilter</span></span>](./Get-AzureRmRouteFilter.md)

[<span data-ttu-id="1ca17-144">Nowe — AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1ca17-144">New-AzureRmRouteFilterRuleConfig</span></span>](./New-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="1ca17-145">Remove-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1ca17-145">Remove-AzureRmRouteFilter</span></span>](./Remove-AzureRmRouteFilter.md)

[<span data-ttu-id="1ca17-146">Set-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1ca17-146">Set-AzureRmRouteFilter</span></span>](./Set-AzureRmRouteFilter.md)
