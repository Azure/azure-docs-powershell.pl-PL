---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/new-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOrigin.md
ms.openlocfilehash: cc7350fb76091d3bf2f8bdab5c037a5afbe8b57a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983418"
---
# <span data-ttu-id="a0ff6-101">New-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="a0ff6-101">New-AzCdnOrigin</span></span>

## <span data-ttu-id="a0ff6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0ff6-102">SYNOPSIS</span></span>
<span data-ttu-id="a0ff6-103">Tworzy nowe pochodzenie sieci CDN</span><span class="sxs-lookup"><span data-stu-id="a0ff6-103">Creates a new CDN origin</span></span>

## <span data-ttu-id="a0ff6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a0ff6-104">SYNTAX</span></span>

### <span data-ttu-id="a0ff6-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="a0ff6-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a0ff6-106">ByFieldsPrivateLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0ff6-106">ByFieldsPrivateLinkParameterSet</span></span>
```
New-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 [-PrivateLinkApprovalMessage <String>] -PrivateLinkLocation <String> -PrivateLinkResourceId <String>
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a0ff6-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0ff6-107">ByObjectParameterSet</span></span>
```
New-AzCdnOrigin -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a0ff6-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="a0ff6-108">DESCRIPTION</span></span>
<span data-ttu-id="a0ff6-109">Ten New-AzCdnOrigin utworzy nowe pochodzenie sieci CDN w określonym punkcie końcowym.</span><span class="sxs-lookup"><span data-stu-id="a0ff6-109">The New-AzCdnOrigin will create a new CDN origin within the specified endpoint.</span></span>

## <span data-ttu-id="a0ff6-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a0ff6-110">EXAMPLES</span></span>

### <span data-ttu-id="a0ff6-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a0ff6-111">Example 1</span></span>
```powershell
PS C:\> New-AzCdnOrigin -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginName $originName -HostName $hostName
```

<span data-ttu-id="a0ff6-112">To polecenie cmdlet utworzy nowe pochodzenie sieci CDN dla określonego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="a0ff6-112">This cmdlet will create a new CDN origin for the specified endpoint.</span></span> <span data-ttu-id="a0ff6-113">Użyje ona podanej nazwy hosta jako pochodzenia.</span><span class="sxs-lookup"><span data-stu-id="a0ff6-113">It will use the provided hostname as the origin.</span></span> 

## <span data-ttu-id="a0ff6-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a0ff6-114">PARAMETERS</span></span>

### <span data-ttu-id="a0ff6-115">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="a0ff6-115">-CdnOrigin</span></span>
<span data-ttu-id="a0ff6-116">Obiekt pochodzenia sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="a0ff6-116">The CDN origin object.</span></span>

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

### <span data-ttu-id="a0ff6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0ff6-117">-DefaultProfile</span></span>
<span data-ttu-id="a0ff6-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a0ff6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0ff6-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="a0ff6-119">-EndpointName</span></span>
<span data-ttu-id="a0ff6-120">Nazwa punktu końcowego sieci Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="a0ff6-120">Azure CDN endpoint name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0ff6-121">-HostName</span><span class="sxs-lookup"><span data-stu-id="a0ff6-121">-HostName</span></span>
<span data-ttu-id="a0ff6-122">Nazwa hosta pochodzenia sieci Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="a0ff6-122">Azure CDN origin host name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0ff6-123">- HttpPort</span><span class="sxs-lookup"><span data-stu-id="a0ff6-123">-HttpPort</span></span>
<span data-ttu-id="a0ff6-124">Port http pochodzenia sieci Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="a0ff6-124">Azure CDN origin http port.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0ff6-125">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="a0ff6-125">-HttpsPort</span></span>
<span data-ttu-id="a0ff6-126">Azure CDN origin https port.</span><span class="sxs-lookup"><span data-stu-id="a0ff6-126">Azure CDN origin https port.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0ff6-127">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="a0ff6-127">-OriginHostHeader</span></span>
<span data-ttu-id="a0ff6-128">Nagłówek hosta pochodzenia sieci Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="a0ff6-128">Azure CDN origin host header.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0ff6-129">-OriginName</span><span class="sxs-lookup"><span data-stu-id="a0ff6-129">-OriginName</span></span>
<span data-ttu-id="a0ff6-130">Nazwa pochodzenia sieci Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="a0ff6-130">Azure CDN origin name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0ff6-131">— Priority (Priorytet)</span><span class="sxs-lookup"><span data-stu-id="a0ff6-131">-Priority</span></span>
<span data-ttu-id="a0ff6-132">Priorytet pochodzenia sieci Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="a0ff6-132">Azure CDN origin priority.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0ff6-133">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="a0ff6-133">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="a0ff6-134">Wiadomość niestandardowa dołączona do żądania zatwierdzenia w celu nawiązania połączenia z linkiem prywatnym.</span><span class="sxs-lookup"><span data-stu-id="a0ff6-134">A custom message to be included in the approval request to connect to the Private Link.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsPrivateLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0ff6-135">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="a0ff6-135">-PrivateLinkLocation</span></span>
<span data-ttu-id="a0ff6-136">Lokalizacja prywatnego linku pochodzenia sieci Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="a0ff6-136">Azure CDN origin private link location.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0ff6-137">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="a0ff6-137">-PrivateLinkResourceId</span></span>
<span data-ttu-id="a0ff6-138">Identyfikator zasobu prywatnego pochodzenia sieci Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="a0ff6-138">Azure CDN origin private link resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0ff6-139">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="a0ff6-139">-ProfileName</span></span>
<span data-ttu-id="a0ff6-140">Nazwa profilu azure CDN.</span><span class="sxs-lookup"><span data-stu-id="a0ff6-140">Azure CDN profile name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0ff6-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0ff6-141">-ResourceGroupName</span></span>
<span data-ttu-id="a0ff6-142">Grupa zasobów profilu azure CDN.</span><span class="sxs-lookup"><span data-stu-id="a0ff6-142">The resource group of the Azure CDN profile.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0ff6-143">— Waga</span><span class="sxs-lookup"><span data-stu-id="a0ff6-143">-Weight</span></span>
<span data-ttu-id="a0ff6-144">Waga pochodzenia sieci Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="a0ff6-144">Azure CDN origin weight.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0ff6-145">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a0ff6-145">-Confirm</span></span>
<span data-ttu-id="a0ff6-146">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a0ff6-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0ff6-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0ff6-147">-WhatIf</span></span>
<span data-ttu-id="a0ff6-148">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0ff6-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a0ff6-149">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a0ff6-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0ff6-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0ff6-150">CommonParameters</span></span>
<span data-ttu-id="a0ff6-151">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0ff6-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0ff6-152">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a0ff6-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0ff6-153">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a0ff6-153">INPUTS</span></span>

### <span data-ttu-id="a0ff6-154">Brak</span><span class="sxs-lookup"><span data-stu-id="a0ff6-154">None</span></span>

## <span data-ttu-id="a0ff6-155">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a0ff6-155">OUTPUTS</span></span>

### <span data-ttu-id="a0ff6-156">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span><span class="sxs-lookup"><span data-stu-id="a0ff6-156">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="a0ff6-157">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a0ff6-157">NOTES</span></span>

## <span data-ttu-id="a0ff6-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a0ff6-158">RELATED LINKS</span></span>
