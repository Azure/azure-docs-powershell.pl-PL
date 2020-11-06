---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayfirewalldisabledrulegroupconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig.md
ms.openlocfilehash: 780e231f2ca512b5becf0ee068c004dd815cea89
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545551"
---
# <span data-ttu-id="cd235-101">New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig</span><span class="sxs-lookup"><span data-stu-id="cd235-101">New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig</span></span>

## <span data-ttu-id="cd235-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cd235-102">SYNOPSIS</span></span>
<span data-ttu-id="cd235-103">Umożliwia utworzenie nowej wyłączonej konfiguracji grupy reguł.</span><span class="sxs-lookup"><span data-stu-id="cd235-103">Creates a new disabled rule group configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd235-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cd235-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName <String>
 [-Rules <System.Collections.Generic.List`1[System.Int32]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cd235-105">Opis</span><span class="sxs-lookup"><span data-stu-id="cd235-105">DESCRIPTION</span></span>
<span data-ttu-id="cd235-106">Polecenie cmdlet **New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig** tworzy nową konfigurację grupy reguł.</span><span class="sxs-lookup"><span data-stu-id="cd235-106">The **New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig** cmdlet creates a new disabled rule group configuration.</span></span>

## <span data-ttu-id="cd235-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cd235-107">EXAMPLES</span></span>

### <span data-ttu-id="cd235-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cd235-108">Example 1</span></span>
```
PS C:\> $disabledRuleGroup1 = New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-942-APPLICATION-ATTACK-SQLI" -Rules 942130,942140
```

<span data-ttu-id="cd235-109">W poleceniu zostanie utworzona nowa wyłączona Konfiguracja grupy reguł dla grupy reguł o nazwie "REQUEST-942-APPLICATION-ataki-SQLI" z regułą 942130 i zasada 942140 jest wyłączona.</span><span class="sxs-lookup"><span data-stu-id="cd235-109">The command creates a new disabled rule group configuration for the rule group named "REQUEST-942-APPLICATION-ATTACK-SQLI" with rule 942130 and rule 942140 being disabled.</span></span> <span data-ttu-id="cd235-110">Nowa konfiguracja grupy reguł wyłączona jest zapisywana w $disabledRuleGroup 1.</span><span class="sxs-lookup"><span data-stu-id="cd235-110">The new disabled rule group configuration is saved in $disabledRuleGroup1.</span></span>

## <span data-ttu-id="cd235-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cd235-111">PARAMETERS</span></span>

### <span data-ttu-id="cd235-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd235-112">-DefaultProfile</span></span>
<span data-ttu-id="cd235-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cd235-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd235-114">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="cd235-114">-RuleGroupName</span></span>
<span data-ttu-id="cd235-115">Nazwa grupy reguł, która będzie wyłączona.</span><span class="sxs-lookup"><span data-stu-id="cd235-115">The name of the rule group that will be disabled.</span></span>

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

### <span data-ttu-id="cd235-116">— Reguły</span><span class="sxs-lookup"><span data-stu-id="cd235-116">-Rules</span></span>
<span data-ttu-id="cd235-117">Lista reguł, które zostaną wyłączone.</span><span class="sxs-lookup"><span data-stu-id="cd235-117">The list of rules that will be disabled.</span></span>
<span data-ttu-id="cd235-118">Jeśli wartość null, wszystkie reguły grupy reguł zostaną wyłączone.</span><span class="sxs-lookup"><span data-stu-id="cd235-118">If null, all rules of the rule group will be disabled.</span></span>

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

### <span data-ttu-id="cd235-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd235-119">CommonParameters</span></span>
<span data-ttu-id="cd235-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd235-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd235-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd235-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd235-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cd235-122">INPUTS</span></span>

### <span data-ttu-id="cd235-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="cd235-123">None</span></span>

## <span data-ttu-id="cd235-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cd235-124">OUTPUTS</span></span>

### <span data-ttu-id="cd235-125">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayFirewallDisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="cd235-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup</span></span>

## <span data-ttu-id="cd235-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cd235-126">NOTES</span></span>

## <span data-ttu-id="cd235-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cd235-127">RELATED LINKS</span></span>

[<span data-ttu-id="cd235-128">Nowe — AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="cd235-128">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="cd235-129">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="cd235-129">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

