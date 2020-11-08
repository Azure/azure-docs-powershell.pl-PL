---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/get-azprivatednsvirtualnetworklink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: 60da913ea7743be288e58eee9e4840c15e4818b4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221880"
---
# <span data-ttu-id="d1477-101">Get-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="d1477-101">Get-AzPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="d1477-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d1477-102">SYNOPSIS</span></span>
<span data-ttu-id="d1477-103">Pobiera wirtualne łącze sieciowe skojarzone z określoną prywatną strefą DNS.</span><span class="sxs-lookup"><span data-stu-id="d1477-103">Gets a virtual network link associated with the specified Private DNS zone.</span></span>

## <span data-ttu-id="d1477-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d1477-104">SYNTAX</span></span>

```
Get-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1477-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d1477-105">DESCRIPTION</span></span>
<span data-ttu-id="d1477-106">Polecenie cmdlet **Get-AzPrivateDnsVirtualNetworkLink** umożliwia pobieranie wirtualnych łączy sieciowych skojarzonych z określoną prywatną strefą DNS w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="d1477-106">The **Get-AzPrivateDnsVirtualNetworkLink** cmdlet gets virtual network links associated with a particular Private DNS zone from the specified resource group.</span></span>
<span data-ttu-id="d1477-107">Jeśli określisz parametr *name* , zwracany jest jeden obiekt **PSPrivateDnsVirtualNetworkLink** .</span><span class="sxs-lookup"><span data-stu-id="d1477-107">If you specify the *Name* parameter, a single **PSPrivateDnsVirtualNetworkLink** object is returned.</span></span>
<span data-ttu-id="d1477-108">Jeśli parametr *name* nie zostanie określony, zostanie zwrócona tablica zawierająca wszystkie linki skojarzone z tą strefą w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="d1477-108">If you do not specify the *Name* parameter, an array containing all of the links associated with the zone in the specified resource group is returned.</span></span>
<span data-ttu-id="d1477-109">Możesz użyć obiektu **PSPrivateDnsVirtualNetworkLink** , aby zaktualizować link.</span><span class="sxs-lookup"><span data-stu-id="d1477-109">You can use the **PSPrivateDnsVirtualNetworkLink** object to update the link.</span></span>

## <span data-ttu-id="d1477-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d1477-110">EXAMPLES</span></span>

### <span data-ttu-id="d1477-111">Przykład 1: Uzyskaj link sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d1477-111">Example 1: Get a virtual network link.</span></span>
```
PS C:\> $Link = Get-AzPrivateDnsVirtualNetworkLink -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "mylink"

The link object returned looks like the following:

Name                    : mylink
ResourceId              : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/privateDnsZones/myzone.com/virtualNetworkLinks/mylink
ResourceGroupName       : MyResourceGroup
ZoneName                : myzone.com
VirtualNetworkId        : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/virtualNetworks/myvirtualnetwork
Location                :
Etag                    : "xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Tags                    : {tag1}
RegistrationEnabled     : True
VirtualNetworkLinkState : Completed
ProvisioningState       : Succeeded
```

<span data-ttu-id="d1477-112">W tym przykładzie zostanie nadane łącze sieci wirtualnej moje łącze skojarzone z prywatną strefą DNS o nazwie myzone.com z poziomu określonej grupy zasobów, a następnie zapisanie go w zmiennej $Link.</span><span class="sxs-lookup"><span data-stu-id="d1477-112">This example gets the virtual network link mylink associated with the Private DNS zone named myzone.com from the specified resource group, and then stores it in the $Link variable.</span></span>

### <span data-ttu-id="d1477-113">Przykład 2: uzyskiwanie wszystkich linków skojarzonych z strefą w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="d1477-113">Example 2: Get all of the links associated with a zone in a resource group.</span></span>
```
PS C:\> $Links = Get-AzPrivateDnsVirtualNetworkLink -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"

