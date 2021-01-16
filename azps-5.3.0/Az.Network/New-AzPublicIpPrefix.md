---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpPrefix.md
ms.openlocfilehash: 231a4f9622aa9fecf0c6d832e5f7602da1bed1b1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490981"
---
# <span data-ttu-id="f2f63-101">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="f2f63-101">New-AzPublicIpPrefix</span></span>

## <span data-ttu-id="f2f63-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f2f63-102">SYNOPSIS</span></span>
<span data-ttu-id="f2f63-103">Tworzy publiczny prefiks IP</span><span class="sxs-lookup"><span data-stu-id="f2f63-103">Creates a Public IP Prefix</span></span>

## <span data-ttu-id="f2f63-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f2f63-104">SYNTAX</span></span>

```
New-AzPublicIpPrefix -Name <String> -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 [-Tier <String>] -PrefixLength <UInt16> [-IpAddressVersion <String>] [-IpTag <PSPublicIpPrefixTag[]>]
 [-Zone <String[]>] [-CustomIpPrefix <PSCustomIpPrefix>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2f63-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f2f63-105">DESCRIPTION</span></span>
<span data-ttu-id="f2f63-106">Polecenie cmdlet **New-AzPublicIpPrefix** tworzy publiczny prefiks adresu IP.</span><span class="sxs-lookup"><span data-stu-id="f2f63-106">The **New-AzPublicIpPrefix** cmdlet creates a public IP prefix.</span></span>

## <span data-ttu-id="f2f63-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f2f63-107">EXAMPLES</span></span>

### <span data-ttu-id="f2f63-108">Przykład 1. Tworzenie nowego publicznego prefiksu adresu IP</span><span class="sxs-lookup"><span data-stu-id="f2f63-108">Example 1: Create a new public Ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = New-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName -PrefixLength 30
```

<span data-ttu-id="f2f63-109">To polecenie tworzy nowy publiczny zasób prefiksu IP.</span><span class="sxs-lookup"><span data-stu-id="f2f63-109">This command creates a new public IP prefix resource.</span></span> 

