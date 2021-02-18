---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePort.md
ms.openlocfilehash: 54cdcbbd1d9564dde4fbe4a9aa0b0bea8a0325a3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240834"
---
# <span data-ttu-id="3ed57-101">New-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="3ed57-101">New-AzExpressRoutePort</span></span>

## <span data-ttu-id="3ed57-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ed57-102">SYNOPSIS</span></span>
<span data-ttu-id="3ed57-103">Tworzy usługę Azure ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="3ed57-103">Creates an Azure ExpressRoutePort.</span></span>

## <span data-ttu-id="3ed57-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3ed57-104">SYNTAX</span></span>

### <span data-ttu-id="3ed57-105">ResourceNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="3ed57-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzExpressRoutePort -ResourceGroupName <String> -Name <String> -PeeringLocation <String>
 -BandwidthInGbps <Int32> -Encapsulation <String> -Location <String> [-Tag <Hashtable>]
 [-Link <PSExpressRouteLink[]>] [-Force] [-AsJob] [-Identity <PSManagedServiceIdentity>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ed57-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ed57-106">ResourceIdParameterSet</span></span>
```
New-AzExpressRoutePort -ResourceId <String> -PeeringLocation <String> -BandwidthInGbps <Int32>
 -Encapsulation <String> -Location <String> [-Tag <Hashtable>] [-Link <PSExpressRouteLink[]>] [-Force] [-AsJob]
 [-Identity <PSManagedServiceIdentity>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3ed57-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="3ed57-107">DESCRIPTION</span></span>
<span data-ttu-id="3ed57-108">Polecenie **cmdlet New-AzExpressRoutePort** tworzy raport usługi Azure ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="3ed57-108">The **New-AzExpressRoutePort** cmdlet creates an Azure ExpressRoutePort</span></span>

## <span data-ttu-id="3ed57-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3ed57-109">EXAMPLES</span></span>

### <span data-ttu-id="3ed57-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3ed57-110">Example 1</span></span>
```powershell
PS C:\> $parameters = @{
    Name='ExpressRoutePort'
    ResourceGroupName='ExpressRouteResourceGroup'
    Location='West US'
    PeeringLocation='Silicon Valley'
    BandwidthInGbps=100
    Encapsulation='QinQ'
}
PS C:\> New-AzExpressRoutePort @parameters
```

### <span data-ttu-id="3ed57-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="3ed57-111">Example 2</span></span>
```powershell
PS C:\> $parameters = @{
    ResourceId='/subscriptions/<SubId>/resourceGroups/<ResourceGroupName>/providers/Microsoft.Network/expressRoutePorts/<PortName>'
    Location='West US'
    PeeringLocation='Silicon Valley'
    BandwidthInGbps=100
    Encapsulation='QinQ'
}
PS C:\> New-AzExpressRoutePort @parameters
```

## <span data-ttu-id="3ed57-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3ed57-112">PARAMETERS</span></span>

### <span data-ttu-id="3ed57-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="3ed57-113">-AsJob</span></span>
<span data-ttu-id="3ed57-114">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="3ed57-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3ed57-115">- BandwidthInGbps</span><span class="sxs-lookup"><span data-stu-id="3ed57-115">-BandwidthInGbps</span></span>
<span data-ttu-id="3ed57-116">Przepustowość portów przesąowanych w Gb/s</span><span class="sxs-lookup"><span data-stu-id="3ed57-116">Bandwidth of procured ports in Gbps</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ed57-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ed57-117">-DefaultProfile</span></span>
<span data-ttu-id="3ed57-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3ed57-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ed57-119">- Encapsulation</span><span class="sxs-lookup"><span data-stu-id="3ed57-119">-Encapsulation</span></span>
<span data-ttu-id="3ed57-120">Metoda enkulacji w portach fizycznych.</span><span class="sxs-lookup"><span data-stu-id="3ed57-120">Encapsulation method on physical ports.</span></span>

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

### <span data-ttu-id="3ed57-121">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="3ed57-121">-Force</span></span>
<span data-ttu-id="3ed57-122">Nie pytaj o potwierdzenie, czy chcesz zastąpić zasób</span><span class="sxs-lookup"><span data-stu-id="3ed57-122">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="3ed57-123">— Tożsamość</span><span class="sxs-lookup"><span data-stu-id="3ed57-123">-Identity</span></span>
<span data-ttu-id="3ed57-124">Tożsamość przypisana do użytkownika do odczytu konfiguracji MacSec</span><span class="sxs-lookup"><span data-stu-id="3ed57-124">User Assigned Identity for reading MacSec configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ed57-125">— Link</span><span class="sxs-lookup"><span data-stu-id="3ed57-125">-Link</span></span>
<span data-ttu-id="3ed57-126">Zestaw fizycznych łączy zasobu ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="3ed57-126">The set of physical links of the ExpressRoutePort resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ed57-127">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="3ed57-127">-Location</span></span>
<span data-ttu-id="3ed57-128">Lokalizacja.</span><span class="sxs-lookup"><span data-stu-id="3ed57-128">The location.</span></span>

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

### <span data-ttu-id="3ed57-129">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="3ed57-129">-Name</span></span>
<span data-ttu-id="3ed57-130">Nazwa portu expressroutePort.</span><span class="sxs-lookup"><span data-stu-id="3ed57-130">The name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ed57-131">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="3ed57-131">-PeeringLocation</span></span>
<span data-ttu-id="3ed57-132">Nazwa lokalizacji komunikacji równorzędnej, która fizycznie jest mapowana na usługę ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="3ed57-132">The name of the peering location that the ExpressRoutePort is mapped to physically.</span></span>

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

### <span data-ttu-id="3ed57-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ed57-133">-ResourceGroupName</span></span>
<span data-ttu-id="3ed57-134">Nazwa grupy zasobów dlaportu ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="3ed57-134">The resource group name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ed57-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3ed57-135">-ResourceId</span></span>
<span data-ttu-id="3ed57-136">ResourceId portu trasy ekspresowej.</span><span class="sxs-lookup"><span data-stu-id="3ed57-136">ResourceId of the express route port.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ed57-137">— Tag</span><span class="sxs-lookup"><span data-stu-id="3ed57-137">-Tag</span></span>
<span data-ttu-id="3ed57-138">Tabela skrótów reprezentująca tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="3ed57-138">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="3ed57-139">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3ed57-139">-Confirm</span></span>
<span data-ttu-id="3ed57-140">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3ed57-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ed57-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ed57-141">-WhatIf</span></span>
<span data-ttu-id="3ed57-142">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ed57-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ed57-143">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="3ed57-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ed57-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ed57-144">CommonParameters</span></span>
<span data-ttu-id="3ed57-145">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ed57-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ed57-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ed57-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ed57-147">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3ed57-147">INPUTS</span></span>

### <span data-ttu-id="3ed57-148">System.String</span><span class="sxs-lookup"><span data-stu-id="3ed57-148">System.String</span></span>

### <span data-ttu-id="3ed57-149">System.Int32</span><span class="sxs-lookup"><span data-stu-id="3ed57-149">System.Int32</span></span>

### <span data-ttu-id="3ed57-150">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="3ed57-150">System.Collections.Hashtable</span></span>

### <span data-ttu-id="3ed57-151">Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink[]</span><span class="sxs-lookup"><span data-stu-id="3ed57-151">Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink[]</span></span>

## <span data-ttu-id="3ed57-152">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3ed57-152">OUTPUTS</span></span>

### <span data-ttu-id="3ed57-153">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="3ed57-153">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="3ed57-154">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3ed57-154">NOTES</span></span>

## <span data-ttu-id="3ed57-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3ed57-155">RELATED LINKS</span></span>

[<span data-ttu-id="3ed57-156">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="3ed57-156">Get-AzExpressRoutePort</span></span>](./Get-AzExpressRoutePort.md)

[<span data-ttu-id="3ed57-157">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="3ed57-157">Remove-AzExpressRoutePort</span></span>](./Remove-AzExpressRoutePort.md)

[<span data-ttu-id="3ed57-158">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="3ed57-158">Set-AzExpressRoutePort</span></span>](./Set-AzExpressRoutePort.md)
