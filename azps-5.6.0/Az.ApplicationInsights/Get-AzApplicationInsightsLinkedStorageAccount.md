---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/get-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: a059209e993f17ffb5eed1b29d1854f8387f3d8c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965233"
---
# <span data-ttu-id="18dd3-101">Get-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="18dd3-101">Get-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="18dd3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18dd3-102">SYNOPSIS</span></span>
<span data-ttu-id="18dd3-103">Uzyskiwanie połączonych kont magazynu szczegółowych informacji o aplikacjach</span><span class="sxs-lookup"><span data-stu-id="18dd3-103">Get application insights linked storage account</span></span>

## <span data-ttu-id="18dd3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="18dd3-104">SYNTAX</span></span>

### <span data-ttu-id="18dd3-105">ByResourceNameParameterSet (Domyślny)</span><span class="sxs-lookup"><span data-stu-id="18dd3-105">ByResourceNameParameterSet (Default)</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18dd3-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="18dd3-106">ByInputObjectParameterSet</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18dd3-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="18dd3-107">ByResourceIdParameterSet</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="18dd3-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="18dd3-108">DESCRIPTION</span></span>
<span data-ttu-id="18dd3-109">Uzyskiwanie połączonych kont magazynu szczegółowych informacji o aplikacjach</span><span class="sxs-lookup"><span data-stu-id="18dd3-109">Get application insights linked storage account</span></span>

## <span data-ttu-id="18dd3-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="18dd3-110">EXAMPLES</span></span>

### <span data-ttu-id="18dd3-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="18dd3-111">Example 1</span></span>
```powershell
Get-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName "rgName" -Name "componentName"
```

<span data-ttu-id="18dd3-112">Uzyskiwanie połączonego konta magazynu skojarzonego ze składnikiem "componentName"</span><span class="sxs-lookup"><span data-stu-id="18dd3-112">Get linked storage account associated with component "componentName"</span></span>

## <span data-ttu-id="18dd3-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="18dd3-113">PARAMETERS</span></span>

### <span data-ttu-id="18dd3-114">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="18dd3-114">-ComponentName</span></span>
<span data-ttu-id="18dd3-115">Nazwa składnika</span><span class="sxs-lookup"><span data-stu-id="18dd3-115">Component Name</span></span>

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

### <span data-ttu-id="18dd3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18dd3-116">-DefaultProfile</span></span>
<span data-ttu-id="18dd3-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="18dd3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18dd3-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="18dd3-118">-InputObject</span></span>
<span data-ttu-id="18dd3-119">PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="18dd3-119">PSApplicationInsightsComponent</span></span>

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

### <span data-ttu-id="18dd3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18dd3-120">-ResourceGroupName</span></span>
<span data-ttu-id="18dd3-121">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="18dd3-121">Resource Group Name</span></span>

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

### <span data-ttu-id="18dd3-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="18dd3-122">-ResourceId</span></span>
<span data-ttu-id="18dd3-123">Component ResourceId</span><span class="sxs-lookup"><span data-stu-id="18dd3-123">Component ResourceId</span></span>

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

### <span data-ttu-id="18dd3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18dd3-124">CommonParameters</span></span>
<span data-ttu-id="18dd3-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18dd3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18dd3-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="18dd3-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18dd3-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="18dd3-127">INPUTS</span></span>

### <span data-ttu-id="18dd3-128">System.String</span><span class="sxs-lookup"><span data-stu-id="18dd3-128">System.String</span></span>

### <span data-ttu-id="18dd3-129">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="18dd3-129">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="18dd3-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="18dd3-130">OUTPUTS</span></span>

### <span data-ttu-id="18dd3-131">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="18dd3-131">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span></span>

## <span data-ttu-id="18dd3-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="18dd3-132">NOTES</span></span>

## <span data-ttu-id="18dd3-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="18dd3-133">RELATED LINKS</span></span>
