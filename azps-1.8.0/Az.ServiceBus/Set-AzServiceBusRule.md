---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusRule.md
ms.openlocfilehash: b6682ae3c35bd16decc6e9e7b1b21de4a9ed42e9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708105"
---
# <span data-ttu-id="1323e-101">Set-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="1323e-101">Set-AzServiceBusRule</span></span>

## <span data-ttu-id="1323e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1323e-102">SYNOPSIS</span></span>
<span data-ttu-id="1323e-103">Umożliwia zaktualizowanie określonego opisu reguły dla danej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="1323e-103">Updates the specified rule description for the given subscription.</span></span>

## <span data-ttu-id="1323e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1323e-104">SYNTAX</span></span>

```
Set-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-InputObject] <PSRulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1323e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1323e-105">DESCRIPTION</span></span>
<span data-ttu-id="1323e-106">Polecenie cmdlet **Set-AzServiceBusRule** umożliwia zaktualizowanie opisu określonej reguły określonego abonamentu.</span><span class="sxs-lookup"><span data-stu-id="1323e-106">The **Set-AzServiceBusRule** cmdlet updates the description for the specified rule of the given subscription.</span></span>

## <span data-ttu-id="1323e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1323e-107">EXAMPLES</span></span>

### <span data-ttu-id="1323e-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1323e-108">Example 1</span></span>
```
PS C:\> $getRule = Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
PS C:\> $getRule.SqlFilter.SqlExpression = "mysqlexpression='condition'"
PS C:\> $setRule = Set-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -InputObject $getRule
```

<span data-ttu-id="1323e-109">aktualizuje warunek sqlexpression **websqlexpress = '** reguły `SBEule` subskrypcji `SBSubscription` w temacie `SBTopic`</span><span class="sxs-lookup"><span data-stu-id="1323e-109">updates the sqlexpression **mysqlexpression='condition'** of the rule `SBEule` of the subscription `SBSubscription` in Topic `SBTopic`</span></span>

## <span data-ttu-id="1323e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1323e-110">PARAMETERS</span></span>

### <span data-ttu-id="1323e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1323e-111">-DefaultProfile</span></span>
<span data-ttu-id="1323e-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1323e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1323e-113">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1323e-113">-InputObject</span></span>
<span data-ttu-id="1323e-114">Definicja reguł ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="1323e-114">ServiceBus Rules definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1323e-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1323e-115">-Name</span></span>
<span data-ttu-id="1323e-116">Nazwa reguły.</span><span class="sxs-lookup"><span data-stu-id="1323e-116">Rule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1323e-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="1323e-117">-Namespace</span></span>
<span data-ttu-id="1323e-118">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="1323e-118">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1323e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1323e-119">-ResourceGroupName</span></span>
<span data-ttu-id="1323e-120">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="1323e-120">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1323e-121">-Subscription</span><span class="sxs-lookup"><span data-stu-id="1323e-121">-Subscription</span></span>
<span data-ttu-id="1323e-122">Nazwa subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="1323e-122">Subscription Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1323e-123">— Temat</span><span class="sxs-lookup"><span data-stu-id="1323e-123">-Topic</span></span>
<span data-ttu-id="1323e-124">Nazwa tematu.</span><span class="sxs-lookup"><span data-stu-id="1323e-124">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1323e-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1323e-125">-Confirm</span></span>
<span data-ttu-id="1323e-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1323e-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1323e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1323e-127">-WhatIf</span></span>
<span data-ttu-id="1323e-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1323e-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1323e-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1323e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1323e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1323e-130">CommonParameters</span></span>
<span data-ttu-id="1323e-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1323e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1323e-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1323e-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1323e-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1323e-133">INPUTS</span></span>

### <span data-ttu-id="1323e-134">System. String</span><span class="sxs-lookup"><span data-stu-id="1323e-134">System.String</span></span>

### <span data-ttu-id="1323e-135">Microsoft. Azure. Commands. ServiceBus. models. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="1323e-135">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="1323e-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1323e-136">OUTPUTS</span></span>

### <span data-ttu-id="1323e-137">Microsoft. Azure. Commands. ServiceBus. models. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="1323e-137">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="1323e-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1323e-138">NOTES</span></span>

## <span data-ttu-id="1323e-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1323e-139">RELATED LINKS</span></span>