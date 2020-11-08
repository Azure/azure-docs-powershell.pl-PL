---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 38917534-49C6-47EA-B815-240F794EE655
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVM.md
ms.openlocfilehash: e9ec68d7c3991d7a3eded2566d8e299ddcc36c85
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223177"
---
# <span data-ttu-id="04966-101">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="04966-101">Update-AzVM</span></span>

## <span data-ttu-id="04966-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="04966-102">SYNOPSIS</span></span>
<span data-ttu-id="04966-103">Umożliwia zaktualizowanie stanu maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="04966-103">Updates the state of an Azure virtual machine.</span></span>

## <span data-ttu-id="04966-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="04966-104">SYNTAX</span></span>

### <span data-ttu-id="04966-105">ResourceGroupNameParameterSetName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="04966-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 [-OsDiskWriteAccelerator <Boolean>] [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>]
 [-ProximityPlacementGroupId <String>] [-HostId <String>] [-EncryptionAtHost <Boolean>] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04966-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="04966-106">ExplicitIdentityParameterSet</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>] [-ProximityPlacementGroupId <String>] [-HostId <String>]
 [-EncryptionAtHost <Boolean>] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04966-107">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="04966-107">IdParameterSetName</span></span>
```
Update-AzVM [-Id] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>] [-ProximityPlacementGroupId <String>] [-HostId <String>]
 [-EncryptionAtHost <Boolean>] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04966-108">Opis</span><span class="sxs-lookup"><span data-stu-id="04966-108">DESCRIPTION</span></span>
<span data-ttu-id="04966-109">Polecenie cmdlet **Update-AzVM** powoduje zaktualizowanie stanu maszyny wirtualnej platformy Azure do stanu obiektu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="04966-109">The **Update-AzVM** cmdlet updates the state of an Azure virtual machine to the state of a virtual machine object.</span></span>

## <span data-ttu-id="04966-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="04966-110">EXAMPLES</span></span>

### <span data-ttu-id="04966-111">Przykład 1: aktualizowanie maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="04966-111">Example 1: Update a virtual machine</span></span>
```
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="04966-112">To polecenie powoduje zaktualizowanie maszyny wirtualnej $VirtualMachine w programie ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="04966-112">This command updates the virtual machine, $VirtualMachine, in ResourceGroup11.</span></span>
<span data-ttu-id="04966-113">Polecenie aktualizuje je za pomocą obiektu maszyny wirtualnej przechowywanego w zmiennej $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="04966-113">The command updates it by using the virtual machine object stored in the $VirtualMachine variable.</span></span>
<span data-ttu-id="04966-114">Aby uzyskać obiekt maszyny wirtualnej, użyj polecenia cmdlet **Get-AzVM** .</span><span class="sxs-lookup"><span data-stu-id="04966-114">To obtain a virtual machine object, use the **Get-AzVM** cmdlet.</span></span>

## <span data-ttu-id="04966-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="04966-115">PARAMETERS</span></span>

### <span data-ttu-id="04966-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="04966-116">-AsJob</span></span>
<span data-ttu-id="04966-117">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="04966-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="04966-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04966-118">-DefaultProfile</span></span>
<span data-ttu-id="04966-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="04966-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04966-120">-HostId</span><span class="sxs-lookup"><span data-stu-id="04966-120">-HostId</span></span>
<span data-ttu-id="04966-121">Identyfikator hosta</span><span class="sxs-lookup"><span data-stu-id="04966-121">The Id of Host</span></span>

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

