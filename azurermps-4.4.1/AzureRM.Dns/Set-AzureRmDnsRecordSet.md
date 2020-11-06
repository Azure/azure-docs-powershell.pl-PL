---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: 99E6C4DD-11AF-4DC0-848B-39811240BE06
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Set-AzureRmDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Set-AzureRmDnsRecordSet.md
ms.openlocfilehash: 9db3efc71b751f291c5bb8636246ed6927200c37
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527585"
---
# <span data-ttu-id="81a02-101">Set-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="81a02-101">Set-AzureRmDnsRecordSet</span></span>

## <span data-ttu-id="81a02-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="81a02-102">SYNOPSIS</span></span>
<span data-ttu-id="81a02-103">Aktualizuje zestaw rekordów DNS.</span><span class="sxs-lookup"><span data-stu-id="81a02-103">Updates a DNS record set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81a02-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="81a02-104">SYNTAX</span></span>

```
Set-AzureRmDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81a02-105">Opis</span><span class="sxs-lookup"><span data-stu-id="81a02-105">DESCRIPTION</span></span>
<span data-ttu-id="81a02-106">Polecenie cmdlet **Set-AzureRmDnsRecordSet** aktualizuje zestaw rekordów w usłudze DNS Azure z lokalnego obiektu **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="81a02-106">The **Set-AzureRmDnsRecordSet** cmdlet updates a record set in the Azure DNS service from a local **RecordSet** object.</span></span>

<span data-ttu-id="81a02-107">Obiekt **Recordset** można przekazać jako parametr lub za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="81a02-107">You can pass a **RecordSet** object as a parameter or by using the pipeline operator.</span></span>

<span data-ttu-id="81a02-108">Za pomocą zmiennej *Confirm* i $ConfirmPreference programu Windows PowerShell można kontrolować, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="81a02-108">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

<span data-ttu-id="81a02-109">Zestaw rekordów nie jest aktualizowany, jeśli został on zmieniony w usłudze DNS Azure, ponieważ został pobrany lokalny obiekt **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="81a02-109">The record set is not updated if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="81a02-110">Zapewnia to ochronę współbieżnych zmian.</span><span class="sxs-lookup"><span data-stu-id="81a02-110">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="81a02-111">Możesz pominąć to zachowanie przy użyciu parametru *Zastąp* , który powoduje zaktualizowanie zestawu rekordów bez względu na jednoczesne zmiany.</span><span class="sxs-lookup"><span data-stu-id="81a02-111">You can suppress this behavior using the *Overwrite* parameter, which updates the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="81a02-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="81a02-112">EXAMPLES</span></span>

### <span data-ttu-id="81a02-113">Przykład 1: Aktualizowanie zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="81a02-113">Example 1: Update a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.16.0.0
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.31.255.255
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# These cmdlets can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A | Add-AzureRmDnsRecordConfig -Ipv4Address 172.16.0.0 | Add-AzureRmDnsRecordConfig -Ipv4Address 172.31.255.255 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="81a02-114">W pierwszym poleceniu jest używane polecenie cmdlet Get-AzureRmDnsRecordSet w celu uzyskania określonego zestawu rekordów, a następnie zapisanie go w zmiennej $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="81a02-114">The first command uses the Get-AzureRmDnsRecordSet cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span>

<span data-ttu-id="81a02-115">Drugie i trzecie polecenia to operacje w trybie online, które umożliwiają dodawanie dwóch rekordów do zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="81a02-115">The second and third commands are off-line operations to add two A records to the record set.</span></span>

<span data-ttu-id="81a02-116">W poleceniu finalnym jest zatwierdzanie aktualizacji przy użyciu polecenia cmdlet **Set-AzureRmDnsRecordSet** .</span><span class="sxs-lookup"><span data-stu-id="81a02-116">The final command uses the **Set-AzureRmDnsRecordSet** cmdlet to commit the update.</span></span>

### <span data-ttu-id="81a02-117">Przykład 2: aktualizowanie rekordu SOA</span><span class="sxs-lookup"><span data-stu-id="81a02-117">Example 2: Update an SOA record</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name "@" -RecordType SOA -Zone $Zone
PS C:\> $RecordSet.Records[0].Email = "admin.myzone.com"
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="81a02-118">W pierwszym poleceniu jest używany polecenie cmdlet **Get-AzureRmDnsRecordset** w celu uzyskania określonego zestawu rekordów, a następnie zapisanie go w zmiennej $Recordset.</span><span class="sxs-lookup"><span data-stu-id="81a02-118">The first command uses the **Get-AzureRmDnsRecordset** cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span>

<span data-ttu-id="81a02-119">Drugie polecenie aktualizuje określony rekord SOA w $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="81a02-119">The second command updates the specified SOA record in $RecordSet.</span></span>

<span data-ttu-id="81a02-120">W poleceniu finalnym jest propagowanie aktualizacji w $RecordSet przy użyciu polecenia cmdlet **Set-AzureRmDnsRecordSet** .</span><span class="sxs-lookup"><span data-stu-id="81a02-120">The final command uses the **Set-AzureRmDnsRecordSet** cmdlet to propagate the update in $RecordSet.</span></span>

## <span data-ttu-id="81a02-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="81a02-121">PARAMETERS</span></span>

### <span data-ttu-id="81a02-122">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="81a02-122">-Overwrite</span></span>
<span data-ttu-id="81a02-123">Wskazuje, że należy zaktualizować zestaw rekordów bez względu na jednoczesne zmiany.</span><span class="sxs-lookup"><span data-stu-id="81a02-123">Indicates to update the record set regardless of concurrent changes.</span></span>

<span data-ttu-id="81a02-124">Zestaw rekordów nie zostanie zaktualizowany, jeśli został on zmieniony w usłudze DNS Azure, ponieważ został pobrany lokalny obiekt **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="81a02-124">The record set will not be updated if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="81a02-125">Zapewnia to ochronę współbieżnych zmian.</span><span class="sxs-lookup"><span data-stu-id="81a02-125">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="81a02-126">Aby pominąć to zachowanie, można użyć parametru *overwrite* , który powoduje Aktualizowanie zestawu rekordów bez względu na jednoczesne zmiany.</span><span class="sxs-lookup"><span data-stu-id="81a02-126">To suppress this behavior, you can use the *Overwrite* parameter, which results in the record set being updated regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="81a02-127">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="81a02-127">-RecordSet</span></span>
<span data-ttu-id="81a02-128">Określa **zestaw rekordów** do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="81a02-128">Specifies the **RecordSet** to update.</span></span>

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

### <span data-ttu-id="81a02-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="81a02-129">-Confirm</span></span>
<span data-ttu-id="81a02-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81a02-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81a02-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81a02-131">-WhatIf</span></span>
<span data-ttu-id="81a02-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81a02-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="81a02-133">Polecenie cmdlet nie jest uruchamiane. Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81a02-133">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="81a02-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="81a02-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81a02-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81a02-135">-DefaultProfile</span></span>
<span data-ttu-id="81a02-136">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="81a02-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81a02-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81a02-137">CommonParameters</span></span>
<span data-ttu-id="81a02-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81a02-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81a02-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81a02-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81a02-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="81a02-140">INPUTS</span></span>

### <span data-ttu-id="81a02-141">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="81a02-141">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="81a02-142">Do tego polecenia cmdlet można przekazać obiekt **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="81a02-142">You can pass a **RecordSet** object to this cmdlet.</span></span>

## <span data-ttu-id="81a02-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="81a02-143">OUTPUTS</span></span>

### <span data-ttu-id="81a02-144">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="81a02-144">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="81a02-145">To polecenie cmdlet zwraca obiekt reprezentujący zaktualizowany obiekt **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="81a02-145">This cmdlet returns an object that represents the updated **RecordSet** object.</span></span>

## <span data-ttu-id="81a02-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="81a02-146">NOTES</span></span>
<span data-ttu-id="81a02-147">Za pomocą parametru *Confirm* można kontrolować, czy to polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="81a02-147">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="81a02-148">Domyślnie polecenie cmdlet monituje o potwierdzenie, jeśli zmienna $ConfirmPreference Windows PowerShell ma wartość średnią lub niższą.</span><span class="sxs-lookup"><span data-stu-id="81a02-148">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="81a02-149">Jeśli określisz pozycję *Potwierdź* lub *Potwierdź: $true* , to polecenie cmdlet wyświetli monit o potwierdzenie przed jego uruchomieniem.</span><span class="sxs-lookup"><span data-stu-id="81a02-149">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="81a02-150">Jeśli określisz pozycję *Confirm (Potwierdź): $false* , polecenie cmdlet nie monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="81a02-150">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span> 

## <span data-ttu-id="81a02-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="81a02-151">RELATED LINKS</span></span>

[<span data-ttu-id="81a02-152">Get-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="81a02-152">Get-AzureRmDnsRecordSet</span></span>](./Get-AzureRmDnsRecordSet.md)

[<span data-ttu-id="81a02-153">Nowe — AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="81a02-153">New-AzureRmDnsRecordSet</span></span>](./New-AzureRmDnsRecordSet.md)

[<span data-ttu-id="81a02-154">Remove-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="81a02-154">Remove-AzureRmDnsRecordSet</span></span>](./Remove-AzureRmDnsRecordSet.md)
