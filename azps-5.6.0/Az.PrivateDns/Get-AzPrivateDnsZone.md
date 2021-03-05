---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/powershell/module/az.privatedns/get-azprivatednszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsZone.md
ms.openlocfilehash: 6cc89d9e5fad05bc26c824221831fcebcf833b21
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996017"
---
# <span data-ttu-id="780f3-101">Get-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="780f3-101">Get-AzPrivateDnsZone</span></span>

## <span data-ttu-id="780f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="780f3-102">SYNOPSIS</span></span>
<span data-ttu-id="780f3-103">Pobiera prywatną strefę DNS.</span><span class="sxs-lookup"><span data-stu-id="780f3-103">Gets a Private DNS zone.</span></span>

## <span data-ttu-id="780f3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="780f3-104">SYNTAX</span></span>

```
Get-AzPrivateDnsZone [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="780f3-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="780f3-105">DESCRIPTION</span></span>
<span data-ttu-id="780f3-106">Polecenie **cmdlet Get-AzPrivateDnsZone** pobiera strefę DNS (Private Domain Name System) z określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="780f3-106">The **Get-AzPrivateDnsZone** cmdlet gets a Private Domain Name System (DNS) zone from the specified resource group.</span></span>
<span data-ttu-id="780f3-107">Jeśli określisz parametr *Name,* zostanie zwrócony jeden obiekt **PrivateDnsZone.**</span><span class="sxs-lookup"><span data-stu-id="780f3-107">If you specify the *Name* parameter, a single **PrivateDnsZone** object is returned.</span></span>
<span data-ttu-id="780f3-108">Jeśli parametr Name  nie zostanie określony, zostanie zwrócona tablica zawierająca wszystkie strefy w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="780f3-108">If you do not specify the *Name* parameter, an array containing all of the zones in the specified resource group is returned.</span></span>
<span data-ttu-id="780f3-109">Za pomocą obiektu **PrivateDnsZone** możesz zaktualizować strefę, na przykład możesz dodać do niego obiekty **RecordSet.**</span><span class="sxs-lookup"><span data-stu-id="780f3-109">You can use the **PrivateDnsZone** object to update the zone, for example you can add **RecordSet** objects to it.</span></span>

## <span data-ttu-id="780f3-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="780f3-110">EXAMPLES</span></span>

### <span data-ttu-id="780f3-111">Przykład 1. Uzyskiwanie strefy</span><span class="sxs-lookup"><span data-stu-id="780f3-111">Example 1: Get a zone</span></span>
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

### <span data-ttu-id="780f3-112">Przykład 2. Uzyskiwanie wszystkich stref w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="780f3-112">Example 2: Get all of the zones in a resource group</span></span>
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

<span data-ttu-id="780f3-113">W tym przykładzie wszystkie prywatne strefy DNS w określonej grupie zasobów są przechowywane w $Zones danych.</span><span class="sxs-lookup"><span data-stu-id="780f3-113">This example gets all of the Private DNS zones in the specified resource group, and then stores it in the $Zones variable.</span></span>

### <span data-ttu-id="780f3-114">Przykład 3. Uzyskiwanie wszystkich stref w subskrypcji</span><span class="sxs-lookup"><span data-stu-id="780f3-114">Example 3: Get all of the zones in a subscription</span></span>
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

<span data-ttu-id="780f3-115">W tym przykładzie wszystkie prywatne strefy DNS w bieżącej subskrypcji platformy Azure są przechowywane w $Zones danych.</span><span class="sxs-lookup"><span data-stu-id="780f3-115">This example gets all of the Private DNS zones in the current Azure subscription, and then stores them in the $Zones variable.</span></span>

## <span data-ttu-id="780f3-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="780f3-116">PARAMETERS</span></span>

### <span data-ttu-id="780f3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="780f3-117">-DefaultProfile</span></span>
<span data-ttu-id="780f3-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="780f3-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="780f3-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="780f3-119">-Name</span></span>
<span data-ttu-id="780f3-120">Określa nazwę prywatnej strefy DNS do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="780f3-120">Specifies the name of the Private DNS zone to get.</span></span>
<span data-ttu-id="780f3-121">Jeśli nie określisz wartości dla *parametru Name,* to polecenie cmdlet pobiera wszystkie prywatne strefy DNS w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="780f3-121">If you do not specify a value for the *Name* parameter, this cmdlet gets all Private DNS zones in the specified resource group.</span></span>
<span data-ttu-id="780f3-122">Jeśli parametr *ResourceGroupName* zostanie pominięty, to polecenie cmdlet pobiera wszystkie prywatne strefy DNS w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="780f3-122">If you also omit the *ResourceGroupName* parameter, this cmdlet gets all Private DNS zones in the current Azure subscription.</span></span>

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

### <span data-ttu-id="780f3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="780f3-123">-ResourceGroupName</span></span>
<span data-ttu-id="780f3-124">Określa nazwę grupy zasobów, która zawiera prywatną strefę DNS do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="780f3-124">Specifies the name of the resource group that contains the Private DNS zone to get.</span></span>
<span data-ttu-id="780f3-125">Jeśli nie określisz *parametru ResourceGroupName,* musisz również pominąć *parametr Name.*</span><span class="sxs-lookup"><span data-stu-id="780f3-125">If you do not specify the *ResourceGroupName*, then you must also omit the *Name* parameter.</span></span>
<span data-ttu-id="780f3-126">W tym przypadku to polecenie cmdlet pobiera wszystkie prywatne strefy DNS w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="780f3-126">In this case, this cmdlet gets all Private DNS zones in the current Azure subscription.</span></span>

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

### <span data-ttu-id="780f3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="780f3-127">CommonParameters</span></span>
<span data-ttu-id="780f3-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="780f3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="780f3-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="780f3-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="780f3-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="780f3-130">INPUTS</span></span>

### <span data-ttu-id="780f3-131">Brak</span><span class="sxs-lookup"><span data-stu-id="780f3-131">None</span></span>

## <span data-ttu-id="780f3-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="780f3-132">OUTPUTS</span></span>

### <span data-ttu-id="780f3-133">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="780f3-133">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

## <span data-ttu-id="780f3-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="780f3-134">NOTES</span></span>

## <span data-ttu-id="780f3-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="780f3-135">RELATED LINKS</span></span>

[<span data-ttu-id="780f3-136">New-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="780f3-136">New-AzPrivateDnsZone</span></span>](./New-AzPrivateDnsZone.md)

[<span data-ttu-id="780f3-137">Remove-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="780f3-137">Remove-AzPrivateDnsZone</span></span>](./Remove-AzPrivateDnsZone.md)

[<span data-ttu-id="780f3-138">Set-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="780f3-138">Set-AzPrivateDnsZone</span></span>](./Set-AzPrivateDnsZone.md)
