---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6A278F91-C078-4DD4-82D0-2E4FA549A089
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteTable.md
ms.openlocfilehash: e7e0b58dfd4ac925110c5f666bc7c360cc222983
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179619"
---
# <span data-ttu-id="9375d-101">New-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="9375d-101">New-AzRouteTable</span></span>

## <span data-ttu-id="9375d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9375d-102">SYNOPSIS</span></span>
<span data-ttu-id="9375d-103">Tworzy tabelę trasy.</span><span class="sxs-lookup"><span data-stu-id="9375d-103">Creates a route table.</span></span>

## <span data-ttu-id="9375d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9375d-104">SYNTAX</span></span>

```
New-AzRouteTable -ResourceGroupName <String> -Name <String> [-DisableBgpRoutePropagation] -Location <String>
 [-Tag <Hashtable>] [-Route <PSRoute[]>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9375d-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="9375d-105">DESCRIPTION</span></span>
<span data-ttu-id="9375d-106">Polecenie **cmdlet New-AzRouteTable** tworzy tabelę trasy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9375d-106">The **New-AzRouteTable** cmdlet creates an Azure route table.</span></span>

## <span data-ttu-id="9375d-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9375d-107">EXAMPLES</span></span>

### <span data-ttu-id="9375d-108">Przykład 1. Tworzenie tabeli trasy zawierającej trasę</span><span class="sxs-lookup"><span data-stu-id="9375d-108">Example 1: Create a route table that contains a route</span></span>
```
PS C:\>$Route = New-AzRouteConfig -Name "Route07" -AddressPrefix 10.1.0.0/16 -NextHopType "VnetLocal"
PS C:\> New-AzRouteTable -Name "RouteTable01" -ResourceGroupName "ResourceGroup11" -Location "EASTUS" -Route $Route
Name              : routetable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/myroutetable
Etag              : W/"db5f4e12-3f34-465b-92dd-0ab3bf6fc274"
ProvisioningState : Succeeded
Tags              :
Routes            : [
                      {
                        "Name": "route07",
                        "Etag": "W/\"db5f4e12-3f34-465b-92dd-0ab3bf6fc274\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/routetable01/routes/route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null,
                        "ProvisioningState": "Succeeded"
                      }
                    ]
