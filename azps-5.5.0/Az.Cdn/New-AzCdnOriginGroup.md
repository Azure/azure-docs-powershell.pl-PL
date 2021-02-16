---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOriginGroup.md
ms.openlocfilehash: 9c499fe716df97edc4644729dc996bd4f9bae992
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200818"
---
# <span data-ttu-id="fca43-101">New-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="fca43-101">New-AzCdnOriginGroup</span></span>

## <span data-ttu-id="fca43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fca43-102">SYNOPSIS</span></span>
<span data-ttu-id="fca43-103">Tworzy nową grupę pochodzenia sieci CDN</span><span class="sxs-lookup"><span data-stu-id="fca43-103">Creates a new CDN origin group</span></span>

## <span data-ttu-id="fca43-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fca43-104">SYNTAX</span></span>

### <span data-ttu-id="fca43-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="fca43-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnOriginGroup -EndpointName <String> -OriginGroupName <String>
 -OriginId <System.Collections.Generic.List`1[System.String]> [-ProbeIntervalInSeconds <Int32>]
 [-ProbePath <String>] [-ProbeProtocol <String>] [-ProbeRequestType <String>] -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fca43-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fca43-106">ByObjectParameterSet</span></span>
```
New-AzCdnOriginGroup -CdnOriginGroup <PSOriginGroup> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fca43-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="fca43-107">DESCRIPTION</span></span>
<span data-ttu-id="fca43-108">Grupa New-AzCdnOriginGroup utworzy nową grupę pochodzenia w określonym punkcie końcowym.</span><span class="sxs-lookup"><span data-stu-id="fca43-108">The New-AzCdnOriginGroup will create a new origin group within the specified endpoint.</span></span> <span data-ttu-id="fca43-109">Jeśli jest to pierwsza grupa pochodzenia dla punktu końcowego, należy również ustawić właściwość DefaultOriginGroup.</span><span class="sxs-lookup"><span data-stu-id="fca43-109">If this is the first origin group for endpoint, then the DefaultOriginGroup property must also be set.</span></span>

## <span data-ttu-id="fca43-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fca43-110">EXAMPLES</span></span>

### <span data-ttu-id="fca43-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fca43-111">Example 1</span></span>
```powershell
PS C:\> New-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName -OriginId $originId
```
<span data-ttu-id="fca43-112">To polecenie cmdlet utworzy nową grupę pochodzenia w określonym punkcie końcowym.</span><span class="sxs-lookup"><span data-stu-id="fca43-112">This cmdlet will create a new origin group within the specified endpoint.</span></span> <span data-ttu-id="fca43-113">Spowoduje to wykorzystanie podanych identyfikatorów pochodzenia jako zestawu pochodzenia.</span><span class="sxs-lookup"><span data-stu-id="fca43-113">It will utilize the given origin ids as the set of origins.</span></span>

## <span data-ttu-id="fca43-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fca43-114">PARAMETERS</span></span>

### <span data-ttu-id="fca43-115">-CdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="fca43-115">-CdnOriginGroup</span></span>
<span data-ttu-id="fca43-116">Obiekt grupy pochodzenia sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="fca43-116">The CDN origin group object.</span></span>

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

### <span data-ttu-id="fca43-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fca43-117">-DefaultProfile</span></span>
<span data-ttu-id="fca43-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fca43-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fca43-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="fca43-119">-EndpointName</span></span>
<span data-ttu-id="fca43-120">Nazwa punktu końcowego sieci Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="fca43-120">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="fca43-121">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="fca43-121">-OriginGroupName</span></span>
<span data-ttu-id="fca43-122">Nazwa grupy pochodzenia sieci Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="fca43-122">Azure CDN origin group name.</span></span>

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

### <span data-ttu-id="fca43-123">-OriginId</span><span class="sxs-lookup"><span data-stu-id="fca43-123">-OriginId</span></span>
<span data-ttu-id="fca43-124">Identyfikatory grup pochodzenia sieci Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="fca43-124">Azure CDN origin group ids.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fca43-125">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="fca43-125">-ProbeIntervalInSeconds</span></span>
<span data-ttu-id="fca43-126">Liczba sekund między kondycją.</span><span class="sxs-lookup"><span data-stu-id="fca43-126">The number of seconds between health probes.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fca43-127">-Path</span><span class="sxs-lookup"><span data-stu-id="fca43-127">-ProbePath</span></span>
<span data-ttu-id="fca43-128">Ścieżka względna względem pochodzenia używanego do określenia kondycji pochodzenia.</span><span class="sxs-lookup"><span data-stu-id="fca43-128">The path relative to the origin that is used to determine the health of the origin.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fca43-129">-Wprotocol</span><span class="sxs-lookup"><span data-stu-id="fca43-129">-ProbeProtocol</span></span>
<span data-ttu-id="fca43-130">Protokół do użycia na użytek kondycji zdrowotnej.</span><span class="sxs-lookup"><span data-stu-id="fca43-130">Protocol to use for health probe.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fca43-131">-SzemraquestType</span><span class="sxs-lookup"><span data-stu-id="fca43-131">-ProbeRequestType</span></span>
<span data-ttu-id="fca43-132">Typ żądania kondycji.</span><span class="sxs-lookup"><span data-stu-id="fca43-132">The type of health probe request that is made.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fca43-133">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="fca43-133">-ProfileName</span></span>
<span data-ttu-id="fca43-134">Nazwa profilu azure CDN.</span><span class="sxs-lookup"><span data-stu-id="fca43-134">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="fca43-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fca43-135">-ResourceGroupName</span></span>
<span data-ttu-id="fca43-136">Grupa zasobów profilu azure CDN.</span><span class="sxs-lookup"><span data-stu-id="fca43-136">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="fca43-137">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fca43-137">-Confirm</span></span>
<span data-ttu-id="fca43-138">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="fca43-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fca43-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fca43-139">-WhatIf</span></span>
<span data-ttu-id="fca43-140">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fca43-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fca43-141">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="fca43-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fca43-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fca43-142">CommonParameters</span></span>
<span data-ttu-id="fca43-143">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fca43-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fca43-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fca43-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fca43-145">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fca43-145">INPUTS</span></span>

### <span data-ttu-id="fca43-146">System.Object</span><span class="sxs-lookup"><span data-stu-id="fca43-146">System.Object</span></span>

## <span data-ttu-id="fca43-147">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fca43-147">OUTPUTS</span></span>

### <span data-ttu-id="fca43-148">System.Object</span><span class="sxs-lookup"><span data-stu-id="fca43-148">System.Object</span></span>

## <span data-ttu-id="fca43-149">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fca43-149">NOTES</span></span>

## <span data-ttu-id="fca43-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fca43-150">RELATED LINKS</span></span>
