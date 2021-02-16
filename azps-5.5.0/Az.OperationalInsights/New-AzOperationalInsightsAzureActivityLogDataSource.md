---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: B4EC9132-8DB9-498D-8B3F-2AB51D8EA03A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsazureactivitylogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsAzureActivityLogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsAzureActivityLogDataSource.md
ms.openlocfilehash: 6dc016e717e89ad60e066be1c1d86e5871309d9e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184106"
---
# <span data-ttu-id="802b0-101">New-AzOperationalInsightsAzureActivityLogDataSource</span><span class="sxs-lookup"><span data-stu-id="802b0-101">New-AzOperationalInsightsAzureActivityLogDataSource</span></span>

## <span data-ttu-id="802b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="802b0-102">SYNOPSIS</span></span>
<span data-ttu-id="802b0-103">Zbierz dziennik aktywności platformy Azure z danej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="802b0-103">Collect Azure Activity log from given subscription.</span></span>

## <span data-ttu-id="802b0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="802b0-104">SYNTAX</span></span>

### <span data-ttu-id="802b0-105">ByWorkspaceName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="802b0-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsAzureActivityLogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-SubscriptionId] <String> [-BackfillStartTime <DateTimeOffset>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="802b0-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="802b0-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsAzureActivityLogDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-SubscriptionId] <String> [-BackfillStartTime <DateTimeOffset>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="802b0-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="802b0-107">DESCRIPTION</span></span>
<span data-ttu-id="802b0-108">Raport New-AzOperationalInsightsAzureActivityLogDataSource umożliwić zbieranie dziennika aktywności platformy Azure z danej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="802b0-108">The New-AzOperationalInsightsAzureActivityLogDataSource enable Log Analytics to collect Azure activity log from given subscription.</span></span>

## <span data-ttu-id="802b0-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="802b0-109">EXAMPLES</span></span>

### <span data-ttu-id="802b0-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="802b0-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="802b0-111">{{ Dodaj przykładowy opis tutaj }}</span><span class="sxs-lookup"><span data-stu-id="802b0-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="802b0-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="802b0-112">PARAMETERS</span></span>

### <span data-ttu-id="802b0-113">-BackfillStartTime</span><span class="sxs-lookup"><span data-stu-id="802b0-113">-BackfillStartTime</span></span>
<span data-ttu-id="802b0-114">Możesz zdecydować, czy dzienniki mają być wypełniane ponownie niż tydzień temu.</span><span class="sxs-lookup"><span data-stu-id="802b0-114">You can choose to backfill logs from a week ago.</span></span>

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

### <span data-ttu-id="802b0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="802b0-115">-DefaultProfile</span></span>
<span data-ttu-id="802b0-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="802b0-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="802b0-117">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="802b0-117">-Force</span></span>
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

### <span data-ttu-id="802b0-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="802b0-118">-Name</span></span>
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

### <span data-ttu-id="802b0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="802b0-119">-ResourceGroupName</span></span>
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

### <span data-ttu-id="802b0-120">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="802b0-120">-SubscriptionId</span></span>
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

### <span data-ttu-id="802b0-121">— Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="802b0-121">-Workspace</span></span>
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

### <span data-ttu-id="802b0-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="802b0-122">-WorkspaceName</span></span>
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

### <span data-ttu-id="802b0-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="802b0-123">-Confirm</span></span>
<span data-ttu-id="802b0-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="802b0-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="802b0-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="802b0-125">-WhatIf</span></span>
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

### <span data-ttu-id="802b0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="802b0-126">CommonParameters</span></span>
<span data-ttu-id="802b0-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="802b0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="802b0-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="802b0-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="802b0-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="802b0-129">INPUTS</span></span>

### <span data-ttu-id="802b0-130">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="802b0-130">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="802b0-131">System.String</span><span class="sxs-lookup"><span data-stu-id="802b0-131">System.String</span></span>

### <span data-ttu-id="802b0-132">System.DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="802b0-132">System.DateTimeOffset</span></span>

## <span data-ttu-id="802b0-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="802b0-133">OUTPUTS</span></span>

### <span data-ttu-id="802b0-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="802b0-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="802b0-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="802b0-135">NOTES</span></span>

## <span data-ttu-id="802b0-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="802b0-136">RELATED LINKS</span></span>
