---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/Set-AzPrivateDnsZone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsZone.md
ms.openlocfilehash: 06b8a8bd7027b95d7f51e186b0184707ffd296a8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179011"
---
# <span data-ttu-id="b2b7b-101">Set-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="b2b7b-101">Set-AzPrivateDnsZone</span></span>

## <span data-ttu-id="b2b7b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2b7b-102">SYNOPSIS</span></span>
<span data-ttu-id="b2b7b-103">Aktualizuje prywatną strefę DNS z grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b2b7b-103">Updates a Private DNS zone from a resource group.</span></span>

## <span data-ttu-id="b2b7b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b2b7b-104">SYNTAX</span></span>

### <span data-ttu-id="b2b7b-105">Pola (domyślne)</span><span class="sxs-lookup"><span data-stu-id="b2b7b-105">Fields (Default)</span></span>
```
Set-AzPrivateDnsZone -ResourceGroupName <String> -Name <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2b7b-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b2b7b-106">ResourceId</span></span>
```
Set-AzPrivateDnsZone -ResourceId <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2b7b-107">Obiekt</span><span class="sxs-lookup"><span data-stu-id="b2b7b-107">Object</span></span>
```
Set-AzPrivateDnsZone -PrivateZone <PSPrivateDnsZone> [-Tag <Hashtable>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2b7b-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="b2b7b-108">DESCRIPTION</span></span>
<span data-ttu-id="b2b7b-109">Polecenie cmdlet **Set-AzPrivateDnsZone** trwale aktualizuje strefę dns (Domain Name System) z określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b2b7b-109">The **Set-AzPrivateDnsZone** cmdlet permanently updates a private Domain Name System (DNS) zone from a specified resource group.</span></span>
<span data-ttu-id="b2b7b-110">Obiekt **PrivateDnsZone** można przekazać za pomocą parametru *PrivateZone* lub za pomocą operatora potoku albo możesz również określić parametry *Name* (Nazwa) i *ResourceGroupName (Nazwa* grupy zasobów).</span><span class="sxs-lookup"><span data-stu-id="b2b7b-110">You can pass a **PrivateDnsZone** object using the *PrivateZone* parameter or by using the pipeline operator, or alternatively you can specify the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="b2b7b-111">Możesz użyć parametru Confirm i $ConfirmPreference zmienną programu Windows PowerShell, aby określić, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b2b7b-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="b2b7b-112">Podczas określania strefy przy użyciu obiektu **PrivateDnsZone** (przekazywanego za pośrednictwem potoku lub parametru *Zone)* strefa nie jest aktualizowana, jeśli została zmieniona w systemie Azure DNS od czasu pobrania lokalnego obiektu **PrivateDnsZone** (tylko operacje bezpośrednio na liczniku zasobów strefy DNS jako zmiany, operacje na zestawach rekordów w strefie nie).</span><span class="sxs-lookup"><span data-stu-id="b2b7b-112">When specifying the zone using a **PrivateDnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not updated if it has been changed in Azure DNS since the local **PrivateDnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="b2b7b-113">Zapewnia to ochronę przed jednoczesnym zmianą strefy.</span><span class="sxs-lookup"><span data-stu-id="b2b7b-113">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="b2b7b-114">Można to pominąć przy użyciu *parametru Zastąp,* który aktualizuje strefę niezależnie od jednoczesnych zmian.</span><span class="sxs-lookup"><span data-stu-id="b2b7b-114">This can be suppressed using the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="b2b7b-115">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b2b7b-115">EXAMPLES</span></span>

### <span data-ttu-id="b2b7b-116">Przykład 1. Aktualizacja strefy prywatnej</span><span class="sxs-lookup"><span data-stu-id="b2b7b-116">Example 1: Updates a private zone</span></span>
```
PS C:\>Set-AzPrivateDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup" -Tag @{tag1="value1";tag2="value2"}


This command updates the zone named myzone.com from the resource group named MyResourceGroup with the tags provided. Use Get-AzPrivateDnsZone to retrieve the updated zone. Updated zone would look something like this:

