---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 40179CF3-7896-4C45-BC18-4CB653B245B6
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/get-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsRecordSet.md
ms.openlocfilehash: b64432364b9c86a1153ba9a535d70645cf15d4d1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196347"
---
# <span data-ttu-id="93ff8-101">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="93ff8-101">Get-AzDnsRecordSet</span></span>

## <span data-ttu-id="93ff8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93ff8-102">SYNOPSIS</span></span>
<span data-ttu-id="93ff8-103">Pobiera zestaw rekordów DNS.</span><span class="sxs-lookup"><span data-stu-id="93ff8-103">Gets a DNS record set.</span></span>

## <span data-ttu-id="93ff8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="93ff8-104">SYNTAX</span></span>

### <span data-ttu-id="93ff8-105">Pola</span><span class="sxs-lookup"><span data-stu-id="93ff8-105">Fields</span></span>
```
Get-AzDnsRecordSet [-Name <String>] -ZoneName <String> -ResourceGroupName <String> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93ff8-106">Obiekt</span><span class="sxs-lookup"><span data-stu-id="93ff8-106">Object</span></span>
```
Get-AzDnsRecordSet [-Name <String>] -Zone <DnsZone> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93ff8-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="93ff8-107">DESCRIPTION</span></span>
<span data-ttu-id="93ff8-108">Polecenie **cmdlet Get-AzDnsRecordSet** pobiera zestaw rekordów DNS (Domain Name System) o określonej nazwie i typie w określonej strefie.</span><span class="sxs-lookup"><span data-stu-id="93ff8-108">The **Get-AzDnsRecordSet** cmdlet gets the Domain Name System (DNS) record set with the specified name and type, in the specified zone.</span></span>
<span data-ttu-id="93ff8-109">Jeśli parametry Name  (Nazwa) lub *RecordType* (Typ Rekordu) nie zostaną określone, to polecenie cmdlet zwróci wszystkie zestawy rekordów określonego typu w strefie.</span><span class="sxs-lookup"><span data-stu-id="93ff8-109">If you do not specify the *Name* or *RecordType* parameters, this cmdlet returns all record sets of the specified type in the zone.</span></span>
<span data-ttu-id="93ff8-110">Jeśli określisz parametr *RecordType,* ale nie parametr *Name,* to polecenie cmdlet zwróci wszystkie zestawy rekordów określonego typu rekordu.</span><span class="sxs-lookup"><span data-stu-id="93ff8-110">If you specify the *RecordType* parameter but not the *Name* parameter, this cmdlet returns all record sets of the specified record type.</span></span>
<span data-ttu-id="93ff8-111">Za pomocą operatora potoku możesz przekazać obiekt **DnsZone** do tego polecenia cmdlet lub przekazać obiekt **DnsZone** jako parametr *Strefy* lub możesz też określić grupę strefy i zasobów według nazwy.</span><span class="sxs-lookup"><span data-stu-id="93ff8-111">You can use the pipeline operator to pass a **DnsZone** object to this cmdlet, or you can pass a **DnsZone** object as the *Zone* parameter, or alternatively you can specify the zone and resource group by name.</span></span>

## <span data-ttu-id="93ff8-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="93ff8-112">EXAMPLES</span></span>

