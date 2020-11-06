---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/New-AzureRmDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/New-AzureRmDnsZone.md
ms.openlocfilehash: 2b04478e80010f0edfac9488d45b36700db45eec
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550007"
---
# <span data-ttu-id="1f10a-101">New-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="1f10a-101">New-AzureRmDnsZone</span></span>

## <span data-ttu-id="1f10a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1f10a-102">SYNOPSIS</span></span>
<span data-ttu-id="1f10a-103">Tworzy nową strefę DNS.</span><span class="sxs-lookup"><span data-stu-id="1f10a-103">Creates a new DNS zone.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f10a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1f10a-104">SYNTAX</span></span>

```
New-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f10a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1f10a-105">DESCRIPTION</span></span>
<span data-ttu-id="1f10a-106">Polecenie cmdlet **New-AzureRmDnsZone** tworzy nową strefę DNS (Domain Name System) w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="1f10a-106">The **New-AzureRmDnsZone** cmdlet creates a new Domain Name System (DNS) zone in the specified resource group.</span></span> <span data-ttu-id="1f10a-107">Musisz określić unikatową nazwę strefy DNS dla parametru *name* lub polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="1f10a-107">You must specify a unique DNS zone name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="1f10a-108">Po utworzeniu strefy Użyj polecenia cmdlet New-AzureRmDnsRecordSet, aby utworzyć zestaw rekordów w strefie.</span><span class="sxs-lookup"><span data-stu-id="1f10a-108">After the zone is created, use the New-AzureRmDnsRecordSet cmdlet to create record sets in the zone.</span></span>

<span data-ttu-id="1f10a-109">Za pomocą zmiennej *Confirm* i $ConfirmPreference programu Windows PowerShell można kontrolować, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1f10a-109">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="1f10a-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1f10a-110">EXAMPLES</span></span>

### <span data-ttu-id="1f10a-111">Przykład 1: Tworzenie strefy DNS</span><span class="sxs-lookup"><span data-stu-id="1f10a-111">Example 1: Create a DNS zone</span></span>
```
PS C:\>$Zone = New-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="1f10a-112">To polecenie tworzy nową strefę DNS o nazwie myzone.com w określonej grupie zasobów, a następnie zapisuje ją w zmiennej $Zone.</span><span class="sxs-lookup"><span data-stu-id="1f10a-112">This command creates a new DNS zone named myzone.com in the specified resource group, and then stores it in the $Zone variable.</span></span>

## <span data-ttu-id="1f10a-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1f10a-113">PARAMETERS</span></span>

### <span data-ttu-id="1f10a-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1f10a-114">-Name</span></span>
<span data-ttu-id="1f10a-115">Określa nazwę strefy DNS do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="1f10a-115">Specifies the name of the DNS zone to create.</span></span>

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

### <span data-ttu-id="1f10a-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f10a-116">-ResourceGroupName</span></span>
<span data-ttu-id="1f10a-117">Określa grupę zasobów, w której ma zostać utworzona strefa.</span><span class="sxs-lookup"><span data-stu-id="1f10a-117">Specifies the resource group in which to create the zone.</span></span>

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

### <span data-ttu-id="1f10a-118">-Tag</span><span class="sxs-lookup"><span data-stu-id="1f10a-118">-Tag</span></span>
<span data-ttu-id="1f10a-119">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="1f10a-119">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="1f10a-120">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="1f10a-120">For example:</span></span>

<span data-ttu-id="1f10a-121">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="1f10a-121">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f10a-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1f10a-122">-Confirm</span></span>
<span data-ttu-id="1f10a-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f10a-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f10a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f10a-124">-WhatIf</span></span>
<span data-ttu-id="1f10a-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f10a-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1f10a-126">Polecenie cmdlet nie jest uruchamiane. Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f10a-126">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1f10a-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1f10a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f10a-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f10a-128">-DefaultProfile</span></span>
<span data-ttu-id="1f10a-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1f10a-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f10a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f10a-130">CommonParameters</span></span>
<span data-ttu-id="1f10a-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f10a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f10a-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f10a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f10a-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1f10a-133">INPUTS</span></span>

### <span data-ttu-id="1f10a-134">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="1f10a-134">None</span></span>
<span data-ttu-id="1f10a-135">Nie możesz popotokować danych wejściowych tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f10a-135">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="1f10a-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1f10a-136">OUTPUTS</span></span>

### <span data-ttu-id="1f10a-137">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="1f10a-137">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="1f10a-138">To polecenie cmdlet zwraca obiekt Microsoft. Azure. Commands. DNS. DnsZone reprezentujący nową strefę DNS.</span><span class="sxs-lookup"><span data-stu-id="1f10a-138">This cmdlet returns a Microsoft.Azure.Commands.Dns.DnsZone object that represents the new DNS zone.</span></span>

## <span data-ttu-id="1f10a-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1f10a-139">NOTES</span></span>
<span data-ttu-id="1f10a-140">Za pomocą parametru *Confirm* można kontrolować, czy to polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1f10a-140">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="1f10a-141">Domyślnie polecenie cmdlet monituje o potwierdzenie, jeśli zmienna $ConfirmPreference Windows PowerShell ma wartość średnią lub niższą.</span><span class="sxs-lookup"><span data-stu-id="1f10a-141">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="1f10a-142">Jeśli określisz pozycję *Potwierdź* lub *Potwierdź: $true* , to polecenie cmdlet wyświetli monit o potwierdzenie przed jego uruchomieniem.</span><span class="sxs-lookup"><span data-stu-id="1f10a-142">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="1f10a-143">Jeśli określisz pozycję *Confirm (Potwierdź): $false* , polecenie cmdlet nie monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1f10a-143">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="1f10a-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1f10a-144">RELATED LINKS</span></span>

[<span data-ttu-id="1f10a-145">Get-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="1f10a-145">Get-AzureRmDnsZone</span></span>](./Get-AzureRmDnsZone.md)

[<span data-ttu-id="1f10a-146">Nowe — AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="1f10a-146">New-AzureRmDnsRecordSet</span></span>](./New-AzureRmDnsRecordSet.md)

[<span data-ttu-id="1f10a-147">Remove-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="1f10a-147">Remove-AzureRmDnsZone</span></span>](./Remove-AzureRmDnsZone.md)
