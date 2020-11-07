---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/get-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsZone.md
ms.openlocfilehash: 9be5ca678b690400e044b9627fd455ea2cbc29c4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705526"
---
# <span data-ttu-id="15219-101">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="15219-101">Get-AzDnsZone</span></span>

## <span data-ttu-id="15219-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="15219-102">SYNOPSIS</span></span>
<span data-ttu-id="15219-103">Pobiera strefę DNS.</span><span class="sxs-lookup"><span data-stu-id="15219-103">Gets a DNS zone.</span></span>

## <span data-ttu-id="15219-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="15219-104">SYNTAX</span></span>

### <span data-ttu-id="15219-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="15219-105">Default (Default)</span></span>
```
Get-AzDnsZone [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15219-106">Przysourceing</span><span class="sxs-lookup"><span data-stu-id="15219-106">ResourceGroup</span></span>
```
Get-AzDnsZone [-Name <String>] -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="15219-107">Opis</span><span class="sxs-lookup"><span data-stu-id="15219-107">DESCRIPTION</span></span>
<span data-ttu-id="15219-108">Polecenie cmdlet **Get-AzDnsZone** pobiera strefę DNS (Domain Name System) z określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="15219-108">The **Get-AzDnsZone** cmdlet gets a Domain Name System (DNS) zone from the specified resource group.</span></span>
<span data-ttu-id="15219-109">Jeśli określisz parametr *name* , zwracany jest jeden obiekt **dnsZone** .</span><span class="sxs-lookup"><span data-stu-id="15219-109">If you specify the *Name* parameter, a single **DnsZone** object is returned.</span></span>
<span data-ttu-id="15219-110">Jeśli parametr *name* nie zostanie określony, zostanie zwrócona tablica zawierająca wszystkie strefy w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="15219-110">If you do not specify the *Name* parameter, an array containing all of the zones in the specified resource group is returned.</span></span>
<span data-ttu-id="15219-111">Za pomocą obiektu **dnsZone** można aktualizować strefę, na przykład dodawać do niej obiekty **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="15219-111">You can use the **DnsZone** object to update the zone, for example you can add **RecordSet** objects to it.</span></span>

## <span data-ttu-id="15219-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="15219-112">EXAMPLES</span></span>

### <span data-ttu-id="15219-113">Przykład 1: uzyskiwanie strefy</span><span class="sxs-lookup"><span data-stu-id="15219-113">Example 1: Get a zone</span></span>
```
PS C:\> $Zone = Get-AzDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"
```

<span data-ttu-id="15219-114">W tym przykładzie otrzymano strefę DNS o nazwie myzone.com z określonej grupy zasobów, a następnie zapisuje ją w zmiennej $Zone.</span><span class="sxs-lookup"><span data-stu-id="15219-114">This example gets the DNS zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="15219-115">Przykład 2: pobieranie wszystkich stref w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="15219-115">Example 2: Get all of the zones in a resource group</span></span>
```
PS C:\> $Zones = Get-AzDnsZone -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="15219-116">W tym przykładzie są pobierane wszystkie strefy DNS w określonej grupie zasobów, a następnie są one przechowywane w zmiennej $Zones.</span><span class="sxs-lookup"><span data-stu-id="15219-116">This example gets all of the DNS zones in the specified resource group, and then stores it in the $Zones variable.</span></span>

### <span data-ttu-id="15219-117">Przykład 3: uzyskiwanie wszystkich stref w ramach abonamentu</span><span class="sxs-lookup"><span data-stu-id="15219-117">Example 3: Get all of the zones in a subscription</span></span>
```
PS C:\> $Zones = Get-AzDnsZone
```

<span data-ttu-id="15219-118">W tym przykładzie są pobierane wszystkie strefy DNS w bieżącej subskrypcji platformy Azure, a następnie są one przechowywane w zmiennej $Zones.</span><span class="sxs-lookup"><span data-stu-id="15219-118">This example gets all of the DNS zones in the current Azure subscription, and then stores them in the $Zones variable.</span></span>

## <span data-ttu-id="15219-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="15219-119">PARAMETERS</span></span>

### <span data-ttu-id="15219-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15219-120">-DefaultProfile</span></span>
<span data-ttu-id="15219-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="15219-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="15219-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="15219-122">-Name</span></span>
<span data-ttu-id="15219-123">Określa nazwę strefy DNS do pobrania.</span><span class="sxs-lookup"><span data-stu-id="15219-123">Specifies the name of the DNS zone to get.</span></span>
<span data-ttu-id="15219-124">Jeśli wartość parametru *name* nie zostanie określona, to polecenie cmdlet będzie pobierać wszystkie strefy DNS w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="15219-124">If you do not specify a value for the *Name* parameter, this cmdlet gets all DNS zones in the specified resource group.</span></span>
<span data-ttu-id="15219-125">W przypadku pominięcia parametru *ResourceGroupName* to polecenie cmdlet umożliwia pobieranie wszystkich stref DNS w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="15219-125">If you also omit the *ResourceGroupName* parameter, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15219-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15219-126">-ResourceGroupName</span></span>
<span data-ttu-id="15219-127">Określa nazwę grupy zasobów zawierającej strefę DNS do pobrania.</span><span class="sxs-lookup"><span data-stu-id="15219-127">Specifies the name of the resource group that contains the DNS zone to get.</span></span>
<span data-ttu-id="15219-128">Jeśli nie określisz *ResourceGroupName* , musisz także pominąć parametr *name (nazwa* ).</span><span class="sxs-lookup"><span data-stu-id="15219-128">If you do not specify the *ResourceGroupName* , then you must also omit the *Name* parameter.</span></span>
<span data-ttu-id="15219-129">W tym przypadku to polecenie cmdlet umożliwia pobieranie wszystkich stref DNS w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="15219-129">In this case, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15219-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15219-130">CommonParameters</span></span>
<span data-ttu-id="15219-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15219-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15219-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15219-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15219-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="15219-133">INPUTS</span></span>

### <span data-ttu-id="15219-134">System. String</span><span class="sxs-lookup"><span data-stu-id="15219-134">System.String</span></span>

## <span data-ttu-id="15219-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="15219-135">OUTPUTS</span></span>

### <span data-ttu-id="15219-136">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="15219-136">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="15219-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="15219-137">NOTES</span></span>

## <span data-ttu-id="15219-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="15219-138">RELATED LINKS</span></span>

[<span data-ttu-id="15219-139">Nowe — AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="15219-139">New-AzDnsZone</span></span>](./New-AzDnsZone.md)

[<span data-ttu-id="15219-140">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="15219-140">Remove-AzDnsZone</span></span>](./Remove-AzDnsZone.md)

[<span data-ttu-id="15219-141">Set-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="15219-141">Set-AzDnsZone</span></span>](./Set-AzDnsZone.md)
