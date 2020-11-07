---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewalldisabledrulegroupconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayFirewallDisabledRuleGroupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayFirewallDisabledRuleGroupConfig.md
ms.openlocfilehash: 5377eabbf027adf18c88204bef6be59c7cf411be
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890590"
---
# <span data-ttu-id="2ff4c-101">New-AzApplicationGatewayFirewallDisabledRuleGroupConfig</span><span class="sxs-lookup"><span data-stu-id="2ff4c-101">New-AzApplicationGatewayFirewallDisabledRuleGroupConfig</span></span>

## <span data-ttu-id="2ff4c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2ff4c-102">SYNOPSIS</span></span>
<span data-ttu-id="2ff4c-103">Umożliwia utworzenie nowej wyłączonej konfiguracji grupy reguł.</span><span class="sxs-lookup"><span data-stu-id="2ff4c-103">Creates a new disabled rule group configuration.</span></span>

## <span data-ttu-id="2ff4c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2ff4c-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName <String>
 [-Rules <System.Collections.Generic.List`1[System.Int32]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2ff4c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2ff4c-105">DESCRIPTION</span></span>
<span data-ttu-id="2ff4c-106">Polecenie cmdlet **New-AzApplicationGatewayFirewallDisabledRuleGroupConfig** tworzy nową konfigurację grupy reguł.</span><span class="sxs-lookup"><span data-stu-id="2ff4c-106">The **New-AzApplicationGatewayFirewallDisabledRuleGroupConfig** cmdlet creates a new disabled rule group configuration.</span></span>

## <span data-ttu-id="2ff4c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2ff4c-107">EXAMPLES</span></span>

### <span data-ttu-id="2ff4c-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2ff4c-108">Example 1</span></span>
```
PS C:\> $disabledRuleGroup1 = New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-942-APPLICATION-ATTACK-SQLI" -Rules 942130,942140
```

<span data-ttu-id="2ff4c-109">W poleceniu zostanie utworzona nowa wyłączona Konfiguracja grupy reguł dla grupy reguł o nazwie "REQUEST-942-APPLICATION-ataki-SQLI" z regułą 942130 i zasada 942140 jest wyłączona.</span><span class="sxs-lookup"><span data-stu-id="2ff4c-109">The command creates a new disabled rule group configuration for the rule group named "REQUEST-942-APPLICATION-ATTACK-SQLI" with rule 942130 and rule 942140 being disabled.</span></span> <span data-ttu-id="2ff4c-110">Nowa konfiguracja grupy reguł wyłączona jest zapisywana w $disabledRuleGroup 1.</span><span class="sxs-lookup"><span data-stu-id="2ff4c-110">The new disabled rule group configuration is saved in $disabledRuleGroup1.</span></span>

## <span data-ttu-id="2ff4c-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2ff4c-111">PARAMETERS</span></span>

### <span data-ttu-id="2ff4c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ff4c-112">-DefaultProfile</span></span>
<span data-ttu-id="2ff4c-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2ff4c-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ff4c-114">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="2ff4c-114">-RuleGroupName</span></span>
<span data-ttu-id="2ff4c-115">Nazwa grupy reguł, która będzie wyłączona.</span><span class="sxs-lookup"><span data-stu-id="2ff4c-115">The name of the rule group that will be disabled.</span></span>

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

### <span data-ttu-id="2ff4c-116">— Reguły</span><span class="sxs-lookup"><span data-stu-id="2ff4c-116">-Rules</span></span>
<span data-ttu-id="2ff4c-117">Lista reguł, które zostaną wyłączone.</span><span class="sxs-lookup"><span data-stu-id="2ff4c-117">The list of rules that will be disabled.</span></span>
<span data-ttu-id="2ff4c-118">Jeśli wartość null, wszystkie reguły grupy reguł zostaną wyłączone.</span><span class="sxs-lookup"><span data-stu-id="2ff4c-118">If null, all rules of the rule group will be disabled.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ff4c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ff4c-119">CommonParameters</span></span>
<span data-ttu-id="2ff4c-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ff4c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ff4c-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ff4c-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ff4c-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2ff4c-122">INPUTS</span></span>

### <span data-ttu-id="2ff4c-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="2ff4c-123">None</span></span>

## <span data-ttu-id="2ff4c-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2ff4c-124">OUTPUTS</span></span>

### <span data-ttu-id="2ff4c-125">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayFirewallDisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="2ff4c-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup</span></span>

## <span data-ttu-id="2ff4c-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2ff4c-126">NOTES</span></span>

## <span data-ttu-id="2ff4c-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2ff4c-127">RELATED LINKS</span></span>

[<span data-ttu-id="2ff4c-128">Nowe — AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="2ff4c-128">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="2ff4c-129">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="2ff4c-129">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

