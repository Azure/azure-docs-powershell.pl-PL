---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/remove-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnOriginGroup.md
ms.openlocfilehash: 081d5a73d6bd3cefff6f0c3bc57d3e0190f785a7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195162"
---
# <span data-ttu-id="67b6f-101">Remove-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="67b6f-101">Remove-AzCdnOriginGroup</span></span>

## <span data-ttu-id="67b6f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67b6f-102">SYNOPSIS</span></span>
<span data-ttu-id="67b6f-103">Usuwa grupę pochodzenia sieci CDN</span><span class="sxs-lookup"><span data-stu-id="67b6f-103">Removes a CDN origin group</span></span>

## <span data-ttu-id="67b6f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="67b6f-104">SYNTAX</span></span>

### <span data-ttu-id="67b6f-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="67b6f-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzCdnOriginGroup -OriginGroupName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="67b6f-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="67b6f-106">ByResourceIdParameterSet</span></span>
```
Remove-AzCdnOriginGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67b6f-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="67b6f-107">ByObjectParameterSet</span></span>
```
Remove-AzCdnOriginGroup [-PassThru] -CdnOriginGroup <PSOriginGroup> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67b6f-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="67b6f-108">DESCRIPTION</span></span>
<span data-ttu-id="67b6f-109">Remove-AzCdnOriginGroup spowoduje usunięcie grupy pochodzenia sieci CDN z określonego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="67b6f-109">Remove-AzCdnOriginGroup will remove a CDN origin group from the specified endpoint.</span></span> 

## <span data-ttu-id="67b6f-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="67b6f-110">EXAMPLES</span></span>

### <span data-ttu-id="67b6f-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="67b6f-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName
```

<span data-ttu-id="67b6f-112">To polecenie cmdlet spowoduje usunięcie określonej grupy pochodzenia z danego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="67b6f-112">This cmdlet will remove the specified origin group from the given endpoint.</span></span> 

## <span data-ttu-id="67b6f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="67b6f-113">PARAMETERS</span></span>

### <span data-ttu-id="67b6f-114">-CdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="67b6f-114">-CdnOriginGroup</span></span>
<span data-ttu-id="67b6f-115">Obiekt grupy pochodzenia sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="67b6f-115">The CDN origin group object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.OriginGroup.PSOriginGroup
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="67b6f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67b6f-116">-DefaultProfile</span></span>
<span data-ttu-id="67b6f-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="67b6f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67b6f-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="67b6f-118">-EndpointName</span></span>
<span data-ttu-id="67b6f-119">Nazwa punktu końcowego sieci Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="67b6f-119">Azure CDN endpoint name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67b6f-120">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="67b6f-120">-OriginGroupName</span></span>
<span data-ttu-id="67b6f-121">Nazwa grupy pochodzenia sieci Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="67b6f-121">Azure CDN origin group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67b6f-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="67b6f-122">-PassThru</span></span>
<span data-ttu-id="67b6f-123">Zwracanie obiektu, jeśli jest określony.</span><span class="sxs-lookup"><span data-stu-id="67b6f-123">Return object if specified.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67b6f-124">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="67b6f-124">-ProfileName</span></span>
<span data-ttu-id="67b6f-125">Nazwa profilu azure CDN.</span><span class="sxs-lookup"><span data-stu-id="67b6f-125">Azure CDN profile name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67b6f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67b6f-126">-ResourceGroupName</span></span>
<span data-ttu-id="67b6f-127">Grupa zasobów profilu azure CDN.</span><span class="sxs-lookup"><span data-stu-id="67b6f-127">The resource group of the Azure CDN profile.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67b6f-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="67b6f-128">-ResourceId</span></span>
<span data-ttu-id="67b6f-129">Identyfikator zasobu grupy pochodzenia sieci Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="67b6f-129">The resource id of the Azure CDN origin group.</span></span>

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

### <span data-ttu-id="67b6f-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="67b6f-130">-Confirm</span></span>
<span data-ttu-id="67b6f-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="67b6f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67b6f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67b6f-132">-WhatIf</span></span>
<span data-ttu-id="67b6f-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67b6f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67b6f-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="67b6f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67b6f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67b6f-135">CommonParameters</span></span>
<span data-ttu-id="67b6f-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67b6f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67b6f-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="67b6f-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67b6f-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="67b6f-138">INPUTS</span></span>

### <span data-ttu-id="67b6f-139">Brak</span><span class="sxs-lookup"><span data-stu-id="67b6f-139">None</span></span>

## <span data-ttu-id="67b6f-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="67b6f-140">OUTPUTS</span></span>

### <span data-ttu-id="67b6f-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="67b6f-141">System.Boolean</span></span>

## <span data-ttu-id="67b6f-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="67b6f-142">NOTES</span></span>

## <span data-ttu-id="67b6f-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="67b6f-143">RELATED LINKS</span></span>
