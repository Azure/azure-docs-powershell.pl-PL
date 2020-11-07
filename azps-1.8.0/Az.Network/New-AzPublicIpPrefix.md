---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpPrefix.md
ms.openlocfilehash: 6ee4f046281a36f0d0da798f1954a29f8d98d9c5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709253"
---
# <span data-ttu-id="39a4a-101">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="39a4a-101">New-AzPublicIpPrefix</span></span>

## <span data-ttu-id="39a4a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="39a4a-102">SYNOPSIS</span></span>
<span data-ttu-id="39a4a-103">Tworzy publiczny prefiks IP</span><span class="sxs-lookup"><span data-stu-id="39a4a-103">Creates a Public IP Prefix</span></span>

## <span data-ttu-id="39a4a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="39a4a-104">SYNTAX</span></span>

```
New-AzPublicIpPrefix -Name <String> -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 -PrefixLength <UInt16> [-IpAddressVersion <String>] [-IpTag <PSPublicIpPrefixTag[]>] [-Zone <String[]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="39a4a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="39a4a-105">DESCRIPTION</span></span>
<span data-ttu-id="39a4a-106">Polecenie cmdlet **New-AzPublicIpPrefix** tworzy publiczny prefiks adresu IP.</span><span class="sxs-lookup"><span data-stu-id="39a4a-106">The **New-AzPublicIpPrefix** cmdlet creates a public IP prefix.</span></span>

## <span data-ttu-id="39a4a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="39a4a-107">EXAMPLES</span></span>

### <span data-ttu-id="39a4a-108">1: Tworzenie nowego publicznego prefiksu adresu IP</span><span class="sxs-lookup"><span data-stu-id="39a4a-108">1: Create a new public Ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = New-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName -PrefixLength 30
```

<span data-ttu-id="39a4a-109">To polecenie tworzy nowy publiczny zasób prefiksu IP.</span><span class="sxs-lookup"><span data-stu-id="39a4a-109">This command creates a new public IP prefix resource.</span></span> 

## <span data-ttu-id="39a4a-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="39a4a-110">PARAMETERS</span></span>

### <span data-ttu-id="39a4a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="39a4a-111">-AsJob</span></span>
<span data-ttu-id="39a4a-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="39a4a-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="39a4a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39a4a-113">-DefaultProfile</span></span>
<span data-ttu-id="39a4a-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="39a4a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39a4a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="39a4a-115">-Force</span></span>
<span data-ttu-id="39a4a-116">Nie pytaj o potwierdzenie, czy zachodzi konieczność przestania się zasobu</span><span class="sxs-lookup"><span data-stu-id="39a4a-116">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="39a4a-117">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="39a4a-117">-IpAddressVersion</span></span>
<span data-ttu-id="39a4a-118">Wersja publicznego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="39a4a-118">The public IP address version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39a4a-119">-IpTag</span><span class="sxs-lookup"><span data-stu-id="39a4a-119">-IpTag</span></span>
<span data-ttu-id="39a4a-120">Lista IpTag.</span><span class="sxs-lookup"><span data-stu-id="39a4a-120">IpTag List.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39a4a-121">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="39a4a-121">-Location</span></span>
<span data-ttu-id="39a4a-122">Publiczna lokalizacja prefiksu IP.</span><span class="sxs-lookup"><span data-stu-id="39a4a-122">The public IP prefix location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39a4a-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="39a4a-123">-Name</span></span>
<span data-ttu-id="39a4a-124">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="39a4a-124">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39a4a-125">-PrefixLength</span><span class="sxs-lookup"><span data-stu-id="39a4a-125">-PrefixLength</span></span>
<span data-ttu-id="39a4a-126">Długość PublicIPPrefix</span><span class="sxs-lookup"><span data-stu-id="39a4a-126">The PublicIPPrefix length</span></span>

```yaml
Type: System.UInt16
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39a4a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39a4a-127">-ResourceGroupName</span></span>
<span data-ttu-id="39a4a-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="39a4a-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39a4a-129">-SKU</span><span class="sxs-lookup"><span data-stu-id="39a4a-129">-Sku</span></span>
<span data-ttu-id="39a4a-130">Nazwa SKU prefiksu publicznego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="39a4a-130">The public IP Prefix Sku name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39a4a-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="39a4a-131">-Tag</span></span>
<span data-ttu-id="39a4a-132">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="39a4a-132">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39a4a-133">-Zone</span><span class="sxs-lookup"><span data-stu-id="39a4a-133">-Zone</span></span>
<span data-ttu-id="39a4a-134">Lista stref dostępności oznaczająca adres IP przydzielony dla zasobu musi pochodzić od.</span><span class="sxs-lookup"><span data-stu-id="39a4a-134">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39a4a-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="39a4a-135">-Confirm</span></span>
<span data-ttu-id="39a4a-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39a4a-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39a4a-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39a4a-137">-WhatIf</span></span>
<span data-ttu-id="39a4a-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39a4a-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39a4a-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="39a4a-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39a4a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39a4a-140">CommonParameters</span></span>
<span data-ttu-id="39a4a-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39a4a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39a4a-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39a4a-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39a4a-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="39a4a-143">INPUTS</span></span>

### <span data-ttu-id="39a4a-144">System. String</span><span class="sxs-lookup"><span data-stu-id="39a4a-144">System.String</span></span>

### <span data-ttu-id="39a4a-145">System. UInt16</span><span class="sxs-lookup"><span data-stu-id="39a4a-145">System.UInt16</span></span>

### <span data-ttu-id="39a4a-146">Microsoft. Azure. Commands. Network. models. PSPublicIpPrefixTag []</span><span class="sxs-lookup"><span data-stu-id="39a4a-146">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag[]</span></span>

### <span data-ttu-id="39a4a-147">System. String []</span><span class="sxs-lookup"><span data-stu-id="39a4a-147">System.String[]</span></span>

### <span data-ttu-id="39a4a-148">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="39a4a-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="39a4a-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="39a4a-149">OUTPUTS</span></span>

### <span data-ttu-id="39a4a-150">Microsoft. Azure. Commands. Network. models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="39a4a-150">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="39a4a-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="39a4a-151">NOTES</span></span>

## <span data-ttu-id="39a4a-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="39a4a-152">RELATED LINKS</span></span>

[<span data-ttu-id="39a4a-153">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="39a4a-153">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="39a4a-154">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="39a4a-154">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)

[<span data-ttu-id="39a4a-155">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="39a4a-155">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)
