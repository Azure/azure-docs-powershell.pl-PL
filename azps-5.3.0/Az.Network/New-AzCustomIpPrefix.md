---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzCustomIpPrefix.md
ms.openlocfilehash: 08df4120e762a7837376af7413504a8fce678230
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491054"
---
# <span data-ttu-id="6c9a2-101">New-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="6c9a2-101">New-AzCustomIpPrefix</span></span>

## <span data-ttu-id="6c9a2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6c9a2-102">SYNOPSIS</span></span>
<span data-ttu-id="6c9a2-103">Tworzy zasób CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="6c9a2-103">Creates a CustomIpPrefix resource</span></span>

## <span data-ttu-id="6c9a2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6c9a2-104">SYNTAX</span></span>

```
New-AzCustomIpPrefix -Name <String> -ResourceGroupName <String> -Location <String> -Cidr <String>
 [-Zone <String[]>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6c9a2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6c9a2-105">DESCRIPTION</span></span>
<span data-ttu-id="6c9a2-106">Polecenie cmdlet **New-AzCustomIpPrefix** tworzy zasób CustomIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="6c9a2-106">The **New-AzCustomIpPrefix** cmdlet creates a CustomIpPrefix resource.</span></span>

## <span data-ttu-id="6c9a2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6c9a2-107">EXAMPLES</span></span>

### <span data-ttu-id="6c9a2-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6c9a2-108">Example 1</span></span>
```powershell
PS C:\> $myCustomIpPrefix = New-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Cidr 40.40.40.0/24 -Location westus
```

<span data-ttu-id="6c9a2-109">To polecenie tworzy nowy zasób CustomIpPrefix o nazwie $prefixName w grupie zasób $rgName za pomocą CIDR o 40.40.40.0/24 na zachód.</span><span class="sxs-lookup"><span data-stu-id="6c9a2-109">This command creates a new CustomIpPrefix resource with name $prefixName in resource group $rgName with a cidr of 40.40.40.0/24 in westus</span></span>

## <span data-ttu-id="6c9a2-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6c9a2-110">PARAMETERS</span></span>

### <span data-ttu-id="6c9a2-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6c9a2-111">-AsJob</span></span>
<span data-ttu-id="6c9a2-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="6c9a2-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c9a2-113">-CIDR</span><span class="sxs-lookup"><span data-stu-id="6c9a2-113">-Cidr</span></span>
<span data-ttu-id="6c9a2-114">CustomIpPrefix CIDR.</span><span class="sxs-lookup"><span data-stu-id="6c9a2-114">The CustomIpPrefix CIDR.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c9a2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c9a2-115">-DefaultProfile</span></span>
<span data-ttu-id="6c9a2-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6c9a2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c9a2-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="6c9a2-117">-Location</span></span>
<span data-ttu-id="6c9a2-118">Lokalizacja CustomIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="6c9a2-118">The CustomIpPrefix location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c9a2-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6c9a2-119">-Name</span></span>
<span data-ttu-id="6c9a2-120">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="6c9a2-120">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c9a2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c9a2-121">-ResourceGroupName</span></span>
<span data-ttu-id="6c9a2-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6c9a2-122">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c9a2-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="6c9a2-123">-Tag</span></span>
<span data-ttu-id="6c9a2-124">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="6c9a2-124">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c9a2-125">-Zone</span><span class="sxs-lookup"><span data-stu-id="6c9a2-125">-Zone</span></span>
<span data-ttu-id="6c9a2-126">Lista stref dostępności oznaczająca adres IP przydzielony dla zasobu musi pochodzić od.</span><span class="sxs-lookup"><span data-stu-id="6c9a2-126">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c9a2-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6c9a2-127">-Confirm</span></span>
<span data-ttu-id="6c9a2-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c9a2-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c9a2-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c9a2-129">-WhatIf</span></span>
<span data-ttu-id="6c9a2-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c9a2-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c9a2-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6c9a2-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c9a2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c9a2-132">CommonParameters</span></span>
<span data-ttu-id="6c9a2-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c9a2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c9a2-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6c9a2-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c9a2-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6c9a2-135">INPUTS</span></span>

### <span data-ttu-id="6c9a2-136">System. String</span><span class="sxs-lookup"><span data-stu-id="6c9a2-136">System.String</span></span>

### <span data-ttu-id="6c9a2-137">System. String []</span><span class="sxs-lookup"><span data-stu-id="6c9a2-137">System.String[]</span></span>

### <span data-ttu-id="6c9a2-138">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="6c9a2-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="6c9a2-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6c9a2-139">OUTPUTS</span></span>

### <span data-ttu-id="6c9a2-140">Microsoft. Azure. Commands. Network. models. PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="6c9a2-140">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

## <span data-ttu-id="6c9a2-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6c9a2-141">NOTES</span></span>

## <span data-ttu-id="6c9a2-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6c9a2-142">RELATED LINKS</span></span>

[<span data-ttu-id="6c9a2-143">Get-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="6c9a2-143">Get-AzCustomIpPrefix</span></span>](./Get-AzCustomIpPrefix.md)

[<span data-ttu-id="6c9a2-144">Remove-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="6c9a2-144">Remove-AzCustomIpPrefix</span></span>](./Remove-AzCustomIpPrefix.md)

[<span data-ttu-id="6c9a2-145">Update-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="6c9a2-145">Update-AzCustomIpPrefix</span></span>](./Update-AzCustomIpPrefix.md)