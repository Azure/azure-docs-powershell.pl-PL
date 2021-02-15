---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpPrefix.md
ms.openlocfilehash: 231a4f9622aa9fecf0c6d832e5f7602da1bed1b1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187026"
---
# <span data-ttu-id="89164-101">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="89164-101">New-AzPublicIpPrefix</span></span>

## <span data-ttu-id="89164-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89164-102">SYNOPSIS</span></span>
<span data-ttu-id="89164-103">Tworzy publiczny prefiks IP</span><span class="sxs-lookup"><span data-stu-id="89164-103">Creates a Public IP Prefix</span></span>

## <span data-ttu-id="89164-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="89164-104">SYNTAX</span></span>

```
New-AzPublicIpPrefix -Name <String> -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 [-Tier <String>] -PrefixLength <UInt16> [-IpAddressVersion <String>] [-IpTag <PSPublicIpPrefixTag[]>]
 [-Zone <String[]>] [-CustomIpPrefix <PSCustomIpPrefix>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89164-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="89164-105">DESCRIPTION</span></span>
<span data-ttu-id="89164-106">Polecenie **cmdlet New-AzPublicIpPrefix** tworzy publiczny prefiks IP.</span><span class="sxs-lookup"><span data-stu-id="89164-106">The **New-AzPublicIpPrefix** cmdlet creates a public IP prefix.</span></span>

## <span data-ttu-id="89164-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="89164-107">EXAMPLES</span></span>

### <span data-ttu-id="89164-108">Przykład 1. Tworzenie nowego publicznego prefiksu IP</span><span class="sxs-lookup"><span data-stu-id="89164-108">Example 1: Create a new public Ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = New-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName -PrefixLength 30
```

<span data-ttu-id="89164-109">To polecenie tworzy nowy publiczny zasób prefiksu IP.</span><span class="sxs-lookup"><span data-stu-id="89164-109">This command creates a new public IP prefix resource.</span></span> 

