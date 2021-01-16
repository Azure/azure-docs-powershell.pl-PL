---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 0EB9F1C9-54CC-4794-9E37-108342341FE5
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOrigin.md
ms.openlocfilehash: 1c3b195f868db5d4e579aa833c4d9ce5a6203c56
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366121"
---
# <span data-ttu-id="fc693-101">Set-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="fc693-101">Set-AzCdnOrigin</span></span>

## <span data-ttu-id="fc693-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fc693-102">SYNOPSIS</span></span>
<span data-ttu-id="fc693-103">Aktualizuje serwer pochodzenia sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="fc693-103">Updates a CDN origin server.</span></span>

## <span data-ttu-id="fc693-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fc693-104">SYNTAX</span></span>

### <span data-ttu-id="fc693-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="fc693-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fc693-106">ByFieldsPrivateLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc693-106">ByFieldsPrivateLinkParameterSet</span></span>
```
Set-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 [-PrivateLinkApprovalMessage <String>] -PrivateLinkLocation <String> -PrivateLinkResourceId <String>
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fc693-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc693-107">ByObjectParameterSet</span></span>
```
Set-AzCdnOrigin -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fc693-108">Opis</span><span class="sxs-lookup"><span data-stu-id="fc693-108">DESCRIPTION</span></span>
<span data-ttu-id="fc693-109">Polecenie cmdlet **Set-AzCdnOrigin** aktualizuje serwer pochodzenia sieci dostarczania zawartości platformy Azure (CDN).</span><span class="sxs-lookup"><span data-stu-id="fc693-109">The **Set-AzCdnOrigin** cmdlet updates an Azure Content Delivery Network (CDN) origin server.</span></span>

## <span data-ttu-id="fc693-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fc693-110">EXAMPLES</span></span>

## <span data-ttu-id="fc693-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fc693-111">PARAMETERS</span></span>

### <span data-ttu-id="fc693-112">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="fc693-112">-CdnOrigin</span></span>
<span data-ttu-id="fc693-113">Określa serwer pochodzenia, który jest aktualizowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc693-113">Specifies the origin server that this cmdlet updates.</span></span>

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

### <span data-ttu-id="fc693-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc693-114">-DefaultProfile</span></span>
<span data-ttu-id="fc693-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="fc693-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fc693-116">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="fc693-116">-EndpointName</span></span>
<span data-ttu-id="fc693-117">Nazwa punktu końcowego usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="fc693-117">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="fc693-118">-HostName</span><span class="sxs-lookup"><span data-stu-id="fc693-118">-HostName</span></span>
<span data-ttu-id="fc693-119">Nazwa hosta pochodzenia usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="fc693-119">Azure CDN origin host name.</span></span>

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

### <span data-ttu-id="fc693-120">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="fc693-120">-HttpPort</span></span>
<span data-ttu-id="fc693-121">Port http pochodzenia usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="fc693-121">Azure CDN origin http port.</span></span>

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

### <span data-ttu-id="fc693-122">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="fc693-122">-HttpsPort</span></span>
<span data-ttu-id="fc693-123">Port https pochodzenia usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="fc693-123">Azure CDN origin https port.</span></span>

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

### <span data-ttu-id="fc693-124">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="fc693-124">-OriginHostHeader</span></span>
<span data-ttu-id="fc693-125">Nagłówek hosta punktu początkowego usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="fc693-125">Azure CDN origin host header.</span></span>

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

### <span data-ttu-id="fc693-126">-Originname</span><span class="sxs-lookup"><span data-stu-id="fc693-126">-OriginName</span></span>
<span data-ttu-id="fc693-127">Nazwa pochodzenia usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="fc693-127">Azure CDN origin name.</span></span>

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

### <span data-ttu-id="fc693-128">-Priority (priorytet)</span><span class="sxs-lookup"><span data-stu-id="fc693-128">-Priority</span></span>
<span data-ttu-id="fc693-129">Priorytet pochodzenia usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="fc693-129">Azure CDN origin priority.</span></span>

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

### <span data-ttu-id="fc693-130">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="fc693-130">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="fc693-131">Niestandardowa wiadomość, która ma być uwzględniona w żądaniu zatwierdzenia w celu nawiązania połączenia z prywatnym linkiem.</span><span class="sxs-lookup"><span data-stu-id="fc693-131">A custom message to be included in the approval request to connect to the Private Link.</span></span>

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

### <span data-ttu-id="fc693-132">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="fc693-132">-PrivateLinkLocation</span></span>
<span data-ttu-id="fc693-133">Lokalizacja prywatnego łącza pochodzenia usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="fc693-133">Azure CDN origin private link location.</span></span>

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

### <span data-ttu-id="fc693-134">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="fc693-134">-PrivateLinkResourceId</span></span>
<span data-ttu-id="fc693-135">Identyfikator zasobu prywatnego łącza pochodzenia usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="fc693-135">Azure CDN origin private link resource id.</span></span>

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

### <span data-ttu-id="fc693-136">-Refilename</span><span class="sxs-lookup"><span data-stu-id="fc693-136">-ProfileName</span></span>
<span data-ttu-id="fc693-137">Nazwa profilu usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="fc693-137">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="fc693-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc693-138">-ResourceGroupName</span></span>
<span data-ttu-id="fc693-139">Grupa zasobów profilu usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="fc693-139">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="fc693-140">-Waga</span><span class="sxs-lookup"><span data-stu-id="fc693-140">-Weight</span></span>
<span data-ttu-id="fc693-141">Waga pochodzenia usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="fc693-141">Azure CDN origin weight.</span></span>

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

### <span data-ttu-id="fc693-142">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fc693-142">-Confirm</span></span>
<span data-ttu-id="fc693-143">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc693-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc693-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc693-144">-WhatIf</span></span>
<span data-ttu-id="fc693-145">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc693-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fc693-146">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fc693-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc693-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc693-147">CommonParameters</span></span>
<span data-ttu-id="fc693-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc693-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc693-149">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fc693-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc693-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fc693-150">INPUTS</span></span>

### <span data-ttu-id="fc693-151">Microsoft. Azure. Commands. CDN. MODELES. Origin. PSOrigin</span><span class="sxs-lookup"><span data-stu-id="fc693-151">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="fc693-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fc693-152">OUTPUTS</span></span>

### <span data-ttu-id="fc693-153">Microsoft. Azure. Commands. CDN. MODELES. Origin. PSOrigin</span><span class="sxs-lookup"><span data-stu-id="fc693-153">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="fc693-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fc693-154">NOTES</span></span>

## <span data-ttu-id="fc693-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fc693-155">RELATED LINKS</span></span>

[<span data-ttu-id="fc693-156">Get-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="fc693-156">Get-AzCdnOrigin</span></span>](./Get-AzCdnOrigin.md)


