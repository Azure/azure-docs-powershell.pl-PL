---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfirewalldisabledrulegroupconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallDisabledRuleGroupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallDisabledRuleGroupConfig.md
ms.openlocfilehash: 5a96ea5ac1ded346e289d44f54762909d5f96e31
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952193"
---
# <span data-ttu-id="ad535-101">New-AzApplicationGatewayFirewallDisabledRuleGroupConfig</span><span class="sxs-lookup"><span data-stu-id="ad535-101">New-AzApplicationGatewayFirewallDisabledRuleGroupConfig</span></span>

## <span data-ttu-id="ad535-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad535-102">SYNOPSIS</span></span>
<span data-ttu-id="ad535-103">Tworzy nową wyłączono konfigurację grupy reguł.</span><span class="sxs-lookup"><span data-stu-id="ad535-103">Creates a new disabled rule group configuration.</span></span>

## <span data-ttu-id="ad535-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ad535-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName <String> [-Rules <Int32[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad535-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="ad535-105">DESCRIPTION</span></span>
<span data-ttu-id="ad535-106">Polecenie **cmdlet New-AzApplicationGatewayFirewallDisabledRuleGroupConfig** tworzy nową konfigurację wyłączonej grupy reguł.</span><span class="sxs-lookup"><span data-stu-id="ad535-106">The **New-AzApplicationGatewayFirewallDisabledRuleGroupConfig** cmdlet creates a new disabled rule group configuration.</span></span>

## <span data-ttu-id="ad535-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ad535-107">EXAMPLES</span></span>

### <span data-ttu-id="ad535-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ad535-108">Example 1</span></span>
```
PS C:\> $disabledRuleGroup1 = New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-942-APPLICATION-ATTACK-SQLI" -Rules 942130,942140
```

<span data-ttu-id="ad535-109">To polecenie tworzy nową konfigurację wyłączonej grupy reguł dla grupy reguł o nazwie "REQUEST-942-APPLICATION-ATTACK-SQLI" z wyłączonymi regułami 942130 i regułą 942140.</span><span class="sxs-lookup"><span data-stu-id="ad535-109">The command creates a new disabled rule group configuration for the rule group named "REQUEST-942-APPLICATION-ATTACK-SQLI" with rule 942130 and rule 942140 being disabled.</span></span> <span data-ttu-id="ad535-110">Nowa wyłączona konfiguracja grupy reguł zostanie zapisana w $disabledRuleGroup 1.</span><span class="sxs-lookup"><span data-stu-id="ad535-110">The new disabled rule group configuration is saved in $disabledRuleGroup1.</span></span>

## <span data-ttu-id="ad535-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ad535-111">PARAMETERS</span></span>

### <span data-ttu-id="ad535-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad535-112">-DefaultProfile</span></span>
<span data-ttu-id="ad535-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ad535-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad535-114">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="ad535-114">-RuleGroupName</span></span>
<span data-ttu-id="ad535-115">Nazwa grupy reguł, która zostanie wyłączona.</span><span class="sxs-lookup"><span data-stu-id="ad535-115">The name of the rule group that will be disabled.</span></span>

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

### <span data-ttu-id="ad535-116">— Reguły</span><span class="sxs-lookup"><span data-stu-id="ad535-116">-Rules</span></span>
<span data-ttu-id="ad535-117">Lista reguł, które zostaną wyłączone.</span><span class="sxs-lookup"><span data-stu-id="ad535-117">The list of rules that will be disabled.</span></span>
<span data-ttu-id="ad535-118">Jeśli wartość null, wszystkie reguły grupy reguł zostaną wyłączone.</span><span class="sxs-lookup"><span data-stu-id="ad535-118">If null, all rules of the rule group will be disabled.</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad535-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad535-119">CommonParameters</span></span>
<span data-ttu-id="ad535-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad535-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad535-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad535-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad535-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ad535-122">INPUTS</span></span>

### <span data-ttu-id="ad535-123">Brak</span><span class="sxs-lookup"><span data-stu-id="ad535-123">None</span></span>

## <span data-ttu-id="ad535-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ad535-124">OUTPUTS</span></span>

### <span data-ttu-id="ad535-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="ad535-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup</span></span>

## <span data-ttu-id="ad535-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ad535-126">NOTES</span></span>

## <span data-ttu-id="ad535-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ad535-127">RELATED LINKS</span></span>

[<span data-ttu-id="ad535-128">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="ad535-128">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="ad535-129">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="ad535-129">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

