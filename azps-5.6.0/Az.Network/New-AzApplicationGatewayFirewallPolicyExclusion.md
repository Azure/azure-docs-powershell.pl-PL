---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfirewallpolicyexclusion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyExclusion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyExclusion.md
ms.openlocfilehash: 04cf39f9c0d8774ffb02688e4edf5804029df669
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974794"
---
# <span data-ttu-id="b97fc-101">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="b97fc-101">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>

## <span data-ttu-id="b97fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b97fc-102">SYNOPSIS</span></span>
<span data-ttu-id="b97fc-103">Tworzy wykluczenie z zasad zapory.</span><span class="sxs-lookup"><span data-stu-id="b97fc-103">Creates an exclusion on the Firewall Policy</span></span>

## <span data-ttu-id="b97fc-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b97fc-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyExclusion -MatchVariable <String> -SelectorMatchOperator <String>
 -Selector <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b97fc-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="b97fc-105">DESCRIPTION</span></span>
<span data-ttu-id="b97fc-106">Polecenie **cmdlet New-AzApplicationGatewayFirewallPolicyExclusion** nowej listy reguł wykluczeń dla zasad zapory.</span><span class="sxs-lookup"><span data-stu-id="b97fc-106">The **New-AzApplicationGatewayFirewallPolicyExclusion** cmdlet a new exclusion rule list for firewall policy.</span></span>

## <span data-ttu-id="b97fc-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b97fc-107">EXAMPLES</span></span>

### <span data-ttu-id="b97fc-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b97fc-108">Example 1</span></span>
```powershell
PS C:\> $exclusionEntry = New-AzApplicationGatewayFirewallPolicyExclusion -MatchVariable "RequestHeaderNames" -SelectorMatchOperator "StartsWith" -Selector "xyz"
```

<span data-ttu-id="b97fc-109">To polecenie tworzy nowy wpis wykluczeń dla zmiennej o nazwach RequestHeaderNames i operatora o nazwach StartsWith i Selector o nazwie xyz.</span><span class="sxs-lookup"><span data-stu-id="b97fc-109">This command creates a new exclusion-entry for the variable named RequestHeaderNames and operator named StartsWith and Selector named xyz.</span></span> <span data-ttu-id="b97fc-110">Wpis wykluczeń zostanie zapisany w $exclusionEntry.</span><span class="sxs-lookup"><span data-stu-id="b97fc-110">The exclusion entry is saved in $exclusionEntry.</span></span>

## <span data-ttu-id="b97fc-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b97fc-111">PARAMETERS</span></span>

### <span data-ttu-id="b97fc-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b97fc-112">-DefaultProfile</span></span>
<span data-ttu-id="b97fc-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b97fc-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b97fc-114">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="b97fc-114">-MatchVariable</span></span>
<span data-ttu-id="b97fc-115">Zmienna do wykluczenia.</span><span class="sxs-lookup"><span data-stu-id="b97fc-115">The variable to be excluded.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RequestHeaderNames, RequestCookieNames, RequestArgNames

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b97fc-116">— Selektor</span><span class="sxs-lookup"><span data-stu-id="b97fc-116">-Selector</span></span>
<span data-ttu-id="b97fc-117">Jeśli zmienna jest kolekcją, operator używany do określania elementów w kolekcji, których dotyczy to wyłączenie.</span><span class="sxs-lookup"><span data-stu-id="b97fc-117">When variable is a collection, operator used to specify which elements in the collection this exclusion applies to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b97fc-118">-SelectorMatchOperator</span><span class="sxs-lookup"><span data-stu-id="b97fc-118">-SelectorMatchOperator</span></span>
<span data-ttu-id="b97fc-119">Jeśli zmienna jest kolekcją, operuj na selektorze, aby określić, których elementów w kolekcji dotyczy to wykluczenia.</span><span class="sxs-lookup"><span data-stu-id="b97fc-119">When variable is a collection, operate on the selector to specify which elements in the collection this exclusion applies to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Equals, Contains, StartsWith, EndsWith, EqualsAny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b97fc-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b97fc-120">CommonParameters</span></span>
<span data-ttu-id="b97fc-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b97fc-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b97fc-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b97fc-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b97fc-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b97fc-123">INPUTS</span></span>

### <span data-ttu-id="b97fc-124">Brak</span><span class="sxs-lookup"><span data-stu-id="b97fc-124">None</span></span>

## <span data-ttu-id="b97fc-125">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b97fc-125">OUTPUTS</span></span>

### <span data-ttu-id="b97fc-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="b97fc-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyExclusion</span></span>

## <span data-ttu-id="b97fc-127">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b97fc-127">NOTES</span></span>

## <span data-ttu-id="b97fc-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b97fc-128">RELATED LINKS</span></span>
