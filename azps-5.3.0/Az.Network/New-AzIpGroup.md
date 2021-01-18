---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpGroup.md
ms.openlocfilehash: 6ae61090f98cbb9929cc5ad1b2745fbf88f21a2a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501267"
---
# <span data-ttu-id="4298a-101">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="4298a-101">New-AzIpGroup</span></span>

## <span data-ttu-id="4298a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4298a-102">SYNOPSIS</span></span>
<span data-ttu-id="4298a-103">Tworzy usługę Azure IpGroup.</span><span class="sxs-lookup"><span data-stu-id="4298a-103">Creates an Azure IpGroup.</span></span>

## <span data-ttu-id="4298a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4298a-104">SYNTAX</span></span>

```
New-AzIpGroup -Name <String> -ResourceGroupName <String> [-IpAddress <String[]>] -Location <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4298a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4298a-105">DESCRIPTION</span></span>
<span data-ttu-id="4298a-106">Polecenie cmdlet **New-AzIpGroup** tworzy składnik Azure IpGroup</span><span class="sxs-lookup"><span data-stu-id="4298a-106">The **New-AzIpGroup** cmdlet creates an Azure IpGroup</span></span>

## <span data-ttu-id="4298a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4298a-107">EXAMPLES</span></span>

### <span data-ttu-id="4298a-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4298a-108">Example 1</span></span>
```powershell
New-AzIpGroup -Name ipGroup -ResourceGroupName ipGroupRG -Location 'West US'
```

### <span data-ttu-id="4298a-109">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="4298a-109">Example 2</span></span>
```powershell
New-AzIpGroup -Name ipGroup -ResourceGroupName ipGroupRG -Location 'West US' -IpAddress 10.0.0.0/24,11.9.0.0/24
```

## <span data-ttu-id="4298a-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4298a-110">PARAMETERS</span></span>

### <span data-ttu-id="4298a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4298a-111">-AsJob</span></span>
<span data-ttu-id="4298a-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="4298a-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4298a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4298a-113">-DefaultProfile</span></span>
<span data-ttu-id="4298a-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4298a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4298a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="4298a-115">-Force</span></span>
<span data-ttu-id="4298a-116">Nie pytaj o potwierdzenie zamiaru zastąpienia zasobu</span><span class="sxs-lookup"><span data-stu-id="4298a-116">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="4298a-117">-Adres_IP</span><span class="sxs-lookup"><span data-stu-id="4298a-117">-IpAddress</span></span>
<span data-ttu-id="4298a-118">Adresy IP zdefiniowane w IpGroup</span><span class="sxs-lookup"><span data-stu-id="4298a-118">IpAddresses defined in the IpGroup</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4298a-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="4298a-119">-Location</span></span>
<span data-ttu-id="4298a-120">Lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="4298a-120">The location.</span></span>

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

### <span data-ttu-id="4298a-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4298a-121">-Name</span></span>
<span data-ttu-id="4298a-122">Nazwa ipgroup.</span><span class="sxs-lookup"><span data-stu-id="4298a-122">The name of the ipgroup.</span></span>

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

### <span data-ttu-id="4298a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4298a-123">-ResourceGroupName</span></span>
<span data-ttu-id="4298a-124">Nazwa grupy zasobów ipgroup.</span><span class="sxs-lookup"><span data-stu-id="4298a-124">The resource group name of the ipgroup.</span></span>

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

### <span data-ttu-id="4298a-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="4298a-125">-Tag</span></span>
<span data-ttu-id="4298a-126">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="4298a-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="4298a-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4298a-127">-Confirm</span></span>
<span data-ttu-id="4298a-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4298a-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4298a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4298a-129">-WhatIf</span></span>
<span data-ttu-id="4298a-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4298a-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4298a-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4298a-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4298a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4298a-132">CommonParameters</span></span>
<span data-ttu-id="4298a-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4298a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4298a-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4298a-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4298a-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4298a-135">INPUTS</span></span>

### <span data-ttu-id="4298a-136">System. String</span><span class="sxs-lookup"><span data-stu-id="4298a-136">System.String</span></span>

### <span data-ttu-id="4298a-137">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="4298a-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="4298a-138">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="4298a-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4298a-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4298a-139">OUTPUTS</span></span>

### <span data-ttu-id="4298a-140">Microsoft. Azure. Commands. Network. models. PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="4298a-140">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="4298a-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4298a-141">NOTES</span></span>

## <span data-ttu-id="4298a-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4298a-142">RELATED LINKS</span></span>
