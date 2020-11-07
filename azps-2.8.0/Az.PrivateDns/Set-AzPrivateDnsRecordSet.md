---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/Set-AzPrivateDnsRecordSet
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsRecordSet.md
ms.openlocfilehash: 7c4f76b9731e82bd134be7ae38461a7d74e31e6a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872827"
---
# <span data-ttu-id="4cc30-101">Set-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="4cc30-101">Set-AzPrivateDnsRecordSet</span></span>

## <span data-ttu-id="4cc30-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4cc30-102">SYNOPSIS</span></span>
<span data-ttu-id="4cc30-103">Aktualizuje/ustawia zestaw rekordów w prywatnej strefie DNS.</span><span class="sxs-lookup"><span data-stu-id="4cc30-103">Updates/Sets a record set in a Private DNS zone.</span></span>

## <span data-ttu-id="4cc30-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4cc30-104">SYNTAX</span></span>

```
Set-AzPrivateDnsRecordSet -RecordSet <PSPrivateDnsRecordSet> [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4cc30-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4cc30-105">DESCRIPTION</span></span>
<span data-ttu-id="4cc30-106">Polecenie cmdlet Set-AzPrivateDnsRecordSet aktualizuje zestaw rekordów w prywatnej usłudze DNS platformy Azure z lokalnego obiektu RecordSet.</span><span class="sxs-lookup"><span data-stu-id="4cc30-106">The Set-AzPrivateDnsRecordSet cmdlet updates a record set in the Azure Private DNS service from a local RecordSet object.</span></span> <span data-ttu-id="4cc30-107">Obiekt RecordSet można przekazać jako parametr lub za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="4cc30-107">You can pass a RecordSet object as a parameter or by using the pipeline operator.</span></span> <span data-ttu-id="4cc30-108">Za pomocą zmiennej Confirm i $ConfirmPreference programu Windows PowerShell można kontrolować, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4cc30-108">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span> <span data-ttu-id="4cc30-109">Zestaw rekordów nie zostanie zaktualizowany, jeśli został on zmieniony w usłudze DNS w usłudze Azure Private, ponieważ został pobrany lokalny obiekt RecordSet.</span><span class="sxs-lookup"><span data-stu-id="4cc30-109">The record set is not updated if it has been changed in Azure Private DNS since the local RecordSet object was retrieved.</span></span> <span data-ttu-id="4cc30-110">Zapewnia to ochronę współbieżnych zmian.</span><span class="sxs-lookup"><span data-stu-id="4cc30-110">This provides protection for concurrent changes.</span></span> <span data-ttu-id="4cc30-111">Możesz pominąć to zachowanie przy użyciu parametru Zastąp, który powoduje zaktualizowanie zestawu rekordów bez względu na jednoczesne zmiany.</span><span class="sxs-lookup"><span data-stu-id="4cc30-111">You can suppress this behavior using the Overwrite parameter, which updates the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="4cc30-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4cc30-112">EXAMPLES</span></span>

### <span data-ttu-id="4cc30-113">Przykład 1: Aktualizowanie zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="4cc30-113">Example 1: Update a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A
PS C:\> Add-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.16.0.0
PS C:\> Add-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.31.255.255
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# These cmdlets can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A | Add-AzPrivateDnsRecordConfig -Ipv4Address 172.16.0.0 | Add-AzPrivateDnsRecordConfig -Ipv4Address 172.31.255.255 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.Netwo
                    rk/privateDnsZones/myzone.com/A/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4, 172.16.0.0, 172.31.255.255}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="4cc30-114">W pierwszym poleceniu jest używane polecenie cmdlet Get-AzPrivateDnsRecordSet w celu uzyskania określonego zestawu rekordów, a następnie zapisanie go w zmiennej $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="4cc30-114">The first command uses the Get-AzPrivateDnsRecordSet cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span> <span data-ttu-id="4cc30-115">Drugie i trzecie polecenia to operacje w trybie online, które umożliwiają dodawanie dwóch rekordów do zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="4cc30-115">The second and third commands are off-line operations to add two A records to the record set.</span></span> <span data-ttu-id="4cc30-116">W poleceniu ostatnim użyto polecenia cmdlet Set-AzPrivateDnsRecordSet, aby zatwierdzić aktualizację.</span><span class="sxs-lookup"><span data-stu-id="4cc30-116">The final command uses the Set-AzPrivateDnsRecordSet cmdlet to commit the update.</span></span>

### <span data-ttu-id="4cc30-117">Przykład 2: aktualizowanie rekordu SOA</span><span class="sxs-lookup"><span data-stu-id="4cc30-117">Example 2: Update an SOA record</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "@" -RecordType SOA -Zone $Zone
PS C:\> $RecordSet.Records[0].Email = "admin.myzone.com"
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/SOA/@
Name              : @
ZoneName          : myzone.com
ResourceGroupName : Myresourcegroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : SOA
Records           : {[internal.cloudapp.net,admin.myzone.com,3600,300,2419200,300]}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="4cc30-118">W pierwszym poleceniu jest używane polecenie cmdlet Get-AzPrivateDnsRecordSet w celu uzyskania określonego zestawu rekordów, a następnie zapisanie go w zmiennej $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="4cc30-118">The first command uses the Get-AzPrivateDnsRecordSet cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span> <span data-ttu-id="4cc30-119">Drugie polecenie aktualizuje określony rekord SOA w $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="4cc30-119">The second command updates the specified SOA record in $RecordSet.</span></span> <span data-ttu-id="4cc30-120">W poleceniu ostatnim użyto polecenia cmdlet Set-AzPrivateDnsRecordSet, aby propagować aktualizację w $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="4cc30-120">The final command uses the Set-AzPrivateDnsRecordSet cmdlet to propagate the update in $RecordSet.</span></span>

## <span data-ttu-id="4cc30-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4cc30-121">PARAMETERS</span></span>

### <span data-ttu-id="4cc30-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cc30-122">-DefaultProfile</span></span>
<span data-ttu-id="4cc30-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4cc30-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4cc30-124">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="4cc30-124">-Overwrite</span></span>
<span data-ttu-id="4cc30-125">Nie używaj pola ETag parametru RecordSet w celu sprawdzenia optymistycznych testów współbieżności.</span><span class="sxs-lookup"><span data-stu-id="4cc30-125">Do not use the ETag field of the RecordSet parameter for optimistic concurrency checks.</span></span>

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

### <span data-ttu-id="4cc30-126">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="4cc30-126">-RecordSet</span></span>
<span data-ttu-id="4cc30-127">Zestaw rekordów, w którym ma zostać dodany rekord.</span><span class="sxs-lookup"><span data-stu-id="4cc30-127">The record set in which to add the record.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4cc30-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4cc30-128">-Confirm</span></span>
<span data-ttu-id="4cc30-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4cc30-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cc30-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4cc30-130">-WhatIf</span></span>
<span data-ttu-id="4cc30-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4cc30-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4cc30-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4cc30-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cc30-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cc30-133">CommonParameters</span></span>
<span data-ttu-id="4cc30-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cc30-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cc30-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cc30-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cc30-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4cc30-136">INPUTS</span></span>

### <span data-ttu-id="4cc30-137">Microsoft. Azure. Commands. PrivateDns. models. PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="4cc30-137">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="4cc30-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4cc30-138">OUTPUTS</span></span>

### <span data-ttu-id="4cc30-139">Microsoft. Azure. Commands. PrivateDns. models. PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="4cc30-139">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="4cc30-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4cc30-140">NOTES</span></span>

## <span data-ttu-id="4cc30-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4cc30-141">RELATED LINKS</span></span>
