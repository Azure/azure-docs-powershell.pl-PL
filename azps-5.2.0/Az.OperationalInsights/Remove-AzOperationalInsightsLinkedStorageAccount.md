---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: 56f9f5b86e3e98ca9bba13604c3086d2189c45c5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98342025"
---
# <span data-ttu-id="56fa8-101">Remove-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="56fa8-101">Remove-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="56fa8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="56fa8-102">SYNOPSIS</span></span>
<span data-ttu-id="56fa8-103">Usuwanie konta połączonego magazynu dla obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="56fa8-103">Delete linked storage account for workspace</span></span>

## <span data-ttu-id="56fa8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="56fa8-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-DataSourceType] <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="56fa8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="56fa8-105">DESCRIPTION</span></span>
<span data-ttu-id="56fa8-106">Usuwanie konta połączonego magazynu dla obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="56fa8-106">Delete linked storage account for workspace</span></span>

## <span data-ttu-id="56fa8-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="56fa8-107">EXAMPLES</span></span>

### <span data-ttu-id="56fa8-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="56fa8-108">Example 1</span></span>
```powershell
Remove-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -DataSourceType CustomLogs
True
```

<span data-ttu-id="56fa8-109">Usuwanie konta połączonego magazynu za pomocą typu "CustomLogs" dla {Workspace-Name}</span><span class="sxs-lookup"><span data-stu-id="56fa8-109">Delete linked storage account with type "CustomLogs" for {workspace-name}</span></span>

## <span data-ttu-id="56fa8-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="56fa8-110">PARAMETERS</span></span>

### <span data-ttu-id="56fa8-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="56fa8-111">-DataSourceType</span></span>
<span data-ttu-id="56fa8-112">Typ źródła danych powinien być jednym z "CustomLogs", "AzureWatson".</span><span class="sxs-lookup"><span data-stu-id="56fa8-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

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

### <span data-ttu-id="56fa8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56fa8-113">-DefaultProfile</span></span>
<span data-ttu-id="56fa8-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="56fa8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56fa8-115">-Force</span><span class="sxs-lookup"><span data-stu-id="56fa8-115">-Force</span></span>
<span data-ttu-id="56fa8-116">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="56fa8-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="56fa8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56fa8-117">-ResourceGroupName</span></span>
<span data-ttu-id="56fa8-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="56fa8-118">The resource group name.</span></span>

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

### <span data-ttu-id="56fa8-119">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="56fa8-119">-WorkspaceName</span></span>
<span data-ttu-id="56fa8-120">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="56fa8-120">The workspace name.</span></span>

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

### <span data-ttu-id="56fa8-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="56fa8-121">-Confirm</span></span>
<span data-ttu-id="56fa8-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56fa8-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56fa8-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56fa8-123">-WhatIf</span></span>
<span data-ttu-id="56fa8-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56fa8-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56fa8-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="56fa8-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56fa8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56fa8-126">CommonParameters</span></span>
<span data-ttu-id="56fa8-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56fa8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56fa8-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="56fa8-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56fa8-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="56fa8-129">INPUTS</span></span>

### <span data-ttu-id="56fa8-130">System. String</span><span class="sxs-lookup"><span data-stu-id="56fa8-130">System.String</span></span>

## <span data-ttu-id="56fa8-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="56fa8-131">OUTPUTS</span></span>

### <span data-ttu-id="56fa8-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="56fa8-132">System.Boolean</span></span>

## <span data-ttu-id="56fa8-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="56fa8-133">NOTES</span></span>

## <span data-ttu-id="56fa8-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="56fa8-134">RELATED LINKS</span></span>