### <span data-ttu-id="f2f63-110">Przykład 2: Tworzenie nowego globalnego publicznego prefiksu adresu IP</span><span class="sxs-lookup"><span data-stu-id="f2f63-110">Example 2: Create a new global public Ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = New-AzPublicIpPrefix -ResourceGroupName $rgname -name $rname -location $location -Tier Global -PrefixLength 30
```

<span data-ttu-id="f2f63-111">To polecenie tworzy nowy globalny publiczny adres IP.</span><span class="sxs-lookup"><span data-stu-id="f2f63-111">This command creates a new global public IP prefix resource.</span></span> 

## <span data-ttu-id="f2f63-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f2f63-112">PARAMETERS</span></span>

### <span data-ttu-id="f2f63-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f2f63-113">-AsJob</span></span>
<span data-ttu-id="f2f63-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="f2f63-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f2f63-115">-CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="f2f63-115">-CustomIpPrefix</span></span>
<span data-ttu-id="f2f63-116">CustomIpPrefix, z którym ten PublicIpPrefix będzie skojarzony</span><span class="sxs-lookup"><span data-stu-id="f2f63-116">The CustomIpPrefix that this PublicIpPrefix will be associated with</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2f63-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2f63-117">-DefaultProfile</span></span>
<span data-ttu-id="f2f63-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f2f63-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2f63-119">-Force</span><span class="sxs-lookup"><span data-stu-id="f2f63-119">-Force</span></span>
<span data-ttu-id="f2f63-120">Nie pytaj o potwierdzenie zamiaru zastąpienia zasobu</span><span class="sxs-lookup"><span data-stu-id="f2f63-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="f2f63-121">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="f2f63-121">-IpAddressVersion</span></span>
<span data-ttu-id="f2f63-122">Wersja publicznego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="f2f63-122">The public IP address version.</span></span>

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

### <span data-ttu-id="f2f63-123">-IpTag</span><span class="sxs-lookup"><span data-stu-id="f2f63-123">-IpTag</span></span>
<span data-ttu-id="f2f63-124">Lista IpTag.</span><span class="sxs-lookup"><span data-stu-id="f2f63-124">IpTag List.</span></span>

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

### <span data-ttu-id="f2f63-125">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="f2f63-125">-Location</span></span>
<span data-ttu-id="f2f63-126">Publiczna lokalizacja prefiksu IP.</span><span class="sxs-lookup"><span data-stu-id="f2f63-126">The public IP prefix location.</span></span>

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

### <span data-ttu-id="f2f63-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f2f63-127">-Name</span></span>
<span data-ttu-id="f2f63-128">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="f2f63-128">The resource name.</span></span>

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

### <span data-ttu-id="f2f63-129">-PrefixLength</span><span class="sxs-lookup"><span data-stu-id="f2f63-129">-PrefixLength</span></span>
<span data-ttu-id="f2f63-130">Długość PublicIPPrefix</span><span class="sxs-lookup"><span data-stu-id="f2f63-130">The PublicIPPrefix length</span></span>

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

### <span data-ttu-id="f2f63-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2f63-131">-ResourceGroupName</span></span>
<span data-ttu-id="f2f63-132">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f2f63-132">The resource group name.</span></span>

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

### <span data-ttu-id="f2f63-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="f2f63-133">-Sku</span></span>
<span data-ttu-id="f2f63-134">Nazwa SKU prefiksu publicznego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="f2f63-134">The public IP Prefix Sku name.</span></span>

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

### <span data-ttu-id="f2f63-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="f2f63-135">-Tag</span></span>
<span data-ttu-id="f2f63-136">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="f2f63-136">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="f2f63-137">-Warstwowy</span><span class="sxs-lookup"><span data-stu-id="f2f63-137">-Tier</span></span>
<span data-ttu-id="f2f63-138">Warstwa SKU prefiksu publicznego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="f2f63-138">The public IP Prefix Sku tier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Regional, Global

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2f63-139">-Zone</span><span class="sxs-lookup"><span data-stu-id="f2f63-139">-Zone</span></span>
<span data-ttu-id="f2f63-140">Lista stref dostępności oznaczająca adres IP przydzielony dla zasobu musi pochodzić od.</span><span class="sxs-lookup"><span data-stu-id="f2f63-140">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="f2f63-141">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f2f63-141">-Confirm</span></span>
<span data-ttu-id="f2f63-142">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2f63-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2f63-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2f63-143">-WhatIf</span></span>
<span data-ttu-id="f2f63-144">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2f63-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2f63-145">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f2f63-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2f63-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2f63-146">CommonParameters</span></span>
<span data-ttu-id="f2f63-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2f63-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2f63-148">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f2f63-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2f63-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f2f63-149">INPUTS</span></span>

### <span data-ttu-id="f2f63-150">System. String</span><span class="sxs-lookup"><span data-stu-id="f2f63-150">System.String</span></span>

### <span data-ttu-id="f2f63-151">System. UInt16</span><span class="sxs-lookup"><span data-stu-id="f2f63-151">System.UInt16</span></span>

### <span data-ttu-id="f2f63-152">Microsoft. Azure. Commands. Network. models. PSPublicIpPrefixTag []</span><span class="sxs-lookup"><span data-stu-id="f2f63-152">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag[]</span></span>

### <span data-ttu-id="f2f63-153">System. String []</span><span class="sxs-lookup"><span data-stu-id="f2f63-153">System.String[]</span></span>

### <span data-ttu-id="f2f63-154">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f2f63-154">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f2f63-155">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f2f63-155">OUTPUTS</span></span>

### <span data-ttu-id="f2f63-156">Microsoft. Azure. Commands. Network. models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="f2f63-156">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="f2f63-157">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f2f63-157">NOTES</span></span>

## <span data-ttu-id="f2f63-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f2f63-158">RELATED LINKS</span></span>

[<span data-ttu-id="f2f63-159">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="f2f63-159">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="f2f63-160">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="f2f63-160">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)

[<span data-ttu-id="f2f63-161">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="f2f63-161">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)
