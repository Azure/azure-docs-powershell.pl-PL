---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6A278F91-C078-4DD4-82D0-2E4FA549A089
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteTable.md
ms.openlocfilehash: f4ef683b65967fe694713b7990d23eb173f02163
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543252"
---
# <span data-ttu-id="4275e-101">New-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="4275e-101">New-AzureRmRouteTable</span></span>

## <span data-ttu-id="4275e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4275e-102">SYNOPSIS</span></span>
<span data-ttu-id="4275e-103">Tworzy tabelę tras.</span><span class="sxs-lookup"><span data-stu-id="4275e-103">Creates a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4275e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4275e-104">SYNTAX</span></span>

```
New-AzureRmRouteTable -Name <String> -ResourceGroupName <String> -Location <String>
 [-Route <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRoute]>]
 [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4275e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4275e-105">DESCRIPTION</span></span>
<span data-ttu-id="4275e-106">Polecenie cmdlet **New-AzureRmRouteTable** tworzy tabelę routingu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4275e-106">The **New-AzureRmRouteTable** cmdlet creates an Azure route table.</span></span>

## <span data-ttu-id="4275e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4275e-107">EXAMPLES</span></span>

### <span data-ttu-id="4275e-108">Przykład 1. Tworzenie tabeli tras zawierającej trasę</span><span class="sxs-lookup"><span data-stu-id="4275e-108">Example 1: Create a route table that contains a route</span></span>
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

<span data-ttu-id="4275e-109">Pierwsze polecenie tworzy trasę o nazwie Route07 przy użyciu polecenia cmdlet New-AzureRmRouteConfig, a następnie zapisuje je w zmiennej $Route.</span><span class="sxs-lookup"><span data-stu-id="4275e-109">The first command creates a route named Route07 by using the New-AzureRmRouteConfig cmdlet, and then stores it in the $Route variable.</span></span> <span data-ttu-id="4275e-110">Ta trasa przekazuje pakiety do lokalnej sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="4275e-110">This route forwards packets to the local virtual network.</span></span>

<span data-ttu-id="4275e-111">Drugie polecenie tworzy tabelę tras o nazwie RouteTable01 i dodaje trasę przechowywaną w $Route do nowej tabeli.</span><span class="sxs-lookup"><span data-stu-id="4275e-111">The second command creates a route table named RouteTable01, and adds the route stored in $Route to the new table.</span></span> <span data-ttu-id="4275e-112">Polecenie określa grupę zasobów, do której należy tabela, oraz lokalizację tabeli.</span><span class="sxs-lookup"><span data-stu-id="4275e-112">The command specifies the resource group to which the table belongs and the location for the table.</span></span>

## <span data-ttu-id="4275e-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4275e-113">PARAMETERS</span></span>

### <span data-ttu-id="4275e-114">-Force</span><span class="sxs-lookup"><span data-stu-id="4275e-114">-Force</span></span>
<span data-ttu-id="4275e-115">Wskazuje, że to polecenie cmdlet tworzy tabelę routingu, nawet jeśli istnieje już tabela tras o takiej samej nazwie.</span><span class="sxs-lookup"><span data-stu-id="4275e-115">Indicates that this cmdlet creates a route table even if a route table that has the same name already exists.</span></span>

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

### <span data-ttu-id="4275e-116">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="4275e-116">-Location</span></span>
<span data-ttu-id="4275e-117">Określa obszar Azure, w którym to polecenie cmdlet tworzy tabelę tras.</span><span class="sxs-lookup"><span data-stu-id="4275e-117">Specifies the Azure region in which this cmdlet creates a route table.</span></span>
<span data-ttu-id="4275e-118">Aby uzyskać więcej informacji, zobacz [regiony platformy Azure](https://azure.microsoft.com/en-us/regions/).</span><span class="sxs-lookup"><span data-stu-id="4275e-118">For more information, see [Azure Regions](https://azure.microsoft.com/en-us/regions/).</span></span>

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

### <span data-ttu-id="4275e-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4275e-119">-Name</span></span>
<span data-ttu-id="4275e-120">Określa nazwę tabeli routingu.</span><span class="sxs-lookup"><span data-stu-id="4275e-120">Specifies a name for the route table.</span></span>

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

### <span data-ttu-id="4275e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4275e-121">-ResourceGroupName</span></span>
<span data-ttu-id="4275e-122">Określa nazwę grupy zasobów, w której to polecenie cmdlet tworzy tabelę tras.</span><span class="sxs-lookup"><span data-stu-id="4275e-122">Specifies the name of the resource group in which this cmdlet creates a route table.</span></span>

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

### <span data-ttu-id="4275e-123">-Route</span><span class="sxs-lookup"><span data-stu-id="4275e-123">-Route</span></span>
<span data-ttu-id="4275e-124">Określa tablicę obiektów **tras** , które mają zostać skojarzone z tabelą tras.</span><span class="sxs-lookup"><span data-stu-id="4275e-124">Specifies an array of **Route** objects to associate with the route table.</span></span>

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

### <span data-ttu-id="4275e-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="4275e-125">-Tag</span></span>
<span data-ttu-id="4275e-126">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="4275e-126">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="4275e-127">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="4275e-127">For example:</span></span>

<span data-ttu-id="4275e-128">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="4275e-128">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="4275e-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4275e-129">-Confirm</span></span>
<span data-ttu-id="4275e-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4275e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4275e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4275e-131">-WhatIf</span></span>
<span data-ttu-id="4275e-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4275e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4275e-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4275e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4275e-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4275e-134">-DefaultProfile</span></span>
<span data-ttu-id="4275e-135">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4275e-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4275e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4275e-136">CommonParameters</span></span>
<span data-ttu-id="4275e-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4275e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4275e-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4275e-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4275e-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4275e-139">INPUTS</span></span>

## <span data-ttu-id="4275e-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4275e-140">OUTPUTS</span></span>

### <span data-ttu-id="4275e-141">Microsoft. Azure. Commands. Network. models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="4275e-141">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="4275e-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4275e-142">NOTES</span></span>

## <span data-ttu-id="4275e-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4275e-143">RELATED LINKS</span></span>

[<span data-ttu-id="4275e-144">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="4275e-144">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="4275e-145">Nowe — AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="4275e-145">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="4275e-146">Remove-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="4275e-146">Remove-AzureRmRouteTable</span></span>](./Remove-AzureRmRouteTable.md)

[<span data-ttu-id="4275e-147">Set-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="4275e-147">Set-AzureRmRouteTable</span></span>](./Set-AzureRmRouteTable.md)
