---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/remove-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsZone.md
ms.openlocfilehash: 633a71788bb9578438053f7a296422e99e7c488e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180746"
---
# <span data-ttu-id="c6f14-101">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="c6f14-101">Remove-AzDnsZone</span></span>

## <span data-ttu-id="c6f14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6f14-102">SYNOPSIS</span></span>
<span data-ttu-id="c6f14-103">Usuwa strefę DNS z grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c6f14-103">Removes a DNS zone from a resource group.</span></span>

## <span data-ttu-id="c6f14-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c6f14-104">SYNTAX</span></span>

### <span data-ttu-id="c6f14-105">Pola</span><span class="sxs-lookup"><span data-stu-id="c6f14-105">Fields</span></span>
```
Remove-AzDnsZone -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6f14-106">Obiekt</span><span class="sxs-lookup"><span data-stu-id="c6f14-106">Object</span></span>
```
Remove-AzDnsZone -Zone <DnsZone> [-Overwrite] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6f14-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="c6f14-107">DESCRIPTION</span></span>
<span data-ttu-id="c6f14-108">Polecenie cmdlet **Remove-AzDnsZone** trwale usuwa strefę DNS (Domain Name System) z określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c6f14-108">The **Remove-AzDnsZone** cmdlet permanently deletes a Domain Name System (DNS) zone from a specified resource group.</span></span>
<span data-ttu-id="c6f14-109">Usuwane są również wszystkie zestawy rekordów zawarte w strefie.</span><span class="sxs-lookup"><span data-stu-id="c6f14-109">All record sets contained in the zone are also deleted.</span></span>
<span data-ttu-id="c6f14-110">Obiekt **DnsZone** można przekazać za pomocą parametru *Name* lub za pomocą operatora potoku. Można też określić parametry *Nazwa_strefy* i *NazwaGrupy Zasobów.*</span><span class="sxs-lookup"><span data-stu-id="c6f14-110">You can pass a **DnsZone** object using the *Name* parameter or by using the pipeline operator, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="c6f14-111">Możesz użyć parametru Confirm i $ConfirmPreference zmienną programu Windows PowerShell, aby określić, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c6f14-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="c6f14-112">Podczas określania strefy przy użyciu obiektu **DnsZone** (przekazywanego za pośrednictwem potoku lub parametru *Zone)* strefa nie jest usuwana, jeśli została zmieniona w systemie Azure DNS od czasu pobrania lokalnego obiektu **DnsZone** (tylko operacje bezpośrednio na zasobie strefy DNS liczą się jako zmiany, operacje na zestawach rekordów w strefie nie).</span><span class="sxs-lookup"><span data-stu-id="c6f14-112">When specifying the zone using a **DnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="c6f14-113">Zapewnia to ochronę przed jednoczesnym zmianą strefy.</span><span class="sxs-lookup"><span data-stu-id="c6f14-113">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="c6f14-114">Można to pominąć przy użyciu *parametru Zastąp,* który usuwa strefę niezależnie od jednoczesnych zmian.</span><span class="sxs-lookup"><span data-stu-id="c6f14-114">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="c6f14-115">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c6f14-115">EXAMPLES</span></span>

