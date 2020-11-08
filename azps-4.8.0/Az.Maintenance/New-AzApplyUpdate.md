---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/new-azapplyupdate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzApplyUpdate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzApplyUpdate.md
ms.openlocfilehash: 05403ce85b80238aeee8749322bdd94d28be68da
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220608"
---
# <span data-ttu-id="3a5ca-101">New-AzApplyUpdate</span><span class="sxs-lookup"><span data-stu-id="3a5ca-101">New-AzApplyUpdate</span></span>

## <span data-ttu-id="3a5ca-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3a5ca-102">SYNOPSIS</span></span>
<span data-ttu-id="3a5ca-103">Stosowanie aktualizacji konserwacji do zasobu</span><span class="sxs-lookup"><span data-stu-id="3a5ca-103">Apply maintenance updates to resource</span></span>

## <span data-ttu-id="3a5ca-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3a5ca-104">SYNTAX</span></span>

```
New-AzApplyUpdate [-ResourceGroupName] <String> [-ProviderName] <String> [-ResourceParentType <String>]
 [-ResourceParentName <String>] [-ResourceType] <String> [-ResourceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a5ca-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3a5ca-105">DESCRIPTION</span></span>
<span data-ttu-id="3a5ca-106">Stosowanie aktualizacji konserwacji do zasobu</span><span class="sxs-lookup"><span data-stu-id="3a5ca-106">Apply maintenance updates to resource</span></span>

## <span data-ttu-id="3a5ca-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3a5ca-107">EXAMPLES</span></span>

### <span data-ttu-id="3a5ca-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3a5ca-108">Example 1</span></span>
```powershell
PS C:\> New-AzApplyUpdate -ResourceGroupName smdtest$region -ResourceParentType hostGroups -ResourceParentName smddhg$region -ResourceType hosts -ResourceName smddh$region -ProviderName Microsoft.Compute


Status         : InProgress
ResourceId     : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2
LastUpdateTime : 11/8/2019 9:39:01 AM
Id             :
/subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2/providers/Microsoft.Maintenance/applyUpdates/cbd4c97d-2011-4fa3-9df1-525f97e74eac
Name           : cbd4c97d-2011-4fa3-9df1-525f97e74eac
Type           : Microsoft.Maintenance/applyUpdates
```

<span data-ttu-id="3a5ca-109">Stosowanie aktualizacji konserwacji do zasobu</span><span class="sxs-lookup"><span data-stu-id="3a5ca-109">Apply maintenance updates to resource</span></span>

## <span data-ttu-id="3a5ca-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3a5ca-110">PARAMETERS</span></span>

### <span data-ttu-id="3a5ca-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3a5ca-111">-AsJob</span></span>
<span data-ttu-id="3a5ca-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="3a5ca-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a5ca-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a5ca-113">-DefaultProfile</span></span>
<span data-ttu-id="3a5ca-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3a5ca-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a5ca-115">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="3a5ca-115">-ProviderName</span></span>
<span data-ttu-id="3a5ca-116">Nazwa dostawcy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3a5ca-116">The resource provider Name.</span></span>

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

### <span data-ttu-id="3a5ca-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a5ca-117">-ResourceGroupName</span></span>
<span data-ttu-id="3a5ca-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3a5ca-118">The resource Group Name.</span></span>

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

### <span data-ttu-id="3a5ca-119">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="3a5ca-119">-ResourceName</span></span>
<span data-ttu-id="3a5ca-120">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="3a5ca-120">The resource name.</span></span>

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

### <span data-ttu-id="3a5ca-121">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="3a5ca-121">-ResourceParentName</span></span>
<span data-ttu-id="3a5ca-122">Nazwa zasobu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="3a5ca-122">The parent resource name.</span></span>

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

### <span data-ttu-id="3a5ca-123">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="3a5ca-123">-ResourceParentType</span></span>
<span data-ttu-id="3a5ca-124">Nadrzędny typ zasobu.</span><span class="sxs-lookup"><span data-stu-id="3a5ca-124">The parent resource type.</span></span>

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

### <span data-ttu-id="3a5ca-125">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="3a5ca-125">-ResourceType</span></span>
<span data-ttu-id="3a5ca-126">Typ zasobu.</span><span class="sxs-lookup"><span data-stu-id="3a5ca-126">The resource type.</span></span>

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

### <span data-ttu-id="3a5ca-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3a5ca-127">-Confirm</span></span>
<span data-ttu-id="3a5ca-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a5ca-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a5ca-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a5ca-129">-WhatIf</span></span>
<span data-ttu-id="3a5ca-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a5ca-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a5ca-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3a5ca-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a5ca-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a5ca-132">CommonParameters</span></span>
<span data-ttu-id="3a5ca-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a5ca-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a5ca-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3a5ca-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a5ca-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3a5ca-135">INPUTS</span></span>

### <span data-ttu-id="3a5ca-136">System. String</span><span class="sxs-lookup"><span data-stu-id="3a5ca-136">System.String</span></span>

## <span data-ttu-id="3a5ca-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3a5ca-137">OUTPUTS</span></span>

### <span data-ttu-id="3a5ca-138">Microsoft. Azure. Commands. Maintenance. models. PSApplyUpdate</span><span class="sxs-lookup"><span data-stu-id="3a5ca-138">Microsoft.Azure.Commands.Maintenance.Models.PSApplyUpdate</span></span>

## <span data-ttu-id="3a5ca-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3a5ca-139">NOTES</span></span>

## <span data-ttu-id="3a5ca-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3a5ca-140">RELATED LINKS</span></span>
