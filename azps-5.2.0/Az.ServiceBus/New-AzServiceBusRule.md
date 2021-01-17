---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusRule.md
ms.openlocfilehash: d667049fb512545aebfd9681b3ad3d9f44651951
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98367983"
---
# <span data-ttu-id="e4b5e-101">New-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="e4b5e-101">New-AzServiceBusRule</span></span>

## <span data-ttu-id="e4b5e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e4b5e-102">SYNOPSIS</span></span>
<span data-ttu-id="e4b5e-103">Tworzy nową regułę dla danej subskrypcji tematu.</span><span class="sxs-lookup"><span data-stu-id="e4b5e-103">Creates a new rule for a given Subscription of Topic.</span></span> 

## <span data-ttu-id="e4b5e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e4b5e-104">SYNTAX</span></span>

### <span data-ttu-id="e4b5e-105">RulePropertiesSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e4b5e-105">RulePropertiesSet (Default)</span></span>
```
New-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-SqlExpression] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4b5e-106">RuleActionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="e4b5e-106">RuleActionPropertiesSet</span></span>
```
New-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-SqlExpression] <String> -ActionSqlExpression <String>
 [-RequiresPreprocessing] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4b5e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e4b5e-107">DESCRIPTION</span></span>
<span data-ttu-id="e4b5e-108">Polecenie cmdlet **New-AzServiceBusRule** tworzy nową regułę dla danej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e4b5e-108">The **New-AzServiceBusRule** cmdlet Creates a new rule for given subscription.</span></span>

## <span data-ttu-id="e4b5e-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e4b5e-109">EXAMPLES</span></span>

### <span data-ttu-id="e4b5e-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e4b5e-110">Example 1</span></span>
```
PS C:\> New-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -SqlExpression "mysqlexpression='test'"
```

<span data-ttu-id="e4b5e-111">Polecenie cmdlet New-AzServiceBusRule tworzy nową regułę dla określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e4b5e-111">The New-AzServiceBusRule cmdlet creates a new rule for the specified Subscription.</span></span>

### <span data-ttu-id="e4b5e-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="e4b5e-112">Example 2</span></span>
```
PS C:\> New-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -SqlExpression "mysqlexpression='test'" -ActionSqlExpression "SET myAction='test'" -RequiresPreprocessing
```

<span data-ttu-id="e4b5e-113">Polecenie cmdlet New-AzServiceBusRule tworzy nową regułę dla określonego abonamentu z ActionFilter.</span><span class="sxs-lookup"><span data-stu-id="e4b5e-113">The New-AzServiceBusRule cmdlet creates a new rule for the specified Subscription with ActionFilter.</span></span>

## <span data-ttu-id="e4b5e-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e4b5e-114">PARAMETERS</span></span>

### <span data-ttu-id="e4b5e-115">-ActionSqlExpression</span><span class="sxs-lookup"><span data-stu-id="e4b5e-115">-ActionSqlExpression</span></span>
<span data-ttu-id="e4b5e-116">Wyrażenie akcji sqlfilter</span><span class="sxs-lookup"><span data-stu-id="e4b5e-116">Action SqlFilter Expression</span></span>

```yaml
Type: System.String
Parameter Sets: RuleActionPropertiesSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4b5e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4b5e-117">-DefaultProfile</span></span>
<span data-ttu-id="e4b5e-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e4b5e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4b5e-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e4b5e-119">-Name</span></span>
<span data-ttu-id="e4b5e-120">Nazwa reguły</span><span class="sxs-lookup"><span data-stu-id="e4b5e-120">Rule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4b5e-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e4b5e-121">-Namespace</span></span>
<span data-ttu-id="e4b5e-122">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="e4b5e-122">Namespace Name</span></span>

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

### <span data-ttu-id="e4b5e-123">-RequiresPreprocessing</span><span class="sxs-lookup"><span data-stu-id="e4b5e-123">-RequiresPreprocessing</span></span>
<span data-ttu-id="e4b5e-124">Akcja wymaga wstępnego przetwarzania</span><span class="sxs-lookup"><span data-stu-id="e4b5e-124">Action Requires Preprocessing</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RuleActionPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4b5e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4b5e-125">-ResourceGroupName</span></span>
<span data-ttu-id="e4b5e-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="e4b5e-126">The name of the resource group</span></span>

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

### <span data-ttu-id="e4b5e-127">-Sqlexpression</span><span class="sxs-lookup"><span data-stu-id="e4b5e-127">-SqlExpression</span></span>
<span data-ttu-id="e4b5e-128">Wyrażenie filtru SQL</span><span class="sxs-lookup"><span data-stu-id="e4b5e-128">Sql Filter Expression</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4b5e-129">-Subscription</span><span class="sxs-lookup"><span data-stu-id="e4b5e-129">-Subscription</span></span>
<span data-ttu-id="e4b5e-130">Nazwa subskrypcji</span><span class="sxs-lookup"><span data-stu-id="e4b5e-130">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4b5e-131">— Temat</span><span class="sxs-lookup"><span data-stu-id="e4b5e-131">-Topic</span></span>
<span data-ttu-id="e4b5e-132">Nazwa tematu</span><span class="sxs-lookup"><span data-stu-id="e4b5e-132">Topic Name</span></span>

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

### <span data-ttu-id="e4b5e-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e4b5e-133">-Confirm</span></span>
<span data-ttu-id="e4b5e-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4b5e-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4b5e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4b5e-135">-WhatIf</span></span>
<span data-ttu-id="e4b5e-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4b5e-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4b5e-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e4b5e-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4b5e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4b5e-138">CommonParameters</span></span>
<span data-ttu-id="e4b5e-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4b5e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4b5e-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4b5e-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4b5e-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e4b5e-141">INPUTS</span></span>

### <span data-ttu-id="e4b5e-142">System. String</span><span class="sxs-lookup"><span data-stu-id="e4b5e-142">System.String</span></span>

## <span data-ttu-id="e4b5e-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e4b5e-143">OUTPUTS</span></span>

### <span data-ttu-id="e4b5e-144">Microsoft. Azure. Commands. ServiceBus. models. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="e4b5e-144">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="e4b5e-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e4b5e-145">NOTES</span></span>

## <span data-ttu-id="e4b5e-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e4b5e-146">RELATED LINKS</span></span>
