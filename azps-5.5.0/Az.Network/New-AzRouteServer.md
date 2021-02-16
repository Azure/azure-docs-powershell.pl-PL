---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azrouteserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteServer.md
ms.openlocfilehash: 15a613f4d2c695fe42df5b02012187bdeee615b2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179626"
---
# <span data-ttu-id="e395b-101">New-AzRouteServer</span><span class="sxs-lookup"><span data-stu-id="e395b-101">New-AzRouteServer</span></span>

## <span data-ttu-id="e395b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e395b-102">SYNOPSIS</span></span>
<span data-ttu-id="e395b-103">Tworzy serwer usługi Azure RouteServer.</span><span class="sxs-lookup"><span data-stu-id="e395b-103">Creates an Azure RouteServer.</span></span>

## <span data-ttu-id="e395b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e395b-104">SYNTAX</span></span>

```
New-AzRouteServer -ResourceGroupName <String> -RouteServerName <String> -HostedSubnet <String>
 -Location <String> [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e395b-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="e395b-105">DESCRIPTION</span></span>
<span data-ttu-id="e395b-106">Polecenie **cmdlet New-AzRouteServer** tworzy serwer Azure RouteServer</span><span class="sxs-lookup"><span data-stu-id="e395b-106">The **New-AzRouteServer** cmdlet creates an Azure RouteServer</span></span>

## <span data-ttu-id="e395b-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e395b-107">EXAMPLES</span></span>

### <span data-ttu-id="e395b-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e395b-108">Example 1</span></span>
```powershell
PS C:\> $subnet = New-AzVirtualNetworkSubnetConfig -Name $subnetName -AddressPrefix 10.0.0.0/24
$vnet = New-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroupName -Location $resourceGroupLocation -AddressPrefix 10.0.0.0/16 -Subnet $subnet
$subnetId = (Get-AzVirtualNetworkSubnetConfig -Name $subnetName -VirtualNetwork $vnet).Id
New-AzRouteServer -RouteServerName $routeServerName -ResourceGroupName $resourceGroupName -Location $resourceGroupLocation -HostedSubnet $subnetId
```

## <span data-ttu-id="e395b-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e395b-109">PARAMETERS</span></span>

### <span data-ttu-id="e395b-110">— AsJob</span><span class="sxs-lookup"><span data-stu-id="e395b-110">-AsJob</span></span>
<span data-ttu-id="e395b-111">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="e395b-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e395b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e395b-112">-DefaultProfile</span></span>
<span data-ttu-id="e395b-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e395b-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e395b-114">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="e395b-114">-Force</span></span>
<span data-ttu-id="e395b-115">Nie pytaj o potwierdzenie, czy chcesz zastąpić zasób</span><span class="sxs-lookup"><span data-stu-id="e395b-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="e395b-116">-HostedSubnet</span><span class="sxs-lookup"><span data-stu-id="e395b-116">-HostedSubnet</span></span>
<span data-ttu-id="e395b-117">Podsieci, w której jest hostowany serwer trasy.</span><span class="sxs-lookup"><span data-stu-id="e395b-117">The subnet where the route server is hosted.</span></span>

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

### <span data-ttu-id="e395b-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="e395b-118">-Location</span></span>
<span data-ttu-id="e395b-119">Lokalizacja.</span><span class="sxs-lookup"><span data-stu-id="e395b-119">The location.</span></span>

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

### <span data-ttu-id="e395b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e395b-120">-ResourceGroupName</span></span>
<span data-ttu-id="e395b-121">Nazwa grupy zasobów serwera trasy.</span><span class="sxs-lookup"><span data-stu-id="e395b-121">The resource group name of the route server.</span></span>

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

### <span data-ttu-id="e395b-122">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="e395b-122">-RouteServerName</span></span>
<span data-ttu-id="e395b-123">Nazwa serwera trasy.</span><span class="sxs-lookup"><span data-stu-id="e395b-123">The name of the route server.</span></span>

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

### <span data-ttu-id="e395b-124">— Tag</span><span class="sxs-lookup"><span data-stu-id="e395b-124">-Tag</span></span>
<span data-ttu-id="e395b-125">Tabela skrótów reprezentująca tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="e395b-125">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="e395b-126">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e395b-126">-Confirm</span></span>
<span data-ttu-id="e395b-127">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e395b-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e395b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e395b-128">-WhatIf</span></span>
<span data-ttu-id="e395b-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e395b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e395b-130">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e395b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e395b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e395b-131">CommonParameters</span></span>
<span data-ttu-id="e395b-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e395b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e395b-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e395b-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e395b-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e395b-134">INPUTS</span></span>

### <span data-ttu-id="e395b-135">System.String</span><span class="sxs-lookup"><span data-stu-id="e395b-135">System.String</span></span>

### <span data-ttu-id="e395b-136">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="e395b-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e395b-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e395b-137">OUTPUTS</span></span>

### <span data-ttu-id="e395b-138">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span><span class="sxs-lookup"><span data-stu-id="e395b-138">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span></span>

## <span data-ttu-id="e395b-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e395b-139">NOTES</span></span>

## <span data-ttu-id="e395b-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e395b-140">RELATED LINKS</span></span>
