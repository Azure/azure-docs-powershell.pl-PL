---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusRule.md
ms.openlocfilehash: 869bfdaa7ff772980b7acf1caee6c7d6a8784d37
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708146"
---
# <span data-ttu-id="c6365-101">New-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="c6365-101">New-AzServiceBusRule</span></span>

## <span data-ttu-id="c6365-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c6365-102">SYNOPSIS</span></span>
<span data-ttu-id="c6365-103">Tworzy nową regułę dla danej subskrypcji tematu.</span><span class="sxs-lookup"><span data-stu-id="c6365-103">Creates a new rule for a given Subscription of Topic.</span></span> 

## <span data-ttu-id="c6365-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c6365-104">SYNTAX</span></span>

### <span data-ttu-id="c6365-105">RulePropertiesSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c6365-105">RulePropertiesSet (Default)</span></span>
```
New-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-SqlExpression] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6365-106">RuleActionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="c6365-106">RuleActionPropertiesSet</span></span>
```
New-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-SqlExpression] <String> -ActionSqlExpression <String>
 [-RequiresPreprocessing] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6365-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c6365-107">DESCRIPTION</span></span>
<span data-ttu-id="c6365-108">Polecenie cmdlet **New-AzServiceBusRule** tworzy nową regułę dla danej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="c6365-108">The **New-AzServiceBusRule** cmdlet Creates a new rule for given subscription.</span></span>

## <span data-ttu-id="c6365-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c6365-109">EXAMPLES</span></span>

### <span data-ttu-id="c6365-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c6365-110">Example 1</span></span>
```
PS C:\> New-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -SqlExpression "mysqlexpression='test'"
```

<span data-ttu-id="c6365-111">Polecenie cmdlet New-AzServiceBusRule tworzy nową regułę dla określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="c6365-111">The New-AzServiceBusRule cmdlet creates a new rule for the specified Subscription.</span></span>

### <span data-ttu-id="c6365-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="c6365-112">Example 2</span></span>
```
PS C:\> New-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -SqlExpression "mysqlexpression='test'" -ActionSqlExpression "SET myAction='test'" -RequiresPreprocessing
```

<span data-ttu-id="c6365-113">Polecenie cmdlet New-AzServiceBusRule tworzy nową regułę dla określonego abonamentu z ActionFilter.</span><span class="sxs-lookup"><span data-stu-id="c6365-113">The New-AzServiceBusRule cmdlet creates a new rule for the specified Subscription with ActionFilter.</span></span>

## <span data-ttu-id="c6365-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c6365-114">PARAMETERS</span></span>

### <span data-ttu-id="c6365-115">-ActionSqlExpression</span><span class="sxs-lookup"><span data-stu-id="c6365-115">-ActionSqlExpression</span></span>
<span data-ttu-id="c6365-116">Wyrażenie akcji SqlFillter</span><span class="sxs-lookup"><span data-stu-id="c6365-116">Action SqlFillter Expression</span></span>

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

### <span data-ttu-id="c6365-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6365-117">-DefaultProfile</span></span>
<span data-ttu-id="c6365-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c6365-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6365-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c6365-119">-Name</span></span>
<span data-ttu-id="c6365-120">Nazwa reguły</span><span class="sxs-lookup"><span data-stu-id="c6365-120">Rule Name</span></span>

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

### <span data-ttu-id="c6365-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c6365-121">-Namespace</span></span>
<span data-ttu-id="c6365-122">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="c6365-122">Namespace Name</span></span>

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

### <span data-ttu-id="c6365-123">-RequiresPreprocessing</span><span class="sxs-lookup"><span data-stu-id="c6365-123">-RequiresPreprocessing</span></span>
<span data-ttu-id="c6365-124">Akcja wymaga wstępnego przetwarzania</span><span class="sxs-lookup"><span data-stu-id="c6365-124">Action Requires Preprocessing</span></span>

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

### <span data-ttu-id="c6365-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6365-125">-ResourceGroupName</span></span>
<span data-ttu-id="c6365-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="c6365-126">The name of the resource group</span></span>

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

### <span data-ttu-id="c6365-127">-Sqlexpression</span><span class="sxs-lookup"><span data-stu-id="c6365-127">-SqlExpression</span></span>
<span data-ttu-id="c6365-128">Wyrażenie SQL Fillter</span><span class="sxs-lookup"><span data-stu-id="c6365-128">Sql Fillter Expression</span></span>

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

### <span data-ttu-id="c6365-129">-Subscription</span><span class="sxs-lookup"><span data-stu-id="c6365-129">-Subscription</span></span>
<span data-ttu-id="c6365-130">Nazwa subskrypcji</span><span class="sxs-lookup"><span data-stu-id="c6365-130">Subscription Name</span></span>

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

### <span data-ttu-id="c6365-131">— Temat</span><span class="sxs-lookup"><span data-stu-id="c6365-131">-Topic</span></span>
<span data-ttu-id="c6365-132">Nazwa tematu</span><span class="sxs-lookup"><span data-stu-id="c6365-132">Topic Name</span></span>

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

### <span data-ttu-id="c6365-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c6365-133">-Confirm</span></span>
<span data-ttu-id="c6365-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6365-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6365-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6365-135">-WhatIf</span></span>
<span data-ttu-id="c6365-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6365-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6365-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c6365-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6365-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6365-138">CommonParameters</span></span>
<span data-ttu-id="c6365-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6365-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6365-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6365-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6365-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c6365-141">INPUTS</span></span>

### <span data-ttu-id="c6365-142">System. String</span><span class="sxs-lookup"><span data-stu-id="c6365-142">System.String</span></span>

## <span data-ttu-id="c6365-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c6365-143">OUTPUTS</span></span>

### <span data-ttu-id="c6365-144">Microsoft. Azure. Commands. ServiceBus. models. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="c6365-144">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="c6365-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c6365-145">NOTES</span></span>

## <span data-ttu-id="c6365-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c6365-146">RELATED LINKS</span></span>
