---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/get-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: 7e879cd4e513ebdad297933269e373c625f2e407
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195283"
---
# <span data-ttu-id="f22a5-101">Get-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f22a5-101">Get-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="f22a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f22a5-102">SYNOPSIS</span></span>
<span data-ttu-id="f22a5-103">Uzyskiwanie połączonych kont magazynu szczegółowych informacji o aplikacjach</span><span class="sxs-lookup"><span data-stu-id="f22a5-103">Get application insights linked storage account</span></span>

## <span data-ttu-id="f22a5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f22a5-104">SYNTAX</span></span>

### <span data-ttu-id="f22a5-105">ByResourceNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="f22a5-105">ByResourceNameParameterSet (Default)</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f22a5-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f22a5-106">ByInputObjectParameterSet</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f22a5-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f22a5-107">ByResourceIdParameterSet</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f22a5-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="f22a5-108">DESCRIPTION</span></span>
<span data-ttu-id="f22a5-109">Uzyskiwanie połączonych kont magazynu szczegółowych informacji o aplikacjach</span><span class="sxs-lookup"><span data-stu-id="f22a5-109">Get application insights linked storage account</span></span>

## <span data-ttu-id="f22a5-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f22a5-110">EXAMPLES</span></span>

### <span data-ttu-id="f22a5-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f22a5-111">Example 1</span></span>
```powershell
Get-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName "rgName" -Name "componentName"
```

<span data-ttu-id="f22a5-112">Uzyskiwanie połączonego konta magazynu skojarzonego ze składnikiem "componentName"</span><span class="sxs-lookup"><span data-stu-id="f22a5-112">Get linked storage account associated with component "componentName"</span></span>

## <span data-ttu-id="f22a5-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f22a5-113">PARAMETERS</span></span>

### <span data-ttu-id="f22a5-114">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="f22a5-114">-ComponentName</span></span>
<span data-ttu-id="f22a5-115">Nazwa składnika</span><span class="sxs-lookup"><span data-stu-id="f22a5-115">Component Name</span></span>

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

### <span data-ttu-id="f22a5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f22a5-116">-DefaultProfile</span></span>
<span data-ttu-id="f22a5-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f22a5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f22a5-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f22a5-118">-InputObject</span></span>
<span data-ttu-id="f22a5-119">PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="f22a5-119">PSApplicationInsightsComponent</span></span>

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

### <span data-ttu-id="f22a5-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f22a5-120">-ResourceGroupName</span></span>
<span data-ttu-id="f22a5-121">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="f22a5-121">Resource Group Name</span></span>

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

### <span data-ttu-id="f22a5-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f22a5-122">-ResourceId</span></span>
<span data-ttu-id="f22a5-123">Component ResourceId</span><span class="sxs-lookup"><span data-stu-id="f22a5-123">Component ResourceId</span></span>

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

### <span data-ttu-id="f22a5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f22a5-124">CommonParameters</span></span>
<span data-ttu-id="f22a5-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f22a5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f22a5-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f22a5-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f22a5-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f22a5-127">INPUTS</span></span>

### <span data-ttu-id="f22a5-128">System.String</span><span class="sxs-lookup"><span data-stu-id="f22a5-128">System.String</span></span>

### <span data-ttu-id="f22a5-129">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="f22a5-129">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="f22a5-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f22a5-130">OUTPUTS</span></span>

### <span data-ttu-id="f22a5-131">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="f22a5-131">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span></span>

## <span data-ttu-id="f22a5-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f22a5-132">NOTES</span></span>

## <span data-ttu-id="f22a5-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f22a5-133">RELATED LINKS</span></span>
