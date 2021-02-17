---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: 56f9f5b86e3e98ca9bba13604c3086d2189c45c5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191482"
---
# <span data-ttu-id="a5aac-101">Remove-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a5aac-101">Remove-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="a5aac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5aac-102">SYNOPSIS</span></span>
<span data-ttu-id="a5aac-103">Usuwanie połączonego konta magazynu dla obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="a5aac-103">Delete linked storage account for workspace</span></span>

## <span data-ttu-id="a5aac-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a5aac-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-DataSourceType] <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a5aac-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="a5aac-105">DESCRIPTION</span></span>
<span data-ttu-id="a5aac-106">Usuwanie połączonego konta magazynu dla obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="a5aac-106">Delete linked storage account for workspace</span></span>

## <span data-ttu-id="a5aac-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a5aac-107">EXAMPLES</span></span>

### <span data-ttu-id="a5aac-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a5aac-108">Example 1</span></span>
```powershell
Remove-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -DataSourceType CustomLogs
True
```

<span data-ttu-id="a5aac-109">Usuń połączone konto magazynu o typie "CustomLogs" dla {workspace-name}</span><span class="sxs-lookup"><span data-stu-id="a5aac-109">Delete linked storage account with type "CustomLogs" for {workspace-name}</span></span>

## <span data-ttu-id="a5aac-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a5aac-110">PARAMETERS</span></span>

### <span data-ttu-id="a5aac-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="a5aac-111">-DataSourceType</span></span>
<span data-ttu-id="a5aac-112">Typ źródła danych powinien być jednym z "CustomLogs", "AzureWatson".</span><span class="sxs-lookup"><span data-stu-id="a5aac-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

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

### <span data-ttu-id="a5aac-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5aac-113">-DefaultProfile</span></span>
<span data-ttu-id="a5aac-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a5aac-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5aac-115">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="a5aac-115">-Force</span></span>
<span data-ttu-id="a5aac-116">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a5aac-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="a5aac-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5aac-117">-ResourceGroupName</span></span>
<span data-ttu-id="a5aac-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a5aac-118">The resource group name.</span></span>

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

### <span data-ttu-id="a5aac-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a5aac-119">-WorkspaceName</span></span>
<span data-ttu-id="a5aac-120">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="a5aac-120">The workspace name.</span></span>

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

### <span data-ttu-id="a5aac-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a5aac-121">-Confirm</span></span>
<span data-ttu-id="a5aac-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a5aac-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5aac-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5aac-123">-WhatIf</span></span>
<span data-ttu-id="a5aac-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5aac-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5aac-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a5aac-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5aac-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5aac-126">CommonParameters</span></span>
<span data-ttu-id="a5aac-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5aac-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5aac-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a5aac-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5aac-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a5aac-129">INPUTS</span></span>

### <span data-ttu-id="a5aac-130">System.String</span><span class="sxs-lookup"><span data-stu-id="a5aac-130">System.String</span></span>

## <span data-ttu-id="a5aac-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a5aac-131">OUTPUTS</span></span>

### <span data-ttu-id="a5aac-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a5aac-132">System.Boolean</span></span>

## <span data-ttu-id="a5aac-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a5aac-133">NOTES</span></span>

## <span data-ttu-id="a5aac-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a5aac-134">RELATED LINKS</span></span>
