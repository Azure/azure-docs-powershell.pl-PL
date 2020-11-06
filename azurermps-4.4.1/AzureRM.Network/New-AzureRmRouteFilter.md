---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteFilter.md
ms.openlocfilehash: 6cc420ccb2ba2c7e555956d711fe0e30d02ef62f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543260"
---
# <span data-ttu-id="7d132-101">New-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="7d132-101">New-AzureRmRouteFilter</span></span>

## <span data-ttu-id="7d132-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7d132-102">SYNOPSIS</span></span>
<span data-ttu-id="7d132-103">Tworzy filtr trasy.</span><span class="sxs-lookup"><span data-stu-id="7d132-103">Creates a route filter.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d132-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7d132-104">SYNTAX</span></span>

```
New-AzureRmRouteFilter -Name <String> -ResourceGroupName <String> -Location <String>
 [-Rule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule]>]
 [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7d132-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7d132-105">DESCRIPTION</span></span>
<span data-ttu-id="7d132-106">Polecenie cmdlet New-AzureRmRouteFilter powoduje utworzenie filtru tras platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7d132-106">The New-AzureRmRouteFilter cmdlet creates an Azure route filter.</span></span>

## <span data-ttu-id="7d132-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7d132-107">EXAMPLES</span></span>

### <span data-ttu-id="7d132-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7d132-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

 
<span data-ttu-id="7d132-109">{{Dodaj opis przykładu}}</span><span class="sxs-lookup"><span data-stu-id="7d132-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="7d132-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7d132-110">PARAMETERS</span></span>

### <span data-ttu-id="7d132-111">-Force</span><span class="sxs-lookup"><span data-stu-id="7d132-111">-Force</span></span>
<span data-ttu-id="7d132-112">Wskazuje, że to polecenie cmdlet tworzy tabelę tras, nawet jeśli filtr trasy o takiej samej nazwie już istnieje.</span><span class="sxs-lookup"><span data-stu-id="7d132-112">Indicates that this cmdlet creates a route table even if a route filter that has the same name already exists.</span></span>

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

### <span data-ttu-id="7d132-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="7d132-113">-Location</span></span>
<span data-ttu-id="7d132-114">Określa obszar Azure, w którym to polecenie cmdlet tworzy filtr trasy.</span><span class="sxs-lookup"><span data-stu-id="7d132-114">Specifies the Azure region in which this cmdlet creates a route filter.</span></span>

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

### <span data-ttu-id="7d132-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7d132-115">-Name</span></span>
<span data-ttu-id="7d132-116">Określa nazwę filtru tras.</span><span class="sxs-lookup"><span data-stu-id="7d132-116">Specifies a name for the route filter.</span></span>

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

### <span data-ttu-id="7d132-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d132-117">-ResourceGroupName</span></span>
<span data-ttu-id="7d132-118">Określa nazwę grupy zasobów, w której to polecenie cmdlet tworzy filtr trasy.</span><span class="sxs-lookup"><span data-stu-id="7d132-118">Specifies the name of the resource group in which this cmdlet creates a route filter.</span></span>

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

### <span data-ttu-id="7d132-119">— Reguła</span><span class="sxs-lookup"><span data-stu-id="7d132-119">-Rule</span></span>
<span data-ttu-id="7d132-120">Określa tablicę obiektów reguł filtrowania tras, które mają zostać skojarzone z filtrem tras.</span><span class="sxs-lookup"><span data-stu-id="7d132-120">Specifies an array of Route Filter Rule objects to associate with the route filter.</span></span>

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

### <span data-ttu-id="7d132-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="7d132-121">-Tag</span></span>
<span data-ttu-id="7d132-122">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="7d132-122">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="7d132-123">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="7d132-123">For example:</span></span>

<span data-ttu-id="7d132-124">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="7d132-124">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="7d132-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7d132-125">-Confirm</span></span>
<span data-ttu-id="7d132-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d132-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d132-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d132-127">-WhatIf</span></span>
<span data-ttu-id="7d132-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d132-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7d132-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7d132-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d132-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d132-130">-DefaultProfile</span></span>
<span data-ttu-id="7d132-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7d132-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d132-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d132-132">CommonParameters</span></span>
<span data-ttu-id="7d132-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d132-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d132-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d132-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d132-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7d132-135">INPUTS</span></span>

## <span data-ttu-id="7d132-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7d132-136">OUTPUTS</span></span>

### <span data-ttu-id="7d132-137">Microsoft. Azure. Commands. Network. models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="7d132-137">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="7d132-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7d132-138">NOTES</span></span>
<span data-ttu-id="7d132-139">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking</span><span class="sxs-lookup"><span data-stu-id="7d132-139">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="7d132-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7d132-140">RELATED LINKS</span></span>

[<span data-ttu-id="7d132-141">Get-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="7d132-141">Get-AzureRmRouteFilter</span></span>](./Get-AzureRmRouteFilter.md)

[<span data-ttu-id="7d132-142">Nowe — AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7d132-142">New-AzureRmRouteFilterRuleConfig</span></span>](./New-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="7d132-143">Remove-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="7d132-143">Remove-AzureRmRouteFilter</span></span>](./Remove-AzureRmRouteFilter.md)

[<span data-ttu-id="7d132-144">Set-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="7d132-144">Set-AzureRmRouteFilter</span></span>](./Set-AzureRmRouteFilter.md)
