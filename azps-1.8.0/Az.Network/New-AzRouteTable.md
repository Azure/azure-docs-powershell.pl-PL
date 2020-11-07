---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6A278F91-C078-4DD4-82D0-2E4FA549A089
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteTable.md
ms.openlocfilehash: ac7b370a6a10aff5a9524a2536b5f4dedaff5a9f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709246"
---
# <span data-ttu-id="eee19-101">New-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="eee19-101">New-AzRouteTable</span></span>

## <span data-ttu-id="eee19-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="eee19-102">SYNOPSIS</span></span>
<span data-ttu-id="eee19-103">Tworzy tabelę tras.</span><span class="sxs-lookup"><span data-stu-id="eee19-103">Creates a route table.</span></span>

## <span data-ttu-id="eee19-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="eee19-104">SYNTAX</span></span>

```
New-AzRouteTable -ResourceGroupName <String> -Name <String> [-DisableBgpRoutePropagation] -Location <String>
 [-Tag <Hashtable>] [-Route <PSRoute[]>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eee19-105">Opis</span><span class="sxs-lookup"><span data-stu-id="eee19-105">DESCRIPTION</span></span>
<span data-ttu-id="eee19-106">Polecenie cmdlet **New-AzRouteTable** tworzy tabelę routingu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="eee19-106">The **New-AzRouteTable** cmdlet creates an Azure route table.</span></span>

## <span data-ttu-id="eee19-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="eee19-107">EXAMPLES</span></span>

### <span data-ttu-id="eee19-108">Przykład 1. Tworzenie tabeli tras zawierającej trasę</span><span class="sxs-lookup"><span data-stu-id="eee19-108">Example 1: Create a route table that contains a route</span></span>
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

<span data-ttu-id="eee19-109">Pierwsze polecenie tworzy trasę o nazwie Route07 przy użyciu polecenia cmdlet New-AzRouteConfig, a następnie zapisuje je w zmiennej $Route.</span><span class="sxs-lookup"><span data-stu-id="eee19-109">The first command creates a route named Route07 by using the New-AzRouteConfig cmdlet, and then stores it in the $Route variable.</span></span> <span data-ttu-id="eee19-110">Ta trasa przekazuje pakiety do lokalnej sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="eee19-110">This route forwards packets to the local virtual network.</span></span>
<span data-ttu-id="eee19-111">Drugie polecenie tworzy tabelę tras o nazwie RouteTable01 i dodaje trasę przechowywaną w $Route do nowej tabeli.</span><span class="sxs-lookup"><span data-stu-id="eee19-111">The second command creates a route table named RouteTable01, and adds the route stored in $Route to the new table.</span></span> <span data-ttu-id="eee19-112">Polecenie określa grupę zasobów, do której należy tabela, oraz lokalizację tabeli.</span><span class="sxs-lookup"><span data-stu-id="eee19-112">The command specifies the resource group to which the table belongs and the location for the table.</span></span>

## <span data-ttu-id="eee19-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="eee19-113">PARAMETERS</span></span>

### <span data-ttu-id="eee19-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eee19-114">-AsJob</span></span>
<span data-ttu-id="eee19-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="eee19-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="eee19-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eee19-116">-DefaultProfile</span></span>
<span data-ttu-id="eee19-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="eee19-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eee19-118">-DisableBgpRoutePropagation</span><span class="sxs-lookup"><span data-stu-id="eee19-118">-DisableBgpRoutePropagation</span></span>
<span data-ttu-id="eee19-119">Wyłącz automatyczną propagację trasy BGP.</span><span class="sxs-lookup"><span data-stu-id="eee19-119">Disable BGP Route auto propagation.</span></span>

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

### <span data-ttu-id="eee19-120">-Force</span><span class="sxs-lookup"><span data-stu-id="eee19-120">-Force</span></span>
<span data-ttu-id="eee19-121">Wskazuje, że to polecenie cmdlet tworzy tabelę routingu, nawet jeśli istnieje już tabela tras o takiej samej nazwie.</span><span class="sxs-lookup"><span data-stu-id="eee19-121">Indicates that this cmdlet creates a route table even if a route table that has the same name already exists.</span></span>

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

### <span data-ttu-id="eee19-122">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="eee19-122">-Location</span></span>
<span data-ttu-id="eee19-123">Określa obszar Azure, w którym to polecenie cmdlet tworzy tabelę tras.</span><span class="sxs-lookup"><span data-stu-id="eee19-123">Specifies the Azure region in which this cmdlet creates a route table.</span></span>
<span data-ttu-id="eee19-124">Aby uzyskać więcej informacji, zobacz [regiony platformy Azure](https://azure.microsoft.com/en-us/regions/).</span><span class="sxs-lookup"><span data-stu-id="eee19-124">For more information, see [Azure Regions](https://azure.microsoft.com/en-us/regions/).</span></span>

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

### <span data-ttu-id="eee19-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="eee19-125">-Name</span></span>
<span data-ttu-id="eee19-126">Określa nazwę tabeli routingu.</span><span class="sxs-lookup"><span data-stu-id="eee19-126">Specifies a name for the route table.</span></span>

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

### <span data-ttu-id="eee19-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eee19-127">-ResourceGroupName</span></span>
<span data-ttu-id="eee19-128">Określa nazwę grupy zasobów, w której to polecenie cmdlet tworzy tabelę tras.</span><span class="sxs-lookup"><span data-stu-id="eee19-128">Specifies the name of the resource group in which this cmdlet creates a route table.</span></span>

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

### <span data-ttu-id="eee19-129">-Route</span><span class="sxs-lookup"><span data-stu-id="eee19-129">-Route</span></span>
<span data-ttu-id="eee19-130">Określa tablicę obiektów **tras** , które mają zostać skojarzone z tabelą tras.</span><span class="sxs-lookup"><span data-stu-id="eee19-130">Specifies an array of **Route** objects to associate with the route table.</span></span>

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

### <span data-ttu-id="eee19-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="eee19-131">-Tag</span></span>
<span data-ttu-id="eee19-132">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="eee19-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="eee19-133">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="eee19-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="eee19-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="eee19-134">-Confirm</span></span>
<span data-ttu-id="eee19-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eee19-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eee19-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eee19-136">-WhatIf</span></span>
<span data-ttu-id="eee19-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eee19-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eee19-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="eee19-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eee19-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eee19-139">CommonParameters</span></span>
<span data-ttu-id="eee19-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eee19-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eee19-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eee19-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eee19-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eee19-142">INPUTS</span></span>

### <span data-ttu-id="eee19-143">System. String</span><span class="sxs-lookup"><span data-stu-id="eee19-143">System.String</span></span>

### <span data-ttu-id="eee19-144">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="eee19-144">System.Collections.Hashtable</span></span>

### <span data-ttu-id="eee19-145">Microsoft. Azure. Commands. Network. models. PSRoute []</span><span class="sxs-lookup"><span data-stu-id="eee19-145">Microsoft.Azure.Commands.Network.Models.PSRoute[]</span></span>

## <span data-ttu-id="eee19-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="eee19-146">OUTPUTS</span></span>

### <span data-ttu-id="eee19-147">Microsoft. Azure. Commands. Network. models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="eee19-147">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="eee19-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="eee19-148">NOTES</span></span>

## <span data-ttu-id="eee19-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="eee19-149">RELATED LINKS</span></span>

[<span data-ttu-id="eee19-150">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="eee19-150">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="eee19-151">Nowe — AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="eee19-151">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="eee19-152">Remove-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="eee19-152">Remove-AzRouteTable</span></span>](./Remove-AzRouteTable.md)

[<span data-ttu-id="eee19-153">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="eee19-153">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)