### <span data-ttu-id="89164-110">Przykład 2. Tworzenie nowego globalnego prefiksu IP</span><span class="sxs-lookup"><span data-stu-id="89164-110">Example 2: Create a new global public Ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = New-AzPublicIpPrefix -ResourceGroupName $rgname -name $rname -location $location -Tier Global -PrefixLength 30
```

<span data-ttu-id="89164-111">To polecenie tworzy nowy globalny publiczny zasób prefiksu IP.</span><span class="sxs-lookup"><span data-stu-id="89164-111">This command creates a new global public IP prefix resource.</span></span> 

## <span data-ttu-id="89164-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="89164-112">PARAMETERS</span></span>

### <span data-ttu-id="89164-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="89164-113">-AsJob</span></span>
<span data-ttu-id="89164-114">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="89164-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="89164-115">- CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="89164-115">-CustomIpPrefix</span></span>
<span data-ttu-id="89164-116">The CustomIpPrefix that this PublicIpPrefix will be associated with</span><span class="sxs-lookup"><span data-stu-id="89164-116">The CustomIpPrefix that this PublicIpPrefix will be associated with</span></span>

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

### <span data-ttu-id="89164-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89164-117">-DefaultProfile</span></span>
<span data-ttu-id="89164-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="89164-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89164-119">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="89164-119">-Force</span></span>
<span data-ttu-id="89164-120">Nie pytaj o potwierdzenie, jeśli chcesz zastąpić zasób</span><span class="sxs-lookup"><span data-stu-id="89164-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="89164-121">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="89164-121">-IpAddressVersion</span></span>
<span data-ttu-id="89164-122">Wersja publicznego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="89164-122">The public IP address version.</span></span>

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

### <span data-ttu-id="89164-123">-IpTag</span><span class="sxs-lookup"><span data-stu-id="89164-123">-IpTag</span></span>
<span data-ttu-id="89164-124">Lista tagów IP.</span><span class="sxs-lookup"><span data-stu-id="89164-124">IpTag List.</span></span>

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

### <span data-ttu-id="89164-125">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="89164-125">-Location</span></span>
<span data-ttu-id="89164-126">Lokalizacja publicznego prefiksu IP.</span><span class="sxs-lookup"><span data-stu-id="89164-126">The public IP prefix location.</span></span>

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

### <span data-ttu-id="89164-127">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="89164-127">-Name</span></span>
<span data-ttu-id="89164-128">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="89164-128">The resource name.</span></span>

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

### <span data-ttu-id="89164-129">-PrefixLength</span><span class="sxs-lookup"><span data-stu-id="89164-129">-PrefixLength</span></span>
<span data-ttu-id="89164-130">Długość publicIPPrefix</span><span class="sxs-lookup"><span data-stu-id="89164-130">The PublicIPPrefix length</span></span>

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

### <span data-ttu-id="89164-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89164-131">-ResourceGroupName</span></span>
<span data-ttu-id="89164-132">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="89164-132">The resource group name.</span></span>

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

### <span data-ttu-id="89164-133">- SKU</span><span class="sxs-lookup"><span data-stu-id="89164-133">-Sku</span></span>
<span data-ttu-id="89164-134">Nazwa publicznego prefiksu IP SKU.</span><span class="sxs-lookup"><span data-stu-id="89164-134">The public IP Prefix Sku name.</span></span>

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

### <span data-ttu-id="89164-135">— Tag</span><span class="sxs-lookup"><span data-stu-id="89164-135">-Tag</span></span>
<span data-ttu-id="89164-136">Tabela skrótów reprezentująca tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="89164-136">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="89164-137">- Warstwa</span><span class="sxs-lookup"><span data-stu-id="89164-137">-Tier</span></span>
<span data-ttu-id="89164-138">Publiczna warstwa SKU prefiksu IP.</span><span class="sxs-lookup"><span data-stu-id="89164-138">The public IP Prefix Sku tier.</span></span>

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

### <span data-ttu-id="89164-139">— Strefa</span><span class="sxs-lookup"><span data-stu-id="89164-139">-Zone</span></span>
<span data-ttu-id="89164-140">Lista stref dostępności oznaczających adresy IP przydzielone do zasobu.</span><span class="sxs-lookup"><span data-stu-id="89164-140">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="89164-141">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="89164-141">-Confirm</span></span>
<span data-ttu-id="89164-142">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="89164-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89164-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89164-143">-WhatIf</span></span>
<span data-ttu-id="89164-144">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89164-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89164-145">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="89164-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89164-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89164-146">CommonParameters</span></span>
<span data-ttu-id="89164-147">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89164-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89164-148">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="89164-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89164-149">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="89164-149">INPUTS</span></span>

### <span data-ttu-id="89164-150">System.String</span><span class="sxs-lookup"><span data-stu-id="89164-150">System.String</span></span>

### <span data-ttu-id="89164-151">System.UInt16</span><span class="sxs-lookup"><span data-stu-id="89164-151">System.UInt16</span></span>

### <span data-ttu-id="89164-152">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag[]</span><span class="sxs-lookup"><span data-stu-id="89164-152">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag[]</span></span>

### <span data-ttu-id="89164-153">System.String[]</span><span class="sxs-lookup"><span data-stu-id="89164-153">System.String[]</span></span>

### <span data-ttu-id="89164-154">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="89164-154">System.Collections.Hashtable</span></span>

## <span data-ttu-id="89164-155">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="89164-155">OUTPUTS</span></span>

### <span data-ttu-id="89164-156">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="89164-156">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="89164-157">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="89164-157">NOTES</span></span>

## <span data-ttu-id="89164-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="89164-158">RELATED LINKS</span></span>

[<span data-ttu-id="89164-159">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="89164-159">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="89164-160">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="89164-160">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)

[<span data-ttu-id="89164-161">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="89164-161">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)
