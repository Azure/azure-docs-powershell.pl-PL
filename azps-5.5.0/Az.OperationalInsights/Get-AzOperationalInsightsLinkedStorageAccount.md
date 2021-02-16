---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: 5095a3d9f989a6600776140239b9207ba3293d53
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179242"
---
# <span data-ttu-id="8f02f-101">Get-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8f02f-101">Get-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="8f02f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f02f-102">SYNOPSIS</span></span>
<span data-ttu-id="8f02f-103">Uzyskiwanie połączonego konta magazynu lub lista kont magazynu połączonego</span><span class="sxs-lookup"><span data-stu-id="8f02f-103">Get or list linked storage account</span></span>

## <span data-ttu-id="8f02f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8f02f-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-DataSourceType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f02f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="8f02f-105">DESCRIPTION</span></span>
<span data-ttu-id="8f02f-106">Uzyskiwanie połączonego konta magazynu, lista wszystkich połączonych kont magazynu, gdy nie określono "-DataSourceType"</span><span class="sxs-lookup"><span data-stu-id="8f02f-106">Get linked storage account, list all linked storage accounts when "-DataSourceType" was not specified</span></span>

## <span data-ttu-id="8f02f-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8f02f-107">EXAMPLES</span></span>

### <span data-ttu-id="8f02f-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8f02f-108">Example 1</span></span>
```powershell
Get-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name}

Id                : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/workspaces/{workspace-name}/linkedStorageAccounts/customlogs
Name              :
Type              : Microsoft.OperationalInsights/workspaces/linkedStorageAccounts
DataSourceType    : CustomLogs
StorageAccountIds : {/subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.Storage/storageAccounts/{account}}
```

<span data-ttu-id="8f02f-109">Lista połączonych ułanów magazynu dla obszaru roboczego {workspace-name}</span><span class="sxs-lookup"><span data-stu-id="8f02f-109">list linked storage accoounts for workspace {workspace-name}</span></span>

## <span data-ttu-id="8f02f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8f02f-110">PARAMETERS</span></span>

### <span data-ttu-id="8f02f-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="8f02f-111">-DataSourceType</span></span>
<span data-ttu-id="8f02f-112">Typ źródła danych powinien być jednym z "CustomLogs", "AzureWatson".</span><span class="sxs-lookup"><span data-stu-id="8f02f-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

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

### <span data-ttu-id="8f02f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f02f-113">-DefaultProfile</span></span>
<span data-ttu-id="8f02f-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8f02f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f02f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f02f-115">-ResourceGroupName</span></span>
<span data-ttu-id="8f02f-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8f02f-116">The resource group name.</span></span>

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

### <span data-ttu-id="8f02f-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="8f02f-117">-WorkspaceName</span></span>
<span data-ttu-id="8f02f-118">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="8f02f-118">The workspace name.</span></span>

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

### <span data-ttu-id="8f02f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f02f-119">CommonParameters</span></span>
<span data-ttu-id="8f02f-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f02f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f02f-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8f02f-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f02f-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8f02f-122">INPUTS</span></span>

### <span data-ttu-id="8f02f-123">System.String</span><span class="sxs-lookup"><span data-stu-id="8f02f-123">System.String</span></span>

## <span data-ttu-id="8f02f-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8f02f-124">OUTPUTS</span></span>

### <span data-ttu-id="8f02f-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span><span class="sxs-lookup"><span data-stu-id="8f02f-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span></span>

## <span data-ttu-id="8f02f-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8f02f-126">NOTES</span></span>

## <span data-ttu-id="8f02f-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8f02f-127">RELATED LINKS</span></span>