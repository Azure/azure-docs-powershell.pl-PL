---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallexclusionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallExclusionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallExclusionConfig.md
ms.openlocfilehash: 58060c488e778510822d9bc86a21de216447e0f4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709381"
---
# <span data-ttu-id="bee74-101">New-AzApplicationGatewayFirewallExclusionConfig</span><span class="sxs-lookup"><span data-stu-id="bee74-101">New-AzApplicationGatewayFirewallExclusionConfig</span></span>

## <span data-ttu-id="bee74-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bee74-102">SYNOPSIS</span></span>
<span data-ttu-id="bee74-103">Tworzy nową listę reguł wykluczeń dla usługi Application Gateway WAF</span><span class="sxs-lookup"><span data-stu-id="bee74-103">Creates a new exclusion rule list for application gateway waf</span></span>

## <span data-ttu-id="bee74-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bee74-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallExclusionConfig -Variable <String> -Operator <String> -Selector <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bee74-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bee74-105">DESCRIPTION</span></span>
<span data-ttu-id="bee74-106">Polecenie cmdlet **New-AzApplicationGatewayFirewallExclusionConfig** z listą reguł wykluczeń dla bramy Application WAF.</span><span class="sxs-lookup"><span data-stu-id="bee74-106">The **New-AzApplicationGatewayFirewallExclusionConfig** cmdlet a new exclusion rule list for application gateway waf.</span></span>

## <span data-ttu-id="bee74-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bee74-107">EXAMPLES</span></span>

### <span data-ttu-id="bee74-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bee74-108">Example 1</span></span>
```powershell
PS C:\> $exclusion1 = New-AzApplicationGatewayFirewallExclusionConfig -Variable "RequestHeaderNames" -Operator "StartsWith" -Selector "xyz"
```

<span data-ttu-id="bee74-109">To polecenie tworzy nową konfigurację listy reguł wykluczeń dla zmiennej o nazwie RequestHeaderNames oraz operatora o nazwie StartsWith i selektora o nazwie xyz.</span><span class="sxs-lookup"><span data-stu-id="bee74-109">This command creates a new exclusion rule lists configuration for the variable named RequestHeaderNames and operator named StartsWith and Selector named xyz.</span></span> <span data-ttu-id="bee74-110">Konfiguracja listy wykluczeń jest zapisywana w $exclusion 1.</span><span class="sxs-lookup"><span data-stu-id="bee74-110">The exclusion list configuration is saved in $exclusion1.</span></span>

## <span data-ttu-id="bee74-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bee74-111">PARAMETERS</span></span>

### <span data-ttu-id="bee74-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bee74-112">-DefaultProfile</span></span>
<span data-ttu-id="bee74-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bee74-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bee74-114">-Operator</span><span class="sxs-lookup"><span data-stu-id="bee74-114">-Operator</span></span>
<span data-ttu-id="bee74-115">Gdy zmienna jest kolekcją, działa na selektorze w celu określenia, których elementów w kolekcji dotyczy wyłączenie.</span><span class="sxs-lookup"><span data-stu-id="bee74-115">When variable is a collection, operate on the selector to specify which elements in the collection this exclusion applies to.</span></span>

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

### <span data-ttu-id="bee74-116">-Selector</span><span class="sxs-lookup"><span data-stu-id="bee74-116">-Selector</span></span>
<span data-ttu-id="bee74-117">Gdy zmienna jest kolekcją, operator służy do określenia, do których elementów w kolekcji odnosi się wyłączenie.</span><span class="sxs-lookup"><span data-stu-id="bee74-117">When variable is a collection, operator used to specify which elements in the collection this exclusion applies to.</span></span>

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

### <span data-ttu-id="bee74-118">-Zmienna</span><span class="sxs-lookup"><span data-stu-id="bee74-118">-Variable</span></span>
<span data-ttu-id="bee74-119">Zmienna, którą należy wykluczyć.</span><span class="sxs-lookup"><span data-stu-id="bee74-119">The variable to be excluded.</span></span>

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

### <span data-ttu-id="bee74-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bee74-120">CommonParameters</span></span>
<span data-ttu-id="bee74-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bee74-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bee74-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bee74-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bee74-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bee74-123">INPUTS</span></span>

### <span data-ttu-id="bee74-124">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="bee74-124">None</span></span>

## <span data-ttu-id="bee74-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bee74-125">OUTPUTS</span></span>

### <span data-ttu-id="bee74-126">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayFirewallExclusion</span><span class="sxs-lookup"><span data-stu-id="bee74-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallExclusion</span></span>

## <span data-ttu-id="bee74-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bee74-127">NOTES</span></span>

## <span data-ttu-id="bee74-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bee74-128">RELATED LINKS</span></span>
