---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOriginGroup.md
ms.openlocfilehash: 58a9d45c29a9a11b31bff510e6b4e1c63844dd5d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349033"
---
# <span data-ttu-id="c9df1-101">Set-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="c9df1-101">Set-AzCdnOriginGroup</span></span>

## <span data-ttu-id="c9df1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c9df1-102">SYNOPSIS</span></span>
<span data-ttu-id="c9df1-103">Aktualizuje grupę źródeł sieci CDN</span><span class="sxs-lookup"><span data-stu-id="c9df1-103">Updates the CDN origin group</span></span>

## <span data-ttu-id="c9df1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c9df1-104">SYNTAX</span></span>

### <span data-ttu-id="c9df1-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c9df1-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzCdnOriginGroup -EndpointName <String> -OriginGroupName <String>
 -OriginId <System.Collections.Generic.List`1[System.String]> [-ProbeIntervalInSeconds <Int32>]
 [-ProbePath <String>] [-ProbeProtocol <String>] [-ProbeRequestType <String>] -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c9df1-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9df1-106">ByObjectParameterSet</span></span>
```
Set-AzCdnOriginGroup -CdnOriginGroup <PSOriginGroup> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9df1-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c9df1-107">DESCRIPTION</span></span>
<span data-ttu-id="c9df1-108">Set-AzCdnOriginGroup zaktualizuje określoną grupę pochodzenia w danym punkcie końcowym.</span><span class="sxs-lookup"><span data-stu-id="c9df1-108">Set-AzCdnOriginGroup will update the specified origin group within the given endpoint.</span></span> 

## <span data-ttu-id="c9df1-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c9df1-109">EXAMPLES</span></span>

### <span data-ttu-id="c9df1-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c9df1-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName -OriginId $originIds -ProbeIntervalInSeconds $probeInterval 
```
<span data-ttu-id="c9df1-111">To polecenie cmdlet spowoduje zaktualizowanie właściwości ProbeIntervalInSeconds w grupie pochodzenie.</span><span class="sxs-lookup"><span data-stu-id="c9df1-111">This cmdlet will update the ProbeIntervalInSeconds property in the origin group.</span></span> 

## <span data-ttu-id="c9df1-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c9df1-112">PARAMETERS</span></span>

### <span data-ttu-id="c9df1-113">-CdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="c9df1-113">-CdnOriginGroup</span></span>
<span data-ttu-id="c9df1-114">Obiekt grupy pochodzenie sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="c9df1-114">The CDN origin group object.</span></span>

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

### <span data-ttu-id="c9df1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9df1-115">-DefaultProfile</span></span>
<span data-ttu-id="c9df1-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c9df1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9df1-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="c9df1-117">-EndpointName</span></span>
<span data-ttu-id="c9df1-118">Nazwa punktu końcowego usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="c9df1-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="c9df1-119">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="c9df1-119">-OriginGroupName</span></span>
<span data-ttu-id="c9df1-120">Nazwa grupy pochodzenia usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="c9df1-120">Azure CDN origin group name.</span></span>

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

### <span data-ttu-id="c9df1-121">-OriginId</span><span class="sxs-lookup"><span data-stu-id="c9df1-121">-OriginId</span></span>
<span data-ttu-id="c9df1-122">Identyfikatory grup pochodzenia usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="c9df1-122">Azure CDN origin group ids.</span></span>

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

### <span data-ttu-id="c9df1-123">-ProbeIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="c9df1-123">-ProbeIntervalInSeconds</span></span>
<span data-ttu-id="c9df1-124">Liczba sekund między badaniami kondycji.</span><span class="sxs-lookup"><span data-stu-id="c9df1-124">The number of seconds between health probes.</span></span>

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

### <span data-ttu-id="c9df1-125">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="c9df1-125">-ProbePath</span></span>
<span data-ttu-id="c9df1-126">Ścieżka odnosząca się do pochodzenia, która jest używana do określania kondycji pochodzenia.</span><span class="sxs-lookup"><span data-stu-id="c9df1-126">The path relative to the origin that is used to determine the health of the origin.</span></span>

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

### <span data-ttu-id="c9df1-127">-ProbeProtocol</span><span class="sxs-lookup"><span data-stu-id="c9df1-127">-ProbeProtocol</span></span>
<span data-ttu-id="c9df1-128">Protokół używany do badania kondycji.</span><span class="sxs-lookup"><span data-stu-id="c9df1-128">Protocol to use for health probe.</span></span>

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

### <span data-ttu-id="c9df1-129">-ProbeRequestType</span><span class="sxs-lookup"><span data-stu-id="c9df1-129">-ProbeRequestType</span></span>
<span data-ttu-id="c9df1-130">Typ żądania badania kondycji, które zostało wykonane.</span><span class="sxs-lookup"><span data-stu-id="c9df1-130">The type of health probe request that is made.</span></span>

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

### <span data-ttu-id="c9df1-131">-Refilename</span><span class="sxs-lookup"><span data-stu-id="c9df1-131">-ProfileName</span></span>
<span data-ttu-id="c9df1-132">Nazwa profilu usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="c9df1-132">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="c9df1-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9df1-133">-ResourceGroupName</span></span>
<span data-ttu-id="c9df1-134">Grupa zasobów profilu usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="c9df1-134">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="c9df1-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c9df1-135">-Confirm</span></span>
<span data-ttu-id="c9df1-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9df1-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9df1-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9df1-137">-WhatIf</span></span>
<span data-ttu-id="c9df1-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9df1-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9df1-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c9df1-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9df1-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9df1-140">CommonParameters</span></span>
<span data-ttu-id="c9df1-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9df1-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9df1-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c9df1-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9df1-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c9df1-143">INPUTS</span></span>

### <span data-ttu-id="c9df1-144">System. Object</span><span class="sxs-lookup"><span data-stu-id="c9df1-144">System.Object</span></span>

## <span data-ttu-id="c9df1-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c9df1-145">OUTPUTS</span></span>

### <span data-ttu-id="c9df1-146">System. Object</span><span class="sxs-lookup"><span data-stu-id="c9df1-146">System.Object</span></span>

## <span data-ttu-id="c9df1-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c9df1-147">NOTES</span></span>

## <span data-ttu-id="c9df1-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c9df1-148">RELATED LINKS</span></span>
