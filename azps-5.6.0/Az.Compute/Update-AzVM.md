---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 38917534-49C6-47EA-B815-240F794EE655
online version: https://docs.microsoft.com/powershell/module/az.compute/update-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVM.md
ms.openlocfilehash: e7a86b191687f72cb538fb017a904890e4958d50
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955969"
---
# <span data-ttu-id="534b9-101">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="534b9-101">Update-AzVM</span></span>

## <span data-ttu-id="534b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="534b9-102">SYNOPSIS</span></span>
<span data-ttu-id="534b9-103">Aktualizuje stan maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="534b9-103">Updates the state of an Azure virtual machine.</span></span>

## <span data-ttu-id="534b9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="534b9-104">SYNTAX</span></span>

### <span data-ttu-id="534b9-105">ResourceGroupNameParameterSetName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="534b9-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 [-OsDiskWriteAccelerator <Boolean>] [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>]
 [-ProximityPlacementGroupId <String>] [-HostId <String>] [-EncryptionAtHost <Boolean>] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="534b9-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="534b9-106">ExplicitIdentityParameterSet</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>] [-ProximityPlacementGroupId <String>] [-HostId <String>]
 [-EncryptionAtHost <Boolean>] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="534b9-107">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="534b9-107">IdParameterSetName</span></span>
```
Update-AzVM [-Id] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>] [-ProximityPlacementGroupId <String>] [-HostId <String>]
 [-EncryptionAtHost <Boolean>] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="534b9-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="534b9-108">DESCRIPTION</span></span>
<span data-ttu-id="534b9-109">Polecenie **cmdlet Update-AzVM** aktualizuje stan maszyny wirtualnej platformy Azure do stanu obiektu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="534b9-109">The **Update-AzVM** cmdlet updates the state of an Azure virtual machine to the state of a virtual machine object.</span></span>

## <span data-ttu-id="534b9-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="534b9-110">EXAMPLES</span></span>

### <span data-ttu-id="534b9-111">Przykład 1. Aktualizowanie maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="534b9-111">Example 1: Update a virtual machine</span></span>
```
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="534b9-112">To polecenie aktualizuje maszynę wirtualną w $VirtualMachine ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="534b9-112">This command updates the virtual machine, $VirtualMachine, in ResourceGroup11.</span></span>
<span data-ttu-id="534b9-113">Polecenie aktualizuje je przy użyciu obiektu maszyny wirtualnej przechowywanego w $VirtualMachine zmienną.</span><span class="sxs-lookup"><span data-stu-id="534b9-113">The command updates it by using the virtual machine object stored in the $VirtualMachine variable.</span></span>
<span data-ttu-id="534b9-114">Aby uzyskać obiekt maszyny wirtualnej, użyj polecenia cmdlet **Get-AzVM.**</span><span class="sxs-lookup"><span data-stu-id="534b9-114">To obtain a virtual machine object, use the **Get-AzVM** cmdlet.</span></span>

## <span data-ttu-id="534b9-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="534b9-115">PARAMETERS</span></span>

### <span data-ttu-id="534b9-116">— AsJob</span><span class="sxs-lookup"><span data-stu-id="534b9-116">-AsJob</span></span>
<span data-ttu-id="534b9-117">Uruchom polecenie cmdlet w tle i zwróć zadanie w celu śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="534b9-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="534b9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="534b9-118">-DefaultProfile</span></span>
<span data-ttu-id="534b9-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="534b9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="534b9-120">-HostId</span><span class="sxs-lookup"><span data-stu-id="534b9-120">-HostId</span></span>
<span data-ttu-id="534b9-121">Identyfikator hosta</span><span class="sxs-lookup"><span data-stu-id="534b9-121">The Id of Host</span></span>

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

### <span data-ttu-id="534b9-122">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="534b9-122">-EncryptionAtHost</span></span>
<span data-ttu-id="534b9-123">Właściwość EncryptionAtHost może być używana przez użytkownika w żądaniu włączenia lub wyłączenia szyfrowania hosta dla zestawu skali maszyny wirtualnej lub maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="534b9-123">EncryptionAtHost property can be used by user in the request to enable or disable the Host Encryption for the virtual machine or virtual machine scale set.</span></span> <span data-ttu-id="534b9-124">Spowoduje to włączenie szyfrowania dla wszystkich dysków, w tym dysku zasobu/tempa na samym hoście.</span><span class="sxs-lookup"><span data-stu-id="534b9-124">This will enable the encryption for all the disks including Resource/Temp disk at host itself.</span></span> 

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

