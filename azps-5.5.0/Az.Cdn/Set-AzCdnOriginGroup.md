---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOriginGroup.md
ms.openlocfilehash: 58a9d45c29a9a11b31bff510e6b4e1c63844dd5d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199443"
---
# <span data-ttu-id="23cbd-101">Set-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="23cbd-101">Set-AzCdnOriginGroup</span></span>

## <span data-ttu-id="23cbd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23cbd-102">SYNOPSIS</span></span>
<span data-ttu-id="23cbd-103">Aktualizuje grupę pochodzenia sieci CDN</span><span class="sxs-lookup"><span data-stu-id="23cbd-103">Updates the CDN origin group</span></span>

## <span data-ttu-id="23cbd-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="23cbd-104">SYNTAX</span></span>

### <span data-ttu-id="23cbd-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="23cbd-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzCdnOriginGroup -EndpointName <String> -OriginGroupName <String>
 -OriginId <System.Collections.Generic.List`1[System.String]> [-ProbeIntervalInSeconds <Int32>]
 [-ProbePath <String>] [-ProbeProtocol <String>] [-ProbeRequestType <String>] -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="23cbd-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="23cbd-106">ByObjectParameterSet</span></span>
```
Set-AzCdnOriginGroup -CdnOriginGroup <PSOriginGroup> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23cbd-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="23cbd-107">DESCRIPTION</span></span>
<span data-ttu-id="23cbd-108">Set-AzCdnOriginGroup zaktualizuje określoną grupę pochodzenia w danym punkcie końcowym.</span><span class="sxs-lookup"><span data-stu-id="23cbd-108">Set-AzCdnOriginGroup will update the specified origin group within the given endpoint.</span></span> 

## <span data-ttu-id="23cbd-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="23cbd-109">EXAMPLES</span></span>

### <span data-ttu-id="23cbd-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="23cbd-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName -OriginId $originIds -ProbeIntervalInSeconds $probeInterval 
```
<span data-ttu-id="23cbd-111">To polecenie cmdlet zaktualizuje właściwośćIntervalInSeconds w grupie pochodzenia.</span><span class="sxs-lookup"><span data-stu-id="23cbd-111">This cmdlet will update the ProbeIntervalInSeconds property in the origin group.</span></span> 

## <span data-ttu-id="23cbd-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="23cbd-112">PARAMETERS</span></span>

### <span data-ttu-id="23cbd-113">-CdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="23cbd-113">-CdnOriginGroup</span></span>
<span data-ttu-id="23cbd-114">Obiekt grupy pochodzenia sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="23cbd-114">The CDN origin group object.</span></span>

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

### <span data-ttu-id="23cbd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23cbd-115">-DefaultProfile</span></span>
<span data-ttu-id="23cbd-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="23cbd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23cbd-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="23cbd-117">-EndpointName</span></span>
<span data-ttu-id="23cbd-118">Nazwa punktu końcowego sieci Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="23cbd-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="23cbd-119">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="23cbd-119">-OriginGroupName</span></span>
<span data-ttu-id="23cbd-120">Nazwa grupy pochodzenia sieci Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="23cbd-120">Azure CDN origin group name.</span></span>

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

### <span data-ttu-id="23cbd-121">-OriginId</span><span class="sxs-lookup"><span data-stu-id="23cbd-121">-OriginId</span></span>
<span data-ttu-id="23cbd-122">Identyfikatory grup pochodzenia sieci Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="23cbd-122">Azure CDN origin group ids.</span></span>

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

### <span data-ttu-id="23cbd-123">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="23cbd-123">-ProbeIntervalInSeconds</span></span>
<span data-ttu-id="23cbd-124">Liczba sekund między kondycją.</span><span class="sxs-lookup"><span data-stu-id="23cbd-124">The number of seconds between health probes.</span></span>

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

### <span data-ttu-id="23cbd-125">-Path</span><span class="sxs-lookup"><span data-stu-id="23cbd-125">-ProbePath</span></span>
<span data-ttu-id="23cbd-126">Ścieżka względna względem pochodzenia używanego do określenia kondycji pochodzenia.</span><span class="sxs-lookup"><span data-stu-id="23cbd-126">The path relative to the origin that is used to determine the health of the origin.</span></span>

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

### <span data-ttu-id="23cbd-127">-Wprotocol</span><span class="sxs-lookup"><span data-stu-id="23cbd-127">-ProbeProtocol</span></span>
<span data-ttu-id="23cbd-128">Protokół do użycia na użytek kondycji zdrowotnej.</span><span class="sxs-lookup"><span data-stu-id="23cbd-128">Protocol to use for health probe.</span></span>

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

### <span data-ttu-id="23cbd-129">-SzemraquestType</span><span class="sxs-lookup"><span data-stu-id="23cbd-129">-ProbeRequestType</span></span>
<span data-ttu-id="23cbd-130">Typ żądania kondycji.</span><span class="sxs-lookup"><span data-stu-id="23cbd-130">The type of health probe request that is made.</span></span>

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

### <span data-ttu-id="23cbd-131">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="23cbd-131">-ProfileName</span></span>
<span data-ttu-id="23cbd-132">Nazwa profilu azure CDN.</span><span class="sxs-lookup"><span data-stu-id="23cbd-132">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="23cbd-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23cbd-133">-ResourceGroupName</span></span>
<span data-ttu-id="23cbd-134">Grupa zasobów profilu azure CDN.</span><span class="sxs-lookup"><span data-stu-id="23cbd-134">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="23cbd-135">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="23cbd-135">-Confirm</span></span>
<span data-ttu-id="23cbd-136">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="23cbd-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23cbd-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23cbd-137">-WhatIf</span></span>
<span data-ttu-id="23cbd-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23cbd-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23cbd-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="23cbd-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23cbd-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23cbd-140">CommonParameters</span></span>
<span data-ttu-id="23cbd-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23cbd-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23cbd-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="23cbd-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23cbd-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="23cbd-143">INPUTS</span></span>

### <span data-ttu-id="23cbd-144">System.Object</span><span class="sxs-lookup"><span data-stu-id="23cbd-144">System.Object</span></span>

## <span data-ttu-id="23cbd-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="23cbd-145">OUTPUTS</span></span>

### <span data-ttu-id="23cbd-146">System.Object</span><span class="sxs-lookup"><span data-stu-id="23cbd-146">System.Object</span></span>

## <span data-ttu-id="23cbd-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="23cbd-147">NOTES</span></span>

## <span data-ttu-id="23cbd-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="23cbd-148">RELATED LINKS</span></span>
