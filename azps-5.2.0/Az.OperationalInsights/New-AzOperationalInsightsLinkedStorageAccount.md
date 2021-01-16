---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: 1293a2d045da5da1856052495516e9311e42e5f2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98351817"
---
# <span data-ttu-id="da979-101">New-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="da979-101">New-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="da979-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="da979-102">SYNOPSIS</span></span>
<span data-ttu-id="da979-103">Tworzenie konta połączonego magazynu dla obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="da979-103">Create linked storage account for workspace</span></span>

## <span data-ttu-id="da979-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="da979-104">SYNTAX</span></span>

```
New-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DataSourceType] <String> [-StorageAccountIds] <String[]> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da979-105">Opis</span><span class="sxs-lookup"><span data-stu-id="da979-105">DESCRIPTION</span></span>
<span data-ttu-id="da979-106">Tworzenie konta połączonego magazynu dla obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="da979-106">Create linked storage account for workspace</span></span>

## <span data-ttu-id="da979-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="da979-107">EXAMPLES</span></span>

### <span data-ttu-id="da979-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="da979-108">Example 1</span></span>
```powershell
$account = Get-AzStorageAccount -ResourceGroupName {rg-name} -Name {account-name}

New-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -DataSourceType CustomLogs -StorageAccountIds $account.Id

Id                : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/workspaces/{workspace-name}/linkedStorageAccounts/CustomLogs
Name              : customlogs
Type              : Microsoft.OperationalInsights/workspaces/linkedStorageAccounts
DataSourceType    : CustomLogs
StorageAccountIds : {/subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.Storage/storageAccounts/{storage-account}}
```

<span data-ttu-id="da979-109">Dodawanie połączonego magazynu dla obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="da979-109">Add linked storage for workspace</span></span>

## <span data-ttu-id="da979-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="da979-110">PARAMETERS</span></span>

### <span data-ttu-id="da979-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="da979-111">-DataSourceType</span></span>
<span data-ttu-id="da979-112">Typ źródła danych powinien być jednym z "CustomLogs", "AzureWatson".</span><span class="sxs-lookup"><span data-stu-id="da979-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

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

### <span data-ttu-id="da979-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da979-113">-DefaultProfile</span></span>
<span data-ttu-id="da979-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="da979-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da979-115">-Force</span><span class="sxs-lookup"><span data-stu-id="da979-115">-Force</span></span>
<span data-ttu-id="da979-116">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="da979-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="da979-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da979-117">-ResourceGroupName</span></span>
<span data-ttu-id="da979-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="da979-118">The resource group name.</span></span>

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

### <span data-ttu-id="da979-119">-StorageAccountIds</span><span class="sxs-lookup"><span data-stu-id="da979-119">-StorageAccountIds</span></span>
<span data-ttu-id="da979-120">Lista identyfikatorów kont magazynu.</span><span class="sxs-lookup"><span data-stu-id="da979-120">list of storage account Id.</span></span>

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

### <span data-ttu-id="da979-121">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="da979-121">-WorkspaceName</span></span>
<span data-ttu-id="da979-122">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="da979-122">The workspace name.</span></span>

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

### <span data-ttu-id="da979-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="da979-123">-Confirm</span></span>
<span data-ttu-id="da979-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da979-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da979-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da979-125">-WhatIf</span></span>
<span data-ttu-id="da979-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da979-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da979-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="da979-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da979-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da979-128">CommonParameters</span></span>
<span data-ttu-id="da979-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da979-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da979-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="da979-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da979-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="da979-131">INPUTS</span></span>

### <span data-ttu-id="da979-132">System. String</span><span class="sxs-lookup"><span data-stu-id="da979-132">System.String</span></span>

## <span data-ttu-id="da979-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="da979-133">OUTPUTS</span></span>

### <span data-ttu-id="da979-134">Microsoft. Azure. Commands. OperationalInsights. models. PSLinkedStorageAccountsResource</span><span class="sxs-lookup"><span data-stu-id="da979-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span></span>

## <span data-ttu-id="da979-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="da979-135">NOTES</span></span>

## <span data-ttu-id="da979-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="da979-136">RELATED LINKS</span></span>
