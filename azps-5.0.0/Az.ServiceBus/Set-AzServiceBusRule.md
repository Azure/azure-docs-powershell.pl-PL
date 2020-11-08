---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusRule.md
ms.openlocfilehash: b86b9629062515afb1ee70e7c7372cbc7687bfa5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232002"
---
# <span data-ttu-id="a2b34-101">Set-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="a2b34-101">Set-AzServiceBusRule</span></span>

## <span data-ttu-id="a2b34-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a2b34-102">SYNOPSIS</span></span>
<span data-ttu-id="a2b34-103">Umożliwia zaktualizowanie określonego opisu reguły dla danej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="a2b34-103">Updates the specified rule description for the given subscription.</span></span>

## <span data-ttu-id="a2b34-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a2b34-104">SYNTAX</span></span>

```
Set-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-InputObject] <PSRulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2b34-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a2b34-105">DESCRIPTION</span></span>
<span data-ttu-id="a2b34-106">Polecenie cmdlet **Set-AzServiceBusRule** umożliwia zaktualizowanie opisu określonej reguły określonego abonamentu.</span><span class="sxs-lookup"><span data-stu-id="a2b34-106">The **Set-AzServiceBusRule** cmdlet updates the description for the specified rule of the given subscription.</span></span>

## <span data-ttu-id="a2b34-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a2b34-107">EXAMPLES</span></span>

### <span data-ttu-id="a2b34-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a2b34-108">Example 1</span></span>
```
PS C:\> $getRule = Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
PS C:\> $getRule.SqlFilter.SqlExpression = "mysqlexpression='condition'"
PS C:\> $setRule = Set-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -InputObject $getRule
```

<span data-ttu-id="a2b34-109">Aktualizuje wyrażenie SQL, **"warunek"** reguły `SBRule` subskrypcji `SBSubscription` w temacie `SBTopic`</span><span class="sxs-lookup"><span data-stu-id="a2b34-109">Updates the sql expression **mysqlexpression='condition'** of the rule `SBRule` of the subscription `SBSubscription` in Topic `SBTopic`</span></span>

## <span data-ttu-id="a2b34-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a2b34-110">PARAMETERS</span></span>

### <span data-ttu-id="a2b34-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2b34-111">-DefaultProfile</span></span>
<span data-ttu-id="a2b34-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a2b34-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a2b34-113">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a2b34-113">-InputObject</span></span>
<span data-ttu-id="a2b34-114">Definicja reguł ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="a2b34-114">ServiceBus Rules definition.</span></span>

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

### <span data-ttu-id="a2b34-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a2b34-115">-Name</span></span>
<span data-ttu-id="a2b34-116">Nazwa reguły.</span><span class="sxs-lookup"><span data-stu-id="a2b34-116">Rule Name.</span></span>

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

### <span data-ttu-id="a2b34-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a2b34-117">-Namespace</span></span>
<span data-ttu-id="a2b34-118">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="a2b34-118">Namespace Name.</span></span>

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

### <span data-ttu-id="a2b34-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2b34-119">-ResourceGroupName</span></span>
<span data-ttu-id="a2b34-120">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="a2b34-120">The name of the resource group</span></span>

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

### <span data-ttu-id="a2b34-121">-Subscription</span><span class="sxs-lookup"><span data-stu-id="a2b34-121">-Subscription</span></span>
<span data-ttu-id="a2b34-122">Nazwa subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="a2b34-122">Subscription Name.</span></span>

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

### <span data-ttu-id="a2b34-123">— Temat</span><span class="sxs-lookup"><span data-stu-id="a2b34-123">-Topic</span></span>
<span data-ttu-id="a2b34-124">Nazwa tematu.</span><span class="sxs-lookup"><span data-stu-id="a2b34-124">Topic Name.</span></span>

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

### <span data-ttu-id="a2b34-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a2b34-125">-Confirm</span></span>
<span data-ttu-id="a2b34-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a2b34-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2b34-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2b34-127">-WhatIf</span></span>
<span data-ttu-id="a2b34-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a2b34-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2b34-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a2b34-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2b34-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2b34-130">CommonParameters</span></span>
<span data-ttu-id="a2b34-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2b34-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2b34-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2b34-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2b34-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a2b34-133">INPUTS</span></span>

### <span data-ttu-id="a2b34-134">System. String</span><span class="sxs-lookup"><span data-stu-id="a2b34-134">System.String</span></span>

### <span data-ttu-id="a2b34-135">Microsoft. Azure. Commands. ServiceBus. models. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="a2b34-135">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="a2b34-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a2b34-136">OUTPUTS</span></span>

### <span data-ttu-id="a2b34-137">Microsoft. Azure. Commands. ServiceBus. models. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="a2b34-137">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="a2b34-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a2b34-138">NOTES</span></span>

## <span data-ttu-id="a2b34-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a2b34-139">RELATED LINKS</span></span>
