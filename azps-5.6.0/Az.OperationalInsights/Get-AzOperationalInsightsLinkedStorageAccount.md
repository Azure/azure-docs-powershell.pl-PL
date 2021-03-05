---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/get-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: 5ae174f31cdbe23a28dd9a21b44b640239e78fdd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976497"
---
# <span data-ttu-id="13770-101">Get-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="13770-101">Get-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="13770-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13770-102">SYNOPSIS</span></span>
<span data-ttu-id="13770-103">Uzyskiwanie połączonego konta magazynu lub lista kont magazynu połączonego</span><span class="sxs-lookup"><span data-stu-id="13770-103">Get or list linked storage account</span></span>

## <span data-ttu-id="13770-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="13770-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-DataSourceType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13770-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="13770-105">DESCRIPTION</span></span>
<span data-ttu-id="13770-106">Uzyskiwanie połączonego konta magazynu, lista wszystkich połączonych kont magazynu, gdy nie określono "-DataSourceType"</span><span class="sxs-lookup"><span data-stu-id="13770-106">Get linked storage account, list all linked storage accounts when "-DataSourceType" was not specified</span></span>

## <span data-ttu-id="13770-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="13770-107">EXAMPLES</span></span>

### <span data-ttu-id="13770-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="13770-108">Example 1</span></span>
```powershell
Get-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name}

Id                : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/workspaces/{workspace-name}/linkedStorageAccounts/customlogs
Name              :
Type              : Microsoft.OperationalInsights/workspaces/linkedStorageAccounts
DataSourceType    : CustomLogs
StorageAccountIds : {/subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.Storage/storageAccounts/{account}}
```

<span data-ttu-id="13770-109">Lista połączonych ułanów magazynu dla obszaru roboczego {workspace-name}</span><span class="sxs-lookup"><span data-stu-id="13770-109">list linked storage accoounts for workspace {workspace-name}</span></span>

## <span data-ttu-id="13770-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="13770-110">PARAMETERS</span></span>

### <span data-ttu-id="13770-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="13770-111">-DataSourceType</span></span>
<span data-ttu-id="13770-112">Typ źródła danych powinien być jednym z "CustomLogs", "AzureWatson".</span><span class="sxs-lookup"><span data-stu-id="13770-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: CustomLogs, AzureWatson

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13770-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13770-113">-DefaultProfile</span></span>
<span data-ttu-id="13770-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="13770-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13770-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13770-115">-ResourceGroupName</span></span>
<span data-ttu-id="13770-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="13770-116">The resource group name.</span></span>

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

### <span data-ttu-id="13770-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="13770-117">-WorkspaceName</span></span>
<span data-ttu-id="13770-118">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="13770-118">The workspace name.</span></span>

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

### <span data-ttu-id="13770-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13770-119">CommonParameters</span></span>
<span data-ttu-id="13770-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13770-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13770-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="13770-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13770-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="13770-122">INPUTS</span></span>

### <span data-ttu-id="13770-123">System.String</span><span class="sxs-lookup"><span data-stu-id="13770-123">System.String</span></span>

## <span data-ttu-id="13770-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="13770-124">OUTPUTS</span></span>

### <span data-ttu-id="13770-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span><span class="sxs-lookup"><span data-stu-id="13770-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span></span>

## <span data-ttu-id="13770-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="13770-126">NOTES</span></span>

## <span data-ttu-id="13770-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="13770-127">RELATED LINKS</span></span>