---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 99E6C4DD-11AF-4DC0-848B-39811240BE06
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/set-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsRecordSet.md
ms.openlocfilehash: c57377156acbf908825638e13f139114fa5d811c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705511"
---
# <span data-ttu-id="f0206-101">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="f0206-101">Set-AzDnsRecordSet</span></span>

## <span data-ttu-id="f0206-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f0206-102">SYNOPSIS</span></span>
<span data-ttu-id="f0206-103">Aktualizuje zestaw rekordów DNS.</span><span class="sxs-lookup"><span data-stu-id="f0206-103">Updates a DNS record set.</span></span>

## <span data-ttu-id="f0206-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f0206-104">SYNTAX</span></span>

```
Set-AzDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0206-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f0206-105">DESCRIPTION</span></span>
<span data-ttu-id="f0206-106">Polecenie cmdlet **Set-AzDnsRecordSet** aktualizuje zestaw rekordów w usłudze DNS Azure z lokalnego obiektu **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="f0206-106">The **Set-AzDnsRecordSet** cmdlet updates a record set in the Azure DNS service from a local **RecordSet** object.</span></span>
<span data-ttu-id="f0206-107">Obiekt **Recordset** można przekazać jako parametr lub za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="f0206-107">You can pass a **RecordSet** object as a parameter or by using the pipeline operator.</span></span>
<span data-ttu-id="f0206-108">Za pomocą zmiennej *Confirm* i $ConfirmPreference programu Windows PowerShell można kontrolować, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f0206-108">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="f0206-109">Zestaw rekordów nie jest aktualizowany, jeśli został on zmieniony w usłudze DNS Azure, ponieważ został pobrany lokalny obiekt **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="f0206-109">The record set is not updated if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="f0206-110">Zapewnia to ochronę współbieżnych zmian.</span><span class="sxs-lookup"><span data-stu-id="f0206-110">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="f0206-111">Możesz pominąć to zachowanie przy użyciu parametru *Zastąp* , który powoduje zaktualizowanie zestawu rekordów bez względu na jednoczesne zmiany.</span><span class="sxs-lookup"><span data-stu-id="f0206-111">You can suppress this behavior using the *Overwrite* parameter, which updates the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="f0206-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f0206-112">EXAMPLES</span></span>

### <span data-ttu-id="f0206-113">Przykład 1: Aktualizowanie zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="f0206-113">Example 1: Update a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.16.0.0
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.31.255.255
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# These cmdlets can also be piped:

PS C:\> Get-AzDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A | Add-AzDnsRecordConfig -Ipv4Address 172.16.0.0 | Add-AzDnsRecordConfig -Ipv4Address 172.31.255.255 | Set-AzDnsRecordSet
```

<span data-ttu-id="f0206-114">W pierwszym poleceniu jest używane polecenie cmdlet Get-AzDnsRecordSet w celu uzyskania określonego zestawu rekordów, a następnie zapisanie go w zmiennej $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="f0206-114">The first command uses the Get-AzDnsRecordSet cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span>
<span data-ttu-id="f0206-115">Drugie i trzecie polecenia to operacje w trybie online, które umożliwiają dodawanie dwóch rekordów do zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="f0206-115">The second and third commands are off-line operations to add two A records to the record set.</span></span>
<span data-ttu-id="f0206-116">W poleceniu finalnym jest zatwierdzanie aktualizacji przy użyciu polecenia cmdlet **Set-AzDnsRecordSet** .</span><span class="sxs-lookup"><span data-stu-id="f0206-116">The final command uses the **Set-AzDnsRecordSet** cmdlet to commit the update.</span></span>

