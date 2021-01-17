---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOrigin.md
ms.openlocfilehash: a9ef1687333851e2ac67dfb3f0146509f3b77183
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98353266"
---
# <span data-ttu-id="e16c7-101">New-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="e16c7-101">New-AzCdnOrigin</span></span>

## <span data-ttu-id="e16c7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e16c7-102">SYNOPSIS</span></span>
<span data-ttu-id="e16c7-103">Tworzy nowy początek sieci CDN</span><span class="sxs-lookup"><span data-stu-id="e16c7-103">Creates a new CDN origin</span></span>

## <span data-ttu-id="e16c7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e16c7-104">SYNTAX</span></span>

### <span data-ttu-id="e16c7-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e16c7-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e16c7-106">ByFieldsPrivateLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="e16c7-106">ByFieldsPrivateLinkParameterSet</span></span>
```
New-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 [-PrivateLinkApprovalMessage <String>] -PrivateLinkLocation <String> -PrivateLinkResourceId <String>
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e16c7-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e16c7-107">ByObjectParameterSet</span></span>
```
New-AzCdnOrigin -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e16c7-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e16c7-108">DESCRIPTION</span></span>
<span data-ttu-id="e16c7-109">New-AzCdnOrigin utworzy nową nazwę pochodzenia sieci CDN w określonym punkcie końcowym.</span><span class="sxs-lookup"><span data-stu-id="e16c7-109">The New-AzCdnOrigin will create a new CDN origin within the specified endpoint.</span></span>

## <span data-ttu-id="e16c7-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e16c7-110">EXAMPLES</span></span>

### <span data-ttu-id="e16c7-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e16c7-111">Example 1</span></span>
```powershell
PS C:\> New-AzCdnOrigin -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginName $originName -HostName $hostName
```

<span data-ttu-id="e16c7-112">To polecenie cmdlet utworzy nowy punkt początkowy sieci CDN dla określonego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="e16c7-112">This cmdlet will create a new CDN origin for the specified endpoint.</span></span> <span data-ttu-id="e16c7-113">Zostanie użyta podana nazwa hosta jako źródło.</span><span class="sxs-lookup"><span data-stu-id="e16c7-113">It will use the provided hostname as the origin.</span></span> 

## <span data-ttu-id="e16c7-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e16c7-114">PARAMETERS</span></span>

### <span data-ttu-id="e16c7-115">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="e16c7-115">-CdnOrigin</span></span>
<span data-ttu-id="e16c7-116">Obiekt pochodzenia sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="e16c7-116">The CDN origin object.</span></span>

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

### <span data-ttu-id="e16c7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e16c7-117">-DefaultProfile</span></span>
<span data-ttu-id="e16c7-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e16c7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e16c7-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="e16c7-119">-EndpointName</span></span>
<span data-ttu-id="e16c7-120">Nazwa punktu końcowego usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="e16c7-120">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="e16c7-121">-HostName</span><span class="sxs-lookup"><span data-stu-id="e16c7-121">-HostName</span></span>
<span data-ttu-id="e16c7-122">Nazwa hosta pochodzenia usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="e16c7-122">Azure CDN origin host name.</span></span>

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

### <span data-ttu-id="e16c7-123">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="e16c7-123">-HttpPort</span></span>
<span data-ttu-id="e16c7-124">Port http pochodzenia usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="e16c7-124">Azure CDN origin http port.</span></span>

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

### <span data-ttu-id="e16c7-125">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="e16c7-125">-HttpsPort</span></span>
<span data-ttu-id="e16c7-126">Port https pochodzenia usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="e16c7-126">Azure CDN origin https port.</span></span>

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

### <span data-ttu-id="e16c7-127">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="e16c7-127">-OriginHostHeader</span></span>
<span data-ttu-id="e16c7-128">Nagłówek hosta punktu początkowego usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="e16c7-128">Azure CDN origin host header.</span></span>

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

### <span data-ttu-id="e16c7-129">-Originname</span><span class="sxs-lookup"><span data-stu-id="e16c7-129">-OriginName</span></span>
<span data-ttu-id="e16c7-130">Nazwa pochodzenia usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="e16c7-130">Azure CDN origin name.</span></span>

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

### <span data-ttu-id="e16c7-131">-Priority (priorytet)</span><span class="sxs-lookup"><span data-stu-id="e16c7-131">-Priority</span></span>
<span data-ttu-id="e16c7-132">Priorytet pochodzenia usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="e16c7-132">Azure CDN origin priority.</span></span>

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

### <span data-ttu-id="e16c7-133">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="e16c7-133">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="e16c7-134">Niestandardowa wiadomość, która ma być uwzględniona w żądaniu zatwierdzenia w celu nawiązania połączenia z prywatnym linkiem.</span><span class="sxs-lookup"><span data-stu-id="e16c7-134">A custom message to be included in the approval request to connect to the Private Link.</span></span>

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

### <span data-ttu-id="e16c7-135">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="e16c7-135">-PrivateLinkLocation</span></span>
<span data-ttu-id="e16c7-136">Lokalizacja prywatnego łącza pochodzenia usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="e16c7-136">Azure CDN origin private link location.</span></span>

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

### <span data-ttu-id="e16c7-137">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="e16c7-137">-PrivateLinkResourceId</span></span>
<span data-ttu-id="e16c7-138">Identyfikator zasobu prywatnego łącza pochodzenia usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="e16c7-138">Azure CDN origin private link resource id.</span></span>

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

### <span data-ttu-id="e16c7-139">-Refilename</span><span class="sxs-lookup"><span data-stu-id="e16c7-139">-ProfileName</span></span>
<span data-ttu-id="e16c7-140">Nazwa profilu usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="e16c7-140">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="e16c7-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e16c7-141">-ResourceGroupName</span></span>
<span data-ttu-id="e16c7-142">Grupa zasobów profilu usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="e16c7-142">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="e16c7-143">-Waga</span><span class="sxs-lookup"><span data-stu-id="e16c7-143">-Weight</span></span>
<span data-ttu-id="e16c7-144">Waga pochodzenia usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="e16c7-144">Azure CDN origin weight.</span></span>

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

### <span data-ttu-id="e16c7-145">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e16c7-145">-Confirm</span></span>
<span data-ttu-id="e16c7-146">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e16c7-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e16c7-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e16c7-147">-WhatIf</span></span>
<span data-ttu-id="e16c7-148">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e16c7-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e16c7-149">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e16c7-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e16c7-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e16c7-150">CommonParameters</span></span>
<span data-ttu-id="e16c7-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e16c7-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e16c7-152">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e16c7-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e16c7-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e16c7-153">INPUTS</span></span>

### <span data-ttu-id="e16c7-154">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="e16c7-154">None</span></span>

## <span data-ttu-id="e16c7-155">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e16c7-155">OUTPUTS</span></span>

### <span data-ttu-id="e16c7-156">Microsoft. Azure. Commands. CDN. MODELES. Origin. PSOrigin</span><span class="sxs-lookup"><span data-stu-id="e16c7-156">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="e16c7-157">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e16c7-157">NOTES</span></span>

## <span data-ttu-id="e16c7-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e16c7-158">RELATED LINKS</span></span>
