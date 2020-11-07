---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/get-azurermdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Get-AzureRmDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Get-AzureRmDnsZone.md
ms.openlocfilehash: d25cca457adb70398d29b1b2a8044ac14af893db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717752"
---
# <span data-ttu-id="1876e-101">Get-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="1876e-101">Get-AzureRmDnsZone</span></span>

## <span data-ttu-id="1876e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1876e-102">SYNOPSIS</span></span>
<span data-ttu-id="1876e-103">Pobiera strefę DNS.</span><span class="sxs-lookup"><span data-stu-id="1876e-103">Gets a DNS zone.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1876e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1876e-104">SYNTAX</span></span>

### <span data-ttu-id="1876e-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="1876e-105">Default (Default)</span></span>
```
Get-AzureRmDnsZone [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1876e-106">Przysourceing</span><span class="sxs-lookup"><span data-stu-id="1876e-106">ResourceGroup</span></span>
```
Get-AzureRmDnsZone [-Name <String>] -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1876e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="1876e-107">DESCRIPTION</span></span>
<span data-ttu-id="1876e-108">Polecenie cmdlet **Get-AzureRmDnsZone** pobiera strefę DNS (Domain Name System) z określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1876e-108">The **Get-AzureRmDnsZone** cmdlet gets a Domain Name System (DNS) zone from the specified resource group.</span></span>
<span data-ttu-id="1876e-109">Jeśli określisz parametr *name* , zwracany jest jeden obiekt **dnsZone** .</span><span class="sxs-lookup"><span data-stu-id="1876e-109">If you specify the *Name* parameter, a single **DnsZone** object is returned.</span></span>
<span data-ttu-id="1876e-110">Jeśli parametr *name* nie zostanie określony, zostanie zwrócona tablica zawierająca wszystkie strefy w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="1876e-110">If you do not specify the *Name* parameter, an array containing all of the zones in the specified resource group is returned.</span></span>
<span data-ttu-id="1876e-111">Za pomocą obiektu **dnsZone** można aktualizować strefę, na przykład dodawać do niej obiekty **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="1876e-111">You can use the **DnsZone** object to update the zone, for example you can add **RecordSet** objects to it.</span></span>

## <span data-ttu-id="1876e-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1876e-112">EXAMPLES</span></span>

### <span data-ttu-id="1876e-113">Przykład 1: uzyskiwanie strefy</span><span class="sxs-lookup"><span data-stu-id="1876e-113">Example 1: Get a zone</span></span>
```
PS C:\> $Zone = Get-AzureRmDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"
```

