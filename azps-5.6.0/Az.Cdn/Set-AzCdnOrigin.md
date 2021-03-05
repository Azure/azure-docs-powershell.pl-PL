---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 0EB9F1C9-54CC-4794-9E37-108342341FE5
online version: https://docs.microsoft.com/powershell/module/az.cdn/set-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOrigin.md
ms.openlocfilehash: 5636aeef0b1c04ffbb0faa7e44161628824e9f1c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013978"
---
# <span data-ttu-id="fd853-101">Set-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="fd853-101">Set-AzCdnOrigin</span></span>

## <span data-ttu-id="fd853-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd853-102">SYNOPSIS</span></span>
<span data-ttu-id="fd853-103">Aktualizuje serwer pochodzenia sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="fd853-103">Updates a CDN origin server.</span></span>

## <span data-ttu-id="fd853-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fd853-104">SYNTAX</span></span>

### <span data-ttu-id="fd853-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="fd853-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fd853-106">ByFieldsPrivateLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd853-106">ByFieldsPrivateLinkParameterSet</span></span>
```
Set-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 [-PrivateLinkApprovalMessage <String>] -PrivateLinkLocation <String> -PrivateLinkResourceId <String>
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fd853-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd853-107">ByObjectParameterSet</span></span>
```
Set-AzCdnOrigin -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fd853-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="fd853-108">DESCRIPTION</span></span>
<span data-ttu-id="fd853-109">Polecenie **cmdlet Set-AzCdnOrigin** aktualizuje serwer pochodzenia usługi Azure Content Delivery Network (CDN).</span><span class="sxs-lookup"><span data-stu-id="fd853-109">The **Set-AzCdnOrigin** cmdlet updates an Azure Content Delivery Network (CDN) origin server.</span></span>

## <span data-ttu-id="fd853-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fd853-110">EXAMPLES</span></span>

## <span data-ttu-id="fd853-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fd853-111">PARAMETERS</span></span>

### <span data-ttu-id="fd853-112">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="fd853-112">-CdnOrigin</span></span>
<span data-ttu-id="fd853-113">Określa serwer pochodzenia, który ma być aktualizowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd853-113">Specifies the origin server that this cmdlet updates.</span></span>

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

### <span data-ttu-id="fd853-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd853-114">-DefaultProfile</span></span>
<span data-ttu-id="fd853-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="fd853-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fd853-116">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="fd853-116">-EndpointName</span></span>
<span data-ttu-id="fd853-117">Nazwa punktu końcowego sieci Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="fd853-117">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="fd853-118">-HostName</span><span class="sxs-lookup"><span data-stu-id="fd853-118">-HostName</span></span>
<span data-ttu-id="fd853-119">Nazwa hosta pochodzenia sieci Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="fd853-119">Azure CDN origin host name.</span></span>

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

### <span data-ttu-id="fd853-120">- HttpPort</span><span class="sxs-lookup"><span data-stu-id="fd853-120">-HttpPort</span></span>
<span data-ttu-id="fd853-121">Port http pochodzenia sieci Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="fd853-121">Azure CDN origin http port.</span></span>

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

### <span data-ttu-id="fd853-122">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="fd853-122">-HttpsPort</span></span>
<span data-ttu-id="fd853-123">Azure CDN origin https port.</span><span class="sxs-lookup"><span data-stu-id="fd853-123">Azure CDN origin https port.</span></span>

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

### <span data-ttu-id="fd853-124">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="fd853-124">-OriginHostHeader</span></span>
<span data-ttu-id="fd853-125">Nagłówek hosta pochodzenia sieci Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="fd853-125">Azure CDN origin host header.</span></span>

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

### <span data-ttu-id="fd853-126">-OriginName</span><span class="sxs-lookup"><span data-stu-id="fd853-126">-OriginName</span></span>
<span data-ttu-id="fd853-127">Nazwa pochodzenia sieci Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="fd853-127">Azure CDN origin name.</span></span>

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

### <span data-ttu-id="fd853-128">— Priority (Priorytet)</span><span class="sxs-lookup"><span data-stu-id="fd853-128">-Priority</span></span>
<span data-ttu-id="fd853-129">Priorytet pochodzenia sieci Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="fd853-129">Azure CDN origin priority.</span></span>

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

### <span data-ttu-id="fd853-130">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="fd853-130">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="fd853-131">Wiadomość niestandardowa dołączona do żądania zatwierdzenia w celu nawiązania połączenia z linkiem prywatnym.</span><span class="sxs-lookup"><span data-stu-id="fd853-131">A custom message to be included in the approval request to connect to the Private Link.</span></span>

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

### <span data-ttu-id="fd853-132">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="fd853-132">-PrivateLinkLocation</span></span>
<span data-ttu-id="fd853-133">Lokalizacja prywatnego linku pochodzenia sieci Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="fd853-133">Azure CDN origin private link location.</span></span>

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

### <span data-ttu-id="fd853-134">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="fd853-134">-PrivateLinkResourceId</span></span>
<span data-ttu-id="fd853-135">Identyfikator zasobu prywatnego pochodzenia sieci Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="fd853-135">Azure CDN origin private link resource id.</span></span>

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

### <span data-ttu-id="fd853-136">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="fd853-136">-ProfileName</span></span>
<span data-ttu-id="fd853-137">Nazwa profilu azure CDN.</span><span class="sxs-lookup"><span data-stu-id="fd853-137">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="fd853-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd853-138">-ResourceGroupName</span></span>
<span data-ttu-id="fd853-139">Grupa zasobów profilu azure CDN.</span><span class="sxs-lookup"><span data-stu-id="fd853-139">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="fd853-140">— Waga</span><span class="sxs-lookup"><span data-stu-id="fd853-140">-Weight</span></span>
<span data-ttu-id="fd853-141">Waga pochodzenia sieci Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="fd853-141">Azure CDN origin weight.</span></span>

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

### <span data-ttu-id="fd853-142">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fd853-142">-Confirm</span></span>
<span data-ttu-id="fd853-143">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="fd853-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd853-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd853-144">-WhatIf</span></span>
<span data-ttu-id="fd853-145">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd853-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fd853-146">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="fd853-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd853-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd853-147">CommonParameters</span></span>
<span data-ttu-id="fd853-148">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd853-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd853-149">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fd853-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd853-150">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fd853-150">INPUTS</span></span>

### <span data-ttu-id="fd853-151">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span><span class="sxs-lookup"><span data-stu-id="fd853-151">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="fd853-152">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fd853-152">OUTPUTS</span></span>

### <span data-ttu-id="fd853-153">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span><span class="sxs-lookup"><span data-stu-id="fd853-153">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="fd853-154">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fd853-154">NOTES</span></span>

## <span data-ttu-id="fd853-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fd853-155">RELATED LINKS</span></span>

[<span data-ttu-id="fd853-156">Get-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="fd853-156">Get-AzCdnOrigin</span></span>](./Get-AzCdnOrigin.md)


