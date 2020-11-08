---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/new-azsippool
schema: 2.0.0
ms.openlocfilehash: 2b04c5c1eb4d0a2b79543bf81bbfc02d1f0fb4ad
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94055850"
---
# <span data-ttu-id="ce870-101">New-AzsIPPool</span><span class="sxs-lookup"><span data-stu-id="ce870-101">New-AzsIPPool</span></span>

## <span data-ttu-id="ce870-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ce870-102">SYNOPSIS</span></span>
<span data-ttu-id="ce870-103">Tworzenie puli adresów IP.</span><span class="sxs-lookup"><span data-stu-id="ce870-103">Create an IP pool.</span></span>
<span data-ttu-id="ce870-104">Po utworzeniu puli adresów IP nie można usunąć.</span><span class="sxs-lookup"><span data-stu-id="ce870-104">Once created an IP pool cannot be deleted.</span></span>

## <span data-ttu-id="ce870-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ce870-105">SYNTAX</span></span>

### <span data-ttu-id="ce870-106">Rozszerzenie (domyślne)</span><span class="sxs-lookup"><span data-stu-id="ce870-106">CreateExpanded (Default)</span></span>
```
New-AzsIPPool -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-AddressPrefix <String>] [-EndIPAddress <String>]
 [-NumberOfAllocatedIPAddress <Int64>] [-NumberOfIPAddress <Int64>] [-NumberOfIPAddressesInTransition <Int64>]
 [-StartIPAddress <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ce870-107">Tworzonych</span><span class="sxs-lookup"><span data-stu-id="ce870-107">Create</span></span>
```
New-AzsIPPool -Name <String> -Pool <IIPPool> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="ce870-108">Opis</span><span class="sxs-lookup"><span data-stu-id="ce870-108">DESCRIPTION</span></span>
<span data-ttu-id="ce870-109">Tworzenie puli adresów IP.</span><span class="sxs-lookup"><span data-stu-id="ce870-109">Create an IP pool.</span></span>
<span data-ttu-id="ce870-110">Po utworzeniu puli adresów IP nie można usunąć.</span><span class="sxs-lookup"><span data-stu-id="ce870-110">Once created an IP pool cannot be deleted.</span></span>

## <span data-ttu-id="ce870-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ce870-111">EXAMPLES</span></span>

### <span data-ttu-id="ce870-112">Przykład 1:</span><span class="sxs-lookup"><span data-stu-id="ce870-112">Example 1:</span></span>
```powershell
PS C:\> New-AzsIpPool -Name IpPool4 -StartIpAddress ***.***.***.*** -EndIpAddress ***.***.***.*** -AddressPrefix ***.***.***.***/24

```

<span data-ttu-id="ce870-113">Tworzenie nowej puli adresów IP.</span><span class="sxs-lookup"><span data-stu-id="ce870-113">Create a new IP pool.</span></span>



## <span data-ttu-id="ce870-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ce870-114">PARAMETERS</span></span>

### <span data-ttu-id="ce870-115">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="ce870-115">-AddressPrefix</span></span>
<span data-ttu-id="ce870-116">Prefiks adresu.</span><span class="sxs-lookup"><span data-stu-id="ce870-116">The address prefix.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ce870-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ce870-117">-AsJob</span></span>
<span data-ttu-id="ce870-118">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="ce870-118">Run the command as a job</span></span>

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

### <span data-ttu-id="ce870-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce870-119">-DefaultProfile</span></span>
<span data-ttu-id="ce870-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ce870-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ce870-121">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="ce870-121">-EndIPAddress</span></span>
<span data-ttu-id="ce870-122">Końcowy adres IP.</span><span class="sxs-lookup"><span data-stu-id="ce870-122">The ending IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ce870-123">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="ce870-123">-Location</span></span>
<span data-ttu-id="ce870-124">Region, w którym znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="ce870-124">The region where the resource is located.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ce870-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ce870-125">-Name</span></span>
<span data-ttu-id="ce870-126">Nazwa puli adresów IP.</span><span class="sxs-lookup"><span data-stu-id="ce870-126">IP pool name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ce870-127">-Nowait</span><span class="sxs-lookup"><span data-stu-id="ce870-127">-NoWait</span></span>
<span data-ttu-id="ce870-128">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="ce870-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ce870-129">-NumberOfAllocatedIPAddress</span><span class="sxs-lookup"><span data-stu-id="ce870-129">-NumberOfAllocatedIPAddress</span></span>
<span data-ttu-id="ce870-130">Liczba obecnie przydzielonych adresów IP.</span><span class="sxs-lookup"><span data-stu-id="ce870-130">The number of currently allocated IP addresses.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ce870-131">-NumberOfIPAddress</span><span class="sxs-lookup"><span data-stu-id="ce870-131">-NumberOfIPAddress</span></span>
<span data-ttu-id="ce870-132">Całkowita liczba adresów IP.</span><span class="sxs-lookup"><span data-stu-id="ce870-132">The total number of IP addresses.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ce870-133">-NumberOfIPAddressesInTransition</span><span class="sxs-lookup"><span data-stu-id="ce870-133">-NumberOfIPAddressesInTransition</span></span>
<span data-ttu-id="ce870-134">Bieżąca liczba adresów IP w obszarze przejścia.</span><span class="sxs-lookup"><span data-stu-id="ce870-134">The current number of IP addresses in transition.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ce870-135">-Pool</span><span class="sxs-lookup"><span data-stu-id="ce870-135">-Pool</span></span>
<span data-ttu-id="ce870-136">Ten zasób definiuje zakres adresów IP, z których adresy są przydzielane węzłom w podsieci.</span><span class="sxs-lookup"><span data-stu-id="ce870-136">This resource defines the range of IP addresses from which addresses are allocated for nodes within a subnet.</span></span>
<span data-ttu-id="ce870-137">Aby skonstruować, zobacz sekcję notatki dla właściwości puli i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="ce870-137">To construct, see NOTES section for POOL properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IIPPool
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="ce870-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce870-138">-ResourceGroupName</span></span>
<span data-ttu-id="ce870-139">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ce870-139">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ce870-140">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="ce870-140">-StartIPAddress</span></span>
<span data-ttu-id="ce870-141">Początkowy adres IP.</span><span class="sxs-lookup"><span data-stu-id="ce870-141">The starting IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ce870-142">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="ce870-142">-SubscriptionId</span></span>
<span data-ttu-id="ce870-143">Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ce870-143">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ce870-144">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="ce870-144">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ce870-145">-Tag</span><span class="sxs-lookup"><span data-stu-id="ce870-145">-Tag</span></span>
<span data-ttu-id="ce870-146">Lista par klucz-wartość.</span><span class="sxs-lookup"><span data-stu-id="ce870-146">List of key-value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ce870-147">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ce870-147">-Confirm</span></span>
<span data-ttu-id="ce870-148">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce870-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce870-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce870-149">-WhatIf</span></span>
<span data-ttu-id="ce870-150">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce870-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce870-151">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ce870-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce870-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce870-152">CommonParameters</span></span>
<span data-ttu-id="ce870-153">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce870-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce870-154">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ce870-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce870-155">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ce870-155">INPUTS</span></span>

