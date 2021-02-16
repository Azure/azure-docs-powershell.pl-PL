---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: 1293a2d045da5da1856052495516e9311e42e5f2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186770"
---
# <span data-ttu-id="dd1b3-101">New-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dd1b3-101">New-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="dd1b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd1b3-102">SYNOPSIS</span></span>
<span data-ttu-id="dd1b3-103">Tworzenie połączonego konta magazynu dla obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="dd1b3-103">Create linked storage account for workspace</span></span>

## <span data-ttu-id="dd1b3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="dd1b3-104">SYNTAX</span></span>

```
New-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DataSourceType] <String> [-StorageAccountIds] <String[]> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd1b3-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="dd1b3-105">DESCRIPTION</span></span>
<span data-ttu-id="dd1b3-106">Tworzenie połączonego konta magazynu dla obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="dd1b3-106">Create linked storage account for workspace</span></span>

## <span data-ttu-id="dd1b3-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="dd1b3-107">EXAMPLES</span></span>

### <span data-ttu-id="dd1b3-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="dd1b3-108">Example 1</span></span>
```powershell
$account = Get-AzStorageAccount -ResourceGroupName {rg-name} -Name {account-name}

New-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -DataSourceType CustomLogs -StorageAccountIds $account.Id

Id                : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/workspaces/{workspace-name}/linkedStorageAccounts/CustomLogs
Name              : customlogs
Type              : Microsoft.OperationalInsights/workspaces/linkedStorageAccounts
DataSourceType    : CustomLogs
StorageAccountIds : {/subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.Storage/storageAccounts/{storage-account}}
```

<span data-ttu-id="dd1b3-109">Dodawanie połączonego miejsca do magazynowania dla obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="dd1b3-109">Add linked storage for workspace</span></span>

## <span data-ttu-id="dd1b3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dd1b3-110">PARAMETERS</span></span>

### <span data-ttu-id="dd1b3-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="dd1b3-111">-DataSourceType</span></span>
<span data-ttu-id="dd1b3-112">Typ źródła danych powinien być jednym z "CustomLogs", "AzureWatson".</span><span class="sxs-lookup"><span data-stu-id="dd1b3-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

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

### <span data-ttu-id="dd1b3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd1b3-113">-DefaultProfile</span></span>
<span data-ttu-id="dd1b3-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="dd1b3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd1b3-115">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="dd1b3-115">-Force</span></span>
<span data-ttu-id="dd1b3-116">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="dd1b3-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="dd1b3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd1b3-117">-ResourceGroupName</span></span>
<span data-ttu-id="dd1b3-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="dd1b3-118">The resource group name.</span></span>

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

### <span data-ttu-id="dd1b3-119">- StorageAccountIds</span><span class="sxs-lookup"><span data-stu-id="dd1b3-119">-StorageAccountIds</span></span>
<span data-ttu-id="dd1b3-120">Lista identyfikatorów kont magazynu.</span><span class="sxs-lookup"><span data-stu-id="dd1b3-120">list of storage account Id.</span></span>

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

### <span data-ttu-id="dd1b3-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="dd1b3-121">-WorkspaceName</span></span>
<span data-ttu-id="dd1b3-122">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="dd1b3-122">The workspace name.</span></span>

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

### <span data-ttu-id="dd1b3-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dd1b3-123">-Confirm</span></span>
<span data-ttu-id="dd1b3-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="dd1b3-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd1b3-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd1b3-125">-WhatIf</span></span>
<span data-ttu-id="dd1b3-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd1b3-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd1b3-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="dd1b3-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd1b3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd1b3-128">CommonParameters</span></span>
<span data-ttu-id="dd1b3-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd1b3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd1b3-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dd1b3-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd1b3-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dd1b3-131">INPUTS</span></span>

### <span data-ttu-id="dd1b3-132">System.String</span><span class="sxs-lookup"><span data-stu-id="dd1b3-132">System.String</span></span>

## <span data-ttu-id="dd1b3-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="dd1b3-133">OUTPUTS</span></span>

### <span data-ttu-id="dd1b3-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span><span class="sxs-lookup"><span data-stu-id="dd1b3-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span></span>

## <span data-ttu-id="dd1b3-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="dd1b3-135">NOTES</span></span>

## <span data-ttu-id="dd1b3-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dd1b3-136">RELATED LINKS</span></span>