### <span data-ttu-id="534b9-125">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="534b9-125">-Id</span></span>
<span data-ttu-id="534b9-126">Określa identyfikator zasobu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="534b9-126">Specifies the resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="534b9-127">- IdentityId</span><span class="sxs-lookup"><span data-stu-id="534b9-127">-IdentityId</span></span>
<span data-ttu-id="534b9-128">Określa listę tożsamości użytkowników skojarzonych z maszyną wirtualną.</span><span class="sxs-lookup"><span data-stu-id="534b9-128">Specifies the list of user identities associated with the virtual machine.</span></span>
<span data-ttu-id="534b9-129">Odwołania do tożsamości użytkownika ARM identyfikatorami zasobów w postaci: "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}"</span><span class="sxs-lookup"><span data-stu-id="534b9-129">The user identity references will be ARM resource IDs in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="534b9-130">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="534b9-130">-IdentityType</span></span>
<span data-ttu-id="534b9-131">Typ tożsamości używany dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="534b9-131">The type of identity used for the virtual machine.</span></span> <span data-ttu-id="534b9-132">Prawidłowe wartości to SystemAssigned, UserAssigned, SystemAssignedUserAssigned i None.</span><span class="sxs-lookup"><span data-stu-id="534b9-132">Valid values are SystemAssigned, UserAssigned, SystemAssignedUserAssigned, and None.</span></span>

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

### <span data-ttu-id="534b9-133">- MaxCena</span><span class="sxs-lookup"><span data-stu-id="534b9-133">-MaxPrice</span></span>
<span data-ttu-id="534b9-134">Określa maksymalną cenę za niską płatność za maszyny wirtualne/maszyny wirtualne o niskim priorytecie.</span><span class="sxs-lookup"><span data-stu-id="534b9-134">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="534b9-135">Ta cena jest w dolarach amerykańskich.</span><span class="sxs-lookup"><span data-stu-id="534b9-135">This price is in US Dollars.</span></span> <span data-ttu-id="534b9-136">Ta cena będzie porównywana z bieżącą ceną o niskim priorytecie dla rozmiaru maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="534b9-136">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="534b9-137">Ponadto ceny są porównywane w czasie tworzenia/aktualizacji maszyny wirtualnej/maszyny wirtualnej o niskim priorytecie, a operacja zakończy się powodzeniem tylko wtedy, gdy wartość maxCena jest większa niż obecna cena o niskim priorytecie.</span><span class="sxs-lookup"><span data-stu-id="534b9-137">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="534b9-138">Cena maksymalna będzie również używana do evicowania maszyny wirtualnej/maszyny wirtualnej o niskim priorytecie, jeśli bieżąca cena o niskim priorytecie przekracza wartość maxCena po utworzeniu maszyny wirtualnej/maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="534b9-138">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="534b9-139">Dopuszczalne wartości to: dowolna wartość dziesiętna większa niż zero.</span><span class="sxs-lookup"><span data-stu-id="534b9-139">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="534b9-140">Przykład: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="534b9-140">Example: 0.01538.</span></span>  <span data-ttu-id="534b9-141">-1 oznacza, że maszyny wirtualnej/maszyny wirtualnej o niskim priorytecie nie należy ich ujednać ze względu na cenę.</span><span class="sxs-lookup"><span data-stu-id="534b9-141">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="534b9-142">Ponadto domyślna maksymalna cena to -1, jeśli nie jest ona przez Ciebie dostarczana.</span><span class="sxs-lookup"><span data-stu-id="534b9-142">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="534b9-143">-NoWait</span><span class="sxs-lookup"><span data-stu-id="534b9-143">-NoWait</span></span>
<span data-ttu-id="534b9-144">Rozpoczyna operację i zwraca bezpośrednio przed jej ukończeniem.</span><span class="sxs-lookup"><span data-stu-id="534b9-144">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="534b9-145">Aby ustalić, czy operacja została pomyślnie ukończona, użyj innego mechanizmu.</span><span class="sxs-lookup"><span data-stu-id="534b9-145">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="534b9-146">-Os JednakowyAccelerator</span><span class="sxs-lookup"><span data-stu-id="534b9-146">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="534b9-147">Określa, czy funkcja WriteAccelerator ma być włączona, czy wyłączona na dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="534b9-147">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="534b9-148">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="534b9-148">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="534b9-149">Identyfikator zasobu grupy Położenie odległości, która ma być używania z tą maszyną wirtualną.</span><span class="sxs-lookup"><span data-stu-id="534b9-149">The resource id of the Proximity Placement Group to use with this virtual machine.</span></span>

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

