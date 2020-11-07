---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: B4EC9132-8DB9-498D-8B3F-2AB51D8EA03A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsazureactivitylogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsAzureActivityLogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsAzureActivityLogDataSource.md
ms.openlocfilehash: 0a7bbc6832c5a0c6c871d2a5c35ac9ee86042fd0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872443"
---
# <span data-ttu-id="507a6-101">New-AzOperationalInsightsAzureActivityLogDataSource</span><span class="sxs-lookup"><span data-stu-id="507a6-101">New-AzOperationalInsightsAzureActivityLogDataSource</span></span>

## <span data-ttu-id="507a6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="507a6-102">SYNOPSIS</span></span>
<span data-ttu-id="507a6-103">Zbieranie dziennika aktywności usługi Azure z danej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="507a6-103">Collect Azure Activity log from given subscription.</span></span>

## <span data-ttu-id="507a6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="507a6-104">SYNTAX</span></span>

### <span data-ttu-id="507a6-105">ByWorkspaceName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="507a6-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsAzureActivityLogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-SubscriptionId] <String> [-BackfillStartTime <DateTimeOffset>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="507a6-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="507a6-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsAzureActivityLogDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-SubscriptionId] <String> [-BackfillStartTime <DateTimeOffset>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="507a6-107">Opis</span><span class="sxs-lookup"><span data-stu-id="507a6-107">DESCRIPTION</span></span>
<span data-ttu-id="507a6-108">New-AzOperationalInsightsAzureActivityLogDataSource Włącz analizę dzienników w celu zebrania dziennika aktywności platformy Azure z danej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="507a6-108">The New-AzOperationalInsightsAzureActivityLogDataSource enable Log Analytics to collect Azure activity log from given subscription.</span></span>

## <span data-ttu-id="507a6-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="507a6-109">EXAMPLES</span></span>

### <span data-ttu-id="507a6-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="507a6-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="507a6-111">{{Dodaj opis przykładu}}</span><span class="sxs-lookup"><span data-stu-id="507a6-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="507a6-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="507a6-112">PARAMETERS</span></span>

### <span data-ttu-id="507a6-113">-BackfillStartTime</span><span class="sxs-lookup"><span data-stu-id="507a6-113">-BackfillStartTime</span></span>
<span data-ttu-id="507a6-114">Możesz wybrać opcję odpełniania dzienników od tygodnia temu.</span><span class="sxs-lookup"><span data-stu-id="507a6-114">You can choose to backfill logs from a week ago.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="507a6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="507a6-115">-DefaultProfile</span></span>
<span data-ttu-id="507a6-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="507a6-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="507a6-117">-Force</span><span class="sxs-lookup"><span data-stu-id="507a6-117">-Force</span></span>
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

### <span data-ttu-id="507a6-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="507a6-118">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="507a6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="507a6-119">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="507a6-120">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="507a6-120">-SubscriptionId</span></span>
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

### <span data-ttu-id="507a6-121">-Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="507a6-121">-Workspace</span></span>
```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="507a6-122">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="507a6-122">-WorkspaceName</span></span>
```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="507a6-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="507a6-123">-Confirm</span></span>
<span data-ttu-id="507a6-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="507a6-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="507a6-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="507a6-125">-WhatIf</span></span>
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

### <span data-ttu-id="507a6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="507a6-126">CommonParameters</span></span>
<span data-ttu-id="507a6-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="507a6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="507a6-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="507a6-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="507a6-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="507a6-129">INPUTS</span></span>

### <span data-ttu-id="507a6-130">Microsoft. Azure. Commands. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="507a6-130">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="507a6-131">System. String</span><span class="sxs-lookup"><span data-stu-id="507a6-131">System.String</span></span>

### <span data-ttu-id="507a6-132">System. DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="507a6-132">System.DateTimeOffset</span></span>

## <span data-ttu-id="507a6-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="507a6-133">OUTPUTS</span></span>

### <span data-ttu-id="507a6-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="507a6-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="507a6-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="507a6-135">NOTES</span></span>

## <span data-ttu-id="507a6-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="507a6-136">RELATED LINKS</span></span>
