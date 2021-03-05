---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzCustomIpPrefix.md
ms.openlocfilehash: 0ac12ba420231d34c5ad278a8fd2a091fe4982da
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960401"
---
# <span data-ttu-id="b03d9-101">New-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="b03d9-101">New-AzCustomIpPrefix</span></span>

## <span data-ttu-id="b03d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b03d9-102">SYNOPSIS</span></span>
<span data-ttu-id="b03d9-103">Tworzy zasób CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="b03d9-103">Creates a CustomIpPrefix resource</span></span>

## <span data-ttu-id="b03d9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b03d9-104">SYNTAX</span></span>

```
New-AzCustomIpPrefix -Name <String> -ResourceGroupName <String> -Location <String> -Cidr <String>
 [-Zone <String[]>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b03d9-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="b03d9-105">DESCRIPTION</span></span>
<span data-ttu-id="b03d9-106">Polecenie **cmdlet New-AzCustomIpPrefix** tworzy zasób CustomIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="b03d9-106">The **New-AzCustomIpPrefix** cmdlet creates a CustomIpPrefix resource.</span></span>

## <span data-ttu-id="b03d9-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b03d9-107">EXAMPLES</span></span>

### <span data-ttu-id="b03d9-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b03d9-108">Example 1</span></span>
```powershell
PS C:\> $myCustomIpPrefix = New-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Cidr 40.40.40.0/24 -Location westus
```

<span data-ttu-id="b03d9-109">To polecenie tworzy nowy zasób CustomIpPrefix o nazwie $prefixName w grupie zasobów $rgName z kodem błędu 40.40.40.0/24 na zachód</span><span class="sxs-lookup"><span data-stu-id="b03d9-109">This command creates a new CustomIpPrefix resource with name $prefixName in resource group $rgName with a cidr of 40.40.40.0/24 in westus</span></span>

## <span data-ttu-id="b03d9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b03d9-110">PARAMETERS</span></span>

### <span data-ttu-id="b03d9-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="b03d9-111">-AsJob</span></span>
<span data-ttu-id="b03d9-112">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="b03d9-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b03d9-113">— Cidr</span><span class="sxs-lookup"><span data-stu-id="b03d9-113">-Cidr</span></span>
<span data-ttu-id="b03d9-114">Kod CIDR CustomIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="b03d9-114">The CustomIpPrefix CIDR.</span></span>

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

### <span data-ttu-id="b03d9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b03d9-115">-DefaultProfile</span></span>
<span data-ttu-id="b03d9-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b03d9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b03d9-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="b03d9-117">-Location</span></span>
<span data-ttu-id="b03d9-118">Lokalizacja customIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="b03d9-118">The CustomIpPrefix location.</span></span>

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

### <span data-ttu-id="b03d9-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b03d9-119">-Name</span></span>
<span data-ttu-id="b03d9-120">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="b03d9-120">The resource name.</span></span>

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

### <span data-ttu-id="b03d9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b03d9-121">-ResourceGroupName</span></span>
<span data-ttu-id="b03d9-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b03d9-122">The resource group name.</span></span>

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

### <span data-ttu-id="b03d9-123">— Tag</span><span class="sxs-lookup"><span data-stu-id="b03d9-123">-Tag</span></span>
<span data-ttu-id="b03d9-124">Tabela skrótów reprezentująca tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="b03d9-124">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="b03d9-125">— Strefa</span><span class="sxs-lookup"><span data-stu-id="b03d9-125">-Zone</span></span>
<span data-ttu-id="b03d9-126">Lista stref dostępności oznaczających adresy IP przydzielone do zasobu.</span><span class="sxs-lookup"><span data-stu-id="b03d9-126">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="b03d9-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b03d9-127">-Confirm</span></span>
<span data-ttu-id="b03d9-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b03d9-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b03d9-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b03d9-129">-WhatIf</span></span>
<span data-ttu-id="b03d9-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b03d9-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b03d9-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b03d9-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b03d9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b03d9-132">CommonParameters</span></span>
<span data-ttu-id="b03d9-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b03d9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b03d9-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b03d9-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b03d9-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b03d9-135">INPUTS</span></span>

### <span data-ttu-id="b03d9-136">System.String</span><span class="sxs-lookup"><span data-stu-id="b03d9-136">System.String</span></span>

### <span data-ttu-id="b03d9-137">System.String[]</span><span class="sxs-lookup"><span data-stu-id="b03d9-137">System.String[]</span></span>

### <span data-ttu-id="b03d9-138">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="b03d9-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b03d9-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b03d9-139">OUTPUTS</span></span>

### <span data-ttu-id="b03d9-140">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="b03d9-140">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

## <span data-ttu-id="b03d9-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b03d9-141">NOTES</span></span>

## <span data-ttu-id="b03d9-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b03d9-142">RELATED LINKS</span></span>

[<span data-ttu-id="b03d9-143">Get-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="b03d9-143">Get-AzCustomIpPrefix</span></span>](./Get-AzCustomIpPrefix.md)

[<span data-ttu-id="b03d9-144">Remove-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="b03d9-144">Remove-AzCustomIpPrefix</span></span>](./Remove-AzCustomIpPrefix.md)

[<span data-ttu-id="b03d9-145">Update-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="b03d9-145">Update-AzCustomIpPrefix</span></span>](./Update-AzCustomIpPrefix.md)