---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8b71c522a8d4dc006428ca2a400160a0ce7ce68b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898928"
---
# <span data-ttu-id="383a3-101">Get-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="383a3-101">Get-AzureRmDnsZone</span></span>

## <span data-ttu-id="383a3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="383a3-102">SYNOPSIS</span></span>
<span data-ttu-id="383a3-103">Pobiera strefę DNS.</span><span class="sxs-lookup"><span data-stu-id="383a3-103">Gets a DNS zone.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="383a3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="383a3-104">SYNTAX</span></span>

### <span data-ttu-id="383a3-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="383a3-105">Default (Default)</span></span>
```
Get-AzureRmDnsZone [<CommonParameters>]
```

### <span data-ttu-id="383a3-106">Przysourceing</span><span class="sxs-lookup"><span data-stu-id="383a3-106">ResourceGroup</span></span>
```
Get-AzureRmDnsZone [-Name <String>] -ResourceGroupName <String> [<CommonParameters>]
```

## <span data-ttu-id="383a3-107">Opis</span><span class="sxs-lookup"><span data-stu-id="383a3-107">DESCRIPTION</span></span>
<span data-ttu-id="383a3-108">Polecenie cmdlet **Get-AzureRmDnsZone** pobiera strefę DNS (Domain Name System) z określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="383a3-108">The **Get-AzureRmDnsZone** cmdlet gets a Domain Name System (DNS) zone from the specified resource group.</span></span>
<span data-ttu-id="383a3-109">Jeśli określisz parametr *name* , zwracany jest jeden obiekt **dnsZone** .</span><span class="sxs-lookup"><span data-stu-id="383a3-109">If you specify the *Name* parameter, a single **DnsZone** object is returned.</span></span>
<span data-ttu-id="383a3-110">Jeśli parametr *name* nie zostanie określony, zostanie zwrócona tablica zawierająca wszystkie strefy w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="383a3-110">If you do not specify the *Name* parameter, an array containing all of the zones in the specified resource group is returned.</span></span>
<span data-ttu-id="383a3-111">Za pomocą obiektu **dnsZone** można aktualizować strefę, na przykład dodawać do niej obiekty **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="383a3-111">You can use the **DnsZone** object to update the zone, for example you can add **RecordSet** objects to it.</span></span>

## <span data-ttu-id="383a3-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="383a3-112">EXAMPLES</span></span>

### <span data-ttu-id="383a3-113">Przykład 1: uzyskiwanie strefy</span><span class="sxs-lookup"><span data-stu-id="383a3-113">Example 1: Get a zone</span></span>
```
PS C:\> $Zone = Get-AzureRmDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"
```

