---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/update-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: 5ef27923fbffc92a0190419cc5949c0b841b95dc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182226"
---
# <span data-ttu-id="8eda6-101">Update-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8eda6-101">Update-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="8eda6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8eda6-102">SYNOPSIS</span></span>
<span data-ttu-id="8eda6-103">Aktualizowanie połączonego konta magazynu szczegółowego szczegółowych informacji o aplikacji</span><span class="sxs-lookup"><span data-stu-id="8eda6-103">Update application insights linked storage account</span></span>

## <span data-ttu-id="8eda6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8eda6-104">SYNTAX</span></span>

### <span data-ttu-id="8eda6-105">ByResourceNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="8eda6-105">ByResourceNameParameterSet (Default)</span></span>
```
Update-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 -LinkedStorageAccountResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8eda6-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8eda6-106">ByInputObjectParameterSet</span></span>
```
Update-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 -LinkedStorageAccountResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8eda6-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8eda6-107">ByResourceIdParameterSet</span></span>
```
Update-AzApplicationInsightsLinkedStorageAccount -ResourceId <String> -LinkedStorageAccountResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8eda6-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="8eda6-108">DESCRIPTION</span></span>
<span data-ttu-id="8eda6-109">Aktualizowanie połączonego konta magazynu szczegółowego szczegółowych informacji o aplikacji</span><span class="sxs-lookup"><span data-stu-id="8eda6-109">Update application insights linked storage account</span></span>

## <span data-ttu-id="8eda6-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8eda6-110">EXAMPLES</span></span>

### <span data-ttu-id="8eda6-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8eda6-111">Example 1</span></span>
```powershell
$account = Get-AzStorageAccount -ResourceGroupName "rgName" -Name "accountName"

Get-AzApplicationInsights -ResourceGroupName "rgName" -Name "componentName" | Update-AzApplicationInsightsLinkedStorageAccount -LinkedStorageAccountResourceId $account.Id
```

<span data-ttu-id="8eda6-112">Zaktualizuj połączone konto magazynu w składniku "componentName", aby skojarzyć je z $account</span><span class="sxs-lookup"><span data-stu-id="8eda6-112">Update linked storage account under component "componentName" to associate with $account</span></span>

## <span data-ttu-id="8eda6-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8eda6-113">PARAMETERS</span></span>

### <span data-ttu-id="8eda6-114">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="8eda6-114">-ComponentName</span></span>
<span data-ttu-id="8eda6-115">Nazwa składnika</span><span class="sxs-lookup"><span data-stu-id="8eda6-115">Component Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8eda6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8eda6-116">-DefaultProfile</span></span>
<span data-ttu-id="8eda6-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8eda6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8eda6-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8eda6-118">-InputObject</span></span>
<span data-ttu-id="8eda6-119">PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="8eda6-119">PSApplicationInsightsComponent</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8eda6-120">-LinkedStorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="8eda6-120">-LinkedStorageAccountResourceId</span></span>
<span data-ttu-id="8eda6-121">Account ResourceId (Konto magazynu)</span><span class="sxs-lookup"><span data-stu-id="8eda6-121">Storage Account ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8eda6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8eda6-122">-ResourceGroupName</span></span>
<span data-ttu-id="8eda6-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="8eda6-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8eda6-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8eda6-124">-ResourceId</span></span>
<span data-ttu-id="8eda6-125">Component ResourceId</span><span class="sxs-lookup"><span data-stu-id="8eda6-125">Component ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8eda6-126">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8eda6-126">-Confirm</span></span>
<span data-ttu-id="8eda6-127">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8eda6-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8eda6-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8eda6-128">-WhatIf</span></span>
<span data-ttu-id="8eda6-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8eda6-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8eda6-130">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8eda6-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8eda6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8eda6-131">CommonParameters</span></span>
<span data-ttu-id="8eda6-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8eda6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8eda6-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8eda6-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8eda6-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8eda6-134">INPUTS</span></span>

### <span data-ttu-id="8eda6-135">System.String</span><span class="sxs-lookup"><span data-stu-id="8eda6-135">System.String</span></span>

### <span data-ttu-id="8eda6-136">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="8eda6-136">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="8eda6-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8eda6-137">OUTPUTS</span></span>

### <span data-ttu-id="8eda6-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="8eda6-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span></span>

## <span data-ttu-id="8eda6-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8eda6-139">NOTES</span></span>

## <span data-ttu-id="8eda6-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8eda6-140">RELATED LINKS</span></span>
