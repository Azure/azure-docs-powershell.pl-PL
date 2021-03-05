---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/powershell/module/az.privatedns/Set-AzPrivateDnsRecordSet
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsRecordSet.md
ms.openlocfilehash: 68e55ae6a0c563ecc72e74fc127360ddb35f73f3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986686"
---
# <span data-ttu-id="5bf0d-101">Set-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="5bf0d-101">Set-AzPrivateDnsRecordSet</span></span>

## <span data-ttu-id="5bf0d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5bf0d-102">SYNOPSIS</span></span>
<span data-ttu-id="5bf0d-103">Aktualizuje/ustawia zestaw rekordów w prywatnej strefie DNS.</span><span class="sxs-lookup"><span data-stu-id="5bf0d-103">Updates/Sets a record set in a Private DNS zone.</span></span>

## <span data-ttu-id="5bf0d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5bf0d-104">SYNTAX</span></span>

```
Set-AzPrivateDnsRecordSet -RecordSet <PSPrivateDnsRecordSet> [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5bf0d-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="5bf0d-105">DESCRIPTION</span></span>
<span data-ttu-id="5bf0d-106">Polecenie Set-AzPrivateDnsRecordSet aktualizuje zestaw rekordów w prywatnej usłudze DNS Platformy Azure z lokalnego obiektu RecordSet.</span><span class="sxs-lookup"><span data-stu-id="5bf0d-106">The Set-AzPrivateDnsRecordSet cmdlet updates a record set in the Azure Private DNS service from a local RecordSet object.</span></span> <span data-ttu-id="5bf0d-107">Obiekt RecordSet można przekazać jako parametr lub za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="5bf0d-107">You can pass a RecordSet object as a parameter or by using the pipeline operator.</span></span> <span data-ttu-id="5bf0d-108">Możesz użyć parametru Confirm i $ConfirmPreference zmienną programu Windows PowerShell, aby określić, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5bf0d-108">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span> <span data-ttu-id="5bf0d-109">Zestaw rekordów nie zostanie zaktualizowany, jeśli został zmieniony w prywatnym systemie DNS platformy Azure od czasu pobrania lokalnego obiektu RecordSet.</span><span class="sxs-lookup"><span data-stu-id="5bf0d-109">The record set is not updated if it has been changed in Azure Private DNS since the local RecordSet object was retrieved.</span></span> <span data-ttu-id="5bf0d-110">Zapewnia to ochronę w przypadku jednoczesnych zmian.</span><span class="sxs-lookup"><span data-stu-id="5bf0d-110">This provides protection for concurrent changes.</span></span> <span data-ttu-id="5bf0d-111">To zachowanie można pominąć przy użyciu parametru Zastąp, który aktualizuje zestaw rekordów niezależnie od jednoczesnych zmian.</span><span class="sxs-lookup"><span data-stu-id="5bf0d-111">You can suppress this behavior using the Overwrite parameter, which updates the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="5bf0d-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5bf0d-112">EXAMPLES</span></span>

### <span data-ttu-id="5bf0d-113">Przykład 1. Aktualizowanie zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="5bf0d-113">Example 1: Update a record set</span></span>
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

<span data-ttu-id="5bf0d-114">Pierwsze polecenie używa Get-AzPrivateDnsRecordSet cmdlet w celu uzyskania określonego zestawu rekordów, a następnie zapisuje go w $RecordSet zmienną.</span><span class="sxs-lookup"><span data-stu-id="5bf0d-114">The first command uses the Get-AzPrivateDnsRecordSet cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span> <span data-ttu-id="5bf0d-115">Drugie i trzecie polecenie to operacje off-line umożliwiające dodanie dwóch rekordów A do zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="5bf0d-115">The second and third commands are off-line operations to add two A records to the record set.</span></span> <span data-ttu-id="5bf0d-116">Ostatnie polecenie użyje polecenia cmdlet Set-AzPrivateDnsRecordSet do zatwierdzenia aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="5bf0d-116">The final command uses the Set-AzPrivateDnsRecordSet cmdlet to commit the update.</span></span>

### <span data-ttu-id="5bf0d-117">Przykład 2. Aktualizowanie rekordu SOA</span><span class="sxs-lookup"><span data-stu-id="5bf0d-117">Example 2: Update an SOA record</span></span>
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

<span data-ttu-id="5bf0d-118">Pierwsze polecenie używa Get-AzPrivateDnsRecordSet cmdlet w celu uzyskania określonego zestawu rekordów, a następnie zapisuje go w $RecordSet zmienną.</span><span class="sxs-lookup"><span data-stu-id="5bf0d-118">The first command uses the Get-AzPrivateDnsRecordSet cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span> <span data-ttu-id="5bf0d-119">Drugie polecenie aktualizuje określony rekord SOA w $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="5bf0d-119">The second command updates the specified SOA record in $RecordSet.</span></span> <span data-ttu-id="5bf0d-120">Ostatnie polecenie propaguje aktualizację Set-AzPrivateDnsRecordSet w programie $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="5bf0d-120">The final command uses the Set-AzPrivateDnsRecordSet cmdlet to propagate the update in $RecordSet.</span></span>

## <span data-ttu-id="5bf0d-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5bf0d-121">PARAMETERS</span></span>

### <span data-ttu-id="5bf0d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bf0d-122">-DefaultProfile</span></span>
<span data-ttu-id="5bf0d-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5bf0d-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5bf0d-124">— Zastąp</span><span class="sxs-lookup"><span data-stu-id="5bf0d-124">-Overwrite</span></span>
<span data-ttu-id="5bf0d-125">W przypadku optymistycznych testów współbieżności nie należy używać pola ETag parametru RecordSet.</span><span class="sxs-lookup"><span data-stu-id="5bf0d-125">Do not use the ETag field of the RecordSet parameter for optimistic concurrency checks.</span></span>

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

### <span data-ttu-id="5bf0d-126">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="5bf0d-126">-RecordSet</span></span>
<span data-ttu-id="5bf0d-127">Zestaw rekordów, w którym należy dodać rekord.</span><span class="sxs-lookup"><span data-stu-id="5bf0d-127">The record set in which to add the record.</span></span>

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

### <span data-ttu-id="5bf0d-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5bf0d-128">-Confirm</span></span>
<span data-ttu-id="5bf0d-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5bf0d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5bf0d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5bf0d-130">-WhatIf</span></span>
<span data-ttu-id="5bf0d-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5bf0d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5bf0d-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="5bf0d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5bf0d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bf0d-133">CommonParameters</span></span>
<span data-ttu-id="5bf0d-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bf0d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bf0d-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5bf0d-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bf0d-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5bf0d-136">INPUTS</span></span>

### <span data-ttu-id="5bf0d-137">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="5bf0d-137">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="5bf0d-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5bf0d-138">OUTPUTS</span></span>

### <span data-ttu-id="5bf0d-139">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="5bf0d-139">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="5bf0d-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5bf0d-140">NOTES</span></span>

## <span data-ttu-id="5bf0d-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5bf0d-141">RELATED LINKS</span></span>
