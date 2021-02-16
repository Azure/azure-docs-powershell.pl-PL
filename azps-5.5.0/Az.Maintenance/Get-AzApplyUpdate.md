---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/get-azapplyupdate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzApplyUpdate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzApplyUpdate.md
ms.openlocfilehash: 35f504731ae176af9d476e770bc243c394ceb7af
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241322"
---
# <span data-ttu-id="ef707-101">Get-AzApplyUpdate</span><span class="sxs-lookup"><span data-stu-id="ef707-101">Get-AzApplyUpdate</span></span>

## <span data-ttu-id="ef707-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef707-102">SYNOPSIS</span></span>
<span data-ttu-id="ef707-103">Śledzenie aktualizacji konserwacji zasobu</span><span class="sxs-lookup"><span data-stu-id="ef707-103">Track maintenance updates to resource</span></span>

## <span data-ttu-id="ef707-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ef707-104">SYNTAX</span></span>

```
Get-AzApplyUpdate [-ResourceGroupName] <String> [-ProviderName] <String> [-ResourceParentType <String>]
 [-ResourceParentName <String>] [-ResourceType] <String> [-ResourceName] <String> -ApplyUpdateName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef707-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="ef707-105">DESCRIPTION</span></span>
<span data-ttu-id="ef707-106">Śledzenie aktualizacji konserwacji zasobu</span><span class="sxs-lookup"><span data-stu-id="ef707-106">Track maintenance updates to resource</span></span>

## <span data-ttu-id="ef707-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ef707-107">EXAMPLES</span></span>

### <span data-ttu-id="ef707-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ef707-108">Example 1</span></span>
```powershell
PS C:\> Get-AzApplyUpdate -ResourceGroupName smdtest$region -ResourceParentType hostGroups -ResourceParentName smddhg$region -ResourceType hosts -ResourceName smddh$region -ProviderName Microsoft.Compute -ApplyUpdateName default


Status         : InProgress
ResourceId     : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2
LastUpdateTime : 11/8/2019 9:39:01 AM
Id             : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2/providers/Microsoft.Maintenance/applyUpdates/default
Name           : default
Type           : Microsoft.Maintenance/applyUpdates
```

<span data-ttu-id="ef707-109">Śledzenie aktualizacji konserwacji zasobu</span><span class="sxs-lookup"><span data-stu-id="ef707-109">Track maintenance updates to resource</span></span>

## <span data-ttu-id="ef707-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ef707-110">PARAMETERS</span></span>

### <span data-ttu-id="ef707-111">-ApplyUpdateName</span><span class="sxs-lookup"><span data-stu-id="ef707-111">-ApplyUpdateName</span></span>
<span data-ttu-id="ef707-112">Zastosowanie nazwy zasobu aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="ef707-112">The apply update resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef707-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef707-113">-DefaultProfile</span></span>
<span data-ttu-id="ef707-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ef707-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef707-115">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="ef707-115">-ProviderName</span></span>
<span data-ttu-id="ef707-116">Nazwa dostawcy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ef707-116">The resource provider Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef707-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef707-117">-ResourceGroupName</span></span>
<span data-ttu-id="ef707-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ef707-118">The resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef707-119">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="ef707-119">-ResourceName</span></span>
<span data-ttu-id="ef707-120">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="ef707-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef707-121">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="ef707-121">-ResourceParentName</span></span>
<span data-ttu-id="ef707-122">Nazwa zasobu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="ef707-122">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef707-123">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="ef707-123">-ResourceParentType</span></span>
<span data-ttu-id="ef707-124">Nadrzędny typ zasobu.</span><span class="sxs-lookup"><span data-stu-id="ef707-124">The parent resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef707-125">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="ef707-125">-ResourceType</span></span>
<span data-ttu-id="ef707-126">Typ zasobu.</span><span class="sxs-lookup"><span data-stu-id="ef707-126">The resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef707-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef707-127">CommonParameters</span></span>
<span data-ttu-id="ef707-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef707-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef707-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ef707-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef707-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ef707-130">INPUTS</span></span>

### <span data-ttu-id="ef707-131">System.String</span><span class="sxs-lookup"><span data-stu-id="ef707-131">System.String</span></span>

## <span data-ttu-id="ef707-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ef707-132">OUTPUTS</span></span>

### <span data-ttu-id="ef707-133">Microsoft.Azure.Commands.Maintenance.Models.PSApplyUpdate</span><span class="sxs-lookup"><span data-stu-id="ef707-133">Microsoft.Azure.Commands.Maintenance.Models.PSApplyUpdate</span></span>

## <span data-ttu-id="ef707-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ef707-134">NOTES</span></span>

## <span data-ttu-id="ef707-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ef707-135">RELATED LINKS</span></span>
