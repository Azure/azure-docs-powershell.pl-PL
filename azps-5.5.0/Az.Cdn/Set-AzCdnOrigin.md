---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 0EB9F1C9-54CC-4794-9E37-108342341FE5
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOrigin.md
ms.openlocfilehash: 1c3b195f868db5d4e579aa833c4d9ce5a6203c56
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100244227"
---
# <span data-ttu-id="df75e-101">Set-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="df75e-101">Set-AzCdnOrigin</span></span>

## <span data-ttu-id="df75e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df75e-102">SYNOPSIS</span></span>
<span data-ttu-id="df75e-103">Aktualizuje serwer pochodzenia sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="df75e-103">Updates a CDN origin server.</span></span>

## <span data-ttu-id="df75e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="df75e-104">SYNTAX</span></span>

### <span data-ttu-id="df75e-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="df75e-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="df75e-106">ByFieldsPrivateLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="df75e-106">ByFieldsPrivateLinkParameterSet</span></span>
```
Set-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 [-PrivateLinkApprovalMessage <String>] -PrivateLinkLocation <String> -PrivateLinkResourceId <String>
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="df75e-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="df75e-107">ByObjectParameterSet</span></span>
```
Set-AzCdnOrigin -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="df75e-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="df75e-108">DESCRIPTION</span></span>
<span data-ttu-id="df75e-109">Polecenie **cmdlet Set-AzCdnOrigin** aktualizuje serwer pochodzenia usługi Azure Content Delivery Network (CDN).</span><span class="sxs-lookup"><span data-stu-id="df75e-109">The **Set-AzCdnOrigin** cmdlet updates an Azure Content Delivery Network (CDN) origin server.</span></span>

## <span data-ttu-id="df75e-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="df75e-110">EXAMPLES</span></span>

## <span data-ttu-id="df75e-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="df75e-111">PARAMETERS</span></span>

### <span data-ttu-id="df75e-112">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="df75e-112">-CdnOrigin</span></span>
<span data-ttu-id="df75e-113">Określa serwer pochodzenia, który ma być aktualizowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df75e-113">Specifies the origin server that this cmdlet updates.</span></span>

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

### <span data-ttu-id="df75e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df75e-114">-DefaultProfile</span></span>
<span data-ttu-id="df75e-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="df75e-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="df75e-116">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="df75e-116">-EndpointName</span></span>
<span data-ttu-id="df75e-117">Nazwa punktu końcowego sieci Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="df75e-117">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="df75e-118">-HostName</span><span class="sxs-lookup"><span data-stu-id="df75e-118">-HostName</span></span>
<span data-ttu-id="df75e-119">Nazwa hosta pochodzenia sieci Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="df75e-119">Azure CDN origin host name.</span></span>

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

### <span data-ttu-id="df75e-120">- HttpPort</span><span class="sxs-lookup"><span data-stu-id="df75e-120">-HttpPort</span></span>
<span data-ttu-id="df75e-121">Port http pochodzenia sieci Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="df75e-121">Azure CDN origin http port.</span></span>

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

### <span data-ttu-id="df75e-122">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="df75e-122">-HttpsPort</span></span>
<span data-ttu-id="df75e-123">Azure CDN origin https port.</span><span class="sxs-lookup"><span data-stu-id="df75e-123">Azure CDN origin https port.</span></span>

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

### <span data-ttu-id="df75e-124">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="df75e-124">-OriginHostHeader</span></span>
<span data-ttu-id="df75e-125">Nagłówek hosta pochodzenia sieci Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="df75e-125">Azure CDN origin host header.</span></span>

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

### <span data-ttu-id="df75e-126">-OriginName</span><span class="sxs-lookup"><span data-stu-id="df75e-126">-OriginName</span></span>
<span data-ttu-id="df75e-127">Nazwa pochodzenia sieci Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="df75e-127">Azure CDN origin name.</span></span>

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

### <span data-ttu-id="df75e-128">— Priority (Priorytet)</span><span class="sxs-lookup"><span data-stu-id="df75e-128">-Priority</span></span>
<span data-ttu-id="df75e-129">Priorytet pochodzenia sieci Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="df75e-129">Azure CDN origin priority.</span></span>

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

### <span data-ttu-id="df75e-130">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="df75e-130">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="df75e-131">Wiadomość niestandardowa dołączona do żądania zatwierdzenia w celu nawiązania połączenia z linkiem prywatnym.</span><span class="sxs-lookup"><span data-stu-id="df75e-131">A custom message to be included in the approval request to connect to the Private Link.</span></span>

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

### <span data-ttu-id="df75e-132">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="df75e-132">-PrivateLinkLocation</span></span>
<span data-ttu-id="df75e-133">Lokalizacja prywatnego linku pochodzenia sieci Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="df75e-133">Azure CDN origin private link location.</span></span>

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

### <span data-ttu-id="df75e-134">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="df75e-134">-PrivateLinkResourceId</span></span>
<span data-ttu-id="df75e-135">Identyfikator zasobu prywatnego pochodzenia sieci Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="df75e-135">Azure CDN origin private link resource id.</span></span>

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

### <span data-ttu-id="df75e-136">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="df75e-136">-ProfileName</span></span>
<span data-ttu-id="df75e-137">Nazwa profilu azure CDN.</span><span class="sxs-lookup"><span data-stu-id="df75e-137">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="df75e-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df75e-138">-ResourceGroupName</span></span>
<span data-ttu-id="df75e-139">Grupa zasobów profilu azure CDN.</span><span class="sxs-lookup"><span data-stu-id="df75e-139">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="df75e-140">— Waga</span><span class="sxs-lookup"><span data-stu-id="df75e-140">-Weight</span></span>
<span data-ttu-id="df75e-141">Waga pochodzenia sieci Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="df75e-141">Azure CDN origin weight.</span></span>

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

### <span data-ttu-id="df75e-142">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="df75e-142">-Confirm</span></span>
<span data-ttu-id="df75e-143">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="df75e-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df75e-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df75e-144">-WhatIf</span></span>
<span data-ttu-id="df75e-145">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df75e-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="df75e-146">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="df75e-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df75e-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df75e-147">CommonParameters</span></span>
<span data-ttu-id="df75e-148">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df75e-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df75e-149">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="df75e-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df75e-150">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="df75e-150">INPUTS</span></span>

### <span data-ttu-id="df75e-151">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span><span class="sxs-lookup"><span data-stu-id="df75e-151">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="df75e-152">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="df75e-152">OUTPUTS</span></span>

### <span data-ttu-id="df75e-153">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span><span class="sxs-lookup"><span data-stu-id="df75e-153">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="df75e-154">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="df75e-154">NOTES</span></span>

## <span data-ttu-id="df75e-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="df75e-155">RELATED LINKS</span></span>

[<span data-ttu-id="df75e-156">Get-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="df75e-156">Get-AzCdnOrigin</span></span>](./Get-AzCdnOrigin.md)