### <span data-ttu-id="ce870-156">Microsoft. Azure. PowerShell. polecenia. FabricAdmin. models. Api20160501. IIPPool</span><span class="sxs-lookup"><span data-stu-id="ce870-156">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IIPPool</span></span>

## <span data-ttu-id="ce870-157">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ce870-157">OUTPUTS</span></span>

### <span data-ttu-id="ce870-158">Microsoft. Azure. PowerShell. polecenia. FabricAdmin. models. Api20160501. IIPPool</span><span class="sxs-lookup"><span data-stu-id="ce870-158">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IIPPool</span></span>



## <span data-ttu-id="ce870-159">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ce870-159">NOTES</span></span>

<span data-ttu-id="ce870-160">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="ce870-160">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ce870-161">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ce870-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="ce870-162">Pula <IIPPool> : ten zasób definiuje zakres adresów IP, z których adresy są przydzielane węzłom w podsieci.</span><span class="sxs-lookup"><span data-stu-id="ce870-162">POOL <IIPPool>: This resource defines the range of IP addresses from which addresses are allocated for nodes within a subnet.</span></span>
  - <span data-ttu-id="ce870-163">`[Location <String>]`: Region, w którym znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="ce870-163">`[Location <String>]`: The region where the resource is located.</span></span>
  - <span data-ttu-id="ce870-164">`[Tag <IResourceTags>]`: Lista par klucz-wartość.</span><span class="sxs-lookup"><span data-stu-id="ce870-164">`[Tag <IResourceTags>]`: List of key-value pairs.</span></span>
    - <span data-ttu-id="ce870-165">`[(Any) <String>]`: Wskazuje, że do tego obiektu można dodać dowolną właściwość.</span><span class="sxs-lookup"><span data-stu-id="ce870-165">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="ce870-166">`[AddressPrefix <String>]`: Prefiks adresu.</span><span class="sxs-lookup"><span data-stu-id="ce870-166">`[AddressPrefix <String>]`: The address prefix.</span></span>
  - <span data-ttu-id="ce870-167">`[EndIPAddress <String>]`: Końcowy adres IP.</span><span class="sxs-lookup"><span data-stu-id="ce870-167">`[EndIPAddress <String>]`: The ending IP address.</span></span>
  - <span data-ttu-id="ce870-168">`[NumberOfAllocatedIPAddresses <Int64?>]`: Liczba obecnie przydzielonych adresów IP.</span><span class="sxs-lookup"><span data-stu-id="ce870-168">`[NumberOfAllocatedIPAddresses <Int64?>]`: The number of currently allocated IP addresses.</span></span>
  - <span data-ttu-id="ce870-169">`[NumberOfIPAddresses <Int64?>]`: Łączna liczba adresów IP.</span><span class="sxs-lookup"><span data-stu-id="ce870-169">`[NumberOfIPAddresses <Int64?>]`: The total number of IP addresses.</span></span>
  - <span data-ttu-id="ce870-170">`[NumberOfIPAddressesInTransition <Int64?>]`: Bieżąca liczba adresów IP w ramach przejścia.</span><span class="sxs-lookup"><span data-stu-id="ce870-170">`[NumberOfIPAddressesInTransition <Int64?>]`: The current number of IP addresses in transition.</span></span>
  - <span data-ttu-id="ce870-171">`[StartIPAddress <String>]`: Początkowy adres IP.</span><span class="sxs-lookup"><span data-stu-id="ce870-171">`[StartIPAddress <String>]`: The starting IP address.</span></span>

## <span data-ttu-id="ce870-172">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ce870-172">RELATED LINKS</span></span>

