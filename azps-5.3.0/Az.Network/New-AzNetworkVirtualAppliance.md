---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkvirtualappliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkVirtualAppliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkVirtualAppliance.md
ms.openlocfilehash: 9b3991a24430afa74853f742bffa12b772dbeaf2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491030"
---
# <span data-ttu-id="547e3-101">New-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="547e3-101">New-AzNetworkVirtualAppliance</span></span>

## <span data-ttu-id="547e3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="547e3-102">SYNOPSIS</span></span>
<span data-ttu-id="547e3-103">Tworzenie sieciowego zasobu urządzenia wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="547e3-103">Create a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="547e3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="547e3-104">SYNTAX</span></span>

### <span data-ttu-id="547e3-105">ResourceNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="547e3-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzNetworkVirtualAppliance -Name <String> -ResourceGroupName <String> -Location <String>
 -VirtualHubId <String> -Sku <PSVirtualApplianceSkuProperties> -VirtualApplianceAsn <Int32>
 [-Identity <PSManagedServiceIdentity>] [-BootStrapConfigurationBlob <String[]>]
 [-CloudInitConfigurationBlob <String[]>] [-CloudInitConfiguration <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="547e3-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="547e3-106">ResourceIdParameterSet</span></span>
```
New-AzNetworkVirtualAppliance -ResourceId <String> -Location <String> -VirtualHubId <String>
 -Sku <PSVirtualApplianceSkuProperties> -VirtualApplianceAsn <Int32> [-Identity <PSManagedServiceIdentity>]
 [-BootStrapConfigurationBlob <String[]>] [-CloudInitConfigurationBlob <String[]>]
 [-CloudInitConfiguration <String>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="547e3-107">Opis</span><span class="sxs-lookup"><span data-stu-id="547e3-107">DESCRIPTION</span></span>
<span data-ttu-id="547e3-108">Polecenie New-AzNetworkVirtualAppliance służy do tworzenia zasobu sieciowego urządzenia wirtualnego na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="547e3-108">The New-AzNetworkVirtualAppliance command creates a Network Virtual Appliance resource in Azure.</span></span>

## <span data-ttu-id="547e3-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="547e3-109">EXAMPLES</span></span>

### <span data-ttu-id="547e3-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="547e3-110">Example 1</span></span>
```powershell
PS C:\> $sku=New-AzVirtualApplianceSkuProperty -VendorName "barracudasdwanrelease" -BundledScaleUnit 1 -MarketPlaceVersion 'latest'
PS C:\> $hub=Get-AzVirtualHub -ResourceGroupName testrg -Name hub
PS C:\> $nva=New-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva -Location eastus2 -VirtualApplianceAsn 1270 -VirtualHubId $hub.Id -Sku $sku -CloudInitConfiguration "echo Hello World!"

```

<span data-ttu-id="547e3-111">Tworzy nowy zasób sieciowego urządzenia wirtualnego w grupie zasób: testrg.</span><span class="sxs-lookup"><span data-stu-id="547e3-111">Creates a new Network Virtual Appliance resource in resource group: testrg.</span></span>

## <span data-ttu-id="547e3-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="547e3-112">PARAMETERS</span></span>

### <span data-ttu-id="547e3-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="547e3-113">-AsJob</span></span>
<span data-ttu-id="547e3-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="547e3-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="547e3-115">-BootStrapConfigurationBlob</span><span class="sxs-lookup"><span data-stu-id="547e3-115">-BootStrapConfigurationBlob</span></span>
<span data-ttu-id="547e3-116">Adres URL obiektu BLOB konfiguracji bootstrap.</span><span class="sxs-lookup"><span data-stu-id="547e3-116">The Bootstrap configuration blob URL.</span></span>

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

### <span data-ttu-id="547e3-117">-CloudInitConfiguration</span><span class="sxs-lookup"><span data-stu-id="547e3-117">-CloudInitConfiguration</span></span>
<span data-ttu-id="547e3-118">Konfiguracja Cloudinit jako zwykły tekst.</span><span class="sxs-lookup"><span data-stu-id="547e3-118">The Cloudinit configuration as plain text.</span></span>

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

### <span data-ttu-id="547e3-119">-CloudInitConfigurationBlob</span><span class="sxs-lookup"><span data-stu-id="547e3-119">-CloudInitConfigurationBlob</span></span>
<span data-ttu-id="547e3-120">Adres URL magazynu obiektów BLOB konfiguracji Cloudinit.</span><span class="sxs-lookup"><span data-stu-id="547e3-120">The Cloudinit configuration blob storage URL.</span></span>

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

### <span data-ttu-id="547e3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="547e3-121">-DefaultProfile</span></span>
<span data-ttu-id="547e3-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="547e3-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="547e3-123">-Force</span><span class="sxs-lookup"><span data-stu-id="547e3-123">-Force</span></span>
<span data-ttu-id="547e3-124">Nie pytaj o potwierdzenie zamiaru zastąpienia zasobu</span><span class="sxs-lookup"><span data-stu-id="547e3-124">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="547e3-125">-Identity (tożsamość)</span><span class="sxs-lookup"><span data-stu-id="547e3-125">-Identity</span></span>
<span data-ttu-id="547e3-126">Tożsamość zarządzana.</span><span class="sxs-lookup"><span data-stu-id="547e3-126">The Managed identity.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="547e3-127">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="547e3-127">-Location</span></span>
<span data-ttu-id="547e3-128">Lokalizacja publicznego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="547e3-128">The public IP address location.</span></span>

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

### <span data-ttu-id="547e3-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="547e3-129">-Name</span></span>
<span data-ttu-id="547e3-130">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="547e3-130">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="547e3-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="547e3-131">-ResourceGroupName</span></span>
<span data-ttu-id="547e3-132">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="547e3-132">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="547e3-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="547e3-133">-ResourceId</span></span>
<span data-ttu-id="547e3-134">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="547e3-134">The resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="547e3-135">-SKU</span><span class="sxs-lookup"><span data-stu-id="547e3-135">-Sku</span></span>
<span data-ttu-id="547e3-136">Wersja SKU urządzenia wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="547e3-136">The Sku of the Virtual Appliance.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="547e3-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="547e3-137">-Tag</span></span>
<span data-ttu-id="547e3-138">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="547e3-138">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="547e3-139">-VirtualApplianceAsn</span><span class="sxs-lookup"><span data-stu-id="547e3-139">-VirtualApplianceAsn</span></span>
<span data-ttu-id="547e3-140">Numer ASN urządzenia wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="547e3-140">The ASN number of the Virtual Appliance.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="547e3-141">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="547e3-141">-VirtualHubId</span></span>
<span data-ttu-id="547e3-142">Identyfikator zasobu koncentratora wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="547e3-142">The Resource Id of the Virtual Hub.</span></span>

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

### <span data-ttu-id="547e3-143">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="547e3-143">-Confirm</span></span>
<span data-ttu-id="547e3-144">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="547e3-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="547e3-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="547e3-145">-WhatIf</span></span>
<span data-ttu-id="547e3-146">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="547e3-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="547e3-147">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="547e3-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="547e3-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="547e3-148">CommonParameters</span></span>
<span data-ttu-id="547e3-149">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="547e3-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="547e3-150">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="547e3-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="547e3-151">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="547e3-151">INPUTS</span></span>

### <span data-ttu-id="547e3-152">System. String</span><span class="sxs-lookup"><span data-stu-id="547e3-152">System.String</span></span>

### <span data-ttu-id="547e3-153">Microsoft. Azure. Commands. Network. models. PSVirtualApplianceSkuProperties</span><span class="sxs-lookup"><span data-stu-id="547e3-153">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties</span></span>

### <span data-ttu-id="547e3-154">System. Int32</span><span class="sxs-lookup"><span data-stu-id="547e3-154">System.Int32</span></span>

### <span data-ttu-id="547e3-155">Microsoft. Azure. Commands. Network. models. PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="547e3-155">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

### <span data-ttu-id="547e3-156">System. String []</span><span class="sxs-lookup"><span data-stu-id="547e3-156">System.String[]</span></span>

### <span data-ttu-id="547e3-157">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="547e3-157">System.Collections.Hashtable</span></span>

## <span data-ttu-id="547e3-158">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="547e3-158">OUTPUTS</span></span>

### <span data-ttu-id="547e3-159">Microsoft. Azure. Commands. Network. models. PSNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="547e3-159">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span></span>

## <span data-ttu-id="547e3-160">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="547e3-160">NOTES</span></span>

## <span data-ttu-id="547e3-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="547e3-161">RELATED LINKS</span></span>
