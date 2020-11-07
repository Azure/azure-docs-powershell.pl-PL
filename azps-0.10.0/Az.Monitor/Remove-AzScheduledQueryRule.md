---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Remove-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Remove-AzScheduledQueryRule.md
ms.openlocfilehash: 689588e8b92b4b76c97f3972aa63c2f8cdc16535
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891073"
---
# <span data-ttu-id="9ff9c-101">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="9ff9c-101">Remove-AzScheduledQueryRule</span></span>

## <span data-ttu-id="9ff9c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9ff9c-102">SYNOPSIS</span></span>
<span data-ttu-id="9ff9c-103">Usuwanie reguły alertów dziennika</span><span class="sxs-lookup"><span data-stu-id="9ff9c-103">Removes a Log Alert Rule</span></span>

## <span data-ttu-id="9ff9c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9ff9c-104">SYNTAX</span></span>

### <span data-ttu-id="9ff9c-105">ByRuleName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9ff9c-105">ByRuleName (Default)</span></span>
```
Remove-AzScheduledQueryRule -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ff9c-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="9ff9c-106">ByInputObject</span></span>
```
Remove-AzScheduledQueryRule -InputObject <PSScheduledQueryRuleResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ff9c-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9ff9c-107">ByResourceId</span></span>
```
Remove-AzScheduledQueryRule -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ff9c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="9ff9c-108">DESCRIPTION</span></span>
<span data-ttu-id="9ff9c-109">Usuwanie reguły alertów dziennika</span><span class="sxs-lookup"><span data-stu-id="9ff9c-109">Removes a Log Alert Rule</span></span>

## <span data-ttu-id="9ff9c-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9ff9c-110">EXAMPLES</span></span>

### <span data-ttu-id="9ff9c-111">Przykład 1-Usuń według nazwy reguły</span><span class="sxs-lookup"><span data-stu-id="9ff9c-111">Example 1 - Remove by rule name</span></span>
```powershell
PS C:\> Remove-AzScheduledQueryRule -ResourceGroupName "MyResourceGroup" -Name "LogAlertRule1"
```

### <span data-ttu-id="9ff9c-112">Przykład 2 — Usuwanie przez obiekt wejściowy</span><span class="sxs-lookup"><span data-stu-id="9ff9c-112">Example 2 - Remove by input object</span></span>
```powershell
PS C:\> Remove-AzScheduledQueryRule -InputObject $PSScheduledQueryRuleResource
```

### <span data-ttu-id="9ff9c-113">Przykład 3 — Usuwanie według identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="9ff9c-113">Example 3 - Remove by resource Id</span></span>
```powershell
PS C:\> Remove-AzScheduledQueryRule -ResourceId "/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledQueryRules/LogAlertRule1"
```

## <span data-ttu-id="9ff9c-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9ff9c-114">PARAMETERS</span></span>

### <span data-ttu-id="9ff9c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ff9c-115">-DefaultProfile</span></span>
<span data-ttu-id="9ff9c-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9ff9c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ff9c-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9ff9c-117">-InputObject</span></span>
<span data-ttu-id="9ff9c-118">Zasób reguły zaplanowanego zapytania</span><span class="sxs-lookup"><span data-stu-id="9ff9c-118">The Scheduled Query Rule resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9ff9c-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9ff9c-119">-Name</span></span>
<span data-ttu-id="9ff9c-120">Nazwa alertu</span><span class="sxs-lookup"><span data-stu-id="9ff9c-120">The alert name</span></span>

```yaml
Type: System.String
Parameter Sets: ByRuleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ff9c-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9ff9c-121">-PassThru</span></span>
<span data-ttu-id="9ff9c-122">Zwraca wartość oznaczającą sukces lub niepowodzenie.</span><span class="sxs-lookup"><span data-stu-id="9ff9c-122">Return a value indicating success or failure.</span></span>
<span data-ttu-id="9ff9c-123">To polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="9ff9c-123">This cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ff9c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ff9c-124">-ResourceGroupName</span></span>
<span data-ttu-id="9ff9c-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="9ff9c-125">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByRuleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ff9c-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9ff9c-126">-ResourceId</span></span>
<span data-ttu-id="9ff9c-127">Identyfikator zasobu</span><span class="sxs-lookup"><span data-stu-id="9ff9c-127">The resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ff9c-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9ff9c-128">-Confirm</span></span>
<span data-ttu-id="9ff9c-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ff9c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ff9c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ff9c-130">-WhatIf</span></span>
<span data-ttu-id="9ff9c-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ff9c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ff9c-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9ff9c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ff9c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ff9c-133">CommonParameters</span></span>
<span data-ttu-id="9ff9c-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ff9c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ff9c-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9ff9c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ff9c-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9ff9c-136">INPUTS</span></span>

### <span data-ttu-id="9ff9c-137">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="9ff9c-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

### <span data-ttu-id="9ff9c-138">System. String</span><span class="sxs-lookup"><span data-stu-id="9ff9c-138">System.String</span></span>

## <span data-ttu-id="9ff9c-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9ff9c-139">OUTPUTS</span></span>

### <span data-ttu-id="9ff9c-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9ff9c-140">System.Boolean</span></span>

## <span data-ttu-id="9ff9c-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9ff9c-141">NOTES</span></span>

## <span data-ttu-id="9ff9c-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9ff9c-142">RELATED LINKS</span></span>
