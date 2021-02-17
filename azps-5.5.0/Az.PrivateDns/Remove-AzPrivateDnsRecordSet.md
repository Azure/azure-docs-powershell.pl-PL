---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/remove-azprivatednsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsRecordSet.md
ms.openlocfilehash: 865ab4ab3cca9d921fc8c40e9c6ae5cd03eaf00a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186634"
---
# <span data-ttu-id="3cc4a-101">Remove-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="3cc4a-101">Remove-AzPrivateDnsRecordSet</span></span>

## <span data-ttu-id="3cc4a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3cc4a-102">SYNOPSIS</span></span>
<span data-ttu-id="3cc4a-103">Usuwa zestaw rekordów z prywatnej strefy DNS.</span><span class="sxs-lookup"><span data-stu-id="3cc4a-103">Deletes a record set from a Private DNS zone.</span></span>

## <span data-ttu-id="3cc4a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3cc4a-104">SYNTAX</span></span>

### <span data-ttu-id="3cc4a-105">Pola (domyślne)</span><span class="sxs-lookup"><span data-stu-id="3cc4a-105">Fields (Default)</span></span>
```
Remove-AzPrivateDnsRecordSet -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -RecordType <RecordType> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3cc4a-106">Mieszany</span><span class="sxs-lookup"><span data-stu-id="3cc4a-106">Mixed</span></span>
```
Remove-AzPrivateDnsRecordSet -Zone <PSPrivateDnsZone> -Name <String> -RecordType <RecordType> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cc4a-107">Obiekt</span><span class="sxs-lookup"><span data-stu-id="3cc4a-107">Object</span></span>
```
Remove-AzPrivateDnsRecordSet -RecordSet <PSPrivateDnsRecordSet> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cc4a-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="3cc4a-108">ResourceId</span></span>
```
Remove-AzPrivateDnsRecordSet -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3cc4a-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="3cc4a-109">DESCRIPTION</span></span>
<span data-ttu-id="3cc4a-110">Polecenie Remove-AzPrivateDnsRecordSet cmdlet usuwa określony zestaw rekordów z określonej strefy.</span><span class="sxs-lookup"><span data-stu-id="3cc4a-110">The Remove-AzPrivateDnsRecordSet cmdlet deletes the specified record set from the specified zone.</span></span> <span data-ttu-id="3cc4a-111">Nie można usuwać rekordów SOA, które są automatycznie tworzone w wierzchołku strefy prywatnej.</span><span class="sxs-lookup"><span data-stu-id="3cc4a-111">You cannot delete SOA records that are automatically created at the private zone apex.</span></span> <span data-ttu-id="3cc4a-112">Obiekt RecordSet można przekazać do tego polecenia cmdlet, używając operatora potoku, parametru lub jako identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="3cc4a-112">You can pass a RecordSet object to this cmdlet by using the pipeline operator or as a parameter or as a ResourceId.</span></span> <span data-ttu-id="3cc4a-113">Aby zidentyfikować zestaw rekordów według nazwy i typu bez użycia obiektu RecordSet, musisz przekazać strefę jako obiekt PSPrivateDnsZone do tego polecenia cmdlet, używając operatora potoku lub parametru. Możesz również określić parametry ZoneName i ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="3cc4a-113">To identify a record set by name and type without using a RecordSet object, you must pass the zone as a PSPrivateDnsZone object to this cmdlet by using the pipeline operator or as a parameter, or alternatively you can specify the ZoneName and ResourceGroupName parameters.</span></span> <span data-ttu-id="3cc4a-114">Możesz użyć parametru Confirm i $ConfirmPreference zmienną programu Windows PowerShell, aby określić, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3cc4a-114">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span> <span data-ttu-id="3cc4a-115">Podczas określania zestawu rekordów przy użyciu obiektu RecordSet zestaw rekordów nie jest usuwany, jeśli został zmieniony w prywatnym systemie DNS platformy Azure od czasu pobrania lokalnego obiektu RecordSet.</span><span class="sxs-lookup"><span data-stu-id="3cc4a-115">When specifying the record set using a RecordSet object, the record set is not deleted if it has been changed in Azure Private DNS since the local RecordSet object was retrieved.</span></span> <span data-ttu-id="3cc4a-116">Zapewnia to ochronę w przypadku jednoczesnych zmian.</span><span class="sxs-lookup"><span data-stu-id="3cc4a-116">This provides protection for concurrent changes.</span></span> <span data-ttu-id="3cc4a-117">Można to pominąć przy użyciu parametru Zastąp, który usuwa zestaw rekordów niezależnie od jednoczesnych zmian.</span><span class="sxs-lookup"><span data-stu-id="3cc4a-117">You can suppress this by using the Overwrite parameter, which deletes the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="3cc4a-118">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3cc4a-118">EXAMPLES</span></span>