### <span data-ttu-id="04966-122">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="04966-122">-EncryptionAtHost</span></span>
<span data-ttu-id="04966-123">Właściwość EncryptionAtHost może być używana przez użytkownika w żądaniu do włączania lub wyłączania szyfrowania hosta dla maszyny wirtualnej lub zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="04966-123">EncryptionAtHost property can be used by user in the request to enable or disable the Host Encryption for the virtual machine or virtual machine scale set.</span></span> <span data-ttu-id="04966-124">Spowoduje to włączenie szyfrowania wszystkich dysków, w tym dysku Resource/temp, na hoście.</span><span class="sxs-lookup"><span data-stu-id="04966-124">This will enable the encryption for all the disks including Resource/Temp disk at host itself.</span></span> 

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04966-125">-ID</span><span class="sxs-lookup"><span data-stu-id="04966-125">-Id</span></span>
<span data-ttu-id="04966-126">Określa identyfikator zasobu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="04966-126">Specifies the resource ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04966-127">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="04966-127">-IdentityId</span></span>
<span data-ttu-id="04966-128">Określa listę tożsamości użytkowników skojarzonych z maszyną wirtualną.</span><span class="sxs-lookup"><span data-stu-id="04966-128">Specifies the list of user identities associated with the virtual machine.</span></span>
<span data-ttu-id="04966-129">Odwołania tożsamości użytkownika będą miały identyfikatory zasobów ARM w formularzu: "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}"</span><span class="sxs-lookup"><span data-stu-id="04966-129">The user identity references will be ARM resource IDs in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: System.String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04966-130">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="04966-130">-IdentityType</span></span>
<span data-ttu-id="04966-131">Typ tożsamości używanej dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="04966-131">The type of identity used for the virtual machine.</span></span> <span data-ttu-id="04966-132">Prawidłowe wartości to SystemAssigned, UserAssigned, SystemAssignedUserAssigned i none.</span><span class="sxs-lookup"><span data-stu-id="04966-132">Valid values are SystemAssigned, UserAssigned, SystemAssignedUserAssigned, and None.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04966-133">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="04966-133">-MaxPrice</span></span>
<span data-ttu-id="04966-134">Określa cenę maksymalną, jaką można zapłacić za niski priorytet maszyny wirtualnej/VMSS.</span><span class="sxs-lookup"><span data-stu-id="04966-134">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="04966-135">Ta cena jest w dolarach amerykańskich.</span><span class="sxs-lookup"><span data-stu-id="04966-135">This price is in US Dollars.</span></span> <span data-ttu-id="04966-136">Ta cena będzie porównywana z bieżącą ceną o niskim priorytecie dla rozmiaru maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="04966-136">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="04966-137">Ceny są również porównywane w czasie tworzenia/aktualizowania o niskim priorytecie maszyny wirtualnej/VMSS, a operacja będzie dostępna tylko wtedy, gdy maxPrice jest większa niż bieżąca cena o niskim priorytecie.</span><span class="sxs-lookup"><span data-stu-id="04966-137">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="04966-138">MaxPrice będzie również stosowany do wykluczania niewielkiego priorytetu maszyn wirtualnych/VMSS, jeśli obecna cena o niskim priorytecie wykracza poza maxPrice po utworzeniu maszyny wirtualnej/VMSS.</span><span class="sxs-lookup"><span data-stu-id="04966-138">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="04966-139">Możliwe wartości: Każda wartość dziesiętna większa niż zero.</span><span class="sxs-lookup"><span data-stu-id="04966-139">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="04966-140">Przykład: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="04966-140">Example: 0.01538.</span></span>  <span data-ttu-id="04966-141">-1 wskazuje, że nie można wykluczyć niskiego priorytetu maszyn wirtualnych/VMSS w celu uzyskania podstawy cenowej.</span><span class="sxs-lookup"><span data-stu-id="04966-141">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="04966-142">Ponadto domyślna cena maksymalna wynosi-1, jeśli nie jest podana przez Ciebie.</span><span class="sxs-lookup"><span data-stu-id="04966-142">Also, the default max price is -1 if it is not provided by you.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04966-143">-Nowait</span><span class="sxs-lookup"><span data-stu-id="04966-143">-NoWait</span></span>
<span data-ttu-id="04966-144">Rozpoczyna operację i wraca natychmiast, zanim operacja zostanie ukończona.</span><span class="sxs-lookup"><span data-stu-id="04966-144">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="04966-145">W celu ustalenia, czy operacja została wykonana pomyślnie, użyj innego mechanizmu.</span><span class="sxs-lookup"><span data-stu-id="04966-145">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="04966-146">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="04966-146">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="04966-147">Określa, czy WriteAccelerator należy włączyć lub wyłączyć na dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="04966-147">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04966-148">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="04966-148">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="04966-149">Identyfikator zasobu grupy położenia zbliżeniowe, który ma być używany z tą maszyną wirtualną.</span><span class="sxs-lookup"><span data-stu-id="04966-149">The resource id of the Proximity Placement Group to use with this virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04966-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04966-150">-ResourceGroupName</span></span>
<span data-ttu-id="04966-151">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="04966-151">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName, ExplicitIdentityParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04966-152">-Tag</span><span class="sxs-lookup"><span data-stu-id="04966-152">-Tag</span></span>
<span data-ttu-id="04966-153">Określa zasoby i grupy zasobów, które można wyznacznikować za pomocą zestawu par nazwa-wartość.</span><span class="sxs-lookup"><span data-stu-id="04966-153">Specifies the resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="04966-154">Dodawanie znaczników do zasobów umożliwia grupowanie zasobów między grupami zasobów i tworzenie własnych widoków.</span><span class="sxs-lookup"><span data-stu-id="04966-154">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="04966-155">Każdy zasób lub Grupa zasobów może zawierać maksymalnie 15 tagów.</span><span class="sxs-lookup"><span data-stu-id="04966-155">Each resource or resource group can have a maximum of 15 tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04966-156">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="04966-156">-UltraSSDEnabled</span></span>
<span data-ttu-id="04966-157">Flaga, która umożliwia lub wyłącza możliwość posiadania jednego lub większej liczby zarządzanych dysków z danymi, UltraSSD_LRS typ konta magazynu na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="04966-157">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="04966-158">Dyski zarządzane z typem konta magazynu UltraSSD_LRS można dodawać do maszyny wirtualnej tylko wtedy, gdy ta właściwość jest włączona.</span><span class="sxs-lookup"><span data-stu-id="04966-158">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04966-159">-VM</span><span class="sxs-lookup"><span data-stu-id="04966-159">-VM</span></span>
<span data-ttu-id="04966-160">Określa obiekt lokalnego maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="04966-160">Specifies a local virtual machine object.</span></span>
<span data-ttu-id="04966-161">Aby uzyskać obiekt maszyny wirtualnej, użyj polecenia cmdlet Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="04966-161">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="04966-162">Ten obiekt maszyny wirtualnej zawiera zaktualizowany stan maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="04966-162">This virtual machine object contains the updated state for the virtual machine.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="04966-163">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="04966-163">-Confirm</span></span>
<span data-ttu-id="04966-164">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04966-164">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04966-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04966-165">-WhatIf</span></span>
<span data-ttu-id="04966-166">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04966-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04966-167">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="04966-167">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```


