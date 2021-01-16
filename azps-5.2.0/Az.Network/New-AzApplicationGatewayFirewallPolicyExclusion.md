---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicyexclusion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyExclusion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyExclusion.md
ms.openlocfilehash: e5ad76625a171e1fd12fc583c6ad8acf593ed817
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98340246"
---
# <span data-ttu-id="3c7b6-101">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="3c7b6-101">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>

## <span data-ttu-id="3c7b6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3c7b6-102">SYNOPSIS</span></span>
<span data-ttu-id="3c7b6-103">Tworzy wykluczenie zasad zapory</span><span class="sxs-lookup"><span data-stu-id="3c7b6-103">Creates an exclusion on the Firewall Policy</span></span>

## <span data-ttu-id="3c7b6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3c7b6-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyExclusion -MatchVariable <String> -SelectorMatchOperator <String>
 -Selector <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3c7b6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3c7b6-105">DESCRIPTION</span></span>
<span data-ttu-id="3c7b6-106">Polecenie cmdlet **New-AzApplicationGatewayFirewallPolicyExclusion** jest listą reguł wykluczeń dla zasad zapory.</span><span class="sxs-lookup"><span data-stu-id="3c7b6-106">The **New-AzApplicationGatewayFirewallPolicyExclusion** cmdlet a new exclusion rule list for firewall policy.</span></span>

## <span data-ttu-id="3c7b6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3c7b6-107">EXAMPLES</span></span>

### <span data-ttu-id="3c7b6-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3c7b6-108">Example 1</span></span>
```powershell
PS C:\> $exclusionEntry = New-AzApplicationGatewayFirewallPolicyExclusion -MatchVariable "RequestHeaderNames" -SelectorMatchOperator "StartsWith" -Selector "xyz"
```

<span data-ttu-id="3c7b6-109">To polecenie tworzy nowy wpis wykluczenia dla zmiennej o nazwie RequestHeaderNames oraz operatora o nazwie StartsWith i selektora o nazwie xyz.</span><span class="sxs-lookup"><span data-stu-id="3c7b6-109">This command creates a new exclusion-entry for the variable named RequestHeaderNames and operator named StartsWith and Selector named xyz.</span></span> <span data-ttu-id="3c7b6-110">Pozycja wykluczenia jest zapisywana w $exclusionEntry.</span><span class="sxs-lookup"><span data-stu-id="3c7b6-110">The exclusion entry is saved in $exclusionEntry.</span></span>

## <span data-ttu-id="3c7b6-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3c7b6-111">PARAMETERS</span></span>

### <span data-ttu-id="3c7b6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c7b6-112">-DefaultProfile</span></span>
<span data-ttu-id="3c7b6-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3c7b6-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c7b6-114">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="3c7b6-114">-MatchVariable</span></span>
<span data-ttu-id="3c7b6-115">Zmienna, którą należy wykluczyć.</span><span class="sxs-lookup"><span data-stu-id="3c7b6-115">The variable to be excluded.</span></span>

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

### <span data-ttu-id="3c7b6-116">-Selector</span><span class="sxs-lookup"><span data-stu-id="3c7b6-116">-Selector</span></span>
<span data-ttu-id="3c7b6-117">Gdy zmienna jest kolekcją, operator służy do określenia, do których elementów w kolekcji odnosi się wyłączenie.</span><span class="sxs-lookup"><span data-stu-id="3c7b6-117">When variable is a collection, operator used to specify which elements in the collection this exclusion applies to.</span></span>

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

### <span data-ttu-id="3c7b6-118">-SelectorMatchOperator</span><span class="sxs-lookup"><span data-stu-id="3c7b6-118">-SelectorMatchOperator</span></span>
<span data-ttu-id="3c7b6-119">Gdy zmienna jest kolekcją, działa na selektorze w celu określenia, których elementów w kolekcji dotyczy wyłączenie.</span><span class="sxs-lookup"><span data-stu-id="3c7b6-119">When variable is a collection, operate on the selector to specify which elements in the collection this exclusion applies to.</span></span>

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

### <span data-ttu-id="3c7b6-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c7b6-120">CommonParameters</span></span>
<span data-ttu-id="3c7b6-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c7b6-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c7b6-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3c7b6-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c7b6-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3c7b6-123">INPUTS</span></span>

### <span data-ttu-id="3c7b6-124">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="3c7b6-124">None</span></span>

## <span data-ttu-id="3c7b6-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3c7b6-125">OUTPUTS</span></span>

### <span data-ttu-id="3c7b6-126">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="3c7b6-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyExclusion</span></span>

## <span data-ttu-id="3c7b6-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3c7b6-127">NOTES</span></span>

## <span data-ttu-id="3c7b6-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3c7b6-128">RELATED LINKS</span></span>
