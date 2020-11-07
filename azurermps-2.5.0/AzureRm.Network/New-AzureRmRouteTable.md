---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6A278F91-C078-4DD4-82D0-2E4FA549A089
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermroutetable
schema: 2.0.0
ms.openlocfilehash: 9ba23a33e82e003413172240264ef8485b12d4e0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899103"
---
# <span data-ttu-id="5e419-101">New-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="5e419-101">New-AzureRmRouteTable</span></span>

## <span data-ttu-id="5e419-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5e419-102">SYNOPSIS</span></span>
<span data-ttu-id="5e419-103">Tworzy tabelę tras.</span><span class="sxs-lookup"><span data-stu-id="5e419-103">Creates a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e419-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5e419-104">SYNTAX</span></span>

```
New-AzureRmRouteTable -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-Route <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRoute]>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e419-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5e419-105">DESCRIPTION</span></span>
<span data-ttu-id="5e419-106">Polecenie cmdlet **New-AzureRmRouteTable** tworzy tabelę routingu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5e419-106">The **New-AzureRmRouteTable** cmdlet creates an Azure route table.</span></span>

## <span data-ttu-id="5e419-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5e419-107">EXAMPLES</span></span>

### <span data-ttu-id="5e419-108">Przykład 1. Tworzenie tabeli tras zawierającej trasę</span><span class="sxs-lookup"><span data-stu-id="5e419-108">Example 1: Create a route table that contains a route</span></span>
```
PS C:\>$Route = New-AzureRmRouteConfig -Name "Route07" -AddressPrefix 10.1.0.0/16 -NextHopType "VnetLocal"
PS C:\> New-AzureRmRouteTable -Name "RouteTable01" -ResourceGroupName "ResourceGroup11" -Location "EASTUS" -Route $Route
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

<span data-ttu-id="5e419-109">Pierwsze polecenie tworzy trasę o nazwie Route07 przy użyciu polecenia cmdlet New-AzureRmRouteConfig, a następnie zapisuje je w zmiennej $Route.</span><span class="sxs-lookup"><span data-stu-id="5e419-109">The first command creates a route named Route07 by using the New-AzureRmRouteConfig cmdlet, and then stores it in the $Route variable.</span></span> <span data-ttu-id="5e419-110">Ta trasa przekazuje pakiety do lokalnej sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5e419-110">This route forwards packets to the local virtual network.</span></span>

<span data-ttu-id="5e419-111">Drugie polecenie tworzy tabelę tras o nazwie RouteTable01 i dodaje trasę przechowywaną w $Route do nowej tabeli.</span><span class="sxs-lookup"><span data-stu-id="5e419-111">The second command creates a route table named RouteTable01, and adds the route stored in $Route to the new table.</span></span> <span data-ttu-id="5e419-112">Polecenie określa grupę zasobów, do której należy tabela, oraz lokalizację tabeli.</span><span class="sxs-lookup"><span data-stu-id="5e419-112">The command specifies the resource group to which the table belongs and the location for the table.</span></span>

## <span data-ttu-id="5e419-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5e419-113">PARAMETERS</span></span>

### <span data-ttu-id="5e419-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5e419-114">-AsJob</span></span>
<span data-ttu-id="5e419-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="5e419-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5e419-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e419-116">-DefaultProfile</span></span>
<span data-ttu-id="5e419-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5e419-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e419-118">-Force</span><span class="sxs-lookup"><span data-stu-id="5e419-118">-Force</span></span>
<span data-ttu-id="5e419-119">Wskazuje, że to polecenie cmdlet tworzy tabelę routingu, nawet jeśli istnieje już tabela tras o takiej samej nazwie.</span><span class="sxs-lookup"><span data-stu-id="5e419-119">Indicates that this cmdlet creates a route table even if a route table that has the same name already exists.</span></span>

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

### <span data-ttu-id="5e419-120">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="5e419-120">-Location</span></span>
<span data-ttu-id="5e419-121">Określa obszar Azure, w którym to polecenie cmdlet tworzy tabelę tras.</span><span class="sxs-lookup"><span data-stu-id="5e419-121">Specifies the Azure region in which this cmdlet creates a route table.</span></span>
<span data-ttu-id="5e419-122">Aby uzyskać więcej informacji, zobacz [regiony platformy Azure](https://azure.microsoft.com/en-us/regions/).</span><span class="sxs-lookup"><span data-stu-id="5e419-122">For more information, see [Azure Regions](https://azure.microsoft.com/en-us/regions/).</span></span>

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

### <span data-ttu-id="5e419-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5e419-123">-Name</span></span>
<span data-ttu-id="5e419-124">Określa nazwę tabeli routingu.</span><span class="sxs-lookup"><span data-stu-id="5e419-124">Specifies a name for the route table.</span></span>

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

### <span data-ttu-id="5e419-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e419-125">-ResourceGroupName</span></span>
<span data-ttu-id="5e419-126">Określa nazwę grupy zasobów, w której to polecenie cmdlet tworzy tabelę tras.</span><span class="sxs-lookup"><span data-stu-id="5e419-126">Specifies the name of the resource group in which this cmdlet creates a route table.</span></span>

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

### <span data-ttu-id="5e419-127">-Route</span><span class="sxs-lookup"><span data-stu-id="5e419-127">-Route</span></span>
<span data-ttu-id="5e419-128">Określa tablicę obiektów **tras** , które mają zostać skojarzone z tabelą tras.</span><span class="sxs-lookup"><span data-stu-id="5e419-128">Specifies an array of **Route** objects to associate with the route table.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRoute]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e419-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="5e419-129">-Tag</span></span>
<span data-ttu-id="5e419-130">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="5e419-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="5e419-131">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="5e419-131">For example:</span></span>

<span data-ttu-id="5e419-132">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="5e419-132">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="5e419-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5e419-133">-Confirm</span></span>
<span data-ttu-id="5e419-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e419-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e419-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e419-135">-WhatIf</span></span>
<span data-ttu-id="5e419-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e419-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e419-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5e419-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e419-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e419-138">CommonParameters</span></span>
<span data-ttu-id="5e419-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e419-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e419-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e419-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e419-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5e419-141">INPUTS</span></span>

## <span data-ttu-id="5e419-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5e419-142">OUTPUTS</span></span>

### <span data-ttu-id="5e419-143">Microsoft. Azure. Commands. Network. models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="5e419-143">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="5e419-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5e419-144">NOTES</span></span>

## <span data-ttu-id="5e419-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5e419-145">RELATED LINKS</span></span>

[<span data-ttu-id="5e419-146">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="5e419-146">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="5e419-147">Nowe — AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="5e419-147">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="5e419-148">Remove-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="5e419-148">Remove-AzureRmRouteTable</span></span>](./Remove-AzureRmRouteTable.md)

[<span data-ttu-id="5e419-149">Set-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="5e419-149">Set-AzureRmRouteTable</span></span>](./Set-AzureRmRouteTable.md)