### <span data-ttu-id="04966-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04966-168">CommonParameters</span></span>
<span data-ttu-id="04966-169">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04966-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04966-170">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="04966-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04966-171">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="04966-171">INPUTS</span></span>

### <span data-ttu-id="04966-172">System. String</span><span class="sxs-lookup"><span data-stu-id="04966-172">System.String</span></span>

### <span data-ttu-id="04966-173">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="04966-173">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="04966-174">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="04966-174">System.Boolean</span></span>

## <span data-ttu-id="04966-175">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="04966-175">OUTPUTS</span></span>

### <span data-ttu-id="04966-176">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="04966-176">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="04966-177">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="04966-177">NOTES</span></span>

## <span data-ttu-id="04966-178">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="04966-178">RELATED LINKS</span></span>

[<span data-ttu-id="04966-179">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="04966-179">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="04966-180">Nowe — AzVM</span><span class="sxs-lookup"><span data-stu-id="04966-180">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="04966-181">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="04966-181">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="04966-182">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="04966-182">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="04966-183">Start — AzVM</span><span class="sxs-lookup"><span data-stu-id="04966-183">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="04966-184">Zatrzymaj — AzVM</span><span class="sxs-lookup"><span data-stu-id="04966-184">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="04966-185">Nowe — AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="04966-185">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


