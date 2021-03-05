---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/remove-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnOrigin.md
ms.openlocfilehash: b6c5a95e8966cfe22b520c1f41b87f88cbdb1361
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985335"
---
# <span data-ttu-id="740cd-101">Remove-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="740cd-101">Remove-AzCdnOrigin</span></span>

## <span data-ttu-id="740cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="740cd-102">SYNOPSIS</span></span>
<span data-ttu-id="740cd-103">Usuwa pochodzenie sieci CDN</span><span class="sxs-lookup"><span data-stu-id="740cd-103">Removes a CDN origin</span></span>

## <span data-ttu-id="740cd-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="740cd-104">SYNTAX</span></span>

### <span data-ttu-id="740cd-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="740cd-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzCdnOrigin -OriginName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="740cd-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="740cd-106">ByResourceIdParameterSet</span></span>
```
Remove-AzCdnOrigin -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="740cd-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="740cd-107">ByObjectParameterSet</span></span>
```
Remove-AzCdnOrigin [-PassThru] -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="740cd-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="740cd-108">DESCRIPTION</span></span>
<span data-ttu-id="740cd-109">Remove-AzCdnOrigin źródła sieci CDN z danego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="740cd-109">Remove-AzCdnOrigin will delete a CDN origin from the given endpoint.</span></span> <span data-ttu-id="740cd-110">Jeśli pochodzenie jest jedynym pochodzeniem w określonym punkcie końcowym, usunięcie nie powiedzie się, ponieważ jest wymagane co najmniej 1 pochodzenie.</span><span class="sxs-lookup"><span data-stu-id="740cd-110">If the origin is the only origin within the specified endpoint, then the deletion will fail since at least 1 origin is needed.</span></span> 

## <span data-ttu-id="740cd-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="740cd-111">EXAMPLES</span></span>

### <span data-ttu-id="740cd-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="740cd-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzCdnOrigin -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginName $originName 
```
<span data-ttu-id="740cd-113">To polecenie cmdlet spowoduje usunięcie określonego pochodzenia z danego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="740cd-113">This cmdlet will remove the specified origin from the given endpoint.</span></span> 

## <span data-ttu-id="740cd-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="740cd-114">PARAMETERS</span></span>

### <span data-ttu-id="740cd-115">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="740cd-115">-CdnOrigin</span></span>
<span data-ttu-id="740cd-116">Obiekt pochodzenia sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="740cd-116">The CDN origin object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="740cd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="740cd-117">-DefaultProfile</span></span>
<span data-ttu-id="740cd-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="740cd-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="740cd-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="740cd-119">-EndpointName</span></span>
<span data-ttu-id="740cd-120">Nazwa punktu końcowego sieci Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="740cd-120">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="740cd-121">-OriginName</span><span class="sxs-lookup"><span data-stu-id="740cd-121">-OriginName</span></span>
<span data-ttu-id="740cd-122">Nazwa pochodzenia sieci Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="740cd-122">Azure CDN origin name.</span></span>

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

### <span data-ttu-id="740cd-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="740cd-123">-PassThru</span></span>
<span data-ttu-id="740cd-124">Zwracanie obiektu, jeśli jest określony.</span><span class="sxs-lookup"><span data-stu-id="740cd-124">Return object if specified.</span></span>

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

### <span data-ttu-id="740cd-125">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="740cd-125">-ProfileName</span></span>
<span data-ttu-id="740cd-126">Nazwa profilu azure CDN.</span><span class="sxs-lookup"><span data-stu-id="740cd-126">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="740cd-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="740cd-127">-ResourceGroupName</span></span>
<span data-ttu-id="740cd-128">Grupa zasobów profilu azure CDN.</span><span class="sxs-lookup"><span data-stu-id="740cd-128">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="740cd-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="740cd-129">-ResourceId</span></span>
<span data-ttu-id="740cd-130">Identyfikator zasobu pochodzenia sieci Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="740cd-130">The resource id of the Azure CDN origin.</span></span>

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

### <span data-ttu-id="740cd-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="740cd-131">-Confirm</span></span>
<span data-ttu-id="740cd-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="740cd-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="740cd-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="740cd-133">-WhatIf</span></span>
<span data-ttu-id="740cd-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="740cd-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="740cd-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="740cd-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="740cd-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="740cd-136">CommonParameters</span></span>
<span data-ttu-id="740cd-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="740cd-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="740cd-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="740cd-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="740cd-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="740cd-139">INPUTS</span></span>

### <span data-ttu-id="740cd-140">Brak</span><span class="sxs-lookup"><span data-stu-id="740cd-140">None</span></span>

## <span data-ttu-id="740cd-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="740cd-141">OUTPUTS</span></span>

### <span data-ttu-id="740cd-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="740cd-142">System.Boolean</span></span>

## <span data-ttu-id="740cd-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="740cd-143">NOTES</span></span>

## <span data-ttu-id="740cd-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="740cd-144">RELATED LINKS</span></span>