### <span data-ttu-id="3cc4a-119">Przykład 1. Usuwanie zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="3cc4a-119">Example 1: Remove a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="3cc4a-120">Pierwsze polecenie pobiera określony zestaw rekordów, a następnie zapisuje go w $RecordSet zmienną. Drugie polecenie usuwa zestaw rekordów z $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="3cc4a-120">The first command gets the specified record set, and then stores it in the $RecordSet variable.The second command removes the record set in $RecordSet.</span></span>

### <span data-ttu-id="3cc4a-121">Przykład 2. Usuwanie zestawu rekordów i pomijanie wszystkich potwierdzeń</span><span class="sxs-lookup"><span data-stu-id="3cc4a-121">Example 2: Remove a record set and suppress all confirmation</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzPrivateDnsRecordSet -RecordSet $RecordSet -Confirm:$False -Overwrite

# Alternatively, the record set can be removed as follows.  In this case,
# because the record set is specified by name rather than by object, the
# Overwrite parameter is not applicable.

PS C:\> Remove-AzPrivateDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Confirm:$False
```

<span data-ttu-id="3cc4a-122">Pierwsze polecenie pobiera określony zestaw rekordów.</span><span class="sxs-lookup"><span data-stu-id="3cc4a-122">The first command gets the specified record set.</span></span> <span data-ttu-id="3cc4a-123">Drugie polecenie usuwa zestaw rekordów, nawet jeśli zmienił się w międzyczasie.</span><span class="sxs-lookup"><span data-stu-id="3cc4a-123">The second command deletes the record set, even if it has changed in the meantime.</span></span> <span data-ttu-id="3cc4a-124">Monity o potwierdzenie są pomijane.</span><span class="sxs-lookup"><span data-stu-id="3cc4a-124">Confirmation prompts are suppressed.</span></span>

## <span data-ttu-id="3cc4a-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3cc4a-125">PARAMETERS</span></span>

### <span data-ttu-id="3cc4a-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cc4a-126">-DefaultProfile</span></span>
<span data-ttu-id="3cc4a-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3cc4a-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3cc4a-128">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="3cc4a-128">-Name</span></span>
<span data-ttu-id="3cc4a-129">Nazwa rekordów w zestawie rekordów (względem nazwy strefy i bez kropki kończącej).</span><span class="sxs-lookup"><span data-stu-id="3cc4a-129">The name of the records in the record set (relative to the name of the zone and without a terminating dot).</span></span>

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

### <span data-ttu-id="3cc4a-130">— Zastąp</span><span class="sxs-lookup"><span data-stu-id="3cc4a-130">-Overwrite</span></span>
<span data-ttu-id="3cc4a-131">Nie używaj pola ETag parametru RecordSet w celu przeprowadzania optymistycznych testów współbieżności.</span><span class="sxs-lookup"><span data-stu-id="3cc4a-131">Do not use the ETag field of the RecordSet parameter for optimistic concurrency checks.</span></span>

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

### <span data-ttu-id="3cc4a-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3cc4a-132">-PassThru</span></span>
<span data-ttu-id="3cc4a-133">Służy do przekazywania wyniku (wartości logicznych) operacji usunięcia strefy prywatnej w dalszej części potoku.</span><span class="sxs-lookup"><span data-stu-id="3cc4a-133">Used for passing the result (boolean) of the operation delete private zone further down the pipeline.</span></span>

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

### <span data-ttu-id="3cc4a-134">- RecordSet</span><span class="sxs-lookup"><span data-stu-id="3cc4a-134">-RecordSet</span></span>
<span data-ttu-id="3cc4a-135">Zestaw rekordów, w którym należy dodać rekord.</span><span class="sxs-lookup"><span data-stu-id="3cc4a-135">The record set in which to add the record.</span></span>

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

### <span data-ttu-id="3cc4a-136">-RecordType</span><span class="sxs-lookup"><span data-stu-id="3cc4a-136">-RecordType</span></span>
<span data-ttu-id="3cc4a-137">Typ prywatnych rekordów DNS w zestawie rekordów.</span><span class="sxs-lookup"><span data-stu-id="3cc4a-137">The type of Private DNS records in the record set.</span></span>

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

### <span data-ttu-id="3cc4a-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cc4a-138">-ResourceGroupName</span></span>
<span data-ttu-id="3cc4a-139">Grupa zasobów, do której należy strefa.</span><span class="sxs-lookup"><span data-stu-id="3cc4a-139">The resource group to which the zone belongs.</span></span>

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

### <span data-ttu-id="3cc4a-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3cc4a-140">-ResourceId</span></span>
<span data-ttu-id="3cc4a-141">Private DNS RecordSet ResourceID.</span><span class="sxs-lookup"><span data-stu-id="3cc4a-141">Private DNS RecordSet ResourceID.</span></span>

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

### <span data-ttu-id="3cc4a-142">— Strefa</span><span class="sxs-lookup"><span data-stu-id="3cc4a-142">-Zone</span></span>
<span data-ttu-id="3cc4a-143">Obiekt PrivateDnsZone reprezentujący strefę, w której należy utworzyć zestaw rekordów.</span><span class="sxs-lookup"><span data-stu-id="3cc4a-143">The PrivateDnsZone object representing the zone in which to create the record set.</span></span>

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

### <span data-ttu-id="3cc4a-144">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="3cc4a-144">-ZoneName</span></span>
<span data-ttu-id="3cc4a-145">Strefa, w której istnieje zestaw rekordów (bez kropki kończącej).</span><span class="sxs-lookup"><span data-stu-id="3cc4a-145">The zone in which the record set exists (without a terminating dot).</span></span>

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

### <span data-ttu-id="3cc4a-146">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3cc4a-146">-Confirm</span></span>
<span data-ttu-id="3cc4a-147">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3cc4a-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3cc4a-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cc4a-148">-WhatIf</span></span>
<span data-ttu-id="3cc4a-149">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3cc4a-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3cc4a-150">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="3cc4a-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3cc4a-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cc4a-151">CommonParameters</span></span>
<span data-ttu-id="3cc4a-152">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cc4a-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cc4a-153">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3cc4a-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cc4a-154">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3cc4a-154">INPUTS</span></span>

### <span data-ttu-id="3cc4a-155">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="3cc4a-155">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

### <span data-ttu-id="3cc4a-156">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="3cc4a-156">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

### <span data-ttu-id="3cc4a-157">System.String</span><span class="sxs-lookup"><span data-stu-id="3cc4a-157">System.String</span></span>

## <span data-ttu-id="3cc4a-158">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3cc4a-158">OUTPUTS</span></span>

### <span data-ttu-id="3cc4a-159">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3cc4a-159">System.Boolean</span></span>

## <span data-ttu-id="3cc4a-160">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3cc4a-160">NOTES</span></span>

## <span data-ttu-id="3cc4a-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3cc4a-161">RELATED LINKS</span></span>
