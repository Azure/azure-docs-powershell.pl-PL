---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/new-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: f1b920c3a67865cbed66c15bc686e3e38e3562db
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977802"
---
# <span data-ttu-id="24ee9-101">New-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="24ee9-101">New-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="24ee9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24ee9-102">SYNOPSIS</span></span>
<span data-ttu-id="24ee9-103">Tworzenie połączonego konta magazynu dla obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="24ee9-103">Create linked storage account for workspace</span></span>

## <span data-ttu-id="24ee9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="24ee9-104">SYNTAX</span></span>

```
New-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DataSourceType] <String> [-StorageAccountIds] <String[]> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24ee9-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="24ee9-105">DESCRIPTION</span></span>
<span data-ttu-id="24ee9-106">Tworzenie połączonego konta magazynu dla obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="24ee9-106">Create linked storage account for workspace</span></span>

## <span data-ttu-id="24ee9-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="24ee9-107">EXAMPLES</span></span>

### <span data-ttu-id="24ee9-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="24ee9-108">Example 1</span></span>
```powershell
$account = Get-AzStorageAccount -ResourceGroupName {rg-name} -Name {account-name}

New-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -DataSourceType CustomLogs -StorageAccountIds $account.Id

Id                : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/workspaces/{workspace-name}/linkedStorageAccounts/CustomLogs
Name              : customlogs
Type              : Microsoft.OperationalInsights/workspaces/linkedStorageAccounts
DataSourceType    : CustomLogs
StorageAccountIds : {/subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.Storage/storageAccounts/{storage-account}}
```

<span data-ttu-id="24ee9-109">Dodawanie połączonego miejsca do magazynowania dla obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="24ee9-109">Add linked storage for workspace</span></span>

## <span data-ttu-id="24ee9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="24ee9-110">PARAMETERS</span></span>

### <span data-ttu-id="24ee9-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="24ee9-111">-DataSourceType</span></span>
<span data-ttu-id="24ee9-112">Typ źródła danych powinien być jednym z "CustomLogs", "AzureWatson".</span><span class="sxs-lookup"><span data-stu-id="24ee9-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: CustomLogs, AzureWatson

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24ee9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24ee9-113">-DefaultProfile</span></span>
<span data-ttu-id="24ee9-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="24ee9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24ee9-115">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="24ee9-115">-Force</span></span>
<span data-ttu-id="24ee9-116">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="24ee9-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="24ee9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24ee9-117">-ResourceGroupName</span></span>
<span data-ttu-id="24ee9-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="24ee9-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24ee9-119">- StorageAccountIds</span><span class="sxs-lookup"><span data-stu-id="24ee9-119">-StorageAccountIds</span></span>
<span data-ttu-id="24ee9-120">Lista identyfikatorów kont magazynu.</span><span class="sxs-lookup"><span data-stu-id="24ee9-120">list of storage account Id.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24ee9-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="24ee9-121">-WorkspaceName</span></span>
<span data-ttu-id="24ee9-122">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="24ee9-122">The workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24ee9-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="24ee9-123">-Confirm</span></span>
<span data-ttu-id="24ee9-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="24ee9-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24ee9-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24ee9-125">-WhatIf</span></span>
<span data-ttu-id="24ee9-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24ee9-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24ee9-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="24ee9-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24ee9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24ee9-128">CommonParameters</span></span>
<span data-ttu-id="24ee9-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24ee9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24ee9-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="24ee9-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24ee9-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="24ee9-131">INPUTS</span></span>

### <span data-ttu-id="24ee9-132">System.String</span><span class="sxs-lookup"><span data-stu-id="24ee9-132">System.String</span></span>

## <span data-ttu-id="24ee9-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="24ee9-133">OUTPUTS</span></span>

### <span data-ttu-id="24ee9-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span><span class="sxs-lookup"><span data-stu-id="24ee9-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span></span>

## <span data-ttu-id="24ee9-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="24ee9-135">NOTES</span></span>

## <span data-ttu-id="24ee9-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="24ee9-136">RELATED LINKS</span></span>
