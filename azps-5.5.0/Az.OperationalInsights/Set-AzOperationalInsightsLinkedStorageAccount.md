---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: b6e57494daf556c3b824ee06735711042d3851b9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240402"
---
# <span data-ttu-id="cd015-101">Set-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cd015-101">Set-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="cd015-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd015-102">SYNOPSIS</span></span>
<span data-ttu-id="cd015-103">Ustawianie połączonego konta magazynu dla obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="cd015-103">Set linked storage account for workspace</span></span>

## <span data-ttu-id="cd015-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="cd015-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DataSourceType] <String> [-StorageAccountIds] <String[]> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd015-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="cd015-105">DESCRIPTION</span></span>
<span data-ttu-id="cd015-106">Ustawianie połączonego konta magazynu dla obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="cd015-106">Set linked storage account for workspace</span></span>

## <span data-ttu-id="cd015-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="cd015-107">EXAMPLES</span></span>

### <span data-ttu-id="cd015-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cd015-108">Example 1</span></span>
```powershell
$account = Get-AzStorageAccount -ResourceGroupName {rg-name} -Name {account-name}

Set-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -DataSourceType CustomLogs -StorageAccountIds $account.Id

Id                : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/workspaces/{workspace-name}/linkedStorageAccounts/CustomLogs
Name              : customlogs
Type              : Microsoft.OperationalInsights/workspaces/linkedStorageAccounts
DataSourceType    : CustomLogs
StorageAccountIds : {/subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.Storage/storageAccounts/{storage-account}}
```

<span data-ttu-id="cd015-109">Ustawianie połączonego miejsca do magazynowania dla obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="cd015-109">Set linked storage for workspace</span></span>

## <span data-ttu-id="cd015-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cd015-110">PARAMETERS</span></span>

### <span data-ttu-id="cd015-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="cd015-111">-DataSourceType</span></span>
<span data-ttu-id="cd015-112">Typ źródła danych powinien być jednym z "CustomLogs", "AzureWatson".</span><span class="sxs-lookup"><span data-stu-id="cd015-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

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

### <span data-ttu-id="cd015-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd015-113">-DefaultProfile</span></span>
<span data-ttu-id="cd015-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="cd015-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd015-115">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="cd015-115">-Force</span></span>
<span data-ttu-id="cd015-116">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="cd015-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="cd015-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd015-117">-ResourceGroupName</span></span>
<span data-ttu-id="cd015-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cd015-118">The resource group name.</span></span>

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

### <span data-ttu-id="cd015-119">- StorageAccountIds</span><span class="sxs-lookup"><span data-stu-id="cd015-119">-StorageAccountIds</span></span>
<span data-ttu-id="cd015-120">Lista identyfikatorów kont magazynu.</span><span class="sxs-lookup"><span data-stu-id="cd015-120">list of storage account Id.</span></span>

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

### <span data-ttu-id="cd015-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="cd015-121">-WorkspaceName</span></span>
<span data-ttu-id="cd015-122">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="cd015-122">The workspace name.</span></span>

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

### <span data-ttu-id="cd015-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cd015-123">-Confirm</span></span>
<span data-ttu-id="cd015-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="cd015-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd015-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd015-125">-WhatIf</span></span>
<span data-ttu-id="cd015-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd015-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd015-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="cd015-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd015-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd015-128">CommonParameters</span></span>
<span data-ttu-id="cd015-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd015-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd015-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cd015-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd015-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cd015-131">INPUTS</span></span>

### <span data-ttu-id="cd015-132">System.String</span><span class="sxs-lookup"><span data-stu-id="cd015-132">System.String</span></span>

## <span data-ttu-id="cd015-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cd015-133">OUTPUTS</span></span>

### <span data-ttu-id="cd015-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span><span class="sxs-lookup"><span data-stu-id="cd015-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span></span>

## <span data-ttu-id="cd015-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="cd015-135">NOTES</span></span>

## <span data-ttu-id="cd015-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cd015-136">RELATED LINKS</span></span>
