---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzSecurityPartnerProvider.md
ms.openlocfilehash: 5af78bb1f915dec55f75749296340ca6d13a3b3d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223081"
---
# <span data-ttu-id="2ebf1-101">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="2ebf1-101">New-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="2ebf1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2ebf1-102">SYNOPSIS</span></span>
<span data-ttu-id="2ebf1-103">Tworzy usługę Azure SecurityPartnerProvider.</span><span class="sxs-lookup"><span data-stu-id="2ebf1-103">Creates an Azure SecurityPartnerProvider.</span></span>

## <span data-ttu-id="2ebf1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2ebf1-104">SYNTAX</span></span>

```
New-AzSecurityPartnerProvider -Name <String> -ResourceGroupName <String> -Location <String>
 -SecurityProviderName <String> [-VirtualHub <PSVirtualHub>] [-VirtualHubId <String>]
 [-VirtualHubName <String>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ebf1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2ebf1-105">DESCRIPTION</span></span>
<span data-ttu-id="2ebf1-106">Polecenie cmdlet **New-AzSecurityPartnerProvider** tworzy składnik Azure SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="2ebf1-106">The **New-AzSecurityPartnerProvider** cmdlet creates an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="2ebf1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2ebf1-107">EXAMPLES</span></span>

### <span data-ttu-id="2ebf1-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2ebf1-108">Example 1</span></span>
```powershell
 New-AzSecurityPartnerProvider -Name securityPartnerProviderName -ResourceGroupName rgname -Location 'West US' -SecurityProviderName 'ZScaler'
```

## <span data-ttu-id="2ebf1-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2ebf1-109">PARAMETERS</span></span>

### <span data-ttu-id="2ebf1-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2ebf1-110">-AsJob</span></span>
<span data-ttu-id="2ebf1-111">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="2ebf1-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2ebf1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ebf1-112">-DefaultProfile</span></span>
<span data-ttu-id="2ebf1-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2ebf1-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ebf1-114">-Force</span><span class="sxs-lookup"><span data-stu-id="2ebf1-114">-Force</span></span>
<span data-ttu-id="2ebf1-115">Nie pytaj o potwierdzenie zamiaru zastąpienia zasobu</span><span class="sxs-lookup"><span data-stu-id="2ebf1-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="2ebf1-116">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="2ebf1-116">-Location</span></span>
<span data-ttu-id="2ebf1-117">pozycję.</span><span class="sxs-lookup"><span data-stu-id="2ebf1-117">location.</span></span>

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

### <span data-ttu-id="2ebf1-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2ebf1-118">-Name</span></span>
<span data-ttu-id="2ebf1-119">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="2ebf1-119">The resource name.</span></span>

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

### <span data-ttu-id="2ebf1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ebf1-120">-ResourceGroupName</span></span>
<span data-ttu-id="2ebf1-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2ebf1-121">The resource group name.</span></span>

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

### <span data-ttu-id="2ebf1-122">-SecurityProviderName</span><span class="sxs-lookup"><span data-stu-id="2ebf1-122">-SecurityProviderName</span></span>
<span data-ttu-id="2ebf1-123">Nazwa dostawcy zabezpieczeń</span><span class="sxs-lookup"><span data-stu-id="2ebf1-123">The Security Provider name</span></span>

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

### <span data-ttu-id="2ebf1-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="2ebf1-124">-Tag</span></span>
<span data-ttu-id="2ebf1-125">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="2ebf1-125">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="2ebf1-126">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="2ebf1-126">-VirtualHub</span></span>
<span data-ttu-id="2ebf1-127">Identyfikator wirtualnego centrum, do którego jest dołączony dostawca partnera zabezpieczeń</span><span class="sxs-lookup"><span data-stu-id="2ebf1-127">The virtual hub Id that the security partner provider is attached to</span></span>

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

### <span data-ttu-id="2ebf1-128">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="2ebf1-128">-VirtualHubId</span></span>
<span data-ttu-id="2ebf1-129">Identyfikator VirtualHub, do którego należy ten VpnGateway musi być skojarzony.</span><span class="sxs-lookup"><span data-stu-id="2ebf1-129">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="2ebf1-130">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="2ebf1-130">-VirtualHubName</span></span>
<span data-ttu-id="2ebf1-131">Identyfikator VirtualHub, do którego należy ten VpnGateway musi być skojarzony.</span><span class="sxs-lookup"><span data-stu-id="2ebf1-131">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="2ebf1-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2ebf1-132">-Confirm</span></span>
<span data-ttu-id="2ebf1-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ebf1-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ebf1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ebf1-134">-WhatIf</span></span>
<span data-ttu-id="2ebf1-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ebf1-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ebf1-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2ebf1-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ebf1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ebf1-137">CommonParameters</span></span>
<span data-ttu-id="2ebf1-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ebf1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ebf1-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2ebf1-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ebf1-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2ebf1-140">INPUTS</span></span>

### <span data-ttu-id="2ebf1-141">System. String</span><span class="sxs-lookup"><span data-stu-id="2ebf1-141">System.String</span></span>

### <span data-ttu-id="2ebf1-142">Microsoft. Azure. Commands. Network. models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="2ebf1-142">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="2ebf1-143">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2ebf1-143">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2ebf1-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2ebf1-144">OUTPUTS</span></span>

### <span data-ttu-id="2ebf1-145">Microsoft. Azure. Commands. Network. models. PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="2ebf1-145">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="2ebf1-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2ebf1-146">NOTES</span></span>

## <span data-ttu-id="2ebf1-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2ebf1-147">RELATED LINKS</span></span>
