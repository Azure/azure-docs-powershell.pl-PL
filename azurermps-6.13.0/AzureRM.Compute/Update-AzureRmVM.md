---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 38917534-49C6-47EA-B815-240F794EE655
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmVM.md
ms.openlocfilehash: e29eb849dfd7ec3417daaea1b0cae447d20f1322
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548808"
---
# <span data-ttu-id="32f6d-101">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="32f6d-101">Update-AzureRmVM</span></span>

## <span data-ttu-id="32f6d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="32f6d-102">SYNOPSIS</span></span>
<span data-ttu-id="32f6d-103">Umożliwia zaktualizowanie stanu maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="32f6d-103">Updates the state of an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="32f6d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="32f6d-104">SYNTAX</span></span>

### <span data-ttu-id="32f6d-105">ResourceGroupNameParameterSetName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="32f6d-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Update-AzureRmVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 [-OsDiskWriteAccelerator <Boolean>] [-UltraSSDEnabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32f6d-106">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="32f6d-106">AssignIdentityParameterSet</span></span>
```
Update-AzureRmVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-AssignIdentity]
 [-OsDiskWriteAccelerator <Boolean>] [-UltraSSDEnabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32f6d-107">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="32f6d-107">ExplicitIdentityParameterSet</span></span>
```
Update-AzureRmVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="32f6d-108">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="32f6d-108">IdParameterSetName</span></span>
```
Update-AzureRmVM [-Id] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="32f6d-109">Opis</span><span class="sxs-lookup"><span data-stu-id="32f6d-109">DESCRIPTION</span></span>
<span data-ttu-id="32f6d-110">Polecenie cmdlet **Update-AzureRmVM** powoduje zaktualizowanie stanu maszyny wirtualnej platformy Azure do stanu obiektu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="32f6d-110">The **Update-AzureRmVM** cmdlet updates the state of an Azure virtual machine to the state of a virtual machine object.</span></span>

## <span data-ttu-id="32f6d-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="32f6d-111">EXAMPLES</span></span>

### <span data-ttu-id="32f6d-112">Przykład 1: aktualizowanie maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="32f6d-112">Example 1: Update a virtual machine</span></span>
```
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="32f6d-113">To polecenie powoduje zaktualizowanie maszyny wirtualnej $VirtualMachine w programie ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="32f6d-113">This command updates the virtual machine, $VirtualMachine, in ResourceGroup11.</span></span>
<span data-ttu-id="32f6d-114">Polecenie aktualizuje je za pomocą obiektu maszyny wirtualnej przechowywanego w zmiennej $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="32f6d-114">The command updates it by using the virtual machine object stored in the $VirtualMachine variable.</span></span>
<span data-ttu-id="32f6d-115">Aby uzyskać obiekt maszyny wirtualnej, użyj polecenia cmdlet **Get-AzureRmVM** .</span><span class="sxs-lookup"><span data-stu-id="32f6d-115">To obtain a virtual machine object, use the **Get-AzureRmVM** cmdlet.</span></span>

## <span data-ttu-id="32f6d-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="32f6d-116">PARAMETERS</span></span>

### <span data-ttu-id="32f6d-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="32f6d-117">-AsJob</span></span>
<span data-ttu-id="32f6d-118">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="32f6d-118">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="32f6d-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="32f6d-119">-AssignIdentity</span></span>
<span data-ttu-id="32f6d-120">Określ tożsamość przypisaną systemowi dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="32f6d-120">Specify the system assigned identity for the virtual machine.</span></span>

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

### <span data-ttu-id="32f6d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32f6d-121">-DefaultProfile</span></span>
<span data-ttu-id="32f6d-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="32f6d-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32f6d-123">-ID</span><span class="sxs-lookup"><span data-stu-id="32f6d-123">-Id</span></span>
<span data-ttu-id="32f6d-124">Określa identyfikator zasobu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="32f6d-124">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="32f6d-125">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="32f6d-125">-IdentityId</span></span>
<span data-ttu-id="32f6d-126">Określa listę tożsamości użytkowników skojarzonych z zestawem skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="32f6d-126">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="32f6d-127">Odwołania tożsamości użytkownika będą miały identyfikatory zasobów ARM w formularzu: "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}"</span><span class="sxs-lookup"><span data-stu-id="32f6d-127">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="32f6d-128">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="32f6d-128">-IdentityType</span></span>
<span data-ttu-id="32f6d-129">Typ tożsamości używanej dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="32f6d-129">The type of identity used for the virtual machine.</span></span> <span data-ttu-id="32f6d-130">Obecnie jedynym obsługiwanym typem jest SystemAssigned ', co powoduje niejawne utworzenie tożsamości.</span><span class="sxs-lookup"><span data-stu-id="32f6d-130">Currently, the only supported type is 'SystemAssigned', which implicitly creates an identity.</span></span>

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