### <span data-ttu-id="f0206-117">Przykład 2: aktualizowanie rekordu SOA</span><span class="sxs-lookup"><span data-stu-id="f0206-117">Example 2: Update an SOA record</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name "@" -RecordType SOA -Zone $Zone
PS C:\> $RecordSet.Records[0].Email = "admin.myzone.com"
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="f0206-118">W pierwszym poleceniu jest używany polecenie cmdlet **Get-AzDnsRecordset** w celu uzyskania określonego zestawu rekordów, a następnie zapisanie go w zmiennej $Recordset.</span><span class="sxs-lookup"><span data-stu-id="f0206-118">The first command uses the **Get-AzDnsRecordset** cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span>
<span data-ttu-id="f0206-119">Drugie polecenie aktualizuje określony rekord SOA w $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="f0206-119">The second command updates the specified SOA record in $RecordSet.</span></span>
<span data-ttu-id="f0206-120">W poleceniu finalnym jest propagowanie aktualizacji w $RecordSet przy użyciu polecenia cmdlet **Set-AzDnsRecordSet** .</span><span class="sxs-lookup"><span data-stu-id="f0206-120">The final command uses the **Set-AzDnsRecordSet** cmdlet to propagate the update in $RecordSet.</span></span>

## <span data-ttu-id="f0206-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f0206-121">PARAMETERS</span></span>

### <span data-ttu-id="f0206-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0206-122">-DefaultProfile</span></span>
<span data-ttu-id="f0206-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="f0206-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f0206-124">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="f0206-124">-Overwrite</span></span>
<span data-ttu-id="f0206-125">Wskazuje, że należy zaktualizować zestaw rekordów bez względu na jednoczesne zmiany.</span><span class="sxs-lookup"><span data-stu-id="f0206-125">Indicates to update the record set regardless of concurrent changes.</span></span>
<span data-ttu-id="f0206-126">Zestaw rekordów nie zostanie zaktualizowany, jeśli został on zmieniony w usłudze DNS Azure, ponieważ został pobrany lokalny obiekt **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="f0206-126">The record set will not be updated if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="f0206-127">Zapewnia to ochronę współbieżnych zmian.</span><span class="sxs-lookup"><span data-stu-id="f0206-127">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="f0206-128">Aby pominąć to zachowanie, można użyć parametru *overwrite* , który powoduje Aktualizowanie zestawu rekordów bez względu na jednoczesne zmiany.</span><span class="sxs-lookup"><span data-stu-id="f0206-128">To suppress this behavior, you can use the *Overwrite* parameter, which results in the record set being updated regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="f0206-129">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="f0206-129">-RecordSet</span></span>
<span data-ttu-id="f0206-130">Określa **zestaw rekordów** do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="f0206-130">Specifies the **RecordSet** to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsRecordSet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f0206-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f0206-131">-Confirm</span></span>
<span data-ttu-id="f0206-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0206-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0206-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0206-133">-WhatIf</span></span>
<span data-ttu-id="f0206-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0206-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f0206-135">Polecenie cmdlet nie jest uruchamiane. Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0206-135">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f0206-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f0206-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0206-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0206-137">CommonParameters</span></span>
<span data-ttu-id="f0206-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0206-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0206-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0206-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0206-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f0206-140">INPUTS</span></span>

### <span data-ttu-id="f0206-141">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="f0206-141">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="f0206-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f0206-142">OUTPUTS</span></span>

### <span data-ttu-id="f0206-143">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="f0206-143">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="f0206-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f0206-144">NOTES</span></span>
<span data-ttu-id="f0206-145">Za pomocą parametru *Confirm* można kontrolować, czy to polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f0206-145">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="f0206-146">Domyślnie polecenie cmdlet monituje o potwierdzenie, jeśli zmienna $ConfirmPreference Windows PowerShell ma wartość średnią lub niższą.</span><span class="sxs-lookup"><span data-stu-id="f0206-146">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="f0206-147">Jeśli określisz pozycję *Potwierdź* lub *Potwierdź: $true* , to polecenie cmdlet wyświetli monit o potwierdzenie przed jego uruchomieniem.</span><span class="sxs-lookup"><span data-stu-id="f0206-147">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="f0206-148">Jeśli określisz pozycję *Confirm (Potwierdź): $false* , polecenie cmdlet nie monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f0206-148">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span> 

## <span data-ttu-id="f0206-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f0206-149">RELATED LINKS</span></span>

[<span data-ttu-id="f0206-150">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="f0206-150">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="f0206-151">Nowe — AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="f0206-151">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="f0206-152">Remove-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="f0206-152">Remove-AzDnsRecordSet</span></span>](./Remove-AzDnsRecordSet.md)
