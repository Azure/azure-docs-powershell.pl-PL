---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/get-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: 7e879cd4e513ebdad297933269e373c625f2e407
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062447"
---
# <span data-ttu-id="5da45-101">Get-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5da45-101">Get-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="5da45-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5da45-102">SYNOPSIS</span></span>
<span data-ttu-id="5da45-103">Uzyskiwanie połączonego konta magazynu połączonego z aplikacją Application Insights</span><span class="sxs-lookup"><span data-stu-id="5da45-103">Get application insights linked storage account</span></span>

## <span data-ttu-id="5da45-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5da45-104">SYNTAX</span></span>

### <span data-ttu-id="5da45-105">ByResourceNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5da45-105">ByResourceNameParameterSet (Default)</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5da45-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5da45-106">ByInputObjectParameterSet</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5da45-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5da45-107">ByResourceIdParameterSet</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5da45-108">Opis</span><span class="sxs-lookup"><span data-stu-id="5da45-108">DESCRIPTION</span></span>
<span data-ttu-id="5da45-109">Uzyskiwanie połączonego konta magazynu połączonego z aplikacją Application Insights</span><span class="sxs-lookup"><span data-stu-id="5da45-109">Get application insights linked storage account</span></span>

## <span data-ttu-id="5da45-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5da45-110">EXAMPLES</span></span>

### <span data-ttu-id="5da45-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5da45-111">Example 1</span></span>
```powershell
Get-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName "rgName" -Name "componentName"
```

<span data-ttu-id="5da45-112">Uzyskiwanie połączonego konta magazynu skojarzonego ze składnikiem "ComponentName"</span><span class="sxs-lookup"><span data-stu-id="5da45-112">Get linked storage account associated with component "componentName"</span></span>

## <span data-ttu-id="5da45-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5da45-113">PARAMETERS</span></span>

### <span data-ttu-id="5da45-114">-Składnikname</span><span class="sxs-lookup"><span data-stu-id="5da45-114">-ComponentName</span></span>
<span data-ttu-id="5da45-115">Nazwa składnika</span><span class="sxs-lookup"><span data-stu-id="5da45-115">Component Name</span></span>

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

### <span data-ttu-id="5da45-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5da45-116">-DefaultProfile</span></span>
<span data-ttu-id="5da45-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5da45-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5da45-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5da45-118">-InputObject</span></span>
<span data-ttu-id="5da45-119">PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="5da45-119">PSApplicationInsightsComponent</span></span>

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

### <span data-ttu-id="5da45-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5da45-120">-ResourceGroupName</span></span>
<span data-ttu-id="5da45-121">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="5da45-121">Resource Group Name</span></span>

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

### <span data-ttu-id="5da45-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5da45-122">-ResourceId</span></span>
<span data-ttu-id="5da45-123">Identyfikator zasobu składnika</span><span class="sxs-lookup"><span data-stu-id="5da45-123">Component ResourceId</span></span>

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

### <span data-ttu-id="5da45-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5da45-124">CommonParameters</span></span>
<span data-ttu-id="5da45-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5da45-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5da45-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5da45-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5da45-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5da45-127">INPUTS</span></span>

### <span data-ttu-id="5da45-128">System. String</span><span class="sxs-lookup"><span data-stu-id="5da45-128">System.String</span></span>

### <span data-ttu-id="5da45-129">Microsoft. Azure. Commands. ApplicationInsights. models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="5da45-129">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="5da45-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5da45-130">OUTPUTS</span></span>

### <span data-ttu-id="5da45-131">Microsoft. Azure. Commands. ApplicationInsights. models. PSComponentLinkedStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="5da45-131">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span></span>

## <span data-ttu-id="5da45-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5da45-132">NOTES</span></span>

## <span data-ttu-id="5da45-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5da45-133">RELATED LINKS</span></span>
