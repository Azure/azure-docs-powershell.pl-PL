---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: d5986694ad0064265bbd4bad6e1efc378683ce97
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203482"
---
# <span data-ttu-id="a7b3f-101">Get-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="a7b3f-101">Get-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="a7b3f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7b3f-102">SYNOPSIS</span></span>
<span data-ttu-id="a7b3f-103">Uzyskiwanie zakresu prywatnego linku</span><span class="sxs-lookup"><span data-stu-id="a7b3f-103">Get private link scope</span></span>

## <span data-ttu-id="a7b3f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a7b3f-104">SYNTAX</span></span>

### <span data-ttu-id="a7b3f-105">ByResourceGroupParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="a7b3f-105">ByResourceGroupParameterSet (Default)</span></span>
```
Get-AzInsightsPrivateLinkScope [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a7b3f-106">ByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a7b3f-106">ByResourceNameParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScope -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a7b3f-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a7b3f-107">ByResourceIdParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScope -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a7b3f-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="a7b3f-108">DESCRIPTION</span></span>
<span data-ttu-id="a7b3f-109">Lista lub uzyskiwanie zakresu prywatnego linku</span><span class="sxs-lookup"><span data-stu-id="a7b3f-109">List or get private link scope</span></span> 

## <span data-ttu-id="a7b3f-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a7b3f-110">EXAMPLES</span></span>

### <span data-ttu-id="a7b3f-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a7b3f-111">Example 1</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name"
```

<span data-ttu-id="a7b3f-112">Lista zakresów prywatnych łączy w grupie zasobów "rg_name"</span><span class="sxs-lookup"><span data-stu-id="a7b3f-112">List private link scopes under resource group "rg_name"</span></span>

### <span data-ttu-id="a7b3f-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a7b3f-113">Example 2</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name"
```

<span data-ttu-id="a7b3f-114">Uzyskiwanie zakresu prywatnego linku o nazwie "scope_name" w grupie zasobów "rg_name"</span><span class="sxs-lookup"><span data-stu-id="a7b3f-114">Get private link scope with name "scope_name" under resource group "rg_name"</span></span>

## <span data-ttu-id="a7b3f-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a7b3f-115">PARAMETERS</span></span>

### <span data-ttu-id="a7b3f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7b3f-116">-DefaultProfile</span></span>
<span data-ttu-id="a7b3f-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a7b3f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7b3f-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a7b3f-118">-Name</span></span>
<span data-ttu-id="a7b3f-119">Nazwa zakresu łącza prywatnego</span><span class="sxs-lookup"><span data-stu-id="a7b3f-119">Private Link Scope Name</span></span>

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

### <span data-ttu-id="a7b3f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7b3f-120">-ResourceGroupName</span></span>
<span data-ttu-id="a7b3f-121">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="a7b3f-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### <span data-ttu-id="a7b3f-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a7b3f-122">-ResourceId</span></span>
<span data-ttu-id="a7b3f-123">Identyfikator zasobu</span><span class="sxs-lookup"><span data-stu-id="a7b3f-123">Resource Id</span></span>

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

### <span data-ttu-id="a7b3f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7b3f-124">CommonParameters</span></span>
<span data-ttu-id="a7b3f-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7b3f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7b3f-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a7b3f-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7b3f-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a7b3f-127">INPUTS</span></span>

### <span data-ttu-id="a7b3f-128">System.String</span><span class="sxs-lookup"><span data-stu-id="a7b3f-128">System.String</span></span>

## <span data-ttu-id="a7b3f-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a7b3f-129">OUTPUTS</span></span>

### <span data-ttu-id="a7b3f-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="a7b3f-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

## <span data-ttu-id="a7b3f-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a7b3f-131">NOTES</span></span>

## <span data-ttu-id="a7b3f-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a7b3f-132">RELATED LINKS</span></span>