<span data-ttu-id="1876e-114">W tym przykładzie otrzymano strefę DNS o nazwie myzone.com z określonej grupy zasobów, a następnie zapisuje ją w zmiennej $Zone.</span><span class="sxs-lookup"><span data-stu-id="1876e-114">This example gets the DNS zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="1876e-115">Przykład 2: pobieranie wszystkich stref w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="1876e-115">Example 2: Get all of the zones in a resource group</span></span>
```
PS C:\> $Zones = Get-AzureRmDnsZone -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="1876e-116">W tym przykładzie są pobierane wszystkie strefy DNS w określonej grupie zasobów, a następnie są one przechowywane w zmiennej $Zones.</span><span class="sxs-lookup"><span data-stu-id="1876e-116">This example gets all of the DNS zones in the specified resource group, and then stores it in the $Zones variable.</span></span>

### <span data-ttu-id="1876e-117">Przykład 3: uzyskiwanie wszystkich stref w ramach abonamentu</span><span class="sxs-lookup"><span data-stu-id="1876e-117">Example 3: Get all of the zones in a subscription</span></span>
```
PS C:\> $Zones = Get-AzureRmDnsZone
```

<span data-ttu-id="1876e-118">W tym przykładzie są pobierane wszystkie strefy DNS w bieżącej subskrypcji platformy Azure, a następnie są one przechowywane w zmiennej $Zones.</span><span class="sxs-lookup"><span data-stu-id="1876e-118">This example gets all of the DNS zones in the current Azure subscription, and then stores them in the $Zones variable.</span></span>

## <span data-ttu-id="1876e-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1876e-119">PARAMETERS</span></span>

### <span data-ttu-id="1876e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1876e-120">-DefaultProfile</span></span>
<span data-ttu-id="1876e-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="1876e-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1876e-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1876e-122">-Name</span></span>
<span data-ttu-id="1876e-123">Określa nazwę strefy DNS do pobrania.</span><span class="sxs-lookup"><span data-stu-id="1876e-123">Specifies the name of the DNS zone to get.</span></span>

<span data-ttu-id="1876e-124">Jeśli wartość parametru *name* nie zostanie określona, to polecenie cmdlet będzie pobierać wszystkie strefy DNS w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="1876e-124">If you do not specify a value for the *Name* parameter, this cmdlet gets all DNS zones in the specified resource group.</span></span>
<span data-ttu-id="1876e-125">W przypadku pominięcia parametru *ResourceGroupName* to polecenie cmdlet umożliwia pobieranie wszystkich stref DNS w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1876e-125">If you also omit the *ResourceGroupName* parameter, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

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

### <span data-ttu-id="1876e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1876e-126">-ResourceGroupName</span></span>
<span data-ttu-id="1876e-127">Określa nazwę grupy zasobów zawierającej strefę DNS do pobrania.</span><span class="sxs-lookup"><span data-stu-id="1876e-127">Specifies the name of the resource group that contains the DNS zone to get.</span></span>

<span data-ttu-id="1876e-128">Jeśli nie określisz *ResourceGroupName* , musisz także pominąć parametr *name (nazwa* ).</span><span class="sxs-lookup"><span data-stu-id="1876e-128">If you do not specify the *ResourceGroupName* , then you must also omit the *Name* parameter.</span></span>
<span data-ttu-id="1876e-129">W tym przypadku to polecenie cmdlet umożliwia pobieranie wszystkich stref DNS w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1876e-129">In this case, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

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

### <span data-ttu-id="1876e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1876e-130">CommonParameters</span></span>
<span data-ttu-id="1876e-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1876e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1876e-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1876e-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1876e-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1876e-133">INPUTS</span></span>

### <span data-ttu-id="1876e-134">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="1876e-134">None</span></span>
<span data-ttu-id="1876e-135">To polecenie cmdlet nie umożliwia wprowadzania danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="1876e-135">This cmdlet does not allow you to pipe input.</span></span>

## <span data-ttu-id="1876e-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1876e-136">OUTPUTS</span></span>

### <span data-ttu-id="1876e-137">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="1876e-137">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="1876e-138">To polecenie cmdlet zwraca obiekt reprezentujący strefę DNS.</span><span class="sxs-lookup"><span data-stu-id="1876e-138">This cmdlet returns an object that represents the DNS zone.</span></span>
<span data-ttu-id="1876e-139">Jeśli nie określono nazwy strefy, zwracana jest tablica obiektów strefy.</span><span class="sxs-lookup"><span data-stu-id="1876e-139">If the zone name is not specified, an array of zone objects is returned.</span></span>

## <span data-ttu-id="1876e-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1876e-140">NOTES</span></span>

## <span data-ttu-id="1876e-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1876e-141">RELATED LINKS</span></span>

[<span data-ttu-id="1876e-142">Nowe — AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="1876e-142">New-AzureRmDnsZone</span></span>](./New-AzureRmDnsZone.md)

[<span data-ttu-id="1876e-143">Remove-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="1876e-143">Remove-AzureRmDnsZone</span></span>](./Remove-AzureRmDnsZone.md)

[<span data-ttu-id="1876e-144">Set-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="1876e-144">Set-AzureRmDnsZone</span></span>](./Set-AzureRmDnsZone.md)
