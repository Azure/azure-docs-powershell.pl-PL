---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: B4EC9132-8DB9-498D-8B3F-2AB51D8EA03A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightsazureactivitylogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsAzureActivityLogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsAzureActivityLogDataSource.md
ms.openlocfilehash: 654663e9fdc44270266aa2872b7deb939be93e83
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543568"
---
# <span data-ttu-id="1c499-101">New-AzureRmOperationalInsightsAzureActivityLogDataSource</span><span class="sxs-lookup"><span data-stu-id="1c499-101">New-AzureRmOperationalInsightsAzureActivityLogDataSource</span></span>

## <span data-ttu-id="1c499-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1c499-102">SYNOPSIS</span></span>
<span data-ttu-id="1c499-103">Zbieranie dziennika aktywności usługi Azure z danej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="1c499-103">Collect Azure Activity log from given subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1c499-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1c499-104">SYNTAX</span></span>

### <span data-ttu-id="1c499-105">ByWorkspaceName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1c499-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsAzureActivityLogDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-SubscriptionId] <String> [-BackfillStartTime <DateTimeOffset>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c499-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="1c499-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsAzureActivityLogDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-SubscriptionId] <String> [-BackfillStartTime <DateTimeOffset>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c499-107">Opis</span><span class="sxs-lookup"><span data-stu-id="1c499-107">DESCRIPTION</span></span>
<span data-ttu-id="1c499-108">New-AzureRmOperationalInsightsAzureActivityLogDataSource Włącz analizę dzienników w celu zebrania dziennika aktywności platformy Azure z danej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="1c499-108">The New-AzureRmOperationalInsightsAzureActivityLogDataSource enable Log Analytics to collect Azure activity log from given subscription.</span></span>

## <span data-ttu-id="1c499-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1c499-109">EXAMPLES</span></span>

### <span data-ttu-id="1c499-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1c499-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="1c499-111">{{Dodaj opis przykładu}}</span><span class="sxs-lookup"><span data-stu-id="1c499-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="1c499-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1c499-112">PARAMETERS</span></span>

### <span data-ttu-id="1c499-113">-BackfillStartTime</span><span class="sxs-lookup"><span data-stu-id="1c499-113">-BackfillStartTime</span></span>
<span data-ttu-id="1c499-114">Możesz wybrać opcję odpełniania dzienników od tygodnia temu.</span><span class="sxs-lookup"><span data-stu-id="1c499-114">You can choose to backfill logs from a week ago.</span></span>

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

### <span data-ttu-id="1c499-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c499-115">-DefaultProfile</span></span>
<span data-ttu-id="1c499-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="1c499-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1c499-117">-Force</span><span class="sxs-lookup"><span data-stu-id="1c499-117">-Force</span></span>
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

### <span data-ttu-id="1c499-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1c499-118">-Name</span></span>
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

### <span data-ttu-id="1c499-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c499-119">-ResourceGroupName</span></span>
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

### <span data-ttu-id="1c499-120">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="1c499-120">-SubscriptionId</span></span>
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

### <span data-ttu-id="1c499-121">-Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="1c499-121">-Workspace</span></span>
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

### <span data-ttu-id="1c499-122">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="1c499-122">-WorkspaceName</span></span>
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

### <span data-ttu-id="1c499-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1c499-123">-Confirm</span></span>
<span data-ttu-id="1c499-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c499-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c499-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c499-125">-WhatIf</span></span>
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

### <span data-ttu-id="1c499-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c499-126">CommonParameters</span></span>
<span data-ttu-id="1c499-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c499-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c499-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c499-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c499-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1c499-129">INPUTS</span></span>

### <span data-ttu-id="1c499-130">Microsoft. Azure. Commands. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="1c499-130">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="1c499-131">Parametry: przestrzeń robocza (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1c499-131">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="1c499-132">System. String</span><span class="sxs-lookup"><span data-stu-id="1c499-132">System.String</span></span>

### <span data-ttu-id="1c499-133">System. DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="1c499-133">System.DateTimeOffset</span></span>

## <span data-ttu-id="1c499-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1c499-134">OUTPUTS</span></span>

### <span data-ttu-id="1c499-135">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="1c499-135">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="1c499-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1c499-136">NOTES</span></span>

## <span data-ttu-id="1c499-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1c499-137">RELATED LINKS</span></span>
