---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: https://docs.microsoft.com/powershell/module/az.dns/get-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsZone.md
ms.openlocfilehash: a788cf3638d124dac164f19171f1be89afc2e385
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984824"
---
# <span data-ttu-id="c263e-101">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="c263e-101">Get-AzDnsZone</span></span>

## <span data-ttu-id="c263e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c263e-102">SYNOPSIS</span></span>
<span data-ttu-id="c263e-103">Pobiera strefę DNS.</span><span class="sxs-lookup"><span data-stu-id="c263e-103">Gets a DNS zone.</span></span>

## <span data-ttu-id="c263e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c263e-104">SYNTAX</span></span>

### <span data-ttu-id="c263e-105">Domyślne (domyślne)</span><span class="sxs-lookup"><span data-stu-id="c263e-105">Default (Default)</span></span>
```
Get-AzDnsZone [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c263e-106">ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c263e-106">ResourceGroup</span></span>
```
Get-AzDnsZone [-Name <String>] -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c263e-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="c263e-107">DESCRIPTION</span></span>
<span data-ttu-id="c263e-108">Polecenie **cmdlet Get-AzDnsZone** pobiera strefę systemu nazw domen (DNS) z określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c263e-108">The **Get-AzDnsZone** cmdlet gets a Domain Name System (DNS) zone from the specified resource group.</span></span>
<span data-ttu-id="c263e-109">W przypadku określenia *parametru Name* zwracany jest jeden obiekt **DnsZone.**</span><span class="sxs-lookup"><span data-stu-id="c263e-109">If you specify the *Name* parameter, a single **DnsZone** object is returned.</span></span>
<span data-ttu-id="c263e-110">Jeśli parametr Name  nie zostanie określony, zostanie zwrócona tablica zawierająca wszystkie strefy w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="c263e-110">If you do not specify the *Name* parameter, an array containing all of the zones in the specified resource group is returned.</span></span>
<span data-ttu-id="c263e-111">Za pomocą obiektu **DnsZone** można zaktualizować strefę, na przykład można dodać do niego obiekty **RecordSet.**</span><span class="sxs-lookup"><span data-stu-id="c263e-111">You can use the **DnsZone** object to update the zone, for example you can add **RecordSet** objects to it.</span></span>

## <span data-ttu-id="c263e-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c263e-112">EXAMPLES</span></span>

### <span data-ttu-id="c263e-113">Przykład 1. Uzyskiwanie strefy</span><span class="sxs-lookup"><span data-stu-id="c263e-113">Example 1: Get a zone</span></span>
```
PS C:\> $Zone = Get-AzDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"
```

<span data-ttu-id="c263e-114">Ten przykład pobiera strefę DNS o nazwie myzone.com z określonej grupy zasobów, a następnie zapisuje ją w $Zone danych.</span><span class="sxs-lookup"><span data-stu-id="c263e-114">This example gets the DNS zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="c263e-115">Przykład 2. Uzyskiwanie wszystkich stref w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="c263e-115">Example 2: Get all of the zones in a resource group</span></span>
```
PS C:\> $Zones = Get-AzDnsZone -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="c263e-116">W tym przykładzie wszystkie strefy DNS w określonej grupie zasobów są przechowywane w $Zones zasobów.</span><span class="sxs-lookup"><span data-stu-id="c263e-116">This example gets all of the DNS zones in the specified resource group, and then stores it in the $Zones variable.</span></span>

### <span data-ttu-id="c263e-117">Przykład 3. Uzyskiwanie wszystkich stref w subskrypcji</span><span class="sxs-lookup"><span data-stu-id="c263e-117">Example 3: Get all of the zones in a subscription</span></span>
```
PS C:\> $Zones = Get-AzDnsZone
```

<span data-ttu-id="c263e-118">W tym przykładzie wszystkie strefy DNS w bieżącej subskrypcji platformy Azure są przechowywane w $Zones danych.</span><span class="sxs-lookup"><span data-stu-id="c263e-118">This example gets all of the DNS zones in the current Azure subscription, and then stores them in the $Zones variable.</span></span>

## <span data-ttu-id="c263e-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c263e-119">PARAMETERS</span></span>

### <span data-ttu-id="c263e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c263e-120">-DefaultProfile</span></span>
<span data-ttu-id="c263e-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="c263e-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c263e-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c263e-122">-Name</span></span>
<span data-ttu-id="c263e-123">Określa nazwę strefy DNS do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="c263e-123">Specifies the name of the DNS zone to get.</span></span>
<span data-ttu-id="c263e-124">Jeśli nie określisz wartości dla *parametru Name,* to polecenie cmdlet pobiera wszystkie strefy DNS w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="c263e-124">If you do not specify a value for the *Name* parameter, this cmdlet gets all DNS zones in the specified resource group.</span></span>
<span data-ttu-id="c263e-125">Jeśli parametr *ResourceGroupName* zostanie pominięty, to polecenie cmdlet pobiera wszystkie strefy DNS w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c263e-125">If you also omit the *ResourceGroupName* parameter, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c263e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c263e-126">-ResourceGroupName</span></span>
<span data-ttu-id="c263e-127">Określa nazwę grupy zasobów zawierającej strefę DNS do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="c263e-127">Specifies the name of the resource group that contains the DNS zone to get.</span></span>
<span data-ttu-id="c263e-128">Jeśli nie określisz *parametru ResourceGroupName,* musisz również pominąć *parametr Name.*</span><span class="sxs-lookup"><span data-stu-id="c263e-128">If you do not specify the *ResourceGroupName*, then you must also omit the *Name* parameter.</span></span>
<span data-ttu-id="c263e-129">W tym przypadku to polecenie cmdlet pobiera wszystkie strefy DNS w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c263e-129">In this case, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c263e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c263e-130">CommonParameters</span></span>
<span data-ttu-id="c263e-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c263e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c263e-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c263e-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c263e-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c263e-133">INPUTS</span></span>

### <span data-ttu-id="c263e-134">System.String</span><span class="sxs-lookup"><span data-stu-id="c263e-134">System.String</span></span>

## <span data-ttu-id="c263e-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c263e-135">OUTPUTS</span></span>

### <span data-ttu-id="c263e-136">Microsoft.Azure.Commands.Dns.DnsZone</span><span class="sxs-lookup"><span data-stu-id="c263e-136">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="c263e-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c263e-137">NOTES</span></span>

## <span data-ttu-id="c263e-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c263e-138">RELATED LINKS</span></span>

[<span data-ttu-id="c263e-139">New-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="c263e-139">New-AzDnsZone</span></span>](./New-AzDnsZone.md)

[<span data-ttu-id="c263e-140">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="c263e-140">Remove-AzDnsZone</span></span>](./Remove-AzDnsZone.md)

[<span data-ttu-id="c263e-141">Set-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="c263e-141">Set-AzDnsZone</span></span>](./Set-AzDnsZone.md)
