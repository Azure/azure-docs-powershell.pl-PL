---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/get-azprivatednszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsZone.md
ms.openlocfilehash: 659281d1f78ea984a3db30817d15a6e92f31cbe2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708751"
---
# <span data-ttu-id="11ff5-101">Get-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="11ff5-101">Get-AzPrivateDnsZone</span></span>

## <span data-ttu-id="11ff5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="11ff5-102">SYNOPSIS</span></span>
<span data-ttu-id="11ff5-103">Pobiera prywatną strefę DNS.</span><span class="sxs-lookup"><span data-stu-id="11ff5-103">Gets a Private DNS zone.</span></span>

## <span data-ttu-id="11ff5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="11ff5-104">SYNTAX</span></span>

```
Get-AzPrivateDnsZone [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="11ff5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="11ff5-105">DESCRIPTION</span></span>
<span data-ttu-id="11ff5-106">Polecenie cmdlet **Get-AzPrivateDnsZone** pobiera prywatną strefę DNS (Domain Name System) z określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="11ff5-106">The **Get-AzPrivateDnsZone** cmdlet gets a Private Domain Name System (DNS) zone from the specified resource group.</span></span>
<span data-ttu-id="11ff5-107">Jeśli określisz parametr *name* , zwracany jest jeden obiekt **PrivateDnsZone** .</span><span class="sxs-lookup"><span data-stu-id="11ff5-107">If you specify the *Name* parameter, a single **PrivateDnsZone** object is returned.</span></span>
<span data-ttu-id="11ff5-108">Jeśli parametr *name* nie zostanie określony, zostanie zwrócona tablica zawierająca wszystkie strefy w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="11ff5-108">If you do not specify the *Name* parameter, an array containing all of the zones in the specified resource group is returned.</span></span>
<span data-ttu-id="11ff5-109">Za pomocą obiektu **PrivateDnsZone** można aktualizować strefę, na przykład dodawać do niej obiekty **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="11ff5-109">You can use the **PrivateDnsZone** object to update the zone, for example you can add **RecordSet** objects to it.</span></span>

## <span data-ttu-id="11ff5-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="11ff5-110">EXAMPLES</span></span>

### <span data-ttu-id="11ff5-111">Przykład 1: uzyskiwanie strefy</span><span class="sxs-lookup"><span data-stu-id="11ff5-111">Example 1: Get a zone</span></span>
```
PS C:\> $Zone = Get-AzPrivateDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"

This example gets the Private DNS zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.
$Zone looks something like this: 

Name                          : myzone.com
ResourceId:                   : "/subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/PrivateZones/myzone.com"
ResourceGroupName             : MyResourceGroup
Location                      : 
Etag                          : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                          : {}
NumberOfRecordSets            : 1
MaxNumberOfRecordSets         : 5000
```

### <span data-ttu-id="11ff5-112">Przykład 2: pobieranie wszystkich stref w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="11ff5-112">Example 2: Get all of the zones in a resource group</span></span>
```
PS C:\> $Zones = Get-AzPrivateDnsZone -ResourceGroupName "MyResourceGroup"

Name                  : zone1.com
ResourceId            : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Micros
                        oft.Network/privateDnsZones/zone1.com
ResourceGroupName     : MyResourceGroup
Location              :
Etag                  : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                  :
NumberOfRecordSets    : 1
MaxNumberOfRecordSets : 5000

Name                  : zone2.com
ResourceId            : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Micros
                        oft.Network/privateDnsZones/zone2.com
ResourceGroupName     : MyResourceGroup
Location              :
Etag                  : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                  :
NumberOfRecordSets    : 1
MaxNumberOfRecordSets : 5000
```

<span data-ttu-id="11ff5-113">W tym przykładzie są pobierane wszystkie prywatne strefy DNS w określonej grupie zasobów, a następnie są one przechowywane w zmiennej $Zones.</span><span class="sxs-lookup"><span data-stu-id="11ff5-113">This example gets all of the Private DNS zones in the specified resource group, and then stores it in the $Zones variable.</span></span>

### <span data-ttu-id="11ff5-114">Przykład 3: uzyskiwanie wszystkich stref w ramach abonamentu</span><span class="sxs-lookup"><span data-stu-id="11ff5-114">Example 3: Get all of the zones in a subscription</span></span>
```
PS C:\> $Zones = Get-AzPrivateDnsZone