### <span data-ttu-id="534b9-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="534b9-150">-ResourceGroupName</span></span>
<span data-ttu-id="534b9-151">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="534b9-151">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="534b9-152">— Tag</span><span class="sxs-lookup"><span data-stu-id="534b9-152">-Tag</span></span>
<span data-ttu-id="534b9-153">Określa zasoby i grupy zasobów, które można otagowyć za pomocą zestawu par nazwa-wartość.</span><span class="sxs-lookup"><span data-stu-id="534b9-153">Specifies the resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="534b9-154">Dodawanie tagów do zasobów umożliwia grupowanie zasobów w różnych grupach zasobów i tworzenie własnych widoków.</span><span class="sxs-lookup"><span data-stu-id="534b9-154">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="534b9-155">Każda grupa zasobów lub zasobu może mieć maksymalnie 15 tagów.</span><span class="sxs-lookup"><span data-stu-id="534b9-155">Each resource or resource group can have a maximum of 15 tags.</span></span>

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

### <span data-ttu-id="534b9-156">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="534b9-156">-UltraSSDEnabled</span></span>
<span data-ttu-id="534b9-157">Flaga umożliwiająca włączenie lub wyłączenie możliwości, aby jedna lub więcej zarządzanych dysków danych UltraSSD_LRS typ konta magazynu na maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="534b9-157">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="534b9-158">Dysk zarządzany z kontem magazynu typu UltraSSD_LRS można dodawać do maszyny wirtualnej tylko wtedy, gdy ta właściwość jest włączona.</span><span class="sxs-lookup"><span data-stu-id="534b9-158">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>

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

### <span data-ttu-id="534b9-159">— MASZYNY WIRTUALNEJ</span><span class="sxs-lookup"><span data-stu-id="534b9-159">-VM</span></span>
<span data-ttu-id="534b9-160">Określa obiekt lokalnej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="534b9-160">Specifies a local virtual machine object.</span></span>
<span data-ttu-id="534b9-161">Aby uzyskać obiekt maszyny wirtualnej, użyj Get-AzVM cmdlet.</span><span class="sxs-lookup"><span data-stu-id="534b9-161">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="534b9-162">Ten obiekt maszyny wirtualnej zawiera zaktualizowany stan maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="534b9-162">This virtual machine object contains the updated state for the virtual machine.</span></span>

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

### <span data-ttu-id="534b9-163">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="534b9-163">-Confirm</span></span>
<span data-ttu-id="534b9-164">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="534b9-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="534b9-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="534b9-165">-WhatIf</span></span>
<span data-ttu-id="534b9-166">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="534b9-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="534b9-167">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="534b9-167">The cmdlet is not run.</span></span>

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


### <span data-ttu-id="534b9-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="534b9-168">CommonParameters</span></span>
<span data-ttu-id="534b9-169">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="534b9-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="534b9-170">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="534b9-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="534b9-171">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="534b9-171">INPUTS</span></span>

### <span data-ttu-id="534b9-172">System.String</span><span class="sxs-lookup"><span data-stu-id="534b9-172">System.String</span></span>

### <span data-ttu-id="534b9-173">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="534b9-173">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="534b9-174">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="534b9-174">System.Boolean</span></span>

## <span data-ttu-id="534b9-175">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="534b9-175">OUTPUTS</span></span>

### <span data-ttu-id="534b9-176">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="534b9-176">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="534b9-177">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="534b9-177">NOTES</span></span>

## <span data-ttu-id="534b9-178">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="534b9-178">RELATED LINKS</span></span>

[<span data-ttu-id="534b9-179">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="534b9-179">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="534b9-180">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="534b9-180">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="534b9-181">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="534b9-181">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="534b9-182">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="534b9-182">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="534b9-183">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="534b9-183">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="534b9-184">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="534b9-184">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="534b9-185">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="534b9-185">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


