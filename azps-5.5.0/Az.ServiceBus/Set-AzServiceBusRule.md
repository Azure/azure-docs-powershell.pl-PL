---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusRule.md
ms.openlocfilehash: b86b9629062515afb1ee70e7c7372cbc7687bfa5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183498"
---
# <span data-ttu-id="681ed-101">Set-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="681ed-101">Set-AzServiceBusRule</span></span>

## <span data-ttu-id="681ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="681ed-102">SYNOPSIS</span></span>
<span data-ttu-id="681ed-103">Aktualizuje opis określonej reguły dla danej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="681ed-103">Updates the specified rule description for the given subscription.</span></span>

## <span data-ttu-id="681ed-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="681ed-104">SYNTAX</span></span>

```
Set-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-InputObject] <PSRulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="681ed-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="681ed-105">DESCRIPTION</span></span>
<span data-ttu-id="681ed-106">Polecenie **cmdlet Set-AzServiceBusRule** aktualizuje opis określonej reguły danej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="681ed-106">The **Set-AzServiceBusRule** cmdlet updates the description for the specified rule of the given subscription.</span></span>

## <span data-ttu-id="681ed-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="681ed-107">EXAMPLES</span></span>

### <span data-ttu-id="681ed-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="681ed-108">Example 1</span></span>
```
PS C:\> $getRule = Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
PS C:\> $getRule.SqlFilter.SqlExpression = "mysqlexpression='condition'"
PS C:\> $setRule = Set-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -InputObject $getRule
```

<span data-ttu-id="681ed-109">Aktualizuje wyrażenie sql **mysqlexpression='condition'** reguły `SBRule` subskrypcji w `SBSubscription` temacie `SBTopic`</span><span class="sxs-lookup"><span data-stu-id="681ed-109">Updates the sql expression **mysqlexpression='condition'** of the rule `SBRule` of the subscription `SBSubscription` in Topic `SBTopic`</span></span>

## <span data-ttu-id="681ed-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="681ed-110">PARAMETERS</span></span>

### <span data-ttu-id="681ed-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="681ed-111">-DefaultProfile</span></span>
<span data-ttu-id="681ed-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="681ed-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="681ed-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="681ed-113">-InputObject</span></span>
<span data-ttu-id="681ed-114">Definicja reguł usługi ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="681ed-114">ServiceBus Rules definition.</span></span>

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

### <span data-ttu-id="681ed-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="681ed-115">-Name</span></span>
<span data-ttu-id="681ed-116">Nazwa reguły.</span><span class="sxs-lookup"><span data-stu-id="681ed-116">Rule Name.</span></span>

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

### <span data-ttu-id="681ed-117">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="681ed-117">-Namespace</span></span>
<span data-ttu-id="681ed-118">Nazwa przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="681ed-118">Namespace Name.</span></span>

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

### <span data-ttu-id="681ed-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="681ed-119">-ResourceGroupName</span></span>
<span data-ttu-id="681ed-120">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="681ed-120">The name of the resource group</span></span>

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

### <span data-ttu-id="681ed-121">— Subskrypcja</span><span class="sxs-lookup"><span data-stu-id="681ed-121">-Subscription</span></span>
<span data-ttu-id="681ed-122">Nazwa subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="681ed-122">Subscription Name.</span></span>

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

### <span data-ttu-id="681ed-123">— Temat</span><span class="sxs-lookup"><span data-stu-id="681ed-123">-Topic</span></span>
<span data-ttu-id="681ed-124">Nazwa tematu.</span><span class="sxs-lookup"><span data-stu-id="681ed-124">Topic Name.</span></span>

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

### <span data-ttu-id="681ed-125">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="681ed-125">-Confirm</span></span>
<span data-ttu-id="681ed-126">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="681ed-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="681ed-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="681ed-127">-WhatIf</span></span>
<span data-ttu-id="681ed-128">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="681ed-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="681ed-129">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="681ed-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="681ed-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="681ed-130">CommonParameters</span></span>
<span data-ttu-id="681ed-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="681ed-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="681ed-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="681ed-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="681ed-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="681ed-133">INPUTS</span></span>

### <span data-ttu-id="681ed-134">System.String</span><span class="sxs-lookup"><span data-stu-id="681ed-134">System.String</span></span>

### <span data-ttu-id="681ed-135">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="681ed-135">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="681ed-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="681ed-136">OUTPUTS</span></span>

### <span data-ttu-id="681ed-137">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="681ed-137">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="681ed-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="681ed-138">NOTES</span></span>

## <span data-ttu-id="681ed-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="681ed-139">RELATED LINKS</span></span>
