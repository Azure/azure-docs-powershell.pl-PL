---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: B4EC9132-8DB9-498D-8B3F-2AB51D8EA03A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightsazureactivitylogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsAzureActivityLogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsAzureActivityLogDataSource.md
ms.openlocfilehash: 6b3009a37a314b70d258f597823f8da062970450
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527990"
---
# <span data-ttu-id="34be5-101">New-AzureRmOperationalInsightsAzureActivityLogDataSource</span><span class="sxs-lookup"><span data-stu-id="34be5-101">New-AzureRmOperationalInsightsAzureActivityLogDataSource</span></span>

## <span data-ttu-id="34be5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="34be5-102">SYNOPSIS</span></span>
<span data-ttu-id="34be5-103">Zbieranie dziennika aktywności usługi Azure z danej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="34be5-103">Collect Azure Activity log from given subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34be5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="34be5-104">SYNTAX</span></span>

### <span data-ttu-id="34be5-105">ByWorkspaceName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="34be5-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsAzureActivityLogDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-SubscriptionId] <String> [-BackfillStartTime <DateTimeOffset>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34be5-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="34be5-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsAzureActivityLogDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-SubscriptionId] <String> [-BackfillStartTime <DateTimeOffset>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34be5-107">Opis</span><span class="sxs-lookup"><span data-stu-id="34be5-107">DESCRIPTION</span></span>
<span data-ttu-id="34be5-108">New-AzureRmOperationalInsightsAzureActivityLogDataSource Włącz analizę dzienników w celu zebrania dziennika aktywności platformy Azure z danej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="34be5-108">The New-AzureRmOperationalInsightsAzureActivityLogDataSource enable Log Analytics to collect Azure activity log from given subscription.</span></span>

## <span data-ttu-id="34be5-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="34be5-109">EXAMPLES</span></span>

### <span data-ttu-id="34be5-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="34be5-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="34be5-111">{{Dodaj opis przykładu}}</span><span class="sxs-lookup"><span data-stu-id="34be5-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="34be5-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="34be5-112">PARAMETERS</span></span>

### <span data-ttu-id="34be5-113">-BackfillStartTime</span><span class="sxs-lookup"><span data-stu-id="34be5-113">-BackfillStartTime</span></span>
<span data-ttu-id="34be5-114">Możesz wybrać opcję odpełniania dzienników od tygodnia temu.</span><span class="sxs-lookup"><span data-stu-id="34be5-114">You can choose to backfill logs from a week ago.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34be5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34be5-115">-DefaultProfile</span></span>
<span data-ttu-id="34be5-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="34be5-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34be5-117">-Force</span><span class="sxs-lookup"><span data-stu-id="34be5-117">-Force</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34be5-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="34be5-118">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34be5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34be5-119">-ResourceGroupName</span></span>
```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34be5-120">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="34be5-120">-SubscriptionId</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34be5-121">-Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="34be5-121">-Workspace</span></span>
```yaml
Type: PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34be5-122">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="34be5-122">-WorkspaceName</span></span>
```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34be5-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="34be5-123">-Confirm</span></span>
<span data-ttu-id="34be5-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34be5-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34be5-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34be5-125">-WhatIf</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34be5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34be5-126">CommonParameters</span></span>
<span data-ttu-id="34be5-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34be5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34be5-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34be5-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34be5-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="34be5-129">INPUTS</span></span>

### <span data-ttu-id="34be5-130">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="34be5-130">PSWorkspace</span></span>
<span data-ttu-id="34be5-131">Parametr "obszar roboczy" akceptuje wartość typu "PSWorkspace" z potoku</span><span class="sxs-lookup"><span data-stu-id="34be5-131">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="34be5-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="34be5-132">OUTPUTS</span></span>

### <span data-ttu-id="34be5-133">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="34be5-133">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="34be5-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="34be5-134">NOTES</span></span>

## <span data-ttu-id="34be5-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="34be5-135">RELATED LINKS</span></span>

