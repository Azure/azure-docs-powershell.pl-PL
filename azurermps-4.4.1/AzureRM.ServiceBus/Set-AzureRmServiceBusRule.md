---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusRule.md
ms.openlocfilehash: 4fb10e2bb438cbc4f40936f9f9ead5c0bb36d861
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718985"
---
# <span data-ttu-id="aa24e-101">Set-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="aa24e-101">Set-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="aa24e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="aa24e-102">SYNOPSIS</span></span>
<span data-ttu-id="aa24e-103">Umożliwia zaktualizowanie określonego opisu reguły dla danej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="aa24e-103">Updates the specified rule description for the given subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aa24e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="aa24e-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-InputObject] <RulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa24e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="aa24e-105">DESCRIPTION</span></span>
<span data-ttu-id="aa24e-106">Polecenie cmdlet **Set-AzureRmServiceBusRule** umożliwia zaktualizowanie opisu określonej reguły określonego abonamentu.</span><span class="sxs-lookup"><span data-stu-id="aa24e-106">The **Set-AzureRmServiceBusRule** cmdlet updates the description for the specified rule of the given subscription.</span></span>

## <span data-ttu-id="aa24e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="aa24e-107">EXAMPLES</span></span>

### <span data-ttu-id="aa24e-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="aa24e-108">Example 1</span></span>
```
PS C:\> $getRule = Get-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
PS C:\> $getRule.SqlFilter.SqlExpression = "mysqlexpression='condition'"
PS C:\> $setRule = Set-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -InputObject $getRule
```

<span data-ttu-id="aa24e-109">aktualizuje warunek sqlexpression **websqlexpress = '** reguły `SBEule` subskrypcji `SBSubscription` w temacie `SBTopic`</span><span class="sxs-lookup"><span data-stu-id="aa24e-109">updates the sqlexpression **mysqlexpression='condition'** of the rule `SBEule` of the subscription `SBSubscription` in Topic `SBTopic`</span></span>

## <span data-ttu-id="aa24e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="aa24e-110">PARAMETERS</span></span>

### <span data-ttu-id="aa24e-111">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="aa24e-111">-Confirm</span></span>
<span data-ttu-id="aa24e-112">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa24e-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa24e-113">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="aa24e-113">-InputObject</span></span>
<span data-ttu-id="aa24e-114">Definicja reguł ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="aa24e-114">ServiceBus Rules definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.RulesAttributes
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa24e-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="aa24e-115">-Name</span></span>
<span data-ttu-id="aa24e-116">Nazwa reguły.</span><span class="sxs-lookup"><span data-stu-id="aa24e-116">Rule Name.</span></span>

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

### <span data-ttu-id="aa24e-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="aa24e-117">-Namespace</span></span>
<span data-ttu-id="aa24e-118">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="aa24e-118">Namespace Name.</span></span>

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

### <span data-ttu-id="aa24e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa24e-119">-ResourceGroupName</span></span>
<span data-ttu-id="aa24e-120">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="aa24e-120">The name of the resource group</span></span>

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

### <span data-ttu-id="aa24e-121">-Subscription</span><span class="sxs-lookup"><span data-stu-id="aa24e-121">-Subscription</span></span>
<span data-ttu-id="aa24e-122">Nazwa subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="aa24e-122">Subscription Name.</span></span>

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

### <span data-ttu-id="aa24e-123">— Temat</span><span class="sxs-lookup"><span data-stu-id="aa24e-123">-Topic</span></span>
<span data-ttu-id="aa24e-124">Nazwa tematu.</span><span class="sxs-lookup"><span data-stu-id="aa24e-124">Topic Name.</span></span>

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

### <span data-ttu-id="aa24e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa24e-125">-WhatIf</span></span>
<span data-ttu-id="aa24e-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa24e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa24e-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="aa24e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa24e-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa24e-128">-DefaultProfile</span></span>
<span data-ttu-id="aa24e-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="aa24e-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa24e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa24e-130">CommonParameters</span></span>
<span data-ttu-id="aa24e-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa24e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa24e-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa24e-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa24e-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aa24e-133">INPUTS</span></span>

### <span data-ttu-id="aa24e-134">System. String</span><span class="sxs-lookup"><span data-stu-id="aa24e-134">System.String</span></span>
<span data-ttu-id="aa24e-135">Microsoft. Azure. Commands. ServiceBus. models. RulesAttributes</span><span class="sxs-lookup"><span data-stu-id="aa24e-135">Microsoft.Azure.Commands.ServiceBus.Models.RulesAttributes</span></span>

## <span data-ttu-id="aa24e-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="aa24e-136">OUTPUTS</span></span>

### <span data-ttu-id="aa24e-137">Microsoft. Azure. Commands. ServiceBus. models. RulesAttributes</span><span class="sxs-lookup"><span data-stu-id="aa24e-137">Microsoft.Azure.Commands.ServiceBus.Models.RulesAttributes</span></span>

## <span data-ttu-id="aa24e-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="aa24e-138">NOTES</span></span>

## <span data-ttu-id="aa24e-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aa24e-139">RELATED LINKS</span></span>

