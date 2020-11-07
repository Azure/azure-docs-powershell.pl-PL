---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/new-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/New-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/New-AzDnsZone.md
ms.openlocfilehash: 0b41ff25823e44b31c7ff7677678a332782e7615
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893150"
---
# <span data-ttu-id="1978d-101">New-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="1978d-101">New-AzDnsZone</span></span>

## <span data-ttu-id="1978d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1978d-102">SYNOPSIS</span></span>
<span data-ttu-id="1978d-103">Tworzy nową strefę DNS.</span><span class="sxs-lookup"><span data-stu-id="1978d-103">Creates a new DNS zone.</span></span>

## <span data-ttu-id="1978d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1978d-104">SYNTAX</span></span>

```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1978d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1978d-105">DESCRIPTION</span></span>
<span data-ttu-id="1978d-106">Polecenie cmdlet **New-AzDnsZone** tworzy nową strefę DNS (Domain Name System) w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="1978d-106">The **New-AzDnsZone** cmdlet creates a new Domain Name System (DNS) zone in the specified resource group.</span></span> <span data-ttu-id="1978d-107">Musisz określić unikatową nazwę strefy DNS dla parametru *name* lub polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="1978d-107">You must specify a unique DNS zone name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="1978d-108">Po utworzeniu strefy Użyj polecenia cmdlet New-AzDnsRecordSet, aby utworzyć zestaw rekordów w strefie.</span><span class="sxs-lookup"><span data-stu-id="1978d-108">After the zone is created, use the New-AzDnsRecordSet cmdlet to create record sets in the zone.</span></span>

<span data-ttu-id="1978d-109">Za pomocą zmiennej *Confirm* i $ConfirmPreference programu Windows PowerShell można kontrolować, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1978d-109">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="1978d-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1978d-110">EXAMPLES</span></span>

### <span data-ttu-id="1978d-111">Przykład 1: Tworzenie strefy DNS</span><span class="sxs-lookup"><span data-stu-id="1978d-111">Example 1: Create a DNS zone</span></span>
```
PS C:\>$Zone = New-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="1978d-112">To polecenie tworzy nową strefę DNS o nazwie myzone.com w określonej grupie zasobów, a następnie zapisuje ją w zmiennej $Zone.</span><span class="sxs-lookup"><span data-stu-id="1978d-112">This command creates a new DNS zone named myzone.com in the specified resource group, and then stores it in the $Zone variable.</span></span>

## <span data-ttu-id="1978d-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1978d-113">PARAMETERS</span></span>

### <span data-ttu-id="1978d-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1978d-114">-Name</span></span>
<span data-ttu-id="1978d-115">Określa nazwę strefy DNS do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="1978d-115">Specifies the name of the DNS zone to create.</span></span>

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

### <span data-ttu-id="1978d-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1978d-116">-ResourceGroupName</span></span>
<span data-ttu-id="1978d-117">Określa grupę zasobów, w której ma zostać utworzona strefa.</span><span class="sxs-lookup"><span data-stu-id="1978d-117">Specifies the resource group in which to create the zone.</span></span>

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

### <span data-ttu-id="1978d-118">-Tag</span><span class="sxs-lookup"><span data-stu-id="1978d-118">-Tag</span></span>
<span data-ttu-id="1978d-119">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="1978d-119">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="1978d-120">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="1978d-120">For example:</span></span>

<span data-ttu-id="1978d-121">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="1978d-121">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1978d-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1978d-122">-Confirm</span></span>
<span data-ttu-id="1978d-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1978d-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1978d-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1978d-124">-WhatIf</span></span>
<span data-ttu-id="1978d-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1978d-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1978d-126">Polecenie cmdlet nie jest uruchamiane. Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1978d-126">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1978d-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1978d-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1978d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1978d-128">CommonParameters</span></span>
<span data-ttu-id="1978d-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1978d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1978d-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1978d-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1978d-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1978d-131">INPUTS</span></span>

### <span data-ttu-id="1978d-132">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="1978d-132">None</span></span>

<span data-ttu-id="1978d-133">Nie możesz popotokować danych wejściowych tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1978d-133">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="1978d-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1978d-134">OUTPUTS</span></span>

### <span data-ttu-id="1978d-135">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="1978d-135">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

<span data-ttu-id="1978d-136">To polecenie cmdlet zwraca obiekt Microsoft. Azure. Commands. DNS. DnsZone reprezentujący nową strefę DNS.</span><span class="sxs-lookup"><span data-stu-id="1978d-136">This cmdlet returns a Microsoft.Azure.Commands.Dns.DnsZone object that represents the new DNS zone.</span></span>

## <span data-ttu-id="1978d-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1978d-137">NOTES</span></span>
<span data-ttu-id="1978d-138">Za pomocą parametru *Confirm* można kontrolować, czy to polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1978d-138">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="1978d-139">Domyślnie polecenie cmdlet monituje o potwierdzenie, jeśli zmienna $ConfirmPreference Windows PowerShell ma wartość średnią lub niższą.</span><span class="sxs-lookup"><span data-stu-id="1978d-139">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="1978d-140">Jeśli określisz pozycję *Potwierdź* lub *Potwierdź: $true* , to polecenie cmdlet wyświetli monit o potwierdzenie przed jego uruchomieniem.</span><span class="sxs-lookup"><span data-stu-id="1978d-140">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="1978d-141">Jeśli określisz pozycję *Confirm (Potwierdź): $false* , polecenie cmdlet nie monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1978d-141">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="1978d-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1978d-142">RELATED LINKS</span></span>

[<span data-ttu-id="1978d-143">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="1978d-143">Get-AzDnsZone</span></span>](./Get-AzDnsZone.md)

[<span data-ttu-id="1978d-144">Nowe — AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="1978d-144">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="1978d-145">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="1978d-145">Remove-AzDnsZone</span></span>](./Remove-AzDnsZone.md)