Name                          : myzone.com
ResourceId                    : "/subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/PrivateZones/myzone.com"
ResourceGroupName             : MyResourceGroup
Location                      : 
Etag                          : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                          : {tag1="value1";tag2="value2"}
NumberOfRecordSets            : 1
MaxNumberOfRecordSets         : 5000
```

## <span data-ttu-id="b2b7b-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b2b7b-117">PARAMETERS</span></span>

### <span data-ttu-id="b2b7b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2b7b-118">-DefaultProfile</span></span>
<span data-ttu-id="b2b7b-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="b2b7b-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b2b7b-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b2b7b-120">-Name</span></span>
<span data-ttu-id="b2b7b-121">Określa nazwę prywatnej strefy DNS, która będzie aktualizowana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2b7b-121">Specifies the name of the Private DNS zone that this cmdlet updates.</span></span>
<span data-ttu-id="b2b7b-122">Musisz także określić parametr *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="b2b7b-122">You must also specify the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="b2b7b-123">Możesz również określić prywatną strefę DNS przy użyciu *parametru Zone.*</span><span class="sxs-lookup"><span data-stu-id="b2b7b-123">Alternatively, you can specify the private DNS zone using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="b2b7b-124">— Zastąp</span><span class="sxs-lookup"><span data-stu-id="b2b7b-124">-Overwrite</span></span>
<span data-ttu-id="b2b7b-125">Podczas określania strefy przy użyciu obiektu **PrivateDnsZone** (przekazywanego za pośrednictwem potoku lub parametru *Zone)* strefa nie jest aktualizowana, jeśli została zmieniona w systemie Azure DNS od czasu pobrania lokalnego obiektu **DnsZone** (tylko operacje bezpośrednio na zasobie strefy DNS są liczone jako zmiany, operacje na zestawach rekordów w obrębie strefy nie).</span><span class="sxs-lookup"><span data-stu-id="b2b7b-125">When specifying the zone using a **PrivateDnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not updated if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="b2b7b-126">Zapewnia to ochronę przed jednoczesnym zmianą strefy.</span><span class="sxs-lookup"><span data-stu-id="b2b7b-126">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="b2b7b-127">Można to pominąć przy użyciu *parametru Zastąp,* który aktualizuje strefę niezależnie od jednoczesnych zmian.</span><span class="sxs-lookup"><span data-stu-id="b2b7b-127">This can be suppressed using the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="b2b7b-128">— PrivateZone</span><span class="sxs-lookup"><span data-stu-id="b2b7b-128">-PrivateZone</span></span>
<span data-ttu-id="b2b7b-129">Obiekt strefy, który należy ustawić.</span><span class="sxs-lookup"><span data-stu-id="b2b7b-129">The zone object to set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b2b7b-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2b7b-130">-ResourceGroupName</span></span>
<span data-ttu-id="b2b7b-131">Określa nazwę grupy zasobów zawierającej strefę do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="b2b7b-131">Specifies the name of the resource group that contains the zone to be updated.</span></span>
<span data-ttu-id="b2b7b-132">Musisz także określić parametr *ZoneName.*</span><span class="sxs-lookup"><span data-stu-id="b2b7b-132">You must also specify the *ZoneName* parameter.</span></span>
<span data-ttu-id="b2b7b-133">Możesz również określić prywatną strefę DNS przy użyciu obiektu **DnsZone** przekazywanego za pośrednictwem potoku lub *parametru Zone.*</span><span class="sxs-lookup"><span data-stu-id="b2b7b-133">Alternatively, you can specify the private DNS zone using a **DnsZone** object, passed via either the pipeline or the *Zone* parameter.</span></span>

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

### <span data-ttu-id="b2b7b-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b2b7b-134">-ResourceId</span></span>
<span data-ttu-id="b2b7b-135">Private DNS Zone ResourceID (Prywatny adres DNS Strefy ResourceID).</span><span class="sxs-lookup"><span data-stu-id="b2b7b-135">Private DNS Zone ResourceID.</span></span>

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

### <span data-ttu-id="b2b7b-136">— Tag</span><span class="sxs-lookup"><span data-stu-id="b2b7b-136">-Tag</span></span>
<span data-ttu-id="b2b7b-137">Tabela skrótów reprezentująca tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="b2b7b-137">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2b7b-138">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b2b7b-138">-Confirm</span></span>
<span data-ttu-id="b2b7b-139">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b2b7b-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2b7b-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2b7b-140">-WhatIf</span></span>
<span data-ttu-id="b2b7b-141">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2b7b-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2b7b-142">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b2b7b-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2b7b-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2b7b-143">CommonParameters</span></span>
<span data-ttu-id="b2b7b-144">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2b7b-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2b7b-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2b7b-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2b7b-146">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b2b7b-146">INPUTS</span></span>

### <span data-ttu-id="b2b7b-147">System.String</span><span class="sxs-lookup"><span data-stu-id="b2b7b-147">System.String</span></span>

### <span data-ttu-id="b2b7b-148">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="b2b7b-148">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

## <span data-ttu-id="b2b7b-149">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b2b7b-149">OUTPUTS</span></span>

### <span data-ttu-id="b2b7b-150">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="b2b7b-150">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

## <span data-ttu-id="b2b7b-151">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b2b7b-151">NOTES</span></span>

## <span data-ttu-id="b2b7b-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b2b7b-152">RELATED LINKS</span></span>

[<span data-ttu-id="b2b7b-153">Get-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="b2b7b-153">Get-AzPrivateDnsZone</span></span>](./Get-AzPrivateDnsZone.md)

[<span data-ttu-id="b2b7b-154">New-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="b2b7b-154">New-AzPrivateDnsZone</span></span>](./New-AzPrivateDnsZone.md)

[<span data-ttu-id="b2b7b-155">Set-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="b2b7b-155">Set-AzPrivateDnsZone</span></span>](./Set-AzPrivateDnsZone.md)