Name                    : mylink1
ResourceId              : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/privateDnsZones/myzone.com/virtualNetworkLinks/mylink1
ResourceGroupName       : MyResourceGroup
ZoneName                : myzone.com
VirtualNetworkId        : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/virtualNetworks/myvirtualnetwork
Location                :
Etag                    : "xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Tags                    : {tag1}
RegistrationEnabled     : True
VirtualNetworkLinkState : Completed
ProvisioningState       : Succeeded

Name                    : mylink2
ResourceId              : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/privateDnsZones/myzone.com/virtualNetworkLinks/mylink2
ResourceGroupName       : MyResourceGroup
ZoneName                : myzone.com
VirtualNetworkId        : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/virtualNetworks/myvirtualnetwork
Location                :
Etag                    : "xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Tags                    : {tag1}
RegistrationEnabled     : True
VirtualNetworkLinkState : Completed
ProvisioningState       : Succeeded
```

<span data-ttu-id="d1477-114">W tym przykładzie są pobierane wszystkie linki sieci wirtualnej skojarzone z prywatną strefą DNS "myzone.com" w określonej grupie zasobów, a następnie są one przechowywane w zmiennej $Links.</span><span class="sxs-lookup"><span data-stu-id="d1477-114">This example gets all of the virtual network links associated with the Private DNS zone "myzone.com" in the specified resource group, and then stores it in the $Links variable.</span></span>

## <span data-ttu-id="d1477-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d1477-115">PARAMETERS</span></span>

### <span data-ttu-id="d1477-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1477-116">-DefaultProfile</span></span>
<span data-ttu-id="d1477-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="d1477-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d1477-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d1477-118">-Name</span></span>
<span data-ttu-id="d1477-119">Określa nazwę linku sieci wirtualnej, który ma zostać wyświetlony.</span><span class="sxs-lookup"><span data-stu-id="d1477-119">Specifies the name of the virtual network link to get.</span></span>
<span data-ttu-id="d1477-120">Jeśli wartość parametru *name* nie zostanie określona, to polecenie cmdlet będzie pobierać wszystkie linki skojarzone z określoną prywatną strefą DNS w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="d1477-120">If you do not specify a value for the *Name* parameter, this cmdlet gets all links associated with the specified Private DNS zone in the specified resource group.</span></span>

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

### <span data-ttu-id="d1477-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1477-121">-ResourceGroupName</span></span>
<span data-ttu-id="d1477-122">Określa nazwę grupy zasobów zawierającej łącze sieci wirtualnej do pobrania.</span><span class="sxs-lookup"><span data-stu-id="d1477-122">Specifies the name of the resource group that contains the virtual network link to get.</span></span>

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

### <span data-ttu-id="d1477-123">-Nazwa_strefy</span><span class="sxs-lookup"><span data-stu-id="d1477-123">-ZoneName</span></span>
<span data-ttu-id="d1477-124">Określa nazwę prywatnej strefy DNS, z którą jest połączony link sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d1477-124">Specifies the name of the Private DNS zone that the virtual network link is linked to.</span></span>


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

### <span data-ttu-id="d1477-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1477-125">CommonParameters</span></span>
<span data-ttu-id="d1477-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1477-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1477-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1477-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1477-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d1477-128">INPUTS</span></span>

### <span data-ttu-id="d1477-129">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="d1477-129">None</span></span>

## <span data-ttu-id="d1477-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d1477-130">OUTPUTS</span></span>

### <span data-ttu-id="d1477-131">Microsoft. Azure. Commands. PrivateDns. models. PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="d1477-131">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="d1477-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d1477-132">NOTES</span></span>

## <span data-ttu-id="d1477-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d1477-133">RELATED LINKS</span></span>

[<span data-ttu-id="d1477-134">Nowe — AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="d1477-134">New-AzPrivateDnsVirtualNetworkLink</span></span>](./New-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="d1477-135">Remove-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="d1477-135">Remove-AzPrivateDnsVirtualNetworkLink</span></span>](./Remove-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="d1477-136">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="d1477-136">Set-AzPrivateDnsVirtualNetworkLink</span></span>](./Set-AzPrivateDnsVirtualNetworkLink.md)
