---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6A278F91-C078-4DD4-82D0-2E4FA549A089
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteTable.md
ms.openlocfilehash: a311d64fbdb086ca1d52ab5a1db725e278c6cc16
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550655"
---
# <span data-ttu-id="684f4-101">New-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="684f4-101">New-AzureRmRouteTable</span></span>

## <span data-ttu-id="684f4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="684f4-102">SYNOPSIS</span></span>
<span data-ttu-id="684f4-103">Tworzy tabelę tras.</span><span class="sxs-lookup"><span data-stu-id="684f4-103">Creates a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="684f4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="684f4-104">SYNTAX</span></span>

```
New-AzureRmRouteTable -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-Route <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRoute]>]
 [-DisableBgpRoutePropagation] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="684f4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="684f4-105">DESCRIPTION</span></span>
<span data-ttu-id="684f4-106">Polecenie cmdlet **New-AzureRmRouteTable** tworzy tabelę routingu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="684f4-106">The **New-AzureRmRouteTable** cmdlet creates an Azure route table.</span></span>

## <span data-ttu-id="684f4-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="684f4-107">EXAMPLES</span></span>

### <span data-ttu-id="684f4-108">Przykład 1. Tworzenie tabeli tras zawierającej trasę</span><span class="sxs-lookup"><span data-stu-id="684f4-108">Example 1: Create a route table that contains a route</span></span>
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

<span data-ttu-id="684f4-109">Pierwsze polecenie tworzy trasę o nazwie Route07 przy użyciu polecenia cmdlet New-AzureRmRouteConfig, a następnie zapisuje je w zmiennej $Route.</span><span class="sxs-lookup"><span data-stu-id="684f4-109">The first command creates a route named Route07 by using the New-AzureRmRouteConfig cmdlet, and then stores it in the $Route variable.</span></span> <span data-ttu-id="684f4-110">Ta trasa przekazuje pakiety do lokalnej sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="684f4-110">This route forwards packets to the local virtual network.</span></span>

<span data-ttu-id="684f4-111">Drugie polecenie tworzy tabelę tras o nazwie RouteTable01 i dodaje trasę przechowywaną w $Route do nowej tabeli.</span><span class="sxs-lookup"><span data-stu-id="684f4-111">The second command creates a route table named RouteTable01, and adds the route stored in $Route to the new table.</span></span> <span data-ttu-id="684f4-112">Polecenie określa grupę zasobów, do której należy tabela, oraz lokalizację tabeli.</span><span class="sxs-lookup"><span data-stu-id="684f4-112">The command specifies the resource group to which the table belongs and the location for the table.</span></span>

## <span data-ttu-id="684f4-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="684f4-113">PARAMETERS</span></span>

### <span data-ttu-id="684f4-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="684f4-114">-AsJob</span></span>
<span data-ttu-id="684f4-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="684f4-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="684f4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="684f4-116">-DefaultProfile</span></span>
<span data-ttu-id="684f4-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="684f4-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="684f4-118">-DisableBgpRoutePropagation</span><span class="sxs-lookup"><span data-stu-id="684f4-118">-DisableBgpRoutePropagation</span></span>
<span data-ttu-id="684f4-119">Wyłącz automatyczną propagację trasy BGP.</span><span class="sxs-lookup"><span data-stu-id="684f4-119">Disable BGP Route auto propagation.</span></span>

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

### <span data-ttu-id="684f4-120">-Force</span><span class="sxs-lookup"><span data-stu-id="684f4-120">-Force</span></span>
<span data-ttu-id="684f4-121">Wskazuje, że to polecenie cmdlet tworzy tabelę routingu, nawet jeśli istnieje już tabela tras o takiej samej nazwie.</span><span class="sxs-lookup"><span data-stu-id="684f4-121">Indicates that this cmdlet creates a route table even if a route table that has the same name already exists.</span></span>

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

### <span data-ttu-id="684f4-122">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="684f4-122">-Location</span></span>
<span data-ttu-id="684f4-123">Określa obszar Azure, w którym to polecenie cmdlet tworzy tabelę tras.</span><span class="sxs-lookup"><span data-stu-id="684f4-123">Specifies the Azure region in which this cmdlet creates a route table.</span></span>
<span data-ttu-id="684f4-124">Aby uzyskać więcej informacji, zobacz [regiony platformy Azure](https://azure.microsoft.com/en-us/regions/).</span><span class="sxs-lookup"><span data-stu-id="684f4-124">For more information, see [Azure Regions](https://azure.microsoft.com/en-us/regions/).</span></span>

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

### <span data-ttu-id="684f4-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="684f4-125">-Name</span></span>
<span data-ttu-id="684f4-126">Określa nazwę tabeli routingu.</span><span class="sxs-lookup"><span data-stu-id="684f4-126">Specifies a name for the route table.</span></span>

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

### <span data-ttu-id="684f4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="684f4-127">-ResourceGroupName</span></span>
<span data-ttu-id="684f4-128">Określa nazwę grupy zasobów, w której to polecenie cmdlet tworzy tabelę tras.</span><span class="sxs-lookup"><span data-stu-id="684f4-128">Specifies the name of the resource group in which this cmdlet creates a route table.</span></span>

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

### <span data-ttu-id="684f4-129">-Route</span><span class="sxs-lookup"><span data-stu-id="684f4-129">-Route</span></span>
<span data-ttu-id="684f4-130">Określa tablicę obiektów **tras** , które mają zostać skojarzone z tabelą tras.</span><span class="sxs-lookup"><span data-stu-id="684f4-130">Specifies an array of **Route** objects to associate with the route table.</span></span>

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

### <span data-ttu-id="684f4-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="684f4-131">-Tag</span></span>
<span data-ttu-id="684f4-132">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="684f4-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="684f4-133">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="684f4-133">For example:</span></span>

<span data-ttu-id="684f4-134">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="684f4-134">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="684f4-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="684f4-135">-Confirm</span></span>
<span data-ttu-id="684f4-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="684f4-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="684f4-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="684f4-137">-WhatIf</span></span>
<span data-ttu-id="684f4-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="684f4-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="684f4-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="684f4-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="684f4-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="684f4-140">CommonParameters</span></span>
<span data-ttu-id="684f4-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="684f4-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="684f4-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="684f4-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="684f4-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="684f4-143">INPUTS</span></span>

### <span data-ttu-id="684f4-144">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="684f4-144">None</span></span>
<span data-ttu-id="684f4-145">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="684f4-145">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="684f4-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="684f4-146">OUTPUTS</span></span>

### <span data-ttu-id="684f4-147">Microsoft. Azure. Commands. Network. models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="684f4-147">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="684f4-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="684f4-148">NOTES</span></span>

## <span data-ttu-id="684f4-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="684f4-149">RELATED LINKS</span></span>

[<span data-ttu-id="684f4-150">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="684f4-150">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="684f4-151">Nowe — AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="684f4-151">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="684f4-152">Remove-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="684f4-152">Remove-AzureRmRouteTable</span></span>](./Remove-AzureRmRouteTable.md)

[<span data-ttu-id="684f4-153">Set-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="684f4-153">Set-AzureRmRouteTable</span></span>](./Set-AzureRmRouteTable.md)