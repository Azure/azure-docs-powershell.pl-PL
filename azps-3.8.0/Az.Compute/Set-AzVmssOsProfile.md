---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3E7B9EFA-8BC2-46EB-9AD7-43EAB7FF3891
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssosprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOsProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOsProfile.md
ms.openlocfilehash: 3d3fdb53bf6dd0338f89bd03f11786bc9942acaa
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053576"
---
# <span data-ttu-id="2e435-101">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="2e435-101">Set-AzVmssOsProfile</span></span>

## <span data-ttu-id="2e435-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2e435-102">SYNOPSIS</span></span>
<span data-ttu-id="2e435-103">Ustawia właściwości profilu systemu operacyjnego VMSS.</span><span class="sxs-lookup"><span data-stu-id="2e435-103">Sets the VMSS operating system profile properties.</span></span>

## <span data-ttu-id="2e435-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2e435-104">SYNTAX</span></span>

```
Set-AzVmssOsProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-ComputerNamePrefix] <String>]
 [[-AdminUsername] <String>] [[-AdminPassword] <String>] [[-CustomData] <String>]
 [[-WindowsConfigurationProvisionVMAgent] <Boolean>] [[-WindowsConfigurationEnableAutomaticUpdate] <Boolean>]
 [[-TimeZone] <String>] [[-AdditionalUnattendContent] <AdditionalUnattendContent[]>]
 [[-Listener] <WinRMListener[]>] [[-LinuxConfigurationDisablePasswordAuthentication] <Boolean>]
 [[-PublicKey] <SshPublicKey[]>] [[-Secret] <VaultSecretGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e435-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2e435-105">DESCRIPTION</span></span>
<span data-ttu-id="2e435-106">Polecenie cmdlet **Set-AzVmssOsProfile** umożliwia ustawienie skali maszyny wirtualnej z ustawionymi właściwościami profilu systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="2e435-106">The **Set-AzVmssOsProfile** cmdlet sets the Virtual Machine Scale Set operating system profile properties.</span></span>

## <span data-ttu-id="2e435-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2e435-107">EXAMPLES</span></span>

### <span data-ttu-id="2e435-108">Przykład 1: Ustawianie właściwości profilu systemu operacyjnego dla VMSS</span><span class="sxs-lookup"><span data-stu-id="2e435-108">Example 1: Set the operating system profile properties for a VMSS</span></span>
```
PS C:\> Set-AzVmssOSProfile -VirtualMachineScaleSet "ContosoVMSS" -ComputerNamePrefix "Test" -AdminUsername $AdminUsername -AdminPassword $AdminPassword
```

<span data-ttu-id="2e435-109">To polecenie ustawia właściwości profilu systemu operacyjnego dla maszyn wirtualnych należących do VMSS o nazwie ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="2e435-109">This command sets operating system profile properties for the virtual machines that belong to the VMSS named ContosoVMSS.</span></span>
<span data-ttu-id="2e435-110">Polecenie ustawia prefiks nazwy komputera dla wszystkich wystąpień maszyny wirtualnej w VMSS, aby przetestować i poświadczyć nazwę użytkownika i hasło administratora.</span><span class="sxs-lookup"><span data-stu-id="2e435-110">The command sets the computer name prefix for all the virtual machine instances in the VMSS to Test and supplies the administrator username and password.</span></span>

## <span data-ttu-id="2e435-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2e435-111">PARAMETERS</span></span>

### <span data-ttu-id="2e435-112">-AdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="2e435-112">-AdditionalUnattendContent</span></span>
<span data-ttu-id="2e435-113">Określa obiekt zawartości nienadzorowanej.</span><span class="sxs-lookup"><span data-stu-id="2e435-113">Specifies an unattended content object.</span></span>
<span data-ttu-id="2e435-114">Aby utworzyć obiekt, możesz użyć Add-AzVMAdditionalUnattendContent.</span><span class="sxs-lookup"><span data-stu-id="2e435-114">You can use the Add-AzVMAdditionalUnattendContent to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.AdditionalUnattendContent[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e435-115">-AdminPassword</span><span class="sxs-lookup"><span data-stu-id="2e435-115">-AdminPassword</span></span>
<span data-ttu-id="2e435-116">Określa hasło administratora, które ma być używane dla wszystkich wystąpień maszyny wirtualnej w VMSS.</span><span class="sxs-lookup"><span data-stu-id="2e435-116">Specifies the administrator password to use for all the virtual machine instances in the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e435-117">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="2e435-117">-AdminUsername</span></span>
<span data-ttu-id="2e435-118">Określa nazwę konta administratora, która ma być używana dla wszystkich wystąpień maszyny wirtualnej w VMSS.</span><span class="sxs-lookup"><span data-stu-id="2e435-118">Specifies the administrator account name to use for all the virtual machine instances in the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e435-119">-ComputerNamePrefix</span><span class="sxs-lookup"><span data-stu-id="2e435-119">-ComputerNamePrefix</span></span>
<span data-ttu-id="2e435-120">Określa prefiks nazwy komputera dla wszystkich wystąpień maszyny wirtualnej w VMSS.</span><span class="sxs-lookup"><span data-stu-id="2e435-120">Specifies the computer name prefix for all the virtual machine instances in the VMSS.</span></span>
<span data-ttu-id="2e435-121">Nazwy komputerów muszą zawierać od 1 do 15 znaków.</span><span class="sxs-lookup"><span data-stu-id="2e435-121">Computer names must be 1 to 15 characters long.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e435-122">-CustomData</span><span class="sxs-lookup"><span data-stu-id="2e435-122">-CustomData</span></span>
<span data-ttu-id="2e435-123">Określa zakodowany ciąg Base-64 z danymi niestandardowymi.</span><span class="sxs-lookup"><span data-stu-id="2e435-123">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="2e435-124">Ta tablica jest zdekodowana do tablicy binarnej zapisanej jako plik na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2e435-124">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="2e435-125">Maksymalna długość tablicy binarnej to 65535 bajtów.</span><span class="sxs-lookup"><span data-stu-id="2e435-125">The maximum length of the binary array is 65535 bytes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e435-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e435-126">-DefaultProfile</span></span>
<span data-ttu-id="2e435-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2e435-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e435-128">-LinuxConfigurationDisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="2e435-128">-LinuxConfigurationDisablePasswordAuthentication</span></span>
<span data-ttu-id="2e435-129">Wskazuje, że to polecenie cmdlet wyłącza uwierzytelnianie hasła.</span><span class="sxs-lookup"><span data-stu-id="2e435-129">Indicates that this cmdlet disables password authentication.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e435-130">-Listener</span><span class="sxs-lookup"><span data-stu-id="2e435-130">-Listener</span></span>
<span data-ttu-id="2e435-131">Określa detektory zdalnego zarządzania systemem Windows (WinRM).</span><span class="sxs-lookup"><span data-stu-id="2e435-131">Specifies the Windows Remote Management (WinRM) listeners.</span></span>
<span data-ttu-id="2e435-132">Spowoduje to włączenie zdalnego środowiska Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2e435-132">This enables remote Windows PowerShell.</span></span>
<span data-ttu-id="2e435-133">Do utworzenia odbiornika można użyć polecenia cmdlet Add-AzVmssWinRMListener.</span><span class="sxs-lookup"><span data-stu-id="2e435-133">You can use the Add-AzVmssWinRMListener cmdlet to create the listener.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.WinRMListener[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e435-134">-PublicKey</span><span class="sxs-lookup"><span data-stu-id="2e435-134">-PublicKey</span></span>
<span data-ttu-id="2e435-135">Określa obiekt klucza publicznego powłoki Secure Shell (SSH).</span><span class="sxs-lookup"><span data-stu-id="2e435-135">Specifies the Secure Shell (SSH) public key object.</span></span>
<span data-ttu-id="2e435-136">Aby utworzyć obiekt, możesz użyć polecenia cmdlet Add-AzVMSshPublicKey.</span><span class="sxs-lookup"><span data-stu-id="2e435-136">You can use the Add-AzVMSshPublicKey cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.SshPublicKey[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e435-137">-Secret</span><span class="sxs-lookup"><span data-stu-id="2e435-137">-Secret</span></span>
<span data-ttu-id="2e435-138">Określa obiekt tajny, który zawiera odwołania do certyfikatu do umieszczenia na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2e435-138">Specifies the secrets object which contains the certificate references to place on the virtual machine.</span></span>
<span data-ttu-id="2e435-139">Aby utworzyć obiekt sekretny, możesz użyć polecenia cmdlet Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="2e435-139">You can use the Add-AzVmssSecret cmdlet to create the secrets object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VaultSecretGroup[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e435-140">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="2e435-140">-TimeZone</span></span>
<span data-ttu-id="2e435-141">Określa strefę czasową dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2e435-141">Specifies the time zone for the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e435-142">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="2e435-142">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="2e435-143">Określa obiekt VMSS.</span><span class="sxs-lookup"><span data-stu-id="2e435-143">Specifies the VMSS object.</span></span>
<span data-ttu-id="2e435-144">Aby utworzyć obiekt, możesz użyć polecenia cmdlet New-AzVmssConfig.</span><span class="sxs-lookup"><span data-stu-id="2e435-144">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2e435-145">-WindowsConfigurationEnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="2e435-145">-WindowsConfigurationEnableAutomaticUpdate</span></span>
<span data-ttu-id="2e435-146">Wskazuje, czy na komputerach wirtualnych w VMSS są włączone aktualizacje automatyczne.</span><span class="sxs-lookup"><span data-stu-id="2e435-146">Indicates whether the virtual machines in the VMSS are enabled for automatic updates.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e435-147">-WindowsConfigurationProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="2e435-147">-WindowsConfigurationProvisionVMAgent</span></span>
<span data-ttu-id="2e435-148">Wskazuje, czy należy zainicjować obsługę administracyjną agenta maszyny wirtualnej na maszynach wirtualnych w VMSS.</span><span class="sxs-lookup"><span data-stu-id="2e435-148">Indicates whether virtual machine agent should be provisioned on the virtual machines in the VMSS.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e435-149">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2e435-149">-Confirm</span></span>
<span data-ttu-id="2e435-150">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e435-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e435-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e435-151">-WhatIf</span></span>
<span data-ttu-id="2e435-152">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e435-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2e435-153">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2e435-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e435-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e435-154">CommonParameters</span></span>
<span data-ttu-id="2e435-155">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e435-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e435-156">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2e435-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e435-157">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2e435-157">INPUTS</span></span>

### <span data-ttu-id="2e435-158">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="2e435-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="2e435-159">System. String</span><span class="sxs-lookup"><span data-stu-id="2e435-159">System.String</span></span>

### <span data-ttu-id="2e435-160">System. Nullable "1 [[System. Boolean, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="2e435-160">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="2e435-161">Microsoft. Azure. Management. COMPUTE. MODELES. AdditionalUnattendContent []</span><span class="sxs-lookup"><span data-stu-id="2e435-161">Microsoft.Azure.Management.Compute.Models.AdditionalUnattendContent[]</span></span>

### <span data-ttu-id="2e435-162">Microsoft. Azure. Management. COMPUTE. MODELES. WinRMListener []</span><span class="sxs-lookup"><span data-stu-id="2e435-162">Microsoft.Azure.Management.Compute.Models.WinRMListener[]</span></span>

### <span data-ttu-id="2e435-163">Microsoft. Azure. Management. COMPUTE. MODELES. SshPublicKey []</span><span class="sxs-lookup"><span data-stu-id="2e435-163">Microsoft.Azure.Management.Compute.Models.SshPublicKey[]</span></span>

### <span data-ttu-id="2e435-164">Microsoft. Azure. Management. COMPUTE. MODELES. VaultSecretGroup []</span><span class="sxs-lookup"><span data-stu-id="2e435-164">Microsoft.Azure.Management.Compute.Models.VaultSecretGroup[]</span></span>

## <span data-ttu-id="2e435-165">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2e435-165">OUTPUTS</span></span>

### <span data-ttu-id="2e435-166">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="2e435-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="2e435-167">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2e435-167">NOTES</span></span>

## <span data-ttu-id="2e435-168">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2e435-168">RELATED LINKS</span></span>

[<span data-ttu-id="2e435-169">Dodaj-AzVMAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="2e435-169">Add-AzVMAdditionalUnattendContent</span></span>](./Add-AzVMAdditionalUnattendContent.md)

[<span data-ttu-id="2e435-170">Dodaj-AzVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="2e435-170">Add-AzVmssWinRMListener</span></span>](./Add-AzVmssWinRMListener.md)

[<span data-ttu-id="2e435-171">Dodaj-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="2e435-171">Add-AzVMSshPublicKey</span></span>](./Add-AzVMSshPublicKey.md)

[<span data-ttu-id="2e435-172">Dodaj-AzVmssSecret</span><span class="sxs-lookup"><span data-stu-id="2e435-172">Add-AzVmssSecret</span></span>](./Add-AzVmssSecret.md)

[<span data-ttu-id="2e435-173">Nowe — AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="2e435-173">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)