<span data-ttu-id="383a3-114">W tym przykładzie otrzymano strefę DNS o nazwie myzone.com z określonej grupy zasobów, a następnie zapisuje ją w zmiennej $Zone.</span><span class="sxs-lookup"><span data-stu-id="383a3-114">This example gets the DNS zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="383a3-115">Przykład 2: pobieranie wszystkich stref w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="383a3-115">Example 2: Get all of the zones in a resource group</span></span>
```
PS C:\> $Zones = Get-AzureRmDnsZone -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="383a3-116">W tym przykładzie są pobierane wszystkie strefy DNS w określonej grupie zasobów, a następnie są one przechowywane w zmiennej $Zones.</span><span class="sxs-lookup"><span data-stu-id="383a3-116">This example gets all of the DNS zones in the specified resource group, and then stores it in the $Zones variable.</span></span>

### <span data-ttu-id="383a3-117">Przykład 3: uzyskiwanie wszystkich stref w ramach abonamentu</span><span class="sxs-lookup"><span data-stu-id="383a3-117">Example 3: Get all of the zones in a subscription</span></span>
```
PS C:\> $Zones = Get-AzureRmDnsZone
```

<span data-ttu-id="383a3-118">W tym przykładzie są pobierane wszystkie strefy DNS w bieżącej subskrypcji platformy Azure, a następnie są one przechowywane w zmiennej $Zones.</span><span class="sxs-lookup"><span data-stu-id="383a3-118">This example gets all of the DNS zones in the current Azure subscription, and then stores them in the $Zones variable.</span></span>

## <span data-ttu-id="383a3-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="383a3-119">PARAMETERS</span></span>

### <span data-ttu-id="383a3-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="383a3-120">-Name</span></span>
<span data-ttu-id="383a3-121">Określa nazwę strefy DNS do pobrania.</span><span class="sxs-lookup"><span data-stu-id="383a3-121">Specifies the name of the DNS zone to get.</span></span>

<span data-ttu-id="383a3-122">Jeśli wartość parametru *name* nie zostanie określona, to polecenie cmdlet będzie pobierać wszystkie strefy DNS w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="383a3-122">If you do not specify a value for the *Name* parameter, this cmdlet gets all DNS zones in the specified resource group.</span></span>
<span data-ttu-id="383a3-123">W przypadku pominięcia parametru *ResourceGroupName* to polecenie cmdlet umożliwia pobieranie wszystkich stref DNS w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="383a3-123">If you also omit the *ResourceGroupName* parameter, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroup
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="383a3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="383a3-124">-ResourceGroupName</span></span>
<span data-ttu-id="383a3-125">Określa nazwę grupy zasobów zawierającej strefę DNS do pobrania.</span><span class="sxs-lookup"><span data-stu-id="383a3-125">Specifies the name of the resource group that contains the DNS zone to get.</span></span>

<span data-ttu-id="383a3-126">Jeśli nie określisz *ResourceGroupName* , musisz także pominąć parametr *name (nazwa* ).</span><span class="sxs-lookup"><span data-stu-id="383a3-126">If you do not specify the *ResourceGroupName* , then you must also omit the *Name* parameter.</span></span>
<span data-ttu-id="383a3-127">W tym przypadku to polecenie cmdlet umożliwia pobieranie wszystkich stref DNS w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="383a3-127">In this case, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="383a3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="383a3-128">CommonParameters</span></span>
<span data-ttu-id="383a3-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="383a3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="383a3-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="383a3-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="383a3-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="383a3-131">INPUTS</span></span>

### <span data-ttu-id="383a3-132">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="383a3-132">None</span></span>
<span data-ttu-id="383a3-133">To polecenie cmdlet nie umożliwia wprowadzania danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="383a3-133">This cmdlet does not allow you to pipe input.</span></span>

## <span data-ttu-id="383a3-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="383a3-134">OUTPUTS</span></span>

### <span data-ttu-id="383a3-135">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="383a3-135">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="383a3-136">To polecenie cmdlet zwraca obiekt reprezentujący strefę DNS.</span><span class="sxs-lookup"><span data-stu-id="383a3-136">This cmdlet returns an object that represents the DNS zone.</span></span>
<span data-ttu-id="383a3-137">Jeśli nie określono nazwy strefy, zwracana jest tablica obiektów strefy.</span><span class="sxs-lookup"><span data-stu-id="383a3-137">If the zone name is not specified, an array of zone objects is returned.</span></span>

## <span data-ttu-id="383a3-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="383a3-138">NOTES</span></span>

## <span data-ttu-id="383a3-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="383a3-139">RELATED LINKS</span></span>

[<span data-ttu-id="383a3-140">Nowe — AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="383a3-140">New-AzureRmDnsZone</span></span>](./New-AzureRmDnsZone.md)

[<span data-ttu-id="383a3-141">Remove-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="383a3-141">Remove-AzureRmDnsZone</span></span>](./Remove-AzureRmDnsZone.md)

[<span data-ttu-id="383a3-142">Set-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="383a3-142">Set-AzureRmDnsZone</span></span>](./Set-AzureRmDnsZone.md)
