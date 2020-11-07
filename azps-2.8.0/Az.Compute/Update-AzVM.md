---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 38917534-49C6-47EA-B815-240F794EE655
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVM.md
ms.openlocfilehash: 339d63fe02c8286dc5867428269dc2e2afe342d3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706119"
---
# <span data-ttu-id="52849-101">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="52849-101">Update-AzVM</span></span>

## <span data-ttu-id="52849-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="52849-102">SYNOPSIS</span></span>
<span data-ttu-id="52849-103">Umożliwia zaktualizowanie stanu maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="52849-103">Updates the state of an Azure virtual machine.</span></span>

## <span data-ttu-id="52849-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="52849-104">SYNTAX</span></span>

### <span data-ttu-id="52849-105">ResourceGroupNameParameterSetName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="52849-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 [-OsDiskWriteAccelerator <Boolean>] [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52849-106">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="52849-106">AssignIdentityParameterSet</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-AssignIdentity]
 [-OsDiskWriteAccelerator <Boolean>] [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52849-107">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="52849-107">ExplicitIdentityParameterSet</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52849-108">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="52849-108">IdParameterSetName</span></span>
```
Update-AzVM [-Id] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52849-109">Opis</span><span class="sxs-lookup"><span data-stu-id="52849-109">DESCRIPTION</span></span>
<span data-ttu-id="52849-110">Polecenie cmdlet **Update-AzVM** powoduje zaktualizowanie stanu maszyny wirtualnej platformy Azure do stanu obiektu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="52849-110">The **Update-AzVM** cmdlet updates the state of an Azure virtual machine to the state of a virtual machine object.</span></span>

## <span data-ttu-id="52849-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="52849-111">EXAMPLES</span></span>

### <span data-ttu-id="52849-112">Przykład 1: aktualizowanie maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="52849-112">Example 1: Update a virtual machine</span></span>
```
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="52849-113">To polecenie powoduje zaktualizowanie maszyny wirtualnej $VirtualMachine w programie ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="52849-113">This command updates the virtual machine, $VirtualMachine, in ResourceGroup11.</span></span>
<span data-ttu-id="52849-114">Polecenie aktualizuje je za pomocą obiektu maszyny wirtualnej przechowywanego w zmiennej $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="52849-114">The command updates it by using the virtual machine object stored in the $VirtualMachine variable.</span></span>
<span data-ttu-id="52849-115">Aby uzyskać obiekt maszyny wirtualnej, użyj polecenia cmdlet **Get-AzVM** .</span><span class="sxs-lookup"><span data-stu-id="52849-115">To obtain a virtual machine object, use the **Get-AzVM** cmdlet.</span></span>

## <span data-ttu-id="52849-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="52849-116">PARAMETERS</span></span>

### <span data-ttu-id="52849-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="52849-117">-AsJob</span></span>
<span data-ttu-id="52849-118">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="52849-118">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="52849-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="52849-119">-AssignIdentity</span></span>
<span data-ttu-id="52849-120">Określ tożsamość przypisaną przez system dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="52849-120">Specify the system-assigned identity for the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AssignIdentityParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52849-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52849-121">-DefaultProfile</span></span>
<span data-ttu-id="52849-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="52849-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52849-123">-ID</span><span class="sxs-lookup"><span data-stu-id="52849-123">-Id</span></span>
<span data-ttu-id="52849-124">Określa identyfikator zasobu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="52849-124">Specifies the resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="52849-125">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="52849-125">-IdentityId</span></span>
<span data-ttu-id="52849-126">Określa listę tożsamości użytkowników skojarzonych z maszyną wirtualną.</span><span class="sxs-lookup"><span data-stu-id="52849-126">Specifies the list of user identities associated with the virtual machine.</span></span>
<span data-ttu-id="52849-127">Odwołania tożsamości użytkownika będą miały identyfikatory zasobów ARM w formularzu: "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}"</span><span class="sxs-lookup"><span data-stu-id="52849-127">The user identity references will be ARM resource IDs in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="52849-128">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="52849-128">-IdentityType</span></span>
<span data-ttu-id="52849-129">Typ tożsamości używanej dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="52849-129">The type of identity used for the virtual machine.</span></span> <span data-ttu-id="52849-130">Prawidłowe wartości to SystemAssigned, UserAssigned, SystemAssignedUserAssigned i none.</span><span class="sxs-lookup"><span data-stu-id="52849-130">Valid values are SystemAssigned, UserAssigned, SystemAssignedUserAssigned, and None.</span></span>

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

### <span data-ttu-id="52849-131">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="52849-131">-MaxPrice</span></span>
<span data-ttu-id="52849-132">Określa cenę maksymalną, jaką można zapłacić za niski priorytet maszyny wirtualnej/VMSS.</span><span class="sxs-lookup"><span data-stu-id="52849-132">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="52849-133">Ta cena jest w dolarach amerykańskich.</span><span class="sxs-lookup"><span data-stu-id="52849-133">This price is in US Dollars.</span></span> <span data-ttu-id="52849-134">Ta cena będzie porównywana z bieżącą ceną o niskim priorytecie dla rozmiaru maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="52849-134">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="52849-135">Ceny są również porównywane w czasie tworzenia/aktualizowania o niskim priorytecie maszyny wirtualnej/VMSS, a operacja będzie dostępna tylko wtedy, gdy maxPrice jest większa niż bieżąca cena o niskim priorytecie.</span><span class="sxs-lookup"><span data-stu-id="52849-135">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="52849-136">MaxPrice będzie również stosowany do wykluczania niewielkiego priorytetu maszyn wirtualnych/VMSS, jeśli obecna cena o niskim priorytecie wykracza poza maxPrice po utworzeniu maszyny wirtualnej/VMSS.</span><span class="sxs-lookup"><span data-stu-id="52849-136">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="52849-137">Możliwe wartości: Każda wartość dziesiętna większa niż zero.</span><span class="sxs-lookup"><span data-stu-id="52849-137">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="52849-138">Przykład: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="52849-138">Example: 0.01538.</span></span>  <span data-ttu-id="52849-139">-1 wskazuje, że nie można wykluczyć niskiego priorytetu maszyn wirtualnych/VMSS w celu uzyskania podstawy cenowej.</span><span class="sxs-lookup"><span data-stu-id="52849-139">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="52849-140">Ponadto domyślna cena maksymalna wynosi-1, jeśli nie jest podana przez Ciebie.</span><span class="sxs-lookup"><span data-stu-id="52849-140">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="52849-141">-Nowait</span><span class="sxs-lookup"><span data-stu-id="52849-141">-NoWait</span></span>
<span data-ttu-id="52849-142">Rozpoczyna operację i wraca natychmiast, zanim operacja zostanie ukończona.</span><span class="sxs-lookup"><span data-stu-id="52849-142">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="52849-143">W celu ustalenia, czy operacja została wykonana pomyślnie, użyj innego mechanizmu.</span><span class="sxs-lookup"><span data-stu-id="52849-143">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="52849-144">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="52849-144">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="52849-145">Określa, czy WriteAccelerator należy włączyć lub wyłączyć na dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="52849-145">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="52849-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52849-146">-ResourceGroupName</span></span>
<span data-ttu-id="52849-147">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="52849-147">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName, AssignIdentityParameterSet, ExplicitIdentityParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52849-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="52849-148">-Tag</span></span>
<span data-ttu-id="52849-149">Określa zasoby i grupy zasobów, które można wyznacznikować za pomocą zestawu par nazwa-wartość.</span><span class="sxs-lookup"><span data-stu-id="52849-149">Specifies the resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="52849-150">Dodawanie znaczników do zasobów umożliwia grupowanie zasobów między grupami zasobów i tworzenie własnych widoków.</span><span class="sxs-lookup"><span data-stu-id="52849-150">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="52849-151">Każdy zasób lub Grupa zasobów może zawierać maksymalnie 15 tagów.</span><span class="sxs-lookup"><span data-stu-id="52849-151">Each resource or resource group can have a maximum of 15 tags.</span></span>

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

### <span data-ttu-id="52849-152">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="52849-152">-UltraSSDEnabled</span></span>
<span data-ttu-id="52849-153">Flaga, która umożliwia lub wyłącza możliwość posiadania jednego lub większej liczby zarządzanych dysków z danymi, UltraSSD_LRS typ konta magazynu na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="52849-153">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="52849-154">Dyski zarządzane z typem konta magazynu UltraSSD_LRS można dodawać do maszyny wirtualnej tylko wtedy, gdy ta właściwość jest włączona.</span><span class="sxs-lookup"><span data-stu-id="52849-154">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>

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

### <span data-ttu-id="52849-155">-VM</span><span class="sxs-lookup"><span data-stu-id="52849-155">-VM</span></span>
<span data-ttu-id="52849-156">Określa obiekt lokalnego maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="52849-156">Specifies a local virtual machine object.</span></span>
<span data-ttu-id="52849-157">Aby uzyskać obiekt maszyny wirtualnej, użyj polecenia cmdlet Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="52849-157">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="52849-158">Ten obiekt maszyny wirtualnej zawiera zaktualizowany stan maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="52849-158">This virtual machine object contains the updated state for the virtual machine.</span></span>

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

### <span data-ttu-id="52849-159">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="52849-159">-Confirm</span></span>
<span data-ttu-id="52849-160">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52849-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52849-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52849-161">-WhatIf</span></span>
<span data-ttu-id="52849-162">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52849-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52849-163">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="52849-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52849-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52849-164">CommonParameters</span></span>
<span data-ttu-id="52849-165">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52849-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52849-166">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="52849-166">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52849-167">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="52849-167">INPUTS</span></span>

### <span data-ttu-id="52849-168">System. String</span><span class="sxs-lookup"><span data-stu-id="52849-168">System.String</span></span>

### <span data-ttu-id="52849-169">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="52849-169">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="52849-170">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="52849-170">System.Boolean</span></span>

## <span data-ttu-id="52849-171">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="52849-171">OUTPUTS</span></span>

### <span data-ttu-id="52849-172">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="52849-172">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="52849-173">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="52849-173">NOTES</span></span>

## <span data-ttu-id="52849-174">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="52849-174">RELATED LINKS</span></span>

[<span data-ttu-id="52849-175">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="52849-175">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="52849-176">Nowe — AzVM</span><span class="sxs-lookup"><span data-stu-id="52849-176">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="52849-177">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="52849-177">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="52849-178">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="52849-178">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="52849-179">Start — AzVM</span><span class="sxs-lookup"><span data-stu-id="52849-179">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="52849-180">Zatrzymaj — AzVM</span><span class="sxs-lookup"><span data-stu-id="52849-180">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="52849-181">Nowe — AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="52849-181">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


