---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOrigin.md
ms.openlocfilehash: a9ef1687333851e2ac67dfb3f0146509f3b77183
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200819"
---
# <span data-ttu-id="a0b7a-101">New-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="a0b7a-101">New-AzCdnOrigin</span></span>

## <span data-ttu-id="a0b7a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0b7a-102">SYNOPSIS</span></span>
<span data-ttu-id="a0b7a-103">Tworzy nowe pochodzenie sieci CDN</span><span class="sxs-lookup"><span data-stu-id="a0b7a-103">Creates a new CDN origin</span></span>

## <span data-ttu-id="a0b7a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a0b7a-104">SYNTAX</span></span>

### <span data-ttu-id="a0b7a-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="a0b7a-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a0b7a-106">ByFieldsPrivateLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0b7a-106">ByFieldsPrivateLinkParameterSet</span></span>
```
New-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 [-PrivateLinkApprovalMessage <String>] -PrivateLinkLocation <String> -PrivateLinkResourceId <String>
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a0b7a-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0b7a-107">ByObjectParameterSet</span></span>
```
New-AzCdnOrigin -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a0b7a-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="a0b7a-108">DESCRIPTION</span></span>
<span data-ttu-id="a0b7a-109">Ten New-AzCdnOrigin utworzy nowe pochodzenie sieci CDN w określonym punkcie końcowym.</span><span class="sxs-lookup"><span data-stu-id="a0b7a-109">The New-AzCdnOrigin will create a new CDN origin within the specified endpoint.</span></span>

## <span data-ttu-id="a0b7a-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a0b7a-110">EXAMPLES</span></span>

### <span data-ttu-id="a0b7a-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a0b7a-111">Example 1</span></span>
```powershell
PS C:\> New-AzCdnOrigin -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginName $originName -HostName $hostName
```

<span data-ttu-id="a0b7a-112">To polecenie cmdlet utworzy nowe pochodzenie sieci CDN dla określonego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="a0b7a-112">This cmdlet will create a new CDN origin for the specified endpoint.</span></span> <span data-ttu-id="a0b7a-113">Użyje ona podanej nazwy hosta jako pochodzenia.</span><span class="sxs-lookup"><span data-stu-id="a0b7a-113">It will use the provided hostname as the origin.</span></span> 

## <span data-ttu-id="a0b7a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a0b7a-114">PARAMETERS</span></span>

### <span data-ttu-id="a0b7a-115">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="a0b7a-115">-CdnOrigin</span></span>
<span data-ttu-id="a0b7a-116">Obiekt pochodzenia sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="a0b7a-116">The CDN origin object.</span></span>

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

### <span data-ttu-id="a0b7a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0b7a-117">-DefaultProfile</span></span>
<span data-ttu-id="a0b7a-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a0b7a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0b7a-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="a0b7a-119">-EndpointName</span></span>
<span data-ttu-id="a0b7a-120">Nazwa punktu końcowego sieci Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="a0b7a-120">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="a0b7a-121">-HostName</span><span class="sxs-lookup"><span data-stu-id="a0b7a-121">-HostName</span></span>
<span data-ttu-id="a0b7a-122">Nazwa hosta pochodzenia sieci Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="a0b7a-122">Azure CDN origin host name.</span></span>

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

### <span data-ttu-id="a0b7a-123">- HttpPort</span><span class="sxs-lookup"><span data-stu-id="a0b7a-123">-HttpPort</span></span>
<span data-ttu-id="a0b7a-124">Port http pochodzenia sieci Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="a0b7a-124">Azure CDN origin http port.</span></span>

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

### <span data-ttu-id="a0b7a-125">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="a0b7a-125">-HttpsPort</span></span>
<span data-ttu-id="a0b7a-126">Azure CDN origin https port.</span><span class="sxs-lookup"><span data-stu-id="a0b7a-126">Azure CDN origin https port.</span></span>

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

### <span data-ttu-id="a0b7a-127">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="a0b7a-127">-OriginHostHeader</span></span>
<span data-ttu-id="a0b7a-128">Nagłówek hosta pochodzenia sieci Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="a0b7a-128">Azure CDN origin host header.</span></span>

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

### <span data-ttu-id="a0b7a-129">-OriginName</span><span class="sxs-lookup"><span data-stu-id="a0b7a-129">-OriginName</span></span>
<span data-ttu-id="a0b7a-130">Nazwa pochodzenia sieci Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="a0b7a-130">Azure CDN origin name.</span></span>

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

### <span data-ttu-id="a0b7a-131">— Priority (Priorytet)</span><span class="sxs-lookup"><span data-stu-id="a0b7a-131">-Priority</span></span>
<span data-ttu-id="a0b7a-132">Priorytet pochodzenia sieci Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="a0b7a-132">Azure CDN origin priority.</span></span>

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

### <span data-ttu-id="a0b7a-133">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="a0b7a-133">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="a0b7a-134">Wiadomość niestandardowa dołączona do żądania zatwierdzenia w celu nawiązania połączenia z linkiem prywatnym.</span><span class="sxs-lookup"><span data-stu-id="a0b7a-134">A custom message to be included in the approval request to connect to the Private Link.</span></span>

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

### <span data-ttu-id="a0b7a-135">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="a0b7a-135">-PrivateLinkLocation</span></span>
<span data-ttu-id="a0b7a-136">Lokalizacja prywatnego linku pochodzenia sieci Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="a0b7a-136">Azure CDN origin private link location.</span></span>

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

### <span data-ttu-id="a0b7a-137">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="a0b7a-137">-PrivateLinkResourceId</span></span>
<span data-ttu-id="a0b7a-138">Identyfikator zasobu prywatnego pochodzenia sieci Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="a0b7a-138">Azure CDN origin private link resource id.</span></span>

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

### <span data-ttu-id="a0b7a-139">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="a0b7a-139">-ProfileName</span></span>
<span data-ttu-id="a0b7a-140">Nazwa profilu azure CDN.</span><span class="sxs-lookup"><span data-stu-id="a0b7a-140">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="a0b7a-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0b7a-141">-ResourceGroupName</span></span>
<span data-ttu-id="a0b7a-142">Grupa zasobów profilu azure CDN.</span><span class="sxs-lookup"><span data-stu-id="a0b7a-142">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="a0b7a-143">— Waga</span><span class="sxs-lookup"><span data-stu-id="a0b7a-143">-Weight</span></span>
<span data-ttu-id="a0b7a-144">Waga pochodzenia sieci Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="a0b7a-144">Azure CDN origin weight.</span></span>

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

### <span data-ttu-id="a0b7a-145">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a0b7a-145">-Confirm</span></span>
<span data-ttu-id="a0b7a-146">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a0b7a-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0b7a-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0b7a-147">-WhatIf</span></span>
<span data-ttu-id="a0b7a-148">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0b7a-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a0b7a-149">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a0b7a-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0b7a-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0b7a-150">CommonParameters</span></span>
<span data-ttu-id="a0b7a-151">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0b7a-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0b7a-152">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a0b7a-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0b7a-153">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a0b7a-153">INPUTS</span></span>

### <span data-ttu-id="a0b7a-154">Brak</span><span class="sxs-lookup"><span data-stu-id="a0b7a-154">None</span></span>

## <span data-ttu-id="a0b7a-155">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a0b7a-155">OUTPUTS</span></span>

### <span data-ttu-id="a0b7a-156">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span><span class="sxs-lookup"><span data-stu-id="a0b7a-156">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="a0b7a-157">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a0b7a-157">NOTES</span></span>

## <span data-ttu-id="a0b7a-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a0b7a-158">RELATED LINKS</span></span>