### <span data-ttu-id="93ff8-113">Przykład 1. Uzyskiwanie zestawów rekordów o określonej nazwie i typie</span><span class="sxs-lookup"><span data-stu-id="93ff8-113">Example 1: Get record sets with a specified name and type</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "www" -RecordType A
```

<span data-ttu-id="93ff8-114">To polecenie pobiera zestaw rekordów typu A o nazwie www w określonej grupie zasobów i strefie, a następnie przechowuje go w $RecordSet zmienną.</span><span class="sxs-lookup"><span data-stu-id="93ff8-114">This command gets the record set of record type A named www in the specified resource group and zone, and then stores it in the $RecordSet variable.</span></span>
<span data-ttu-id="93ff8-115">Ponieważ parametry *Name (Nazwa)* *i RecordType (Typ* Rekordu) są określone, zwracany jest tylko jeden obiekt **RecordSet.**</span><span class="sxs-lookup"><span data-stu-id="93ff8-115">Because the *Name* and *RecordType* parameters are specified, only one **RecordSet** object is returned.</span></span>

### <span data-ttu-id="93ff8-116">Przykład 2. Uzyskiwanie zestawów rekordów określonego typu</span><span class="sxs-lookup"><span data-stu-id="93ff8-116">Example 2: Get record sets of a specified type</span></span>
```
PS C:\>$RecordSets = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -RecordType A
```

<span data-ttu-id="93ff8-117">To polecenie pobiera tablicę wszystkich zestawów rekordów typu A w strefie myzone.com w grupie zasobów o nazwie MyResourceGroup, a następnie przechowuje je w $RecordSets zmienną.</span><span class="sxs-lookup"><span data-stu-id="93ff8-117">This command gets an array of all record sets of record type A in the zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="93ff8-118">Przykład 3. Uzyskiwanie wszystkich zestawów rekordów w strefie</span><span class="sxs-lookup"><span data-stu-id="93ff8-118">Example 3: Get all record sets in a zone</span></span>
```
PS C:\>$RecordSets = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
```

<span data-ttu-id="93ff8-119">To polecenie pobiera tablicę wszystkich zestawów rekordów w strefie o nazwie myzone.com w grupie zasobów o nazwie MyResourceGroup, a następnie przechowuje je w $RecordSets zmienną.</span><span class="sxs-lookup"><span data-stu-id="93ff8-119">This command gets an array of all record sets in the zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="93ff8-120">Przykład 4. Uzyskiwanie wszystkich zestawów rekordów w strefie przy użyciu obiektu DnsZone</span><span class="sxs-lookup"><span data-stu-id="93ff8-120">Example 4: Get all record sets in a zone, using a DnsZone object</span></span>
```
PS C:\> $Zone = Get-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $RecordSets = Get-AzDnsRecordSet -Zone $Zone
```

<span data-ttu-id="93ff8-121">Ten przykład jest odpowiednikiem powyższego przykładu 3.</span><span class="sxs-lookup"><span data-stu-id="93ff8-121">This example is equivalent to Example 3 above.</span></span>
<span data-ttu-id="93ff8-122">Tym razem strefa jest określana przy użyciu obiektu strefy.</span><span class="sxs-lookup"><span data-stu-id="93ff8-122">This time, the zone is specified using a zone object.</span></span>

## <span data-ttu-id="93ff8-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="93ff8-123">PARAMETERS</span></span>

### <span data-ttu-id="93ff8-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93ff8-124">-DefaultProfile</span></span>
<span data-ttu-id="93ff8-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="93ff8-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="93ff8-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="93ff8-126">-Name</span></span>
<span data-ttu-id="93ff8-127">Określa nazwę zestawu rekordów **do** uzyskania.</span><span class="sxs-lookup"><span data-stu-id="93ff8-127">Specifies the name of the **RecordSet** to get.</span></span>
<span data-ttu-id="93ff8-128">Jeśli parametr Name nie zostanie *określony,* zostaną zwrócone wszystkie zestawy rekordów określonego typu.</span><span class="sxs-lookup"><span data-stu-id="93ff8-128">If you do not specify the *Name* parameter, all record sets of the specified type are returned.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93ff8-129">-RecordType</span><span class="sxs-lookup"><span data-stu-id="93ff8-129">-RecordType</span></span>
<span data-ttu-id="93ff8-130">Określa typ rekordu DNS, który otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93ff8-130">Specifies the type of DNS record that this cmdlet gets.</span></span>
<span data-ttu-id="93ff8-131">Prawidłowe wartości to:</span><span class="sxs-lookup"><span data-stu-id="93ff8-131">Valid values are:</span></span> 
- <span data-ttu-id="93ff8-132">A</span><span class="sxs-lookup"><span data-stu-id="93ff8-132">A</span></span>
- <span data-ttu-id="93ff8-133">AAAA</span><span class="sxs-lookup"><span data-stu-id="93ff8-133">AAAA</span></span>
- <span data-ttu-id="93ff8-134">CNAME</span><span class="sxs-lookup"><span data-stu-id="93ff8-134">CNAME</span></span>
- <span data-ttu-id="93ff8-135">MX</span><span class="sxs-lookup"><span data-stu-id="93ff8-135">MX</span></span>
- <span data-ttu-id="93ff8-136">NS</span><span class="sxs-lookup"><span data-stu-id="93ff8-136">NS</span></span>
- <span data-ttu-id="93ff8-137">PTR</span><span class="sxs-lookup"><span data-stu-id="93ff8-137">PTR</span></span>
- <span data-ttu-id="93ff8-138">SOA</span><span class="sxs-lookup"><span data-stu-id="93ff8-138">SOA</span></span>
- <span data-ttu-id="93ff8-139">SRV</span><span class="sxs-lookup"><span data-stu-id="93ff8-139">SRV</span></span>
- <span data-ttu-id="93ff8-140">TXT Jeśli nie określisz *parametru RecordType,* musisz również pominąć parametr *Name.*</span><span class="sxs-lookup"><span data-stu-id="93ff8-140">TXT If you do not specify the *RecordType* parameter, you must also omit the *Name* parameter.</span></span> <span data-ttu-id="93ff8-141">To polecenie cmdlet zwraca wszystkie zestawy rekordów w strefie (wszystkie nazwy i typy).</span><span class="sxs-lookup"><span data-stu-id="93ff8-141">This cmdlet then returns all record sets in the zone (of all names and types).</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Dns.Models.RecordType]
Parameter Sets: (All)
Aliases:
Accepted values: A, AAAA, CAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93ff8-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93ff8-142">-ResourceGroupName</span></span>
<span data-ttu-id="93ff8-143">Określa grupę zasobów zawierającą strefę DNS.</span><span class="sxs-lookup"><span data-stu-id="93ff8-143">Specifies the resource group that contains the DNS zone.</span></span>
<span data-ttu-id="93ff8-144">Należy również określić nazwę strefy przy użyciu *parametru ZoneName.*</span><span class="sxs-lookup"><span data-stu-id="93ff8-144">The zone name must also be specified, using the *ZoneName* parameter.</span></span>
<span data-ttu-id="93ff8-145">Możesz również określić strefę i grupę zasobów, przechodząc do obiektu **DnsZone** przy użyciu *parametru Zone.*</span><span class="sxs-lookup"><span data-stu-id="93ff8-145">Alternatively, you can specify the zone and resource group by passing in a **DnsZone** object using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="93ff8-146">— Strefa</span><span class="sxs-lookup"><span data-stu-id="93ff8-146">-Zone</span></span>
<span data-ttu-id="93ff8-147">Określa strefę DNS zawierającą zestaw rekordów, który otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93ff8-147">Specifies the DNS zone that contains the record set that this cmdlet gets.</span></span>
<span data-ttu-id="93ff8-148">Można również określić strefę przy użyciu parametrów *Nazwa_strefy* i *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="93ff8-148">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="93ff8-149">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="93ff8-149">-ZoneName</span></span>
<span data-ttu-id="93ff8-150">Określa nazwę strefy DNS zawierającej zestaw rekordów do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="93ff8-150">Specifies the name of the DNS zone that contains the record set to get.</span></span>
<span data-ttu-id="93ff8-151">Grupę zasobów zawierającą strefę należy również określić przy użyciu *parametru ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="93ff8-151">The resource group containing the zone must also be specified, using the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="93ff8-152">Możesz również określić strefę i grupę zasobów, przechodząc do obiektu DNS Zone przy użyciu *parametru Zone.*</span><span class="sxs-lookup"><span data-stu-id="93ff8-152">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="93ff8-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93ff8-153">CommonParameters</span></span>
<span data-ttu-id="93ff8-154">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93ff8-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93ff8-155">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93ff8-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93ff8-156">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="93ff8-156">INPUTS</span></span>

### <span data-ttu-id="93ff8-157">System.String</span><span class="sxs-lookup"><span data-stu-id="93ff8-157">System.String</span></span>

### <span data-ttu-id="93ff8-158">Microsoft.Azure.Commands.Dns.DnsZone</span><span class="sxs-lookup"><span data-stu-id="93ff8-158">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

### <span data-ttu-id="93ff8-159">System.Nullable'1[[Microsoft.Azure.Management.Dns.Models.RecordType, Microsoft.Azure.Management.Dns, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="93ff8-159">System.Nullable\`1[[Microsoft.Azure.Management.Dns.Models.RecordType, Microsoft.Azure.Management.Dns, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="93ff8-160">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="93ff8-160">OUTPUTS</span></span>

### <span data-ttu-id="93ff8-161">Microsoft.Azure.Commands.Dns.DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="93ff8-161">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="93ff8-162">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="93ff8-162">NOTES</span></span>

## <span data-ttu-id="93ff8-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="93ff8-163">RELATED LINKS</span></span>

[<span data-ttu-id="93ff8-164">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="93ff8-164">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="93ff8-165">Remove-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="93ff8-165">Remove-AzDnsRecordSet</span></span>](./Remove-AzDnsRecordSet.md)

[<span data-ttu-id="93ff8-166">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="93ff8-166">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)


