---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: 5095a3d9f989a6600776140239b9207ba3293d53
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345805"
---
# <span data-ttu-id="444e9-101">Get-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="444e9-101">Get-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="444e9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="444e9-102">SYNOPSIS</span></span>
<span data-ttu-id="444e9-103">Uzyskiwanie lub wyświetlanie listy połączonych kont magazynu</span><span class="sxs-lookup"><span data-stu-id="444e9-103">Get or list linked storage account</span></span>

## <span data-ttu-id="444e9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="444e9-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-DataSourceType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="444e9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="444e9-105">DESCRIPTION</span></span>
<span data-ttu-id="444e9-106">Uzyskiwanie połączonego konta magazynu, wyświetlanie listy wszystkich połączonych kont magazynu, gdy nie podano parametru "-sourceType"</span><span class="sxs-lookup"><span data-stu-id="444e9-106">Get linked storage account, list all linked storage accounts when "-DataSourceType" was not specified</span></span>

## <span data-ttu-id="444e9-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="444e9-107">EXAMPLES</span></span>

### <span data-ttu-id="444e9-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="444e9-108">Example 1</span></span>
```powershell
Get-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name}

Id                : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/workspaces/{workspace-name}/linkedStorageAccounts/customlogs
Name              :
Type              : Microsoft.OperationalInsights/workspaces/linkedStorageAccounts
DataSourceType    : CustomLogs
StorageAccountIds : {/subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.Storage/storageAccounts/{account}}
```

<span data-ttu-id="444e9-109">Lista połączonych accoounts magazynu w obszarze roboczym {Workspace-Name}</span><span class="sxs-lookup"><span data-stu-id="444e9-109">list linked storage accoounts for workspace {workspace-name}</span></span>

## <span data-ttu-id="444e9-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="444e9-110">PARAMETERS</span></span>

### <span data-ttu-id="444e9-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="444e9-111">-DataSourceType</span></span>
<span data-ttu-id="444e9-112">Typ źródła danych powinien być jednym z "CustomLogs", "AzureWatson".</span><span class="sxs-lookup"><span data-stu-id="444e9-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

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

### <span data-ttu-id="444e9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="444e9-113">-DefaultProfile</span></span>
<span data-ttu-id="444e9-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="444e9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="444e9-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="444e9-115">-ResourceGroupName</span></span>
<span data-ttu-id="444e9-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="444e9-116">The resource group name.</span></span>

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

### <span data-ttu-id="444e9-117">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="444e9-117">-WorkspaceName</span></span>
<span data-ttu-id="444e9-118">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="444e9-118">The workspace name.</span></span>

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

### <span data-ttu-id="444e9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="444e9-119">CommonParameters</span></span>
<span data-ttu-id="444e9-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="444e9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="444e9-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="444e9-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="444e9-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="444e9-122">INPUTS</span></span>

### <span data-ttu-id="444e9-123">System. String</span><span class="sxs-lookup"><span data-stu-id="444e9-123">System.String</span></span>

## <span data-ttu-id="444e9-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="444e9-124">OUTPUTS</span></span>

### <span data-ttu-id="444e9-125">Microsoft. Azure. Commands. OperationalInsights. models. PSLinkedStorageAccountsResource</span><span class="sxs-lookup"><span data-stu-id="444e9-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span></span>

## <span data-ttu-id="444e9-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="444e9-126">NOTES</span></span>

## <span data-ttu-id="444e9-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="444e9-127">RELATED LINKS</span></span>