---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/remove-azprivatednsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsRecordSet.md
ms.openlocfilehash: 7c1b98f1d4408bddec94830a81bf06fa7c78baa7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708734"
---
# <span data-ttu-id="50bce-101">Remove-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="50bce-101">Remove-AzPrivateDnsRecordSet</span></span>

## <span data-ttu-id="50bce-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="50bce-102">SYNOPSIS</span></span>
<span data-ttu-id="50bce-103">Usuwa zestaw rekordów z prywatnej strefy DNS.</span><span class="sxs-lookup"><span data-stu-id="50bce-103">Deletes a record set from a Private DNS zone.</span></span>

## <span data-ttu-id="50bce-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="50bce-104">SYNTAX</span></span>

### <span data-ttu-id="50bce-105">Pola (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="50bce-105">Fields (Default)</span></span>
```
Remove-AzPrivateDnsRecordSet -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -RecordType <RecordType> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="50bce-106">Karoten</span><span class="sxs-lookup"><span data-stu-id="50bce-106">Mixed</span></span>
```
Remove-AzPrivateDnsRecordSet -Zone <PSPrivateDnsZone> -Name <String> -RecordType <RecordType> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50bce-107">Stream</span><span class="sxs-lookup"><span data-stu-id="50bce-107">Object</span></span>
```
Remove-AzPrivateDnsRecordSet -RecordSet <PSPrivateDnsRecordSet> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50bce-108">Zasobów</span><span class="sxs-lookup"><span data-stu-id="50bce-108">ResourceId</span></span>
```
Remove-AzPrivateDnsRecordSet -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50bce-109">Opis</span><span class="sxs-lookup"><span data-stu-id="50bce-109">DESCRIPTION</span></span>
<span data-ttu-id="50bce-110">Polecenie cmdlet Remove-AzPrivateDnsRecordSet powoduje usunięcie określonego zestawu rekordów z określonej strefy.</span><span class="sxs-lookup"><span data-stu-id="50bce-110">The Remove-AzPrivateDnsRecordSet cmdlet deletes the specified record set from the specified zone.</span></span> <span data-ttu-id="50bce-111">Nie można usuwać rekordów SOA, które są automatycznie tworzone w strefie prywatnej Apex.</span><span class="sxs-lookup"><span data-stu-id="50bce-111">You cannot delete SOA records that are automatically created at the private zone apex.</span></span> <span data-ttu-id="50bce-112">Do tego polecenia cmdlet można przekazać obiekt RecordSet za pomocą operatora potoku lub jako parametru lub jako ResourceId.</span><span class="sxs-lookup"><span data-stu-id="50bce-112">You can pass a RecordSet object to this cmdlet by using the pipeline operator or as a parameter or as a ResourceId.</span></span> <span data-ttu-id="50bce-113">Aby zidentyfikować zestaw rekordów i wpisać go bez użycia obiektu RecordSet, należy przekazać strefę jako obiekt PSPrivateDnsZone do tego polecenia cmdlet, korzystając z operatora potoku lub jako parametru lub można też określić parametry zonename i ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="50bce-113">To identify a record set by name and type without using a RecordSet object, you must pass the zone as a PSPrivateDnsZone object to this cmdlet by using the pipeline operator or as a parameter, or alternatively you can specify the ZoneName and ResourceGroupName parameters.</span></span> <span data-ttu-id="50bce-114">Za pomocą zmiennej Confirm i $ConfirmPreference programu Windows PowerShell można kontrolować, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="50bce-114">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span> <span data-ttu-id="50bce-115">Podczas określania zestawu rekordów za pomocą obiektu RecordSet zestaw rekordów nie jest usuwany, jeśli został zmieniony w usłudze Azure Private DNS od momentu pobrania lokalnego obiektu RecordSet.</span><span class="sxs-lookup"><span data-stu-id="50bce-115">When specifying the record set using a RecordSet object, the record set is not deleted if it has been changed in Azure Private DNS since the local RecordSet object was retrieved.</span></span> <span data-ttu-id="50bce-116">Zapewnia to ochronę współbieżnych zmian.</span><span class="sxs-lookup"><span data-stu-id="50bce-116">This provides protection for concurrent changes.</span></span> <span data-ttu-id="50bce-117">Można to pominąć, używając parametru zastępowania, który usuwa zestaw rekordów bez względu na zmiany współbieżne.</span><span class="sxs-lookup"><span data-stu-id="50bce-117">You can suppress this by using the Overwrite parameter, which deletes the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="50bce-118">Przykłady</span><span class="sxs-lookup"><span data-stu-id="50bce-118">EXAMPLES</span></span>

### <span data-ttu-id="50bce-119">Przykład 1: usuwanie zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="50bce-119">Example 1: Remove a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="50bce-120">Pierwsze polecenie pobiera określony zestaw rekordów, a następnie zapisuje go w zmiennej $RecordSet. Drugie polecenie usuwa zestaw rekordów w $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="50bce-120">The first command gets the specified record set, and then stores it in the $RecordSet variable.The second command removes the record set in $RecordSet.</span></span>

### <span data-ttu-id="50bce-121">Przykład 2: usunięcie zestawu rekordów i pominięcie wszystkich potwierdzeń</span><span class="sxs-lookup"><span data-stu-id="50bce-121">Example 2: Remove a record set and suppress all confirmation</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzPrivateDnsRecordSet -RecordSet $RecordSet -Confirm:$False -Overwrite

# Alternatively, the record set can be removed as follows.  In this case,
# because the record set is specified by name rather than by object, the
# Overwrite parameter is not applicable.

