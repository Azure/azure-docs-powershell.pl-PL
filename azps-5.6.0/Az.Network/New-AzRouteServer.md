---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azrouteserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteServer.md
ms.openlocfilehash: 24e53b7f7bfd0f09e93184b2862deed4608af544
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958193"
---
# <span data-ttu-id="7738e-101">New-AzRouteServer</span><span class="sxs-lookup"><span data-stu-id="7738e-101">New-AzRouteServer</span></span>

## <span data-ttu-id="7738e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7738e-102">SYNOPSIS</span></span>
<span data-ttu-id="7738e-103">Tworzy serwer azure routeserver.</span><span class="sxs-lookup"><span data-stu-id="7738e-103">Creates an Azure RouteServer.</span></span>

## <span data-ttu-id="7738e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7738e-104">SYNTAX</span></span>

```
New-AzRouteServer -ResourceGroupName <String> -RouteServerName <String> -HostedSubnet <String>
 -Location <String> [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7738e-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="7738e-105">DESCRIPTION</span></span>
<span data-ttu-id="7738e-106">Polecenie **cmdlet New-AzRouteServer** tworzy serwer Azure RouteServer</span><span class="sxs-lookup"><span data-stu-id="7738e-106">The **New-AzRouteServer** cmdlet creates an Azure RouteServer</span></span>

## <span data-ttu-id="7738e-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7738e-107">EXAMPLES</span></span>

### <span data-ttu-id="7738e-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7738e-108">Example 1</span></span>
```powershell
PS C:\> $subnet = New-AzVirtualNetworkSubnetConfig -Name $subnetName -AddressPrefix 10.0.0.0/24
$vnet = New-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroupName -Location $resourceGroupLocation -AddressPrefix 10.0.0.0/16 -Subnet $subnet
$subnetId = (Get-AzVirtualNetworkSubnetConfig -Name $subnetName -VirtualNetwork $vnet).Id
New-AzRouteServer -RouteServerName $routeServerName -ResourceGroupName $resourceGroupName -Location $resourceGroupLocation -HostedSubnet $subnetId
```

## <span data-ttu-id="7738e-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7738e-109">PARAMETERS</span></span>

### <span data-ttu-id="7738e-110">— AsJob</span><span class="sxs-lookup"><span data-stu-id="7738e-110">-AsJob</span></span>
<span data-ttu-id="7738e-111">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="7738e-111">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7738e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7738e-112">-DefaultProfile</span></span>
<span data-ttu-id="7738e-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7738e-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7738e-114">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="7738e-114">-Force</span></span>
<span data-ttu-id="7738e-115">Nie pytaj o potwierdzenie, jeśli chcesz zastąpić zasób</span><span class="sxs-lookup"><span data-stu-id="7738e-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7738e-116">-HostedSubnet</span><span class="sxs-lookup"><span data-stu-id="7738e-116">-HostedSubnet</span></span>
<span data-ttu-id="7738e-117">Podsieci, w której jest hostowany serwer trasy.</span><span class="sxs-lookup"><span data-stu-id="7738e-117">The subnet where the route server is hosted.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7738e-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="7738e-118">-Location</span></span>
<span data-ttu-id="7738e-119">Lokalizacja.</span><span class="sxs-lookup"><span data-stu-id="7738e-119">The location.</span></span>

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

### <span data-ttu-id="7738e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7738e-120">-ResourceGroupName</span></span>
<span data-ttu-id="7738e-121">Nazwa grupy zasobów serwera trasy.</span><span class="sxs-lookup"><span data-stu-id="7738e-121">The resource group name of the route server.</span></span>

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

### <span data-ttu-id="7738e-122">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="7738e-122">-RouteServerName</span></span>
<span data-ttu-id="7738e-123">Nazwa serwera trasy.</span><span class="sxs-lookup"><span data-stu-id="7738e-123">The name of the route server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7738e-124">— Tag</span><span class="sxs-lookup"><span data-stu-id="7738e-124">-Tag</span></span>
<span data-ttu-id="7738e-125">Tabela skrótów reprezentująca tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="7738e-125">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7738e-126">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7738e-126">-Confirm</span></span>
<span data-ttu-id="7738e-127">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7738e-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7738e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7738e-128">-WhatIf</span></span>
<span data-ttu-id="7738e-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7738e-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7738e-130">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="7738e-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7738e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7738e-131">CommonParameters</span></span>
<span data-ttu-id="7738e-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7738e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7738e-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7738e-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7738e-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7738e-134">INPUTS</span></span>

### <span data-ttu-id="7738e-135">System.String</span><span class="sxs-lookup"><span data-stu-id="7738e-135">System.String</span></span>

### <span data-ttu-id="7738e-136">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="7738e-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="7738e-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7738e-137">OUTPUTS</span></span>

### <span data-ttu-id="7738e-138">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span><span class="sxs-lookup"><span data-stu-id="7738e-138">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span></span>

## <span data-ttu-id="7738e-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7738e-139">NOTES</span></span>

## <span data-ttu-id="7738e-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7738e-140">RELATED LINKS</span></span>
