---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusRule.md
ms.openlocfilehash: d667049fb512545aebfd9681b3ad3d9f44651951
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201651"
---
# <span data-ttu-id="b36b4-101">New-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="b36b4-101">New-AzServiceBusRule</span></span>

## <span data-ttu-id="b36b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b36b4-102">SYNOPSIS</span></span>
<span data-ttu-id="b36b4-103">Tworzy nową regułę dla danej subskrypcji tematu.</span><span class="sxs-lookup"><span data-stu-id="b36b4-103">Creates a new rule for a given Subscription of Topic.</span></span> 

## <span data-ttu-id="b36b4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b36b4-104">SYNTAX</span></span>

### <span data-ttu-id="b36b4-105">RulePropertiesSet (Default)</span><span class="sxs-lookup"><span data-stu-id="b36b4-105">RulePropertiesSet (Default)</span></span>
```
New-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-SqlExpression] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b36b4-106">RuleActionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="b36b4-106">RuleActionPropertiesSet</span></span>
```
New-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-SqlExpression] <String> -ActionSqlExpression <String>
 [-RequiresPreprocessing] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b36b4-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="b36b4-107">DESCRIPTION</span></span>
<span data-ttu-id="b36b4-108">Polecenie **cmdlet New-AzServiceBusRule** tworzy nową regułę dla danej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="b36b4-108">The **New-AzServiceBusRule** cmdlet Creates a new rule for given subscription.</span></span>

## <span data-ttu-id="b36b4-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b36b4-109">EXAMPLES</span></span>

### <span data-ttu-id="b36b4-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b36b4-110">Example 1</span></span>
```
PS C:\> New-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -SqlExpression "mysqlexpression='test'"
```

<span data-ttu-id="b36b4-111">Polecenie New-AzServiceBusRule cmdlet tworzy nową regułę dla określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="b36b4-111">The New-AzServiceBusRule cmdlet creates a new rule for the specified Subscription.</span></span>

### <span data-ttu-id="b36b4-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="b36b4-112">Example 2</span></span>
```
PS C:\> New-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -SqlExpression "mysqlexpression='test'" -ActionSqlExpression "SET myAction='test'" -RequiresPreprocessing
```

<span data-ttu-id="b36b4-113">Polecenie New-AzServiceBusRule cmdlet tworzy nową regułę dla określonej subskrypcji za pomocą Filtru Akcji.</span><span class="sxs-lookup"><span data-stu-id="b36b4-113">The New-AzServiceBusRule cmdlet creates a new rule for the specified Subscription with ActionFilter.</span></span>

## <span data-ttu-id="b36b4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b36b4-114">PARAMETERS</span></span>

### <span data-ttu-id="b36b4-115">-ActionSqlExpression</span><span class="sxs-lookup"><span data-stu-id="b36b4-115">-ActionSqlExpression</span></span>
<span data-ttu-id="b36b4-116">Wyrażenie Action SqlFilter</span><span class="sxs-lookup"><span data-stu-id="b36b4-116">Action SqlFilter Expression</span></span>

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

### <span data-ttu-id="b36b4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b36b4-117">-DefaultProfile</span></span>
<span data-ttu-id="b36b4-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b36b4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b36b4-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b36b4-119">-Name</span></span>
<span data-ttu-id="b36b4-120">Nazwa reguły</span><span class="sxs-lookup"><span data-stu-id="b36b4-120">Rule Name</span></span>

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

### <span data-ttu-id="b36b4-121">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="b36b4-121">-Namespace</span></span>
<span data-ttu-id="b36b4-122">Nazwa przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="b36b4-122">Namespace Name</span></span>

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

### <span data-ttu-id="b36b4-123">— Wymaga Przetworzenia</span><span class="sxs-lookup"><span data-stu-id="b36b4-123">-RequiresPreprocessing</span></span>
<span data-ttu-id="b36b4-124">Akcja wymaga wstępnego przetworzenia</span><span class="sxs-lookup"><span data-stu-id="b36b4-124">Action Requires Preprocessing</span></span>

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

### <span data-ttu-id="b36b4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b36b4-125">-ResourceGroupName</span></span>
<span data-ttu-id="b36b4-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="b36b4-126">The name of the resource group</span></span>

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

### <span data-ttu-id="b36b4-127">-SqlExpression</span><span class="sxs-lookup"><span data-stu-id="b36b4-127">-SqlExpression</span></span>
<span data-ttu-id="b36b4-128">Wyrażenie filtru sql</span><span class="sxs-lookup"><span data-stu-id="b36b4-128">Sql Filter Expression</span></span>

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

### <span data-ttu-id="b36b4-129">— Subskrypcja</span><span class="sxs-lookup"><span data-stu-id="b36b4-129">-Subscription</span></span>
<span data-ttu-id="b36b4-130">Nazwa subskrypcji</span><span class="sxs-lookup"><span data-stu-id="b36b4-130">Subscription Name</span></span>

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

### <span data-ttu-id="b36b4-131">— Temat</span><span class="sxs-lookup"><span data-stu-id="b36b4-131">-Topic</span></span>
<span data-ttu-id="b36b4-132">Nazwa tematu</span><span class="sxs-lookup"><span data-stu-id="b36b4-132">Topic Name</span></span>

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

### <span data-ttu-id="b36b4-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b36b4-133">-Confirm</span></span>
<span data-ttu-id="b36b4-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b36b4-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b36b4-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b36b4-135">-WhatIf</span></span>
<span data-ttu-id="b36b4-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b36b4-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b36b4-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b36b4-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b36b4-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b36b4-138">CommonParameters</span></span>
<span data-ttu-id="b36b4-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b36b4-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b36b4-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b36b4-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b36b4-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b36b4-141">INPUTS</span></span>

### <span data-ttu-id="b36b4-142">System.String</span><span class="sxs-lookup"><span data-stu-id="b36b4-142">System.String</span></span>

## <span data-ttu-id="b36b4-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b36b4-143">OUTPUTS</span></span>

### <span data-ttu-id="b36b4-144">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="b36b4-144">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="b36b4-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b36b4-145">NOTES</span></span>

## <span data-ttu-id="b36b4-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b36b4-146">RELATED LINKS</span></span>
