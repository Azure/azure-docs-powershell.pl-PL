---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: b6e57494daf556c3b824ee06735711042d3851b9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98337549"
---
# <span data-ttu-id="2e539-101">Set-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2e539-101">Set-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="2e539-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2e539-102">SYNOPSIS</span></span>
<span data-ttu-id="2e539-103">Ustawianie konta połączonego magazynu dla obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="2e539-103">Set linked storage account for workspace</span></span>

## <span data-ttu-id="2e539-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2e539-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DataSourceType] <String> [-StorageAccountIds] <String[]> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e539-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2e539-105">DESCRIPTION</span></span>
<span data-ttu-id="2e539-106">Ustawianie konta połączonego magazynu dla obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="2e539-106">Set linked storage account for workspace</span></span>

## <span data-ttu-id="2e539-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2e539-107">EXAMPLES</span></span>

### <span data-ttu-id="2e539-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2e539-108">Example 1</span></span>
```powershell
$account = Get-AzStorageAccount -ResourceGroupName {rg-name} -Name {account-name}

Set-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -DataSourceType CustomLogs -StorageAccountIds $account.Id

Id                : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/workspaces/{workspace-name}/linkedStorageAccounts/CustomLogs
Name              : customlogs
Type              : Microsoft.OperationalInsights/workspaces/linkedStorageAccounts
DataSourceType    : CustomLogs
StorageAccountIds : {/subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.Storage/storageAccounts/{storage-account}}
```

<span data-ttu-id="2e539-109">Ustawianie połączonego magazynu dla obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="2e539-109">Set linked storage for workspace</span></span>

## <span data-ttu-id="2e539-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2e539-110">PARAMETERS</span></span>

### <span data-ttu-id="2e539-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="2e539-111">-DataSourceType</span></span>
<span data-ttu-id="2e539-112">Typ źródła danych powinien być jednym z "CustomLogs", "AzureWatson".</span><span class="sxs-lookup"><span data-stu-id="2e539-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

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

### <span data-ttu-id="2e539-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e539-113">-DefaultProfile</span></span>
<span data-ttu-id="2e539-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2e539-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e539-115">-Force</span><span class="sxs-lookup"><span data-stu-id="2e539-115">-Force</span></span>
<span data-ttu-id="2e539-116">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2e539-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="2e539-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e539-117">-ResourceGroupName</span></span>
<span data-ttu-id="2e539-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2e539-118">The resource group name.</span></span>

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

### <span data-ttu-id="2e539-119">-StorageAccountIds</span><span class="sxs-lookup"><span data-stu-id="2e539-119">-StorageAccountIds</span></span>
<span data-ttu-id="2e539-120">Lista identyfikatorów kont magazynu.</span><span class="sxs-lookup"><span data-stu-id="2e539-120">list of storage account Id.</span></span>

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

### <span data-ttu-id="2e539-121">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="2e539-121">-WorkspaceName</span></span>
<span data-ttu-id="2e539-122">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="2e539-122">The workspace name.</span></span>

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

### <span data-ttu-id="2e539-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2e539-123">-Confirm</span></span>
<span data-ttu-id="2e539-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e539-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e539-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e539-125">-WhatIf</span></span>
<span data-ttu-id="2e539-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e539-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e539-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2e539-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e539-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e539-128">CommonParameters</span></span>
<span data-ttu-id="2e539-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e539-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e539-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2e539-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e539-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2e539-131">INPUTS</span></span>

### <span data-ttu-id="2e539-132">System. String</span><span class="sxs-lookup"><span data-stu-id="2e539-132">System.String</span></span>

## <span data-ttu-id="2e539-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2e539-133">OUTPUTS</span></span>

### <span data-ttu-id="2e539-134">Microsoft. Azure. Commands. OperationalInsights. models. PSLinkedStorageAccountsResource</span><span class="sxs-lookup"><span data-stu-id="2e539-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span></span>

## <span data-ttu-id="2e539-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2e539-135">NOTES</span></span>

## <span data-ttu-id="2e539-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2e539-136">RELATED LINKS</span></span>
