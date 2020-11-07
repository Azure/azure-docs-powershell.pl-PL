---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 38917534-49C6-47EA-B815-240F794EE655
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzVM.md
ms.openlocfilehash: 8dd18c97a1636e4b6422d58fa7aca28d8798001b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891585"
---
# <span data-ttu-id="a141d-101">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="a141d-101">Update-AzVM</span></span>

## <span data-ttu-id="a141d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a141d-102">SYNOPSIS</span></span>
<span data-ttu-id="a141d-103">Umożliwia zaktualizowanie stanu maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a141d-103">Updates the state of an Azure virtual machine.</span></span>

## <span data-ttu-id="a141d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a141d-104">SYNTAX</span></span>

### <span data-ttu-id="a141d-105">ResourceGroupNameParameterSetName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a141d-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 [-OsDiskWriteAccelerator <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a141d-106">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="a141d-106">AssignIdentityParameterSet</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-AssignIdentity]
 [-OsDiskWriteAccelerator <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a141d-107">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="a141d-107">ExplicitIdentityParameterSet</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-OsDiskWriteAccelerator <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a141d-108">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="a141d-108">IdParameterSetName</span></span>
```
Update-AzVM [-Id] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-OsDiskWriteAccelerator <Boolean>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a141d-109">Opis</span><span class="sxs-lookup"><span data-stu-id="a141d-109">DESCRIPTION</span></span>
<span data-ttu-id="a141d-110">Polecenie cmdlet **Update-AzVM** powoduje zaktualizowanie stanu maszyny wirtualnej platformy Azure do stanu obiektu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a141d-110">The **Update-AzVM** cmdlet updates the state of an Azure virtual machine to the state of a virtual machine object.</span></span>

## <span data-ttu-id="a141d-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a141d-111">EXAMPLES</span></span>

### <span data-ttu-id="a141d-112">Przykład 1: aktualizowanie maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="a141d-112">Example 1: Update a virtual machine</span></span>
```
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="a141d-113">To polecenie powoduje zaktualizowanie maszyny wirtualnej $VirtualMachine w programie ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="a141d-113">This command updates the virtual machine, $VirtualMachine, in ResourceGroup11.</span></span>
<span data-ttu-id="a141d-114">Polecenie aktualizuje je za pomocą obiektu maszyny wirtualnej przechowywanego w zmiennej $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="a141d-114">The command updates it by using the virtual machine object stored in the $VirtualMachine variable.</span></span>
<span data-ttu-id="a141d-115">Aby uzyskać obiekt maszyny wirtualnej, użyj polecenia cmdlet **Get-AzVM** .</span><span class="sxs-lookup"><span data-stu-id="a141d-115">To obtain a virtual machine object, use the **Get-AzVM** cmdlet.</span></span>

## <span data-ttu-id="a141d-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a141d-116">PARAMETERS</span></span>

### <span data-ttu-id="a141d-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a141d-117">-AsJob</span></span>
<span data-ttu-id="a141d-118">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="a141d-118">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a141d-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="a141d-119">-AssignIdentity</span></span>
<span data-ttu-id="a141d-120">Określ tożsamość przypisaną systemowi dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a141d-120">Specify the system assigned identity for the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AssignIdentityParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a141d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a141d-121">-DefaultProfile</span></span>
<span data-ttu-id="a141d-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a141d-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a141d-123">-ID</span><span class="sxs-lookup"><span data-stu-id="a141d-123">-Id</span></span>
<span data-ttu-id="a141d-124">Określa identyfikator zasobu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a141d-124">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a141d-125">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="a141d-125">-IdentityId</span></span>
<span data-ttu-id="a141d-126">Określa listę tożsamości użytkowników skojarzonych z zestawem skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a141d-126">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="a141d-127">Odwołania tożsamości użytkownika będą miały identyfikatory zasobów ARM w formularzu: "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}"</span><span class="sxs-lookup"><span data-stu-id="a141d-127">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a141d-128">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="a141d-128">-IdentityType</span></span>
<span data-ttu-id="a141d-129">Typ tożsamości używanej dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a141d-129">The type of identity used for the virtual machine.</span></span> <span data-ttu-id="a141d-130">Obecnie jedynym obsługiwanym typem jest SystemAssigned ', co powoduje niejawne utworzenie tożsamości.</span><span class="sxs-lookup"><span data-stu-id="a141d-130">Currently, the only supported type is 'SystemAssigned', which implicitly creates an identity.</span></span>

```yaml
Type: ResourceIdentityType
Parameter Sets: ExplicitIdentityParameterSet
Aliases: 
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a141d-131">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="a141d-131">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="a141d-132">Określa, czy WriteAccelerator należy włączyć lub wyłączyć na dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="a141d-132">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a141d-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a141d-133">-ResourceGroupName</span></span>
<span data-ttu-id="a141d-134">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a141d-134">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSetName, AssignIdentityParameterSet, ExplicitIdentityParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a141d-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="a141d-135">-Tag</span></span>
<span data-ttu-id="a141d-136">Określa zasoby i grupy zasobów, które można wyznacznikować za pomocą zestawu par nazwa-wartość.</span><span class="sxs-lookup"><span data-stu-id="a141d-136">Specifies the resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="a141d-137">Dodawanie znaczników do zasobów umożliwia grupowanie zasobów między grupami zasobów i tworzenie własnych widoków.</span><span class="sxs-lookup"><span data-stu-id="a141d-137">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="a141d-138">Każdy zasób lub Grupa zasobów może zawierać maksymalnie 15 tagów.</span><span class="sxs-lookup"><span data-stu-id="a141d-138">Each resource or resource group can have a maximum of 15 tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a141d-139">-VM</span><span class="sxs-lookup"><span data-stu-id="a141d-139">-VM</span></span>
<span data-ttu-id="a141d-140">Określa obiekt lokalnego maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a141d-140">Specifies a local virtual machine object.</span></span>
<span data-ttu-id="a141d-141">Aby uzyskać obiekt maszyny wirtualnej, użyj polecenia cmdlet Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="a141d-141">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="a141d-142">Ten obiekt maszyny wirtualnej zawiera zaktualizowany stan maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a141d-142">This virtual machine object contains the updated state for the virtual machine.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a141d-143">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a141d-143">-Confirm</span></span>
<span data-ttu-id="a141d-144">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a141d-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a141d-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a141d-145">-WhatIf</span></span>
<span data-ttu-id="a141d-146">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a141d-146">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="a141d-147">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a141d-147">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a141d-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a141d-148">CommonParameters</span></span>
<span data-ttu-id="a141d-149">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a141d-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a141d-150">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a141d-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a141d-151">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a141d-151">INPUTS</span></span>

### <span data-ttu-id="a141d-152">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="a141d-152">PSVirtualMachine</span></span>
<span data-ttu-id="a141d-153">Parametr "VM" akceptuje wartość typu "PSVirtualMachine" z procesu</span><span class="sxs-lookup"><span data-stu-id="a141d-153">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="a141d-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a141d-154">OUTPUTS</span></span>

### <span data-ttu-id="a141d-155">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="a141d-155">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="a141d-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a141d-156">NOTES</span></span>

## <span data-ttu-id="a141d-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a141d-157">RELATED LINKS</span></span>

[<span data-ttu-id="a141d-158">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="a141d-158">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="a141d-159">Nowe — AzVM</span><span class="sxs-lookup"><span data-stu-id="a141d-159">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="a141d-160">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="a141d-160">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="a141d-161">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="a141d-161">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="a141d-162">Start — AzVM</span><span class="sxs-lookup"><span data-stu-id="a141d-162">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="a141d-163">Zatrzymaj — AzVM</span><span class="sxs-lookup"><span data-stu-id="a141d-163">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="a141d-164">Nowe — AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="a141d-164">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


