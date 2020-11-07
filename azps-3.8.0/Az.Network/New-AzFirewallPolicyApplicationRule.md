---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicyapplicationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyApplicationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyApplicationRule.md
ms.openlocfilehash: 1b9fd10e11cb283f880979e7e4a5d703521c9a87
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93894142"
---
# <span data-ttu-id="53e19-101">New-AzFirewallPolicyApplicationRule</span><span class="sxs-lookup"><span data-stu-id="53e19-101">New-AzFirewallPolicyApplicationRule</span></span>

## <span data-ttu-id="53e19-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="53e19-102">SYNOPSIS</span></span>
<span data-ttu-id="53e19-103">Tworzenie nowej reguły aplikacji zasady zapory Azure</span><span class="sxs-lookup"><span data-stu-id="53e19-103">Create a new Azure Firewall Policy Application Rule</span></span>

## <span data-ttu-id="53e19-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="53e19-104">SYNTAX</span></span>

### <span data-ttu-id="53e19-105">TargetFqdn (domyślny)</span><span class="sxs-lookup"><span data-stu-id="53e19-105">TargetFqdn (Default)</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 -TargetFqdn <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="53e19-106">FqdnTag</span><span class="sxs-lookup"><span data-stu-id="53e19-106">FqdnTag</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 -FqdnTag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53e19-107">Opis</span><span class="sxs-lookup"><span data-stu-id="53e19-107">DESCRIPTION</span></span>
<span data-ttu-id="53e19-108">Polecenie cmdlet **New-AzFirewallPolicyApplicationRule** tworzy regułę aplikacji dla zasad zapory platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="53e19-108">The **New-AzFirewallPolicyApplicationRule** cmdlet creates an Application Rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="53e19-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="53e19-109">EXAMPLES</span></span>

### <span data-ttu-id="53e19-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="53e19-110">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyApplicationRule -Name AR1 -SourceAddress "192.168.0.0/16" -Protocol "http:80","https:443" -TargetFqdn "*.ro", "*.com"
```

<span data-ttu-id="53e19-111">W tym przykładzie tworzona jest reguła aplikacji zawierająca adres źródłowy, protokół i docelowe nazwy FQDN.</span><span class="sxs-lookup"><span data-stu-id="53e19-111">This example creates an application rule with the source address, protocol and the target fqdns.</span></span>

## <span data-ttu-id="53e19-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="53e19-112">PARAMETERS</span></span>

### <span data-ttu-id="53e19-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53e19-113">-DefaultProfile</span></span>
<span data-ttu-id="53e19-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="53e19-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53e19-115">— Opis</span><span class="sxs-lookup"><span data-stu-id="53e19-115">-Description</span></span>
<span data-ttu-id="53e19-116">Opis reguły</span><span class="sxs-lookup"><span data-stu-id="53e19-116">The description of the rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53e19-117">-FqdnTag</span><span class="sxs-lookup"><span data-stu-id="53e19-117">-FqdnTag</span></span>
<span data-ttu-id="53e19-118">Tagi FQDN reguły</span><span class="sxs-lookup"><span data-stu-id="53e19-118">The FQDN Tags of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: FqdnTag
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53e19-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="53e19-119">-Name</span></span>
<span data-ttu-id="53e19-120">Nazwa reguły aplikacji</span><span class="sxs-lookup"><span data-stu-id="53e19-120">The name of the Application Rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53e19-121">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="53e19-121">-Protocol</span></span>
<span data-ttu-id="53e19-122">Protokoły reguły</span><span class="sxs-lookup"><span data-stu-id="53e19-122">The protocols of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: TargetFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53e19-123">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="53e19-123">-SourceAddress</span></span>
<span data-ttu-id="53e19-124">Adresy źródłowe reguły</span><span class="sxs-lookup"><span data-stu-id="53e19-124">The source addresses of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53e19-125">-TargetFqdn</span><span class="sxs-lookup"><span data-stu-id="53e19-125">-TargetFqdn</span></span>
<span data-ttu-id="53e19-126">Docelowe nazwy FQDN reguły</span><span class="sxs-lookup"><span data-stu-id="53e19-126">The target FQDNs of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: TargetFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53e19-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="53e19-127">-Confirm</span></span>
<span data-ttu-id="53e19-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53e19-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53e19-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53e19-129">-WhatIf</span></span>
<span data-ttu-id="53e19-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53e19-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53e19-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="53e19-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53e19-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53e19-132">CommonParameters</span></span>
<span data-ttu-id="53e19-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53e19-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53e19-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="53e19-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53e19-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="53e19-135">INPUTS</span></span>

### <span data-ttu-id="53e19-136">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="53e19-136">None</span></span>

## <span data-ttu-id="53e19-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="53e19-137">OUTPUTS</span></span>

### <span data-ttu-id="53e19-138">Microsoft. Azure. Commands. Network. models. PSAzureFirewallPolicyApplicationRule</span><span class="sxs-lookup"><span data-stu-id="53e19-138">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyApplicationRule</span></span>

## <span data-ttu-id="53e19-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="53e19-139">NOTES</span></span>

## <span data-ttu-id="53e19-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="53e19-140">RELATED LINKS</span></span>