Subnets           : []
```

<span data-ttu-id="9375d-109">Pierwsze polecenie tworzy trasę o nazwie Route07 za pomocą polecenia cmdlet New-AzRouteConfig, a następnie zapisuje ją w $Route danych.</span><span class="sxs-lookup"><span data-stu-id="9375d-109">The first command creates a route named Route07 by using the New-AzRouteConfig cmdlet, and then stores it in the $Route variable.</span></span> <span data-ttu-id="9375d-110">Ta trasa przesyła pakiety do lokalnej sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9375d-110">This route forwards packets to the local virtual network.</span></span>
<span data-ttu-id="9375d-111">Drugie polecenie tworzy tabelę trasy o nazwie RouteTable01 i dodaje trasę przechowywaną w $Route do nowej tabeli.</span><span class="sxs-lookup"><span data-stu-id="9375d-111">The second command creates a route table named RouteTable01, and adds the route stored in $Route to the new table.</span></span> <span data-ttu-id="9375d-112">To polecenie określa grupę zasobów, do której należy tabela, oraz lokalizację tabeli.</span><span class="sxs-lookup"><span data-stu-id="9375d-112">The command specifies the resource group to which the table belongs and the location for the table.</span></span>

## <span data-ttu-id="9375d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9375d-113">PARAMETERS</span></span>

### <span data-ttu-id="9375d-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="9375d-114">-AsJob</span></span>
<span data-ttu-id="9375d-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="9375d-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9375d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9375d-116">-DefaultProfile</span></span>
<span data-ttu-id="9375d-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9375d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9375d-118">-DisableBgpRoutePropagation</span><span class="sxs-lookup"><span data-stu-id="9375d-118">-DisableBgpRoutePropagation</span></span>
<span data-ttu-id="9375d-119">Wyłącz automatyczne propagację trasy BGP.</span><span class="sxs-lookup"><span data-stu-id="9375d-119">Disable BGP Route auto propagation.</span></span>

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

### <span data-ttu-id="9375d-120">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="9375d-120">-Force</span></span>
<span data-ttu-id="9375d-121">Wskazuje, że to polecenie cmdlet tworzy tabelę trasy, nawet jeśli istnieje już tabela trasy o takiej samej nazwie.</span><span class="sxs-lookup"><span data-stu-id="9375d-121">Indicates that this cmdlet creates a route table even if a route table that has the same name already exists.</span></span>

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

### <span data-ttu-id="9375d-122">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="9375d-122">-Location</span></span>
<span data-ttu-id="9375d-123">Określa region platformy Azure, w którym to polecenie cmdlet tworzy tabelę trasy.</span><span class="sxs-lookup"><span data-stu-id="9375d-123">Specifies the Azure region in which this cmdlet creates a route table.</span></span>
<span data-ttu-id="9375d-124">Aby uzyskać więcej informacji, zobacz [Regiony platformy Azure.](http://azure.microsoft.com/en-us/regions/)</span><span class="sxs-lookup"><span data-stu-id="9375d-124">For more information, see [Azure Regions](http://azure.microsoft.com/en-us/regions/).</span></span>

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

### <span data-ttu-id="9375d-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9375d-125">-Name</span></span>
<span data-ttu-id="9375d-126">Określa nazwę tabeli trasy.</span><span class="sxs-lookup"><span data-stu-id="9375d-126">Specifies a name for the route table.</span></span>

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

### <span data-ttu-id="9375d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9375d-127">-ResourceGroupName</span></span>
<span data-ttu-id="9375d-128">Określa nazwę grupy zasobów, w której to polecenie cmdlet tworzy tabelę trasy.</span><span class="sxs-lookup"><span data-stu-id="9375d-128">Specifies the name of the resource group in which this cmdlet creates a route table.</span></span>

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

### <span data-ttu-id="9375d-129">— Trasa</span><span class="sxs-lookup"><span data-stu-id="9375d-129">-Route</span></span>
<span data-ttu-id="9375d-130">Określa tablicę obiektów **trasy** do skojarzenia z tabelą trasy.</span><span class="sxs-lookup"><span data-stu-id="9375d-130">Specifies an array of **Route** objects to associate with the route table.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRoute[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9375d-131">— Tag</span><span class="sxs-lookup"><span data-stu-id="9375d-131">-Tag</span></span>
<span data-ttu-id="9375d-132">Pary klucz-wartość w postaci tabeli skrótu.</span><span class="sxs-lookup"><span data-stu-id="9375d-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="9375d-133">Na przykład: @{key0="value0";key1=$null;key2="wartość2"}</span><span class="sxs-lookup"><span data-stu-id="9375d-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="9375d-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9375d-134">-Confirm</span></span>
<span data-ttu-id="9375d-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9375d-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9375d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9375d-136">-WhatIf</span></span>
<span data-ttu-id="9375d-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9375d-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9375d-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="9375d-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9375d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9375d-139">CommonParameters</span></span>
<span data-ttu-id="9375d-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9375d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9375d-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9375d-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9375d-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9375d-142">INPUTS</span></span>

### <span data-ttu-id="9375d-143">System.String</span><span class="sxs-lookup"><span data-stu-id="9375d-143">System.String</span></span>

### <span data-ttu-id="9375d-144">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="9375d-144">System.Collections.Hashtable</span></span>

### <span data-ttu-id="9375d-145">Microsoft.Azure.Commands.Network.Models.PSRoute[]</span><span class="sxs-lookup"><span data-stu-id="9375d-145">Microsoft.Azure.Commands.Network.Models.PSRoute[]</span></span>

## <span data-ttu-id="9375d-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9375d-146">OUTPUTS</span></span>

### <span data-ttu-id="9375d-147">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="9375d-147">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="9375d-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9375d-148">NOTES</span></span>

## <span data-ttu-id="9375d-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9375d-149">RELATED LINKS</span></span>

[<span data-ttu-id="9375d-150">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="9375d-150">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="9375d-151">New-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="9375d-151">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="9375d-152">Remove-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="9375d-152">Remove-AzRouteTable</span></span>](./Remove-AzRouteTable.md)

[<span data-ttu-id="9375d-153">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="9375d-153">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)
