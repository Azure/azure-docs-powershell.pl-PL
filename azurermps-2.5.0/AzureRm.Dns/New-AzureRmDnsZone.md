---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 46b14399d1cae624f4735111d809702cfd14180e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898510"
---
# <span data-ttu-id="45a8f-101">New-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="45a8f-101">New-AzureRmDnsZone</span></span>

## <span data-ttu-id="45a8f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="45a8f-102">SYNOPSIS</span></span>
<span data-ttu-id="45a8f-103">Tworzy nową strefę DNS.</span><span class="sxs-lookup"><span data-stu-id="45a8f-103">Creates a new DNS zone.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45a8f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="45a8f-104">SYNTAX</span></span>

```
New-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="45a8f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="45a8f-105">DESCRIPTION</span></span>
<span data-ttu-id="45a8f-106">Polecenie cmdlet **New-AzureRmDnsZone** tworzy nową strefę DNS (Domain Name System) w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="45a8f-106">The **New-AzureRmDnsZone** cmdlet creates a new Domain Name System (DNS) zone in the specified resource group.</span></span> <span data-ttu-id="45a8f-107">Musisz określić unikatową nazwę strefy DNS dla parametru *name* lub polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="45a8f-107">You must specify a unique DNS zone name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="45a8f-108">Po utworzeniu strefy Użyj polecenia cmdlet New-AzureRmDnsRecordSet, aby utworzyć zestaw rekordów w strefie.</span><span class="sxs-lookup"><span data-stu-id="45a8f-108">After the zone is created, use the New-AzureRmDnsRecordSet cmdlet to create record sets in the zone.</span></span>

<span data-ttu-id="45a8f-109">Za pomocą zmiennej *Confirm* i $ConfirmPreference programu Windows PowerShell można kontrolować, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="45a8f-109">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="45a8f-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="45a8f-110">EXAMPLES</span></span>

### <span data-ttu-id="45a8f-111">Przykład 1: Tworzenie strefy DNS</span><span class="sxs-lookup"><span data-stu-id="45a8f-111">Example 1: Create a DNS zone</span></span>
```
PS C:\>$Zone = New-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="45a8f-112">To polecenie tworzy nową strefę DNS o nazwie myzone.com w określonej grupie zasobów, a następnie zapisuje ją w zmiennej $Zone.</span><span class="sxs-lookup"><span data-stu-id="45a8f-112">This command creates a new DNS zone named myzone.com in the specified resource group, and then stores it in the $Zone variable.</span></span>

## <span data-ttu-id="45a8f-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="45a8f-113">PARAMETERS</span></span>

### <span data-ttu-id="45a8f-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="45a8f-114">-Name</span></span>
<span data-ttu-id="45a8f-115">Określa nazwę strefy DNS do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="45a8f-115">Specifies the name of the DNS zone to create.</span></span>

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

### <span data-ttu-id="45a8f-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45a8f-116">-ResourceGroupName</span></span>
<span data-ttu-id="45a8f-117">Określa grupę zasobów, w której ma zostać utworzona strefa.</span><span class="sxs-lookup"><span data-stu-id="45a8f-117">Specifies the resource group in which to create the zone.</span></span>

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

### <span data-ttu-id="45a8f-118">-Tag</span><span class="sxs-lookup"><span data-stu-id="45a8f-118">-Tag</span></span>
<span data-ttu-id="45a8f-119">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="45a8f-119">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="45a8f-120">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="45a8f-120">For example:</span></span>

<span data-ttu-id="45a8f-121">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="45a8f-121">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="45a8f-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="45a8f-122">-Confirm</span></span>
<span data-ttu-id="45a8f-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45a8f-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45a8f-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45a8f-124">-WhatIf</span></span>
<span data-ttu-id="45a8f-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45a8f-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="45a8f-126">Polecenie cmdlet nie jest uruchamiane. Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45a8f-126">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="45a8f-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="45a8f-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45a8f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45a8f-128">CommonParameters</span></span>
<span data-ttu-id="45a8f-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45a8f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45a8f-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45a8f-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45a8f-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="45a8f-131">INPUTS</span></span>

### <span data-ttu-id="45a8f-132">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="45a8f-132">None</span></span>

<span data-ttu-id="45a8f-133">Nie możesz popotokować danych wejściowych tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45a8f-133">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="45a8f-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="45a8f-134">OUTPUTS</span></span>

### <span data-ttu-id="45a8f-135">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="45a8f-135">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

<span data-ttu-id="45a8f-136">To polecenie cmdlet zwraca obiekt Microsoft. Azure. Commands. DNS. DnsZone reprezentujący nową strefę DNS.</span><span class="sxs-lookup"><span data-stu-id="45a8f-136">This cmdlet returns a Microsoft.Azure.Commands.Dns.DnsZone object that represents the new DNS zone.</span></span>

## <span data-ttu-id="45a8f-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="45a8f-137">NOTES</span></span>
<span data-ttu-id="45a8f-138">Za pomocą parametru *Confirm* można kontrolować, czy to polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="45a8f-138">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="45a8f-139">Domyślnie polecenie cmdlet monituje o potwierdzenie, jeśli zmienna $ConfirmPreference Windows PowerShell ma wartość średnią lub niższą.</span><span class="sxs-lookup"><span data-stu-id="45a8f-139">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="45a8f-140">Jeśli określisz pozycję *Potwierdź* lub *Potwierdź: $true* , to polecenie cmdlet wyświetli monit o potwierdzenie przed jego uruchomieniem.</span><span class="sxs-lookup"><span data-stu-id="45a8f-140">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="45a8f-141">Jeśli określisz pozycję *Confirm (Potwierdź): $false* , polecenie cmdlet nie monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="45a8f-141">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="45a8f-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="45a8f-142">RELATED LINKS</span></span>

[<span data-ttu-id="45a8f-143">Get-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="45a8f-143">Get-AzureRmDnsZone</span></span>](./Get-AzureRmDnsZone.md)

[<span data-ttu-id="45a8f-144">Nowe — AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="45a8f-144">New-AzureRmDnsRecordSet</span></span>](./New-AzureRmDnsRecordSet.md)

[<span data-ttu-id="45a8f-145">Remove-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="45a8f-145">Remove-AzureRmDnsZone</span></span>](./Remove-AzureRmDnsZone.md)