### <span data-ttu-id="c6f14-116">Przykład 1. Usuwanie strefy</span><span class="sxs-lookup"><span data-stu-id="c6f14-116">Example 1: Remove a zone</span></span>
```
PS C:\>Remove-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="c6f14-117">To polecenie usuwa strefę o nazwie myzone.com z grupy zasobów o nazwie MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="c6f14-117">This command removes the zone named myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="c6f14-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c6f14-118">PARAMETERS</span></span>

### <span data-ttu-id="c6f14-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6f14-119">-DefaultProfile</span></span>
<span data-ttu-id="c6f14-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="c6f14-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c6f14-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c6f14-121">-Name</span></span>
<span data-ttu-id="c6f14-122">Określa nazwę strefy DNS, która jest usuwana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6f14-122">Specifies the name of the DNS zone that this cmdlet removes.</span></span>
<span data-ttu-id="c6f14-123">Musisz także określić parametr *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="c6f14-123">You must also specify the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="c6f14-124">Możesz również określić strefę DNS, używając *parametru Zone.*</span><span class="sxs-lookup"><span data-stu-id="c6f14-124">Alternatively, you can specify the DNS zone using the *Zone* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6f14-125">— Zastąp</span><span class="sxs-lookup"><span data-stu-id="c6f14-125">-Overwrite</span></span>
<span data-ttu-id="c6f14-126">Podczas określania strefy przy użyciu obiektu **DnsZone** (przekazywanego za pośrednictwem potoku lub parametru *Zone)* strefa nie jest usuwana, jeśli została zmieniona w systemie Azure DNS od czasu pobrania lokalnego obiektu **DnsZone** (tylko operacje bezpośrednio na zasobie strefy DNS liczą się jako zmiany, operacje na zestawach rekordów w strefie nie).</span><span class="sxs-lookup"><span data-stu-id="c6f14-126">When specifying the zone using a **DnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="c6f14-127">Zapewnia to ochronę przed jednoczesnym zmianą strefy.</span><span class="sxs-lookup"><span data-stu-id="c6f14-127">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="c6f14-128">Można to pominąć przy użyciu *parametru Zastąp,* który usuwa strefę niezależnie od jednoczesnych zmian.</span><span class="sxs-lookup"><span data-stu-id="c6f14-128">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="c6f14-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c6f14-129">-PassThru</span></span>
<span data-ttu-id="c6f14-130">passthru</span><span class="sxs-lookup"><span data-stu-id="c6f14-130">passthru</span></span>

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

### <span data-ttu-id="c6f14-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6f14-131">-ResourceGroupName</span></span>
<span data-ttu-id="c6f14-132">Określa nazwę grupy zasobów zawierającej strefę do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="c6f14-132">Specifies the name of the resource group that contains the zone to remove.</span></span>
<span data-ttu-id="c6f14-133">Musisz także określić parametr *ZoneName.*</span><span class="sxs-lookup"><span data-stu-id="c6f14-133">You must also specify the *ZoneName* parameter.</span></span>
<span data-ttu-id="c6f14-134">Możesz również określić strefę DNS, używając obiektu **DnsZone,** przekazywanego przez parametr pipeline lub *Zone.*</span><span class="sxs-lookup"><span data-stu-id="c6f14-134">Alternatively, you can specify the DNS zone using a **DnsZone** object, passed via either the pipeline or the *Zone* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6f14-135">— Strefa</span><span class="sxs-lookup"><span data-stu-id="c6f14-135">-Zone</span></span>
<span data-ttu-id="c6f14-136">Określa strefę DNS do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="c6f14-136">Specifies the DNS zone to delete.</span></span>
<span data-ttu-id="c6f14-137">Obiekt **DnsZone** może być również przekazany za pośrednictwem potoku.</span><span class="sxs-lookup"><span data-stu-id="c6f14-137">The **DnsZone** object passed can also be passed via the pipeline.</span></span>
<span data-ttu-id="c6f14-138">Możesz również określić strefę DNS do usunięcia, używając parametrów *ZoneName* i *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="c6f14-138">Alternatively, you can specify the DNS zone to delete by using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c6f14-139">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c6f14-139">-Confirm</span></span>
<span data-ttu-id="c6f14-140">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c6f14-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6f14-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6f14-141">-WhatIf</span></span>
<span data-ttu-id="c6f14-142">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6f14-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6f14-143">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c6f14-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6f14-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6f14-144">CommonParameters</span></span>
<span data-ttu-id="c6f14-145">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6f14-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6f14-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6f14-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6f14-147">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c6f14-147">INPUTS</span></span>

### <span data-ttu-id="c6f14-148">System.String</span><span class="sxs-lookup"><span data-stu-id="c6f14-148">System.String</span></span>

### <span data-ttu-id="c6f14-149">Microsoft.Azure.Commands.Dns.DnsZone</span><span class="sxs-lookup"><span data-stu-id="c6f14-149">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="c6f14-150">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c6f14-150">OUTPUTS</span></span>

### <span data-ttu-id="c6f14-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c6f14-151">System.Boolean</span></span>

## <span data-ttu-id="c6f14-152">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c6f14-152">NOTES</span></span>
<span data-ttu-id="c6f14-153">Ze względu na potencjalnie duży wpływ usuwania strefy DNS to polecenie cmdlet domyślnie wyświetla monit o potwierdzenie, jeśli zmienna programu $ConfirmPreference Windows PowerShell ma dowolną wartość inną niż Brak.</span><span class="sxs-lookup"><span data-stu-id="c6f14-153">Due to the potentially high impact of deleting a DNS zone, by default, this cmdlet prompts for confirmation if the $ConfirmPreference Windows PowerShell variable has any value other than None.</span></span>
<span data-ttu-id="c6f14-154">Jeśli określisz *potwierdź* *lub potwierdź:$True,* to polecenie cmdlet wyświetli monit o potwierdzenie przed jego rozpoczęciem.</span><span class="sxs-lookup"><span data-stu-id="c6f14-154">If you specify *Confirm* or *Confirm:$True*, this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="c6f14-155">Jeśli określisz *polecenie Potwierdź:$False,* polecenie cmdlet nie wyświetli monitu o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c6f14-155">If you specify *Confirm:$False*, the cmdlet does not prompt you for confirmation.</span></span> 

## <span data-ttu-id="c6f14-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c6f14-156">RELATED LINKS</span></span>

[<span data-ttu-id="c6f14-157">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="c6f14-157">Get-AzDnsZone</span></span>](./Get-AzDnsZone.md)

[<span data-ttu-id="c6f14-158">New-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="c6f14-158">New-AzDnsZone</span></span>](./New-AzDnsZone.md)

[<span data-ttu-id="c6f14-159">Set-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="c6f14-159">Set-AzDnsZone</span></span>](./Set-AzDnsZone.md)