PS C:\> Remove-AzPrivateDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Confirm:$False
```

<span data-ttu-id="50bce-122">Pierwsze polecenie pobiera określony zestaw rekordów.</span><span class="sxs-lookup"><span data-stu-id="50bce-122">The first command gets the specified record set.</span></span> <span data-ttu-id="50bce-123">Drugie polecenie usuwa zestaw rekordów, nawet jeśli został on zmieniony w międzyczasie.</span><span class="sxs-lookup"><span data-stu-id="50bce-123">The second command deletes the record set, even if it has changed in the meantime.</span></span> <span data-ttu-id="50bce-124">Monity o potwierdzenie są pomijane.</span><span class="sxs-lookup"><span data-stu-id="50bce-124">Confirmation prompts are suppressed.</span></span>

## <span data-ttu-id="50bce-125">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="50bce-125">PARAMETERS</span></span>

### <span data-ttu-id="50bce-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50bce-126">-DefaultProfile</span></span>
<span data-ttu-id="50bce-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="50bce-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50bce-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="50bce-128">-Name</span></span>
<span data-ttu-id="50bce-129">Nazwy rekordów w zestawie rekordów (względem nazwy strefy i bez kropki przerywanej).</span><span class="sxs-lookup"><span data-stu-id="50bce-129">The name of the records in the record set (relative to the name of the zone and without a terminating dot).</span></span>

```yaml
Type: System.String
Parameter Sets: Fields, Mixed
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50bce-130">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="50bce-130">-Overwrite</span></span>
<span data-ttu-id="50bce-131">Nie używaj pola ETag parametru RecordSet w celu sprawdzenia optymistycznych testów współbieżności.</span><span class="sxs-lookup"><span data-stu-id="50bce-131">Do not use the ETag field of the RecordSet parameter for optimistic concurrency checks.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50bce-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="50bce-132">-PassThru</span></span>
<span data-ttu-id="50bce-133">Służy do przekazywania wyniku (wartości logicznej) operacji Usuń strefę prywatną potoku.</span><span class="sxs-lookup"><span data-stu-id="50bce-133">Used for passing the result (boolean) of the operation delete private zone further down the pipeline.</span></span>

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

### <span data-ttu-id="50bce-134">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="50bce-134">-RecordSet</span></span>
<span data-ttu-id="50bce-135">Zestaw rekordów, w którym ma zostać dodany rekord.</span><span class="sxs-lookup"><span data-stu-id="50bce-135">The record set in which to add the record.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="50bce-136">-Records</span><span class="sxs-lookup"><span data-stu-id="50bce-136">-RecordType</span></span>
<span data-ttu-id="50bce-137">Typ prywatnych rekordów DNS w zestawie rekordów.</span><span class="sxs-lookup"><span data-stu-id="50bce-137">The type of Private DNS records in the record set.</span></span>

```yaml
Type: Microsoft.Azure.Management.PrivateDns.Models.RecordType
Parameter Sets: Fields, Mixed
Aliases:
Accepted values: A, AAAA, CNAME, MX, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50bce-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50bce-138">-ResourceGroupName</span></span>
<span data-ttu-id="50bce-139">Grupa zasobów, do której należy strefa.</span><span class="sxs-lookup"><span data-stu-id="50bce-139">The resource group to which the zone belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50bce-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="50bce-140">-ResourceId</span></span>
<span data-ttu-id="50bce-141">Prywatny identyfikator ResourceID RecprdSet DNS.</span><span class="sxs-lookup"><span data-stu-id="50bce-141">Private DNS RecprdSet ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50bce-142">-Zone</span><span class="sxs-lookup"><span data-stu-id="50bce-142">-Zone</span></span>
<span data-ttu-id="50bce-143">Obiekt PrivateDnsZone reprezentujący strefę, w której ma zostać utworzony zestaw rekordów.</span><span class="sxs-lookup"><span data-stu-id="50bce-143">The PrivateDnsZone object representing the zone in which to create the record set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone
Parameter Sets: Mixed
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="50bce-144">-Nazwa_strefy</span><span class="sxs-lookup"><span data-stu-id="50bce-144">-ZoneName</span></span>
<span data-ttu-id="50bce-145">Strefa, w której istnieje zestaw rekordów (bez przerywanej kropki).</span><span class="sxs-lookup"><span data-stu-id="50bce-145">The zone in which the record set exists (without a terminating dot).</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50bce-146">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="50bce-146">-Confirm</span></span>
<span data-ttu-id="50bce-147">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50bce-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50bce-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50bce-148">-WhatIf</span></span>
<span data-ttu-id="50bce-149">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50bce-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50bce-150">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="50bce-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50bce-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50bce-151">CommonParameters</span></span>
<span data-ttu-id="50bce-152">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50bce-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50bce-153">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50bce-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50bce-154">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="50bce-154">INPUTS</span></span>

### <span data-ttu-id="50bce-155">Microsoft. Azure. Commands. PrivateDns. models. PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="50bce-155">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

### <span data-ttu-id="50bce-156">Microsoft. Azure. Commands. PrivateDns. models. PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="50bce-156">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

### <span data-ttu-id="50bce-157">System. String</span><span class="sxs-lookup"><span data-stu-id="50bce-157">System.String</span></span>

## <span data-ttu-id="50bce-158">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="50bce-158">OUTPUTS</span></span>

### <span data-ttu-id="50bce-159">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="50bce-159">System.Boolean</span></span>

## <span data-ttu-id="50bce-160">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="50bce-160">NOTES</span></span>

## <span data-ttu-id="50bce-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="50bce-161">RELATED LINKS</span></span>