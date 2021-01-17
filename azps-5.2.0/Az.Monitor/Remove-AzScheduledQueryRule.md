---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzScheduledQueryRule.md
ms.openlocfilehash: ea7679b2e3214c55463f9f6fd4ccaf2b22d32841
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98362047"
---
# <span data-ttu-id="15d71-101">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="15d71-101">Remove-AzScheduledQueryRule</span></span>

## <span data-ttu-id="15d71-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="15d71-102">SYNOPSIS</span></span>
<span data-ttu-id="15d71-103">Usuwanie reguły alertów dziennika</span><span class="sxs-lookup"><span data-stu-id="15d71-103">Removes a Log Alert Rule</span></span>

## <span data-ttu-id="15d71-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="15d71-104">SYNTAX</span></span>

### <span data-ttu-id="15d71-105">ByRuleName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="15d71-105">ByRuleName (Default)</span></span>
```
Remove-AzScheduledQueryRule -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15d71-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="15d71-106">ByInputObject</span></span>
```
Remove-AzScheduledQueryRule -InputObject <PSScheduledQueryRuleResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15d71-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="15d71-107">ByResourceId</span></span>
```
Remove-AzScheduledQueryRule -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15d71-108">Opis</span><span class="sxs-lookup"><span data-stu-id="15d71-108">DESCRIPTION</span></span>
<span data-ttu-id="15d71-109">Usuwanie reguły alertów dziennika</span><span class="sxs-lookup"><span data-stu-id="15d71-109">Removes a Log Alert Rule</span></span>

## <span data-ttu-id="15d71-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="15d71-110">EXAMPLES</span></span>

### <span data-ttu-id="15d71-111">Przykład 1. Usuń według nazwy reguły</span><span class="sxs-lookup"><span data-stu-id="15d71-111">Example 1: Remove by rule name</span></span>
```powershell
PS C:\> Remove-AzScheduledQueryRule -ResourceGroupName "MyResourceGroup" -Name "LogAlertRule1"
```

### <span data-ttu-id="15d71-112">Przykład 2: usuwanie przez obiekt wejściowy</span><span class="sxs-lookup"><span data-stu-id="15d71-112">Example 2: Remove by input object</span></span>
```powershell
PS C:\> Remove-AzScheduledQueryRule -InputObject $PSScheduledQueryRuleResource
```

### <span data-ttu-id="15d71-113">Przykład 3: Usuwanie według identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="15d71-113">Example 3: Remove by resource Id</span></span>
```powershell
PS C:\> Remove-AzScheduledQueryRule -ResourceId "/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledQueryRules/LogAlertRule1"
```

## <span data-ttu-id="15d71-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="15d71-114">PARAMETERS</span></span>

### <span data-ttu-id="15d71-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15d71-115">-DefaultProfile</span></span>
<span data-ttu-id="15d71-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="15d71-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15d71-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="15d71-117">-InputObject</span></span>
<span data-ttu-id="15d71-118">Zasób reguły zaplanowanego zapytania</span><span class="sxs-lookup"><span data-stu-id="15d71-118">The Scheduled Query Rule resource</span></span>

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

### <span data-ttu-id="15d71-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="15d71-119">-Name</span></span>
<span data-ttu-id="15d71-120">Nazwa alertu</span><span class="sxs-lookup"><span data-stu-id="15d71-120">The alert name</span></span>

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

### <span data-ttu-id="15d71-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="15d71-121">-PassThru</span></span>
<span data-ttu-id="15d71-122">Zwraca wartość oznaczającą sukces lub niepowodzenie.</span><span class="sxs-lookup"><span data-stu-id="15d71-122">Return a value indicating success or failure.</span></span>
<span data-ttu-id="15d71-123">To polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="15d71-123">This cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="15d71-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15d71-124">-ResourceGroupName</span></span>
<span data-ttu-id="15d71-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="15d71-125">The resource group name</span></span>

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

### <span data-ttu-id="15d71-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="15d71-126">-ResourceId</span></span>
<span data-ttu-id="15d71-127">Identyfikator zasobu</span><span class="sxs-lookup"><span data-stu-id="15d71-127">The resource Id</span></span>

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

### <span data-ttu-id="15d71-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="15d71-128">-Confirm</span></span>
<span data-ttu-id="15d71-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15d71-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15d71-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15d71-130">-WhatIf</span></span>
<span data-ttu-id="15d71-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15d71-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15d71-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="15d71-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15d71-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15d71-133">CommonParameters</span></span>
<span data-ttu-id="15d71-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15d71-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15d71-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="15d71-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15d71-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="15d71-136">INPUTS</span></span>

### <span data-ttu-id="15d71-137">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="15d71-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

### <span data-ttu-id="15d71-138">System. String</span><span class="sxs-lookup"><span data-stu-id="15d71-138">System.String</span></span>

## <span data-ttu-id="15d71-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="15d71-139">OUTPUTS</span></span>

### <span data-ttu-id="15d71-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="15d71-140">System.Boolean</span></span>

## <span data-ttu-id="15d71-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="15d71-141">NOTES</span></span>

## <span data-ttu-id="15d71-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="15d71-142">RELATED LINKS</span></span>
