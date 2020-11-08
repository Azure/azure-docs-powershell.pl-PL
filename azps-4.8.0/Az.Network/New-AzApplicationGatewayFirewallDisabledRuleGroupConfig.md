---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewalldisabledrulegroupconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallDisabledRuleGroupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallDisabledRuleGroupConfig.md
ms.openlocfilehash: 5eafcfc825b710e31954e247e4114d0f90e97c41
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221995"
---
# <span data-ttu-id="fb493-101">New-AzApplicationGatewayFirewallDisabledRuleGroupConfig</span><span class="sxs-lookup"><span data-stu-id="fb493-101">New-AzApplicationGatewayFirewallDisabledRuleGroupConfig</span></span>

## <span data-ttu-id="fb493-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fb493-102">SYNOPSIS</span></span>
<span data-ttu-id="fb493-103">Umożliwia utworzenie nowej wyłączonej konfiguracji grupy reguł.</span><span class="sxs-lookup"><span data-stu-id="fb493-103">Creates a new disabled rule group configuration.</span></span>

## <span data-ttu-id="fb493-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fb493-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName <String> [-Rules <Int32[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb493-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fb493-105">DESCRIPTION</span></span>
<span data-ttu-id="fb493-106">Polecenie cmdlet **New-AzApplicationGatewayFirewallDisabledRuleGroupConfig** tworzy nową konfigurację grupy reguł.</span><span class="sxs-lookup"><span data-stu-id="fb493-106">The **New-AzApplicationGatewayFirewallDisabledRuleGroupConfig** cmdlet creates a new disabled rule group configuration.</span></span>

## <span data-ttu-id="fb493-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fb493-107">EXAMPLES</span></span>

### <span data-ttu-id="fb493-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fb493-108">Example 1</span></span>
```
PS C:\> $disabledRuleGroup1 = New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-942-APPLICATION-ATTACK-SQLI" -Rules 942130,942140
```

<span data-ttu-id="fb493-109">W poleceniu zostanie utworzona nowa wyłączona Konfiguracja grupy reguł dla grupy reguł o nazwie "REQUEST-942-APPLICATION-ataki-SQLI" z regułą 942130 i zasada 942140 jest wyłączona.</span><span class="sxs-lookup"><span data-stu-id="fb493-109">The command creates a new disabled rule group configuration for the rule group named "REQUEST-942-APPLICATION-ATTACK-SQLI" with rule 942130 and rule 942140 being disabled.</span></span> <span data-ttu-id="fb493-110">Nowa konfiguracja grupy reguł wyłączona jest zapisywana w $disabledRuleGroup 1.</span><span class="sxs-lookup"><span data-stu-id="fb493-110">The new disabled rule group configuration is saved in $disabledRuleGroup1.</span></span>

## <span data-ttu-id="fb493-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fb493-111">PARAMETERS</span></span>

### <span data-ttu-id="fb493-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb493-112">-DefaultProfile</span></span>
<span data-ttu-id="fb493-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fb493-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb493-114">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="fb493-114">-RuleGroupName</span></span>
<span data-ttu-id="fb493-115">Nazwa grupy reguł, która będzie wyłączona.</span><span class="sxs-lookup"><span data-stu-id="fb493-115">The name of the rule group that will be disabled.</span></span>

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

### <span data-ttu-id="fb493-116">— Reguły</span><span class="sxs-lookup"><span data-stu-id="fb493-116">-Rules</span></span>
<span data-ttu-id="fb493-117">Lista reguł, które zostaną wyłączone.</span><span class="sxs-lookup"><span data-stu-id="fb493-117">The list of rules that will be disabled.</span></span>
<span data-ttu-id="fb493-118">Jeśli wartość null, wszystkie reguły grupy reguł zostaną wyłączone.</span><span class="sxs-lookup"><span data-stu-id="fb493-118">If null, all rules of the rule group will be disabled.</span></span>

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

### <span data-ttu-id="fb493-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb493-119">CommonParameters</span></span>
<span data-ttu-id="fb493-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb493-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb493-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb493-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb493-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fb493-122">INPUTS</span></span>

### <span data-ttu-id="fb493-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="fb493-123">None</span></span>

## <span data-ttu-id="fb493-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fb493-124">OUTPUTS</span></span>

### <span data-ttu-id="fb493-125">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayFirewallDisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="fb493-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup</span></span>

## <span data-ttu-id="fb493-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fb493-126">NOTES</span></span>

## <span data-ttu-id="fb493-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fb493-127">RELATED LINKS</span></span>

[<span data-ttu-id="fb493-128">Nowe — AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="fb493-128">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="fb493-129">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="fb493-129">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

