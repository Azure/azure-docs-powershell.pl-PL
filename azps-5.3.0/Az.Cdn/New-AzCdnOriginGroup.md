---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOriginGroup.md
ms.openlocfilehash: 9c499fe716df97edc4644729dc996bd4f9bae992
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504195"
---
# <span data-ttu-id="c3e05-101">New-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="c3e05-101">New-AzCdnOriginGroup</span></span>

## <span data-ttu-id="c3e05-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c3e05-102">SYNOPSIS</span></span>
<span data-ttu-id="c3e05-103">Tworzy nową grupę pochodzenia sieci CDN</span><span class="sxs-lookup"><span data-stu-id="c3e05-103">Creates a new CDN origin group</span></span>

## <span data-ttu-id="c3e05-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c3e05-104">SYNTAX</span></span>

### <span data-ttu-id="c3e05-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c3e05-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnOriginGroup -EndpointName <String> -OriginGroupName <String>
 -OriginId <System.Collections.Generic.List`1[System.String]> [-ProbeIntervalInSeconds <Int32>]
 [-ProbePath <String>] [-ProbeProtocol <String>] [-ProbeRequestType <String>] -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c3e05-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3e05-106">ByObjectParameterSet</span></span>
```
New-AzCdnOriginGroup -CdnOriginGroup <PSOriginGroup> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3e05-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c3e05-107">DESCRIPTION</span></span>
<span data-ttu-id="c3e05-108">New-AzCdnOriginGroup utworzy nową grupę źródłową w określonym punkcie końcowym.</span><span class="sxs-lookup"><span data-stu-id="c3e05-108">The New-AzCdnOriginGroup will create a new origin group within the specified endpoint.</span></span> <span data-ttu-id="c3e05-109">Jeśli jest to pierwsza grupa źródłowa punktu końcowego, należy również ustawić właściwość DefaultOriginGroup.</span><span class="sxs-lookup"><span data-stu-id="c3e05-109">If this is the first origin group for endpoint, then the DefaultOriginGroup property must also be set.</span></span>

## <span data-ttu-id="c3e05-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c3e05-110">EXAMPLES</span></span>

### <span data-ttu-id="c3e05-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c3e05-111">Example 1</span></span>
```powershell
PS C:\> New-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName -OriginId $originId
```
<span data-ttu-id="c3e05-112">To polecenie cmdlet spowoduje utworzenie nowej grupy źródłowej w określonym punkcie końcowym.</span><span class="sxs-lookup"><span data-stu-id="c3e05-112">This cmdlet will create a new origin group within the specified endpoint.</span></span> <span data-ttu-id="c3e05-113">Będzie ona używać podanych identyfikatorów pochodzenia jako zestawu źródeł.</span><span class="sxs-lookup"><span data-stu-id="c3e05-113">It will utilize the given origin ids as the set of origins.</span></span>

## <span data-ttu-id="c3e05-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c3e05-114">PARAMETERS</span></span>

### <span data-ttu-id="c3e05-115">-CdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="c3e05-115">-CdnOriginGroup</span></span>
<span data-ttu-id="c3e05-116">Obiekt grupy pochodzenie sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="c3e05-116">The CDN origin group object.</span></span>

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

### <span data-ttu-id="c3e05-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3e05-117">-DefaultProfile</span></span>
<span data-ttu-id="c3e05-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c3e05-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3e05-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="c3e05-119">-EndpointName</span></span>
<span data-ttu-id="c3e05-120">Nazwa punktu końcowego usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="c3e05-120">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="c3e05-121">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="c3e05-121">-OriginGroupName</span></span>
<span data-ttu-id="c3e05-122">Nazwa grupy pochodzenia usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="c3e05-122">Azure CDN origin group name.</span></span>

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

### <span data-ttu-id="c3e05-123">-OriginId</span><span class="sxs-lookup"><span data-stu-id="c3e05-123">-OriginId</span></span>
<span data-ttu-id="c3e05-124">Identyfikatory grup pochodzenia usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="c3e05-124">Azure CDN origin group ids.</span></span>

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

### <span data-ttu-id="c3e05-125">-ProbeIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="c3e05-125">-ProbeIntervalInSeconds</span></span>
<span data-ttu-id="c3e05-126">Liczba sekund między badaniami kondycji.</span><span class="sxs-lookup"><span data-stu-id="c3e05-126">The number of seconds between health probes.</span></span>

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

### <span data-ttu-id="c3e05-127">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="c3e05-127">-ProbePath</span></span>
<span data-ttu-id="c3e05-128">Ścieżka odnosząca się do pochodzenia, która jest używana do określania kondycji pochodzenia.</span><span class="sxs-lookup"><span data-stu-id="c3e05-128">The path relative to the origin that is used to determine the health of the origin.</span></span>

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

### <span data-ttu-id="c3e05-129">-ProbeProtocol</span><span class="sxs-lookup"><span data-stu-id="c3e05-129">-ProbeProtocol</span></span>
<span data-ttu-id="c3e05-130">Protokół używany do badania kondycji.</span><span class="sxs-lookup"><span data-stu-id="c3e05-130">Protocol to use for health probe.</span></span>

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

### <span data-ttu-id="c3e05-131">-ProbeRequestType</span><span class="sxs-lookup"><span data-stu-id="c3e05-131">-ProbeRequestType</span></span>
<span data-ttu-id="c3e05-132">Typ żądania badania kondycji, które zostało wykonane.</span><span class="sxs-lookup"><span data-stu-id="c3e05-132">The type of health probe request that is made.</span></span>

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

### <span data-ttu-id="c3e05-133">-Refilename</span><span class="sxs-lookup"><span data-stu-id="c3e05-133">-ProfileName</span></span>
<span data-ttu-id="c3e05-134">Nazwa profilu usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="c3e05-134">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="c3e05-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3e05-135">-ResourceGroupName</span></span>
<span data-ttu-id="c3e05-136">Grupa zasobów profilu usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="c3e05-136">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="c3e05-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c3e05-137">-Confirm</span></span>
<span data-ttu-id="c3e05-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3e05-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3e05-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3e05-139">-WhatIf</span></span>
<span data-ttu-id="c3e05-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3e05-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c3e05-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c3e05-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3e05-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3e05-142">CommonParameters</span></span>
<span data-ttu-id="c3e05-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3e05-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3e05-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c3e05-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3e05-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c3e05-145">INPUTS</span></span>

### <span data-ttu-id="c3e05-146">System. Object</span><span class="sxs-lookup"><span data-stu-id="c3e05-146">System.Object</span></span>

## <span data-ttu-id="c3e05-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c3e05-147">OUTPUTS</span></span>

### <span data-ttu-id="c3e05-148">System. Object</span><span class="sxs-lookup"><span data-stu-id="c3e05-148">System.Object</span></span>

## <span data-ttu-id="c3e05-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c3e05-149">NOTES</span></span>

## <span data-ttu-id="c3e05-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c3e05-150">RELATED LINKS</span></span>
