---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: 1293a2d045da5da1856052495516e9311e42e5f2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504312"
---
# <span data-ttu-id="c8337-101">New-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c8337-101">New-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="c8337-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c8337-102">SYNOPSIS</span></span>
<span data-ttu-id="c8337-103">Tworzenie konta połączonego magazynu dla obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="c8337-103">Create linked storage account for workspace</span></span>

## <span data-ttu-id="c8337-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c8337-104">SYNTAX</span></span>

```
New-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DataSourceType] <String> [-StorageAccountIds] <String[]> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8337-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c8337-105">DESCRIPTION</span></span>
<span data-ttu-id="c8337-106">Tworzenie konta połączonego magazynu dla obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="c8337-106">Create linked storage account for workspace</span></span>

## <span data-ttu-id="c8337-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c8337-107">EXAMPLES</span></span>

### <span data-ttu-id="c8337-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c8337-108">Example 1</span></span>
```powershell
$account = Get-AzStorageAccount -ResourceGroupName {rg-name} -Name {account-name}

New-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -DataSourceType CustomLogs -StorageAccountIds $account.Id

Id                : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/workspaces/{workspace-name}/linkedStorageAccounts/CustomLogs
Name              : customlogs
Type              : Microsoft.OperationalInsights/workspaces/linkedStorageAccounts
DataSourceType    : CustomLogs
StorageAccountIds : {/subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.Storage/storageAccounts/{storage-account}}
```

<span data-ttu-id="c8337-109">Dodawanie połączonego magazynu dla obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="c8337-109">Add linked storage for workspace</span></span>

## <span data-ttu-id="c8337-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c8337-110">PARAMETERS</span></span>

### <span data-ttu-id="c8337-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="c8337-111">-DataSourceType</span></span>
<span data-ttu-id="c8337-112">Typ źródła danych powinien być jednym z "CustomLogs", "AzureWatson".</span><span class="sxs-lookup"><span data-stu-id="c8337-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

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

### <span data-ttu-id="c8337-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8337-113">-DefaultProfile</span></span>
<span data-ttu-id="c8337-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c8337-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8337-115">-Force</span><span class="sxs-lookup"><span data-stu-id="c8337-115">-Force</span></span>
<span data-ttu-id="c8337-116">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c8337-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="c8337-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8337-117">-ResourceGroupName</span></span>
<span data-ttu-id="c8337-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c8337-118">The resource group name.</span></span>

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

### <span data-ttu-id="c8337-119">-StorageAccountIds</span><span class="sxs-lookup"><span data-stu-id="c8337-119">-StorageAccountIds</span></span>
<span data-ttu-id="c8337-120">Lista identyfikatorów kont magazynu.</span><span class="sxs-lookup"><span data-stu-id="c8337-120">list of storage account Id.</span></span>

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

### <span data-ttu-id="c8337-121">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="c8337-121">-WorkspaceName</span></span>
<span data-ttu-id="c8337-122">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="c8337-122">The workspace name.</span></span>

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

### <span data-ttu-id="c8337-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c8337-123">-Confirm</span></span>
<span data-ttu-id="c8337-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8337-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8337-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8337-125">-WhatIf</span></span>
<span data-ttu-id="c8337-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8337-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8337-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c8337-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8337-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8337-128">CommonParameters</span></span>
<span data-ttu-id="c8337-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8337-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8337-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c8337-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8337-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c8337-131">INPUTS</span></span>

### <span data-ttu-id="c8337-132">System. String</span><span class="sxs-lookup"><span data-stu-id="c8337-132">System.String</span></span>

## <span data-ttu-id="c8337-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c8337-133">OUTPUTS</span></span>

### <span data-ttu-id="c8337-134">Microsoft. Azure. Commands. OperationalInsights. models. PSLinkedStorageAccountsResource</span><span class="sxs-lookup"><span data-stu-id="c8337-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span></span>

## <span data-ttu-id="c8337-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c8337-135">NOTES</span></span>

## <span data-ttu-id="c8337-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c8337-136">RELATED LINKS</span></span>