Name                  : zone1.com
ResourceId            : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup1/providers/Micros
                        oft.Network/privateDnsZones/zone1.com
ResourceGroupName     : MyResourceGroup1
Location              :
Etag                  : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                  :
NumberOfRecordSets    : 1
MaxNumberOfRecordSets : 5000

Name                  : zone2.com
ResourceId            : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup2/providers/Micros
                        oft.Network/privateDnsZones/zone2.com
ResourceGroupName     : MyResourceGroup2
Location              :
Etag                  : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                  :
NumberOfRecordSets    : 1
MaxNumberOfRecordSets : 5000
```

<span data-ttu-id="11ff5-115">W tym przykładzie są pobierane wszystkie prywatne strefy DNS w bieżącej subskrypcji platformy Azure, a następnie są one przechowywane w zmiennej $Zones.</span><span class="sxs-lookup"><span data-stu-id="11ff5-115">This example gets all of the Private DNS zones in the current Azure subscription, and then stores them in the $Zones variable.</span></span>

## <span data-ttu-id="11ff5-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="11ff5-116">PARAMETERS</span></span>

### <span data-ttu-id="11ff5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11ff5-117">-DefaultProfile</span></span>
<span data-ttu-id="11ff5-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="11ff5-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="11ff5-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="11ff5-119">-Name</span></span>
<span data-ttu-id="11ff5-120">Określa nazwę prywatnej strefy DNS do pobrania.</span><span class="sxs-lookup"><span data-stu-id="11ff5-120">Specifies the name of the Private DNS zone to get.</span></span>
<span data-ttu-id="11ff5-121">Jeśli wartość parametru *name* nie zostanie określona, to polecenie cmdlet spowoduje wyświetlenie wszystkich prywatnych stref DNS w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="11ff5-121">If you do not specify a value for the *Name* parameter, this cmdlet gets all Private DNS zones in the specified resource group.</span></span>
<span data-ttu-id="11ff5-122">W przypadku pominięcia parametru *ResourceGroupName* to polecenie cmdlet umożliwia pobieranie wszystkich prywatnych stref DNS w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="11ff5-122">If you also omit the *ResourceGroupName* parameter, this cmdlet gets all Private DNS zones in the current Azure subscription.</span></span>

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

### <span data-ttu-id="11ff5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11ff5-123">-ResourceGroupName</span></span>
<span data-ttu-id="11ff5-124">Określa nazwę grupy zasobów zawierającej prywatną strefę DNS do pobrania.</span><span class="sxs-lookup"><span data-stu-id="11ff5-124">Specifies the name of the resource group that contains the Private DNS zone to get.</span></span>
<span data-ttu-id="11ff5-125">Jeśli nie określisz *ResourceGroupName* , musisz także pominąć parametr *name (nazwa* ).</span><span class="sxs-lookup"><span data-stu-id="11ff5-125">If you do not specify the *ResourceGroupName* , then you must also omit the *Name* parameter.</span></span>
<span data-ttu-id="11ff5-126">W tym przypadku to polecenie cmdlet umożliwia pobieranie wszystkich prywatnych stref DNS w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="11ff5-126">In this case, this cmdlet gets all Private DNS zones in the current Azure subscription.</span></span>

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

### <span data-ttu-id="11ff5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11ff5-127">CommonParameters</span></span>
<span data-ttu-id="11ff5-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11ff5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11ff5-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11ff5-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11ff5-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="11ff5-130">INPUTS</span></span>

### <span data-ttu-id="11ff5-131">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="11ff5-131">None</span></span>

## <span data-ttu-id="11ff5-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="11ff5-132">OUTPUTS</span></span>

### <span data-ttu-id="11ff5-133">Microsoft. Azure. Commands. PrivateDns. models. PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="11ff5-133">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

## <span data-ttu-id="11ff5-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="11ff5-134">NOTES</span></span>

## <span data-ttu-id="11ff5-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="11ff5-135">RELATED LINKS</span></span>

[<span data-ttu-id="11ff5-136">Nowe — AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="11ff5-136">New-AzPrivateDnsZone</span></span>](./New-AzPrivateDnsZone.md)

[<span data-ttu-id="11ff5-137">Remove-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="11ff5-137">Remove-AzPrivateDnsZone</span></span>](./Remove-AzPrivateDnsZone.md)

[<span data-ttu-id="11ff5-138">Set-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="11ff5-138">Set-AzPrivateDnsZone</span></span>](./Set-AzPrivateDnsZone.md)