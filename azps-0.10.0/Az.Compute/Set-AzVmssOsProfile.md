---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 3E7B9EFA-8BC2-46EB-9AD7-43EAB7FF3891
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssosprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVmssOsProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVmssOsProfile.md
ms.openlocfilehash: 98ebce4e139d230607da77536492d0ba40d0760f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893326"
---
# <span data-ttu-id="cc626-101">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="cc626-101">Set-AzVmssOsProfile</span></span>

## <span data-ttu-id="cc626-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cc626-102">SYNOPSIS</span></span>
<span data-ttu-id="cc626-103">Ustawia właściwości profilu systemu operacyjnego VMSS.</span><span class="sxs-lookup"><span data-stu-id="cc626-103">Sets the VMSS operating system profile properties.</span></span>

## <span data-ttu-id="cc626-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cc626-104">SYNTAX</span></span>

```
Set-AzVmssOsProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-ComputerNamePrefix] <String>]
 [[-AdminUsername] <String>] [[-AdminPassword] <String>] [[-CustomData] <String>]
 [[-WindowsConfigurationProvisionVMAgent] <Boolean>] [[-WindowsConfigurationEnableAutomaticUpdate] <Boolean>]
 [[-TimeZone] <String>] [[-AdditionalUnattendContent] <AdditionalUnattendContent[]>]
 [[-Listener] <WinRMListener[]>] [[-LinuxConfigurationDisablePasswordAuthentication] <Boolean>]
 [[-PublicKey] <SshPublicKey[]>] [[-Secret] <VaultSecretGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc626-105">Opis</span><span class="sxs-lookup"><span data-stu-id="cc626-105">DESCRIPTION</span></span>
<span data-ttu-id="cc626-106">Polecenie cmdlet **Set-AzVmssOsProfile** umożliwia ustawienie skali maszyny wirtualnej z ustawionymi właściwościami profilu systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="cc626-106">The **Set-AzVmssOsProfile** cmdlet sets the Virtual Machine Scale Set operating system profile properties.</span></span>

## <span data-ttu-id="cc626-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cc626-107">EXAMPLES</span></span>

### <span data-ttu-id="cc626-108">Przykład 1: Ustawianie właściwości profilu systemu operacyjnego dla VMSS</span><span class="sxs-lookup"><span data-stu-id="cc626-108">Example 1: Set the operating system profile properties for a VMSS</span></span>
```
PS C:\> Set-AzVmssOSProfile -VirtualMachineScaleSet "ContosoVMSS" -ComputerNamePrefix "Test" -AdminUsername $AdminUsername -AdminPassword $AdminPassword
```

<span data-ttu-id="cc626-109">To polecenie ustawia właściwości profilu systemu operacyjnego dla maszyn wirtualnych należących do VMSS o nazwie ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="cc626-109">This command sets operating system profile properties for the virtual machines that belong to the VMSS named ContosoVMSS.</span></span>
<span data-ttu-id="cc626-110">Polecenie ustawia prefiks nazwy komputera dla wszystkich wystąpień maszyny wirtualnej w VMSS, aby przetestować i poświadczyć nazwę użytkownika i hasło administratora.</span><span class="sxs-lookup"><span data-stu-id="cc626-110">The command sets the computer name prefix for all the virtual machine instances in the VMSS to Test and supplies the administrator username and password.</span></span>

## <span data-ttu-id="cc626-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cc626-111">PARAMETERS</span></span>

### <span data-ttu-id="cc626-112">-AdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="cc626-112">-AdditionalUnattendContent</span></span>
<span data-ttu-id="cc626-113">Określa obiekt zawartości nienadzorowanej.</span><span class="sxs-lookup"><span data-stu-id="cc626-113">Specifies an unattended content object.</span></span>
<span data-ttu-id="cc626-114">Aby utworzyć obiekt, możesz użyć Add-AzVMAdditionalUnattendContent.</span><span class="sxs-lookup"><span data-stu-id="cc626-114">You can use the Add-AzVMAdditionalUnattendContent to create the object.</span></span>

```yaml
Type: AdditionalUnattendContent[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc626-115">-AdminPassword</span><span class="sxs-lookup"><span data-stu-id="cc626-115">-AdminPassword</span></span>
<span data-ttu-id="cc626-116">Określa hasło administratora, które ma być używane dla wszystkich wystąpień maszyny wirtualnej w VMSS.</span><span class="sxs-lookup"><span data-stu-id="cc626-116">Specifies the administrator password to use for all the virtual machine instances in the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc626-117">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="cc626-117">-AdminUsername</span></span>
<span data-ttu-id="cc626-118">Określa nazwę konta administratora, która ma być używana dla wszystkich wystąpień maszyny wirtualnej w VMSS.</span><span class="sxs-lookup"><span data-stu-id="cc626-118">Specifies the administrator account name to use for all the virtual machine instances in the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc626-119">-ComputerNamePrefix</span><span class="sxs-lookup"><span data-stu-id="cc626-119">-ComputerNamePrefix</span></span>
<span data-ttu-id="cc626-120">Określa prefiks nazwy komputera dla wszystkich wystąpień maszyny wirtualnej w VMSS.</span><span class="sxs-lookup"><span data-stu-id="cc626-120">Specifies the computer name prefix for all the virtual machine instances in the VMSS.</span></span>
<span data-ttu-id="cc626-121">Nazwy komputerów muszą zawierać od 1 do 15 znaków.</span><span class="sxs-lookup"><span data-stu-id="cc626-121">Computer names must be 1 to 15 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc626-122">-CustomData</span><span class="sxs-lookup"><span data-stu-id="cc626-122">-CustomData</span></span>
<span data-ttu-id="cc626-123">Określa zakodowany ciąg Base-64 z danymi niestandardowymi.</span><span class="sxs-lookup"><span data-stu-id="cc626-123">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="cc626-124">Ta tablica jest zdekodowana do tablicy binarnej zapisanej jako plik na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="cc626-124">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="cc626-125">Maksymalna długość tablicy binarnej to 65535 bajtów.</span><span class="sxs-lookup"><span data-stu-id="cc626-125">The maximum length of the binary array is 65535 bytes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc626-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc626-126">-DefaultProfile</span></span>
<span data-ttu-id="cc626-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cc626-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc626-128">-LinuxConfigurationDisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="cc626-128">-LinuxConfigurationDisablePasswordAuthentication</span></span>
<span data-ttu-id="cc626-129">Wskazuje, że to polecenie cmdlet wyłącza uwierzytelnianie hasła.</span><span class="sxs-lookup"><span data-stu-id="cc626-129">Indicates that this cmdlet disables password authentication.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc626-130">-Listener</span><span class="sxs-lookup"><span data-stu-id="cc626-130">-Listener</span></span>
<span data-ttu-id="cc626-131">Określa detektory zdalnego zarządzania systemem Windows (WinRM).</span><span class="sxs-lookup"><span data-stu-id="cc626-131">Specifies the Windows Remote Management (WinRM) listeners.</span></span>
<span data-ttu-id="cc626-132">Spowoduje to włączenie zdalnego środowiska Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="cc626-132">This enables remote Windows PowerShell.</span></span>
<span data-ttu-id="cc626-133">Do utworzenia odbiornika można użyć polecenia cmdlet Add-AzVmssWinRMListener.</span><span class="sxs-lookup"><span data-stu-id="cc626-133">You can use the Add-AzVmssWinRMListener cmdlet to create the listener.</span></span>

```yaml
Type: WinRMListener[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc626-134">-PublicKey</span><span class="sxs-lookup"><span data-stu-id="cc626-134">-PublicKey</span></span>
<span data-ttu-id="cc626-135">Określa obiekt klucza publicznego powłoki Secure Shell (SSH).</span><span class="sxs-lookup"><span data-stu-id="cc626-135">Specifies the Secure Shell (SSH) public key object.</span></span>
<span data-ttu-id="cc626-136">Aby utworzyć obiekt, możesz użyć polecenia cmdlet Add-AzVMSshPublicKey.</span><span class="sxs-lookup"><span data-stu-id="cc626-136">You can use the Add-AzVMSshPublicKey cmdlet to create the object.</span></span>

```yaml
Type: SshPublicKey[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc626-137">-Secret</span><span class="sxs-lookup"><span data-stu-id="cc626-137">-Secret</span></span>
<span data-ttu-id="cc626-138">Określa obiekt tajny, który zawiera odwołania do certyfikatu do umieszczenia na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="cc626-138">Specifies the secrets object which contains the certificate references to place on the virtual machine.</span></span>
<span data-ttu-id="cc626-139">Aby utworzyć obiekt sekretny, możesz użyć polecenia cmdlet Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="cc626-139">You can use the Add-AzVmssSecret cmdlet to create the secrets object.</span></span>

```yaml
Type: VaultSecretGroup[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc626-140">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="cc626-140">-TimeZone</span></span>
<span data-ttu-id="cc626-141">Określa strefę czasową dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="cc626-141">Specifies the time zone for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc626-142">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="cc626-142">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="cc626-143">Określa obiekt VMSS.</span><span class="sxs-lookup"><span data-stu-id="cc626-143">Specifies the VMSS object.</span></span>
<span data-ttu-id="cc626-144">Aby utworzyć obiekt, możesz użyć polecenia cmdlet New-AzVmssConfig.</span><span class="sxs-lookup"><span data-stu-id="cc626-144">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cc626-145">-WindowsConfigurationEnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="cc626-145">-WindowsConfigurationEnableAutomaticUpdate</span></span>
<span data-ttu-id="cc626-146">Wskazuje, czy na komputerach wirtualnych w VMSS są włączone aktualizacje automatyczne.</span><span class="sxs-lookup"><span data-stu-id="cc626-146">Indicates whether the virtual machines in the VMSS are enabled for automatic updates.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc626-147">-WindowsConfigurationProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="cc626-147">-WindowsConfigurationProvisionVMAgent</span></span>
<span data-ttu-id="cc626-148">Wskazuje, czy należy zainicjować obsługę administracyjną agenta maszyny wirtualnej na maszynach wirtualnych w VMSS.</span><span class="sxs-lookup"><span data-stu-id="cc626-148">Indicates whether virtual machine agent should be provisioned on the virtual machines in the VMSS.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc626-149">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cc626-149">-Confirm</span></span>
<span data-ttu-id="cc626-150">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc626-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc626-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc626-151">-WhatIf</span></span>
<span data-ttu-id="cc626-152">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc626-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cc626-153">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="cc626-153">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc626-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc626-154">CommonParameters</span></span>
<span data-ttu-id="cc626-155">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc626-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc626-156">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc626-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc626-157">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cc626-157">INPUTS</span></span>

### <span data-ttu-id="cc626-158">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="cc626-158">VirtualMachineScaleSet</span></span>
<span data-ttu-id="cc626-159">Parametr "VirtualMachineScaleSet" akceptuje wartość typu "VirtualMachineScaleSet" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="cc626-159">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="cc626-160">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cc626-160">OUTPUTS</span></span>

### <span data-ttu-id="cc626-161">To polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="cc626-161">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="cc626-162">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cc626-162">NOTES</span></span>

## <span data-ttu-id="cc626-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cc626-163">RELATED LINKS</span></span>

[<span data-ttu-id="cc626-164">Dodaj-AzVMAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="cc626-164">Add-AzVMAdditionalUnattendContent</span></span>](./Add-AzVMAdditionalUnattendContent.md)

[<span data-ttu-id="cc626-165">Dodaj-AzVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="cc626-165">Add-AzVmssWinRMListener</span></span>](./Add-AzVmssWinRMListener.md)

[<span data-ttu-id="cc626-166">Dodaj-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="cc626-166">Add-AzVMSshPublicKey</span></span>](./Add-AzVMSshPublicKey.md)

[<span data-ttu-id="cc626-167">Dodaj-AzVmssSecret</span><span class="sxs-lookup"><span data-stu-id="cc626-167">Add-AzVmssSecret</span></span>](./Add-AzVmssSecret.md)

[<span data-ttu-id="cc626-168">Nowe — AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="cc626-168">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)


