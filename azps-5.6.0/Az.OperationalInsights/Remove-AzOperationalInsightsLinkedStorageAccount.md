---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/remove-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: 8e4dd13b93a0aadf8c69325bc6d79a2a1b3e1359
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989787"
---
# <span data-ttu-id="51805-101">Remove-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="51805-101">Remove-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="51805-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51805-102">SYNOPSIS</span></span>
<span data-ttu-id="51805-103">Usuwanie połączonego konta magazynu dla obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="51805-103">Delete linked storage account for workspace</span></span>

## <span data-ttu-id="51805-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="51805-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-DataSourceType] <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="51805-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="51805-105">DESCRIPTION</span></span>
<span data-ttu-id="51805-106">Usuwanie połączonego konta magazynu dla obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="51805-106">Delete linked storage account for workspace</span></span>

## <span data-ttu-id="51805-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="51805-107">EXAMPLES</span></span>

### <span data-ttu-id="51805-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="51805-108">Example 1</span></span>
```powershell
Remove-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -DataSourceType CustomLogs
True
```

<span data-ttu-id="51805-109">Usuń połączone konto magazynu o typie "CustomLogs" dla {workspace-name}</span><span class="sxs-lookup"><span data-stu-id="51805-109">Delete linked storage account with type "CustomLogs" for {workspace-name}</span></span>

## <span data-ttu-id="51805-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="51805-110">PARAMETERS</span></span>

### <span data-ttu-id="51805-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="51805-111">-DataSourceType</span></span>
<span data-ttu-id="51805-112">Typ źródła danych powinien być jednym z "CustomLogs", "AzureWatson".</span><span class="sxs-lookup"><span data-stu-id="51805-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

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

### <span data-ttu-id="51805-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51805-113">-DefaultProfile</span></span>
<span data-ttu-id="51805-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="51805-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51805-115">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="51805-115">-Force</span></span>
<span data-ttu-id="51805-116">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="51805-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="51805-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51805-117">-ResourceGroupName</span></span>
<span data-ttu-id="51805-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="51805-118">The resource group name.</span></span>

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

### <span data-ttu-id="51805-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="51805-119">-WorkspaceName</span></span>
<span data-ttu-id="51805-120">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="51805-120">The workspace name.</span></span>

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

### <span data-ttu-id="51805-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="51805-121">-Confirm</span></span>
<span data-ttu-id="51805-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="51805-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51805-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51805-123">-WhatIf</span></span>
<span data-ttu-id="51805-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51805-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51805-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="51805-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51805-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51805-126">CommonParameters</span></span>
<span data-ttu-id="51805-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51805-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51805-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="51805-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51805-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="51805-129">INPUTS</span></span>

### <span data-ttu-id="51805-130">System.String</span><span class="sxs-lookup"><span data-stu-id="51805-130">System.String</span></span>

## <span data-ttu-id="51805-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="51805-131">OUTPUTS</span></span>

### <span data-ttu-id="51805-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="51805-132">System.Boolean</span></span>

## <span data-ttu-id="51805-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="51805-133">NOTES</span></span>

## <span data-ttu-id="51805-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="51805-134">RELATED LINKS</span></span>
