---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzSecurityPartnerProvider.md
ms.openlocfilehash: 5af78bb1f915dec55f75749296340ca6d13a3b3d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179618"
---
# <span data-ttu-id="3b69f-101">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="3b69f-101">New-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="3b69f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b69f-102">SYNOPSIS</span></span>
<span data-ttu-id="3b69f-103">Tworzy narzędzie Azure SecurityPartnerProvider.</span><span class="sxs-lookup"><span data-stu-id="3b69f-103">Creates an Azure SecurityPartnerProvider.</span></span>

## <span data-ttu-id="3b69f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3b69f-104">SYNTAX</span></span>

```
New-AzSecurityPartnerProvider -Name <String> -ResourceGroupName <String> -Location <String>
 -SecurityProviderName <String> [-VirtualHub <PSVirtualHub>] [-VirtualHubId <String>]
 [-VirtualHubName <String>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b69f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="3b69f-105">DESCRIPTION</span></span>
<span data-ttu-id="3b69f-106">Polecenie **cmdlet New-AzSecurityPartnerProvider** tworzy narzędzie Azure SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="3b69f-106">The **New-AzSecurityPartnerProvider** cmdlet creates an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="3b69f-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3b69f-107">EXAMPLES</span></span>

### <span data-ttu-id="3b69f-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3b69f-108">Example 1</span></span>
```powershell
 New-AzSecurityPartnerProvider -Name securityPartnerProviderName -ResourceGroupName rgname -Location 'West US' -SecurityProviderName 'ZScaler'
```

## <span data-ttu-id="3b69f-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3b69f-109">PARAMETERS</span></span>

### <span data-ttu-id="3b69f-110">— AsJob</span><span class="sxs-lookup"><span data-stu-id="3b69f-110">-AsJob</span></span>
<span data-ttu-id="3b69f-111">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="3b69f-111">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b69f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b69f-112">-DefaultProfile</span></span>
<span data-ttu-id="3b69f-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3b69f-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b69f-114">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="3b69f-114">-Force</span></span>
<span data-ttu-id="3b69f-115">Nie pytaj o potwierdzenie, czy chcesz zastąpić zasób</span><span class="sxs-lookup"><span data-stu-id="3b69f-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b69f-116">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="3b69f-116">-Location</span></span>
<span data-ttu-id="3b69f-117">.</span><span class="sxs-lookup"><span data-stu-id="3b69f-117">location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b69f-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="3b69f-118">-Name</span></span>
<span data-ttu-id="3b69f-119">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="3b69f-119">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b69f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b69f-120">-ResourceGroupName</span></span>
<span data-ttu-id="3b69f-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3b69f-121">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b69f-122">-SecurityProviderName</span><span class="sxs-lookup"><span data-stu-id="3b69f-122">-SecurityProviderName</span></span>
<span data-ttu-id="3b69f-123">Nazwa dostawcy zabezpieczeń</span><span class="sxs-lookup"><span data-stu-id="3b69f-123">The Security Provider name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: ZScaler, IBoss, Checkpoint

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b69f-124">— Tag</span><span class="sxs-lookup"><span data-stu-id="3b69f-124">-Tag</span></span>
<span data-ttu-id="3b69f-125">Tabela skrótów reprezentująca tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="3b69f-125">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b69f-126">— VirtualHub</span><span class="sxs-lookup"><span data-stu-id="3b69f-126">-VirtualHub</span></span>
<span data-ttu-id="3b69f-127">Identyfikator centrum wirtualnego, do których jest dołączony dostawca partnerów zabezpieczeń</span><span class="sxs-lookup"><span data-stu-id="3b69f-127">The virtual hub Id that the security partner provider is attached to</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3b69f-128">- VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="3b69f-128">-VirtualHubId</span></span>
<span data-ttu-id="3b69f-129">Z identyfikatorem aplikacji VirtualHub musi być skojarzona ta aplikacja VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="3b69f-129">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b69f-130">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="3b69f-130">-VirtualHubName</span></span>
<span data-ttu-id="3b69f-131">Identyfikator aplikacji VirtualHub, z tą bramą VpnGateway, musi być skojarzony.</span><span class="sxs-lookup"><span data-stu-id="3b69f-131">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b69f-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3b69f-132">-Confirm</span></span>
<span data-ttu-id="3b69f-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3b69f-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b69f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b69f-134">-WhatIf</span></span>
<span data-ttu-id="3b69f-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b69f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b69f-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="3b69f-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b69f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b69f-137">CommonParameters</span></span>
<span data-ttu-id="3b69f-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b69f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b69f-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3b69f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b69f-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3b69f-140">INPUTS</span></span>

### <span data-ttu-id="3b69f-141">System.String</span><span class="sxs-lookup"><span data-stu-id="3b69f-141">System.String</span></span>

### <span data-ttu-id="3b69f-142">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="3b69f-142">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="3b69f-143">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="3b69f-143">System.Collections.Hashtable</span></span>

## <span data-ttu-id="3b69f-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3b69f-144">OUTPUTS</span></span>

### <span data-ttu-id="3b69f-145">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="3b69f-145">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="3b69f-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3b69f-146">NOTES</span></span>

## <span data-ttu-id="3b69f-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3b69f-147">RELATED LINKS</span></span>
