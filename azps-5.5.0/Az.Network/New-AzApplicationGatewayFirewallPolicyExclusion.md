---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicyexclusion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyExclusion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyExclusion.md
ms.openlocfilehash: e5ad76625a171e1fd12fc583c6ad8acf593ed817
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179778"
---
# <span data-ttu-id="d31c1-101">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="d31c1-101">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>

## <span data-ttu-id="d31c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d31c1-102">SYNOPSIS</span></span>
<span data-ttu-id="d31c1-103">Tworzy wykluczenie z zasad zapory.</span><span class="sxs-lookup"><span data-stu-id="d31c1-103">Creates an exclusion on the Firewall Policy</span></span>

## <span data-ttu-id="d31c1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d31c1-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyExclusion -MatchVariable <String> -SelectorMatchOperator <String>
 -Selector <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d31c1-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d31c1-105">DESCRIPTION</span></span>
<span data-ttu-id="d31c1-106">Polecenie **cmdlet New-AzApplicationGatewayFirewallPolicyExclusion** nowej listy reguł wykluczeń dla zasad zapory.</span><span class="sxs-lookup"><span data-stu-id="d31c1-106">The **New-AzApplicationGatewayFirewallPolicyExclusion** cmdlet a new exclusion rule list for firewall policy.</span></span>

## <span data-ttu-id="d31c1-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d31c1-107">EXAMPLES</span></span>

### <span data-ttu-id="d31c1-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d31c1-108">Example 1</span></span>
```powershell
PS C:\> $exclusionEntry = New-AzApplicationGatewayFirewallPolicyExclusion -MatchVariable "RequestHeaderNames" -SelectorMatchOperator "StartsWith" -Selector "xyz"
```

<span data-ttu-id="d31c1-109">To polecenie tworzy nowy wpis wykluczeń dla zmiennej o nazwach RequestHeaderNames i operatora o nazwach StartsWith i Selector o nazwie xyz.</span><span class="sxs-lookup"><span data-stu-id="d31c1-109">This command creates a new exclusion-entry for the variable named RequestHeaderNames and operator named StartsWith and Selector named xyz.</span></span> <span data-ttu-id="d31c1-110">Wpis wykluczeń zostanie zapisany w $exclusionEntry.</span><span class="sxs-lookup"><span data-stu-id="d31c1-110">The exclusion entry is saved in $exclusionEntry.</span></span>

## <span data-ttu-id="d31c1-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d31c1-111">PARAMETERS</span></span>

### <span data-ttu-id="d31c1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d31c1-112">-DefaultProfile</span></span>
<span data-ttu-id="d31c1-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d31c1-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d31c1-114">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="d31c1-114">-MatchVariable</span></span>
<span data-ttu-id="d31c1-115">Zmienna do wykluczenia.</span><span class="sxs-lookup"><span data-stu-id="d31c1-115">The variable to be excluded.</span></span>

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

### <span data-ttu-id="d31c1-116">— Selektor</span><span class="sxs-lookup"><span data-stu-id="d31c1-116">-Selector</span></span>
<span data-ttu-id="d31c1-117">Jeśli zmienna jest kolekcją, operator używany do określania elementów w kolekcji, których dotyczy to wyłączenie.</span><span class="sxs-lookup"><span data-stu-id="d31c1-117">When variable is a collection, operator used to specify which elements in the collection this exclusion applies to.</span></span>

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

### <span data-ttu-id="d31c1-118">-SelectorMatchOperator</span><span class="sxs-lookup"><span data-stu-id="d31c1-118">-SelectorMatchOperator</span></span>
<span data-ttu-id="d31c1-119">Jeśli zmienna jest kolekcją, operuj na selektorze, aby określić, których elementów w kolekcji dotyczy to wykluczenia.</span><span class="sxs-lookup"><span data-stu-id="d31c1-119">When variable is a collection, operate on the selector to specify which elements in the collection this exclusion applies to.</span></span>

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

### <span data-ttu-id="d31c1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d31c1-120">CommonParameters</span></span>
<span data-ttu-id="d31c1-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d31c1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d31c1-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d31c1-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d31c1-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d31c1-123">INPUTS</span></span>

### <span data-ttu-id="d31c1-124">Brak</span><span class="sxs-lookup"><span data-stu-id="d31c1-124">None</span></span>

## <span data-ttu-id="d31c1-125">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d31c1-125">OUTPUTS</span></span>

### <span data-ttu-id="d31c1-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="d31c1-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyExclusion</span></span>

## <span data-ttu-id="d31c1-127">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d31c1-127">NOTES</span></span>

## <span data-ttu-id="d31c1-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d31c1-128">RELATED LINKS</span></span>
