---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/get-azapplyupdate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzApplyUpdate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzApplyUpdate.md
ms.openlocfilehash: 35f504731ae176af9d476e770bc243c394ceb7af
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385875"
---
# <span data-ttu-id="92f7c-101">Get-AzApplyUpdate</span><span class="sxs-lookup"><span data-stu-id="92f7c-101">Get-AzApplyUpdate</span></span>

## <span data-ttu-id="92f7c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="92f7c-102">SYNOPSIS</span></span>
<span data-ttu-id="92f7c-103">Śledzenie aktualizacji konserwacji zasobów</span><span class="sxs-lookup"><span data-stu-id="92f7c-103">Track maintenance updates to resource</span></span>

## <span data-ttu-id="92f7c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="92f7c-104">SYNTAX</span></span>

```
Get-AzApplyUpdate [-ResourceGroupName] <String> [-ProviderName] <String> [-ResourceParentType <String>]
 [-ResourceParentName <String>] [-ResourceType] <String> [-ResourceName] <String> -ApplyUpdateName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92f7c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="92f7c-105">DESCRIPTION</span></span>
<span data-ttu-id="92f7c-106">Śledzenie aktualizacji konserwacji zasobów</span><span class="sxs-lookup"><span data-stu-id="92f7c-106">Track maintenance updates to resource</span></span>

## <span data-ttu-id="92f7c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="92f7c-107">EXAMPLES</span></span>

### <span data-ttu-id="92f7c-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="92f7c-108">Example 1</span></span>
```powershell
PS C:\> Get-AzApplyUpdate -ResourceGroupName smdtest$region -ResourceParentType hostGroups -ResourceParentName smddhg$region -ResourceType hosts -ResourceName smddh$region -ProviderName Microsoft.Compute -ApplyUpdateName default


Status         : InProgress
ResourceId     : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2
LastUpdateTime : 11/8/2019 9:39:01 AM
Id             : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2/providers/Microsoft.Maintenance/applyUpdates/default
Name           : default
Type           : Microsoft.Maintenance/applyUpdates
```

<span data-ttu-id="92f7c-109">Śledzenie aktualizacji konserwacji zasobów</span><span class="sxs-lookup"><span data-stu-id="92f7c-109">Track maintenance updates to resource</span></span>

## <span data-ttu-id="92f7c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="92f7c-110">PARAMETERS</span></span>

### <span data-ttu-id="92f7c-111">-ApplyUpdateName</span><span class="sxs-lookup"><span data-stu-id="92f7c-111">-ApplyUpdateName</span></span>
<span data-ttu-id="92f7c-112">Nazwa zasobu aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="92f7c-112">The apply update resource name.</span></span>

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

### <span data-ttu-id="92f7c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92f7c-113">-DefaultProfile</span></span>
<span data-ttu-id="92f7c-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="92f7c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92f7c-115">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="92f7c-115">-ProviderName</span></span>
<span data-ttu-id="92f7c-116">Nazwa dostawcy zasobów.</span><span class="sxs-lookup"><span data-stu-id="92f7c-116">The resource provider Name.</span></span>

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

### <span data-ttu-id="92f7c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92f7c-117">-ResourceGroupName</span></span>
<span data-ttu-id="92f7c-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="92f7c-118">The resource Group Name.</span></span>

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

### <span data-ttu-id="92f7c-119">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="92f7c-119">-ResourceName</span></span>
<span data-ttu-id="92f7c-120">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="92f7c-120">The resource name.</span></span>

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

### <span data-ttu-id="92f7c-121">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="92f7c-121">-ResourceParentName</span></span>
<span data-ttu-id="92f7c-122">Nazwa zasobu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="92f7c-122">The parent resource name.</span></span>

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

### <span data-ttu-id="92f7c-123">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="92f7c-123">-ResourceParentType</span></span>
<span data-ttu-id="92f7c-124">Nadrzędny typ zasobu.</span><span class="sxs-lookup"><span data-stu-id="92f7c-124">The parent resource type.</span></span>

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

### <span data-ttu-id="92f7c-125">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="92f7c-125">-ResourceType</span></span>
<span data-ttu-id="92f7c-126">Typ zasobu.</span><span class="sxs-lookup"><span data-stu-id="92f7c-126">The resource type.</span></span>

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

### <span data-ttu-id="92f7c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92f7c-127">CommonParameters</span></span>
<span data-ttu-id="92f7c-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92f7c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92f7c-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="92f7c-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92f7c-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="92f7c-130">INPUTS</span></span>

### <span data-ttu-id="92f7c-131">System. String</span><span class="sxs-lookup"><span data-stu-id="92f7c-131">System.String</span></span>

## <span data-ttu-id="92f7c-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="92f7c-132">OUTPUTS</span></span>

### <span data-ttu-id="92f7c-133">Microsoft. Azure. Commands. Maintenance. models. PSApplyUpdate</span><span class="sxs-lookup"><span data-stu-id="92f7c-133">Microsoft.Azure.Commands.Maintenance.Models.PSApplyUpdate</span></span>

## <span data-ttu-id="92f7c-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="92f7c-134">NOTES</span></span>

## <span data-ttu-id="92f7c-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="92f7c-135">RELATED LINKS</span></span>
