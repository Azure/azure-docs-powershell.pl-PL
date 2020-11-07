---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpPrefix.md
ms.openlocfilehash: d52bc8737392bf6fce004a90b1f2fe5207cffea9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719083"
---
# <span data-ttu-id="88c07-101">New-AzureRmPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="88c07-101">New-AzureRmPublicIpPrefix</span></span>

## <span data-ttu-id="88c07-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="88c07-102">SYNOPSIS</span></span>
<span data-ttu-id="88c07-103">Tworzy publiczny prefiks IP</span><span class="sxs-lookup"><span data-stu-id="88c07-103">Creates a Public IP Prefix</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88c07-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="88c07-104">SYNTAX</span></span>

```
New-AzureRmPublicIpPrefix -Name <String> -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 -PrefixLength <UInt16> [-IpAddressVersion <String>]
 [-IpTag <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag]>]
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88c07-105">Opis</span><span class="sxs-lookup"><span data-stu-id="88c07-105">DESCRIPTION</span></span>
<span data-ttu-id="88c07-106">Polecenie cmdlet **New-AzureRmPublicIpPrefix** tworzy publiczny prefiks adresu IP.</span><span class="sxs-lookup"><span data-stu-id="88c07-106">The **New-AzureRmPublicIpPrefix** cmdlet creates a public IP prefix.</span></span>

## <span data-ttu-id="88c07-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="88c07-107">EXAMPLES</span></span>

### <span data-ttu-id="88c07-108">1: Tworzenie nowego publicznego prefiksu adresu IP</span><span class="sxs-lookup"><span data-stu-id="88c07-108">1: Create a new public Ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = New-AzureRmPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName -PrefixLength 30
```

<span data-ttu-id="88c07-109">To polecenie tworzy nowy publiczny zasób prefiksu IP.</span><span class="sxs-lookup"><span data-stu-id="88c07-109">This command creates a new public IP prefix resource.</span></span> 

## <span data-ttu-id="88c07-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="88c07-110">PARAMETERS</span></span>

### <span data-ttu-id="88c07-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="88c07-111">-AsJob</span></span>
<span data-ttu-id="88c07-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="88c07-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="88c07-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88c07-113">-DefaultProfile</span></span>
<span data-ttu-id="88c07-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="88c07-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88c07-115">-Force</span><span class="sxs-lookup"><span data-stu-id="88c07-115">-Force</span></span>
<span data-ttu-id="88c07-116">Nie pytaj o potwierdzenie, czy zachodzi konieczność przestania się zasobu</span><span class="sxs-lookup"><span data-stu-id="88c07-116">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="88c07-117">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="88c07-117">-IpAddressVersion</span></span>
<span data-ttu-id="88c07-118">Wersja publicznego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="88c07-118">The public IP address version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88c07-119">-IpTag</span><span class="sxs-lookup"><span data-stu-id="88c07-119">-IpTag</span></span>
<span data-ttu-id="88c07-120">Lista IpTag.</span><span class="sxs-lookup"><span data-stu-id="88c07-120">IpTag List.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88c07-121">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="88c07-121">-Location</span></span>
<span data-ttu-id="88c07-122">Publiczna lokalizacja prefiksu IP.</span><span class="sxs-lookup"><span data-stu-id="88c07-122">The public IP prefix location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88c07-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="88c07-123">-Name</span></span>
<span data-ttu-id="88c07-124">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="88c07-124">The resource name.</span></span>

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

### <span data-ttu-id="88c07-125">-PrefixLength</span><span class="sxs-lookup"><span data-stu-id="88c07-125">-PrefixLength</span></span>
<span data-ttu-id="88c07-126">Długość PublicIPPrefix</span><span class="sxs-lookup"><span data-stu-id="88c07-126">The PublicIPPrefix length</span></span>

```yaml
Type: UInt16
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88c07-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88c07-127">-ResourceGroupName</span></span>
<span data-ttu-id="88c07-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="88c07-128">The resource group name.</span></span>

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

### <span data-ttu-id="88c07-129">-SKU</span><span class="sxs-lookup"><span data-stu-id="88c07-129">-Sku</span></span>
<span data-ttu-id="88c07-130">Nazwa SKU prefiksu publicznego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="88c07-130">The public IP Prefix Sku name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88c07-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="88c07-131">-Tag</span></span>
<span data-ttu-id="88c07-132">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="88c07-132">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="88c07-133">-Zone</span><span class="sxs-lookup"><span data-stu-id="88c07-133">-Zone</span></span>
<span data-ttu-id="88c07-134">Lista stref dostępności oznaczająca adres IP przydzielony dla zasobu musi pochodzić od.</span><span class="sxs-lookup"><span data-stu-id="88c07-134">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88c07-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="88c07-135">-Confirm</span></span>
<span data-ttu-id="88c07-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88c07-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88c07-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88c07-137">-WhatIf</span></span>
<span data-ttu-id="88c07-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88c07-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88c07-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="88c07-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88c07-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88c07-140">CommonParameters</span></span>
<span data-ttu-id="88c07-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88c07-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="88c07-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88c07-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88c07-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="88c07-143">INPUTS</span></span>

### <span data-ttu-id="88c07-144">System. String</span><span class="sxs-lookup"><span data-stu-id="88c07-144">System.String</span></span>
<span data-ttu-id="88c07-145">System. UInt16 system. Collections. kolekcje. Generic. lista `1[[Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag, Microsoft.Azure.Commands.Network, Version=6.4.0.0, Culture=neutral, PublicKeyToken=null]]
System.Collections.Generic.List` 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]] system. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="88c07-145">System.UInt16 System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag, Microsoft.Azure.Commands.Network, Version=6.4.0.0, Culture=neutral, PublicKeyToken=null]]
System.Collections.Generic.List`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.Collections.Hashtable</span></span>


## <span data-ttu-id="88c07-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="88c07-146">OUTPUTS</span></span>

### <span data-ttu-id="88c07-147">Microsoft. Azure. Commands. Network. models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="88c07-147">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>


## <span data-ttu-id="88c07-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="88c07-148">NOTES</span></span>

## <span data-ttu-id="88c07-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="88c07-149">RELATED LINKS</span></span>
