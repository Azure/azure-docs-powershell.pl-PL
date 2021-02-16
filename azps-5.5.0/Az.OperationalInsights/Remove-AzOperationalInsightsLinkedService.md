---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightslinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedService.md
ms.openlocfilehash: c62dcefc2a4cfabc908c45454f3907c2da060f6c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186714"
---
# <span data-ttu-id="564fd-101">Remove-AzOperationalInsightsLinkedService</span><span class="sxs-lookup"><span data-stu-id="564fd-101">Remove-AzOperationalInsightsLinkedService</span></span>

## <span data-ttu-id="564fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="564fd-102">SYNOPSIS</span></span>
<span data-ttu-id="564fd-103">Odłącz usługę dla obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="564fd-103">Unlink service for workspace</span></span>

## <span data-ttu-id="564fd-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="564fd-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsLinkedService [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-LinkedServiceName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="564fd-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="564fd-105">DESCRIPTION</span></span>
<span data-ttu-id="564fd-106">Odłącz usługę dla obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="564fd-106">Unlink service for workspace</span></span>

## <span data-ttu-id="564fd-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="564fd-107">EXAMPLES</span></span>

### <span data-ttu-id="564fd-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="564fd-108">Example 1</span></span>
```powershell
Remove-AzOperationalInsightsLinkedService -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -LinkedServiceName cluster

true
```

<span data-ttu-id="564fd-109">Odłączanie połączonej usługi dla obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="564fd-109">Unlink linked service for workspace</span></span>

## <span data-ttu-id="564fd-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="564fd-110">PARAMETERS</span></span>

### <span data-ttu-id="564fd-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="564fd-111">-AsJob</span></span>
<span data-ttu-id="564fd-112">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="564fd-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="564fd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="564fd-113">-DefaultProfile</span></span>
<span data-ttu-id="564fd-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="564fd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="564fd-115">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="564fd-115">-LinkedServiceName</span></span>
<span data-ttu-id="564fd-116">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="564fd-116">The Workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="564fd-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="564fd-117">-ResourceGroupName</span></span>
<span data-ttu-id="564fd-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="564fd-118">The resource group name.</span></span>

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

### <span data-ttu-id="564fd-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="564fd-119">-WorkspaceName</span></span>
<span data-ttu-id="564fd-120">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="564fd-120">The Workspace name.</span></span>

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

### <span data-ttu-id="564fd-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="564fd-121">-Confirm</span></span>
<span data-ttu-id="564fd-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="564fd-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="564fd-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="564fd-123">-WhatIf</span></span>
<span data-ttu-id="564fd-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="564fd-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="564fd-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="564fd-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="564fd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="564fd-126">CommonParameters</span></span>
<span data-ttu-id="564fd-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="564fd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="564fd-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="564fd-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="564fd-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="564fd-129">INPUTS</span></span>

### <span data-ttu-id="564fd-130">System.String</span><span class="sxs-lookup"><span data-stu-id="564fd-130">System.String</span></span>

## <span data-ttu-id="564fd-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="564fd-131">OUTPUTS</span></span>

### <span data-ttu-id="564fd-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="564fd-132">System.Boolean</span></span>

## <span data-ttu-id="564fd-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="564fd-133">NOTES</span></span>

## <span data-ttu-id="564fd-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="564fd-134">RELATED LINKS</span></span>
