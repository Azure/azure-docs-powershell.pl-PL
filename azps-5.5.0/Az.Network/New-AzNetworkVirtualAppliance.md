---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkvirtualappliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkVirtualAppliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkVirtualAppliance.md
ms.openlocfilehash: 9b3991a24430afa74853f742bffa12b772dbeaf2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202772"
---
# <span data-ttu-id="a687e-101">New-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="a687e-101">New-AzNetworkVirtualAppliance</span></span>

## <span data-ttu-id="a687e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a687e-102">SYNOPSIS</span></span>
<span data-ttu-id="a687e-103">Utwórz zasób urządzenia wirtualnego sieci.</span><span class="sxs-lookup"><span data-stu-id="a687e-103">Create a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="a687e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a687e-104">SYNTAX</span></span>

### <span data-ttu-id="a687e-105">ResourceNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="a687e-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzNetworkVirtualAppliance -Name <String> -ResourceGroupName <String> -Location <String>
 -VirtualHubId <String> -Sku <PSVirtualApplianceSkuProperties> -VirtualApplianceAsn <Int32>
 [-Identity <PSManagedServiceIdentity>] [-BootStrapConfigurationBlob <String[]>]
 [-CloudInitConfigurationBlob <String[]>] [-CloudInitConfiguration <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a687e-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a687e-106">ResourceIdParameterSet</span></span>
```
New-AzNetworkVirtualAppliance -ResourceId <String> -Location <String> -VirtualHubId <String>
 -Sku <PSVirtualApplianceSkuProperties> -VirtualApplianceAsn <Int32> [-Identity <PSManagedServiceIdentity>]
 [-BootStrapConfigurationBlob <String[]>] [-CloudInitConfigurationBlob <String[]>]
 [-CloudInitConfiguration <String>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a687e-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="a687e-107">DESCRIPTION</span></span>
<span data-ttu-id="a687e-108">Polecenie New-AzNetworkVirtualAppliance umożliwia utworzenie zasobu Network Virtual Appliance na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="a687e-108">The New-AzNetworkVirtualAppliance command creates a Network Virtual Appliance resource in Azure.</span></span>

## <span data-ttu-id="a687e-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a687e-109">EXAMPLES</span></span>

### <span data-ttu-id="a687e-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a687e-110">Example 1</span></span>
```powershell
PS C:\> $sku=New-AzVirtualApplianceSkuProperty -VendorName "barracudasdwanrelease" -BundledScaleUnit 1 -MarketPlaceVersion 'latest'
PS C:\> $hub=Get-AzVirtualHub -ResourceGroupName testrg -Name hub
PS C:\> $nva=New-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva -Location eastus2 -VirtualApplianceAsn 1270 -VirtualHubId $hub.Id -Sku $sku -CloudInitConfiguration "echo Hello World!"

```

<span data-ttu-id="a687e-111">Tworzy nowy zasób wirtualnego urządzenia sieciowego w grupie zasobów: testrg.</span><span class="sxs-lookup"><span data-stu-id="a687e-111">Creates a new Network Virtual Appliance resource in resource group: testrg.</span></span>

## <span data-ttu-id="a687e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a687e-112">PARAMETERS</span></span>

### <span data-ttu-id="a687e-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="a687e-113">-AsJob</span></span>
<span data-ttu-id="a687e-114">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="a687e-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a687e-115">-BootStrapConfigurationBlob</span><span class="sxs-lookup"><span data-stu-id="a687e-115">-BootStrapConfigurationBlob</span></span>
<span data-ttu-id="a687e-116">Adres URL obiektu blob konfiguracji Bootstrap.</span><span class="sxs-lookup"><span data-stu-id="a687e-116">The Bootstrap configuration blob URL.</span></span>

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

### <span data-ttu-id="a687e-117">— CloudInitConfiguration</span><span class="sxs-lookup"><span data-stu-id="a687e-117">-CloudInitConfiguration</span></span>
<span data-ttu-id="a687e-118">Konfiguracja Cloudinit jako zwykły tekst.</span><span class="sxs-lookup"><span data-stu-id="a687e-118">The Cloudinit configuration as plain text.</span></span>

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

### <span data-ttu-id="a687e-119">-CloudInitConfigurationBlob</span><span class="sxs-lookup"><span data-stu-id="a687e-119">-CloudInitConfigurationBlob</span></span>
<span data-ttu-id="a687e-120">Adres URL magazynu obiektów blob konfiguracji cloudinitu.</span><span class="sxs-lookup"><span data-stu-id="a687e-120">The Cloudinit configuration blob storage URL.</span></span>

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

### <span data-ttu-id="a687e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a687e-121">-DefaultProfile</span></span>
<span data-ttu-id="a687e-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a687e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a687e-123">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="a687e-123">-Force</span></span>
<span data-ttu-id="a687e-124">Nie pytaj o potwierdzenie, jeśli chcesz zastąpić zasób</span><span class="sxs-lookup"><span data-stu-id="a687e-124">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="a687e-125">— Tożsamość</span><span class="sxs-lookup"><span data-stu-id="a687e-125">-Identity</span></span>
<span data-ttu-id="a687e-126">Tożsamość zarządzana.</span><span class="sxs-lookup"><span data-stu-id="a687e-126">The Managed identity.</span></span>

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

### <span data-ttu-id="a687e-127">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="a687e-127">-Location</span></span>
<span data-ttu-id="a687e-128">Lokalizacja publicznego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="a687e-128">The public IP address location.</span></span>

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

### <span data-ttu-id="a687e-129">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a687e-129">-Name</span></span>
<span data-ttu-id="a687e-130">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="a687e-130">The resource name.</span></span>

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

### <span data-ttu-id="a687e-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a687e-131">-ResourceGroupName</span></span>
<span data-ttu-id="a687e-132">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a687e-132">The resource group name.</span></span>

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

### <span data-ttu-id="a687e-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a687e-133">-ResourceId</span></span>
<span data-ttu-id="a687e-134">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="a687e-134">The resource Id.</span></span>

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

### <span data-ttu-id="a687e-135">- SKU</span><span class="sxs-lookup"><span data-stu-id="a687e-135">-Sku</span></span>
<span data-ttu-id="a687e-136">SKU urządzenia wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="a687e-136">The Sku of the Virtual Appliance.</span></span>

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

### <span data-ttu-id="a687e-137">— Tag</span><span class="sxs-lookup"><span data-stu-id="a687e-137">-Tag</span></span>
<span data-ttu-id="a687e-138">Tabela skrótów reprezentująca tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="a687e-138">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="a687e-139">-VirtualApplianceAsn</span><span class="sxs-lookup"><span data-stu-id="a687e-139">-VirtualApplianceAsn</span></span>
<span data-ttu-id="a687e-140">Numer ASN urządzenia wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="a687e-140">The ASN number of the Virtual Appliance.</span></span>

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

### <span data-ttu-id="a687e-141">- VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="a687e-141">-VirtualHubId</span></span>
<span data-ttu-id="a687e-142">Identyfikator zasobu centrum wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="a687e-142">The Resource Id of the Virtual Hub.</span></span>

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

### <span data-ttu-id="a687e-143">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a687e-143">-Confirm</span></span>
<span data-ttu-id="a687e-144">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a687e-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a687e-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a687e-145">-WhatIf</span></span>
<span data-ttu-id="a687e-146">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a687e-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a687e-147">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a687e-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a687e-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a687e-148">CommonParameters</span></span>
<span data-ttu-id="a687e-149">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a687e-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a687e-150">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a687e-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a687e-151">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a687e-151">INPUTS</span></span>

### <span data-ttu-id="a687e-152">System.String</span><span class="sxs-lookup"><span data-stu-id="a687e-152">System.String</span></span>

### <span data-ttu-id="a687e-153">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties</span><span class="sxs-lookup"><span data-stu-id="a687e-153">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties</span></span>

### <span data-ttu-id="a687e-154">System.Int32</span><span class="sxs-lookup"><span data-stu-id="a687e-154">System.Int32</span></span>

### <span data-ttu-id="a687e-155">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="a687e-155">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

### <span data-ttu-id="a687e-156">System.String[]</span><span class="sxs-lookup"><span data-stu-id="a687e-156">System.String[]</span></span>

### <span data-ttu-id="a687e-157">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="a687e-157">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a687e-158">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a687e-158">OUTPUTS</span></span>

### <span data-ttu-id="a687e-159">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="a687e-159">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span></span>

## <span data-ttu-id="a687e-160">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a687e-160">NOTES</span></span>

## <span data-ttu-id="a687e-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a687e-161">RELATED LINKS</span></span>