### <span data-ttu-id="32f6d-131">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="32f6d-131">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="32f6d-132">Określa, czy WriteAccelerator należy włączyć lub wyłączyć na dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="32f6d-132">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="32f6d-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32f6d-133">-ResourceGroupName</span></span>
<span data-ttu-id="32f6d-134">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="32f6d-134">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="32f6d-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="32f6d-135">-Tag</span></span>
<span data-ttu-id="32f6d-136">Określa zasoby i grupy zasobów, które można wyznacznikować za pomocą zestawu par nazwa-wartość.</span><span class="sxs-lookup"><span data-stu-id="32f6d-136">Specifies the resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="32f6d-137">Dodawanie znaczników do zasobów umożliwia grupowanie zasobów między grupami zasobów i tworzenie własnych widoków.</span><span class="sxs-lookup"><span data-stu-id="32f6d-137">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="32f6d-138">Każdy zasób lub Grupa zasobów może zawierać maksymalnie 15 tagów.</span><span class="sxs-lookup"><span data-stu-id="32f6d-138">Each resource or resource group can have a maximum of 15 tags.</span></span>

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

### <span data-ttu-id="32f6d-139">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="32f6d-139">-UltraSSDEnabled</span></span>
<span data-ttu-id="32f6d-140">Flaga, która umożliwia lub wyłącza możliwość posiadania jednego lub większej liczby zarządzanych dysków z danymi, UltraSSD_LRS typ konta magazynu na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="32f6d-140">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="32f6d-141">Dyski zarządzane z typem konta magazynu UltraSSD_LRS można dodawać do maszyny wirtualnej tylko wtedy, gdy ta właściwość jest włączona.</span><span class="sxs-lookup"><span data-stu-id="32f6d-141">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>

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

### <span data-ttu-id="32f6d-142">-VM</span><span class="sxs-lookup"><span data-stu-id="32f6d-142">-VM</span></span>
<span data-ttu-id="32f6d-143">Określa obiekt lokalnego maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="32f6d-143">Specifies a local virtual machine object.</span></span>
<span data-ttu-id="32f6d-144">Aby uzyskać obiekt maszyny wirtualnej, użyj polecenia cmdlet Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="32f6d-144">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>
<span data-ttu-id="32f6d-145">Ten obiekt maszyny wirtualnej zawiera zaktualizowany stan maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="32f6d-145">This virtual machine object contains the updated state for the virtual machine.</span></span>

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

### <span data-ttu-id="32f6d-146">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="32f6d-146">-Confirm</span></span>
<span data-ttu-id="32f6d-147">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32f6d-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32f6d-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32f6d-148">-WhatIf</span></span>
<span data-ttu-id="32f6d-149">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32f6d-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32f6d-150">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="32f6d-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32f6d-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32f6d-151">CommonParameters</span></span>
<span data-ttu-id="32f6d-152">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32f6d-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32f6d-153">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32f6d-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32f6d-154">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="32f6d-154">INPUTS</span></span>

### <span data-ttu-id="32f6d-155">System. String</span><span class="sxs-lookup"><span data-stu-id="32f6d-155">System.String</span></span>

### <span data-ttu-id="32f6d-156">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="32f6d-156">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="32f6d-157">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="32f6d-157">OUTPUTS</span></span>

### <span data-ttu-id="32f6d-158">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="32f6d-158">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="32f6d-159">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="32f6d-159">NOTES</span></span>

## <span data-ttu-id="32f6d-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="32f6d-160">RELATED LINKS</span></span>

[<span data-ttu-id="32f6d-161">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="32f6d-161">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="32f6d-162">Nowe — AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="32f6d-162">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="32f6d-163">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="32f6d-163">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="32f6d-164">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="32f6d-164">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="32f6d-165">Start — AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="32f6d-165">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="32f6d-166">Zatrzymaj — AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="32f6d-166">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="32f6d-167">Nowe — AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="32f6d-167">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)


