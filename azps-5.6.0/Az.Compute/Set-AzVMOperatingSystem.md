---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 39AADD19-2EDD-4C1F-BC9E-22186DD9A085
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmoperatingsystem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
ms.openlocfilehash: 75eb0ef60443cdbf2dfe3fa53202d3c8141d4888
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990445"
---
# <span data-ttu-id="07e3f-101">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="07e3f-101">Set-AzVMOperatingSystem</span></span>

## <span data-ttu-id="07e3f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07e3f-102">SYNOPSIS</span></span>
<span data-ttu-id="07e3f-103">Ustawia właściwości systemu operacyjnego dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="07e3f-103">Sets operating system properties for a virtual machine.</span></span>

## <span data-ttu-id="07e3f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="07e3f-104">SYNTAX</span></span>

### <span data-ttu-id="07e3f-105">Windows (domyślne)</span><span class="sxs-lookup"><span data-stu-id="07e3f-105">Windows (Default)</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-PatchMode <String>] [-EnableHotpatching]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07e3f-106">WindowsWinRmHttps</span><span class="sxs-lookup"><span data-stu-id="07e3f-106">WindowsWinRmHttps</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri> [-PatchMode <String>]
 [-EnableHotpatching] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07e3f-107">WindowsDisableVMAgent</span><span class="sxs-lookup"><span data-stu-id="07e3f-107">WindowsDisableVMAgent</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-PatchMode <String>] [-EnableHotpatching]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07e3f-108">WindowsDisableVMAgentWinRmHttps</span><span class="sxs-lookup"><span data-stu-id="07e3f-108">WindowsDisableVMAgentWinRmHttps</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri> [-PatchMode <String>]
 [-EnableHotpatching] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07e3f-109">Linux</span><span class="sxs-lookup"><span data-stu-id="07e3f-109">Linux</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Linux] [-ComputerName] <String> [-Credential] <PSCredential>
 [[-CustomData] <String>] [-PatchMode <String>] [-DisablePasswordAuthentication]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07e3f-110">OPIS</span><span class="sxs-lookup"><span data-stu-id="07e3f-110">DESCRIPTION</span></span>
<span data-ttu-id="07e3f-111">Polecenie **cmdlet Set-AzVMOperatingSystem** ustawia właściwości systemu operacyjnego maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="07e3f-111">The **Set-AzVMOperatingSystem** cmdlet sets operating system properties for a virtual machine.</span></span>
<span data-ttu-id="07e3f-112">Możesz określić poświadczenia logowania, nazwę komputera i typ systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="07e3f-112">You can specify logon credentials, computer name, and operating system type.</span></span>

## <span data-ttu-id="07e3f-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="07e3f-113">EXAMPLES</span></span>

### <span data-ttu-id="07e3f-114">Przykład 1. Ustawianie właściwości systemu operacyjnego dla nowej maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="07e3f-114">Example 1: Set operating system properties for a new virtual machine</span></span>
```
$SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
$AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
$VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
$ComputerName = "ContosoVM122"
$WinRMCertUrl = "http://keyVaultName.vault.azure.net/secrets/secretName/secretVersion"
$TimeZone = "Pacific Standard Time"
$CustomData = "echo 'Hello World'"
$VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -WinRMHttp -WinRMHttps -WinRMCertificateUrl $WinRMCertUrl -ProvisionVMAgent -EnableAutoUpdate -TimeZone $TimeZone -PatchMode "AutomaticByPlatform"
```

<span data-ttu-id="07e3f-115">Pierwsze polecenie konwertuje hasło na bezpieczny ciąg, a następnie zapisuje je w $SecurePassword danych.</span><span class="sxs-lookup"><span data-stu-id="07e3f-115">The first command converts a password to a secure string, and then stores it in the $SecurePassword variable.</span></span>
<span data-ttu-id="07e3f-116">Aby uzyskać więcej informacji, wpisz `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="07e3f-116">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>
<span data-ttu-id="07e3f-117">Drugie polecenie tworzy poświadczenia dla użytkownika FullerP i hasło przechowywane w programie $SecurePassword, a następnie przechowuje poświadczenia w $Credential danych.</span><span class="sxs-lookup"><span data-stu-id="07e3f-117">The second command creates a credential for the user FullerP and the password stored in $SecurePassword, and then stores the credential in the $Credential variable.</span></span>
<span data-ttu-id="07e3f-118">Aby uzyskać więcej informacji, wpisz `Get-Help New-Object` .</span><span class="sxs-lookup"><span data-stu-id="07e3f-118">For more information, type `Get-Help New-Object`.</span></span>
<span data-ttu-id="07e3f-119">Trzecie polecenie pobiera zestaw dostępności o nazwie AvailabilitySet03 w grupie zasobów o nazwie ResourceGroup11, a następnie przechowuje ten obiekt w $AvailabilitySet zasobów.</span><span class="sxs-lookup"><span data-stu-id="07e3f-119">The third command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="07e3f-120">Czwarte polecenie tworzy obiekt maszyny wirtualnej, a następnie przechowuje go w $VirtualMachine zmienną.</span><span class="sxs-lookup"><span data-stu-id="07e3f-120">The fourth command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="07e3f-121">To polecenie przypisuje nazwę i rozmiar do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="07e3f-121">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="07e3f-122">Maszynę wirtualną należy do zestawu dostępności przechowywanego w $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="07e3f-122">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="07e3f-123">Następne cztery polecenia przypiszą wartości do zmiennych, których można użyć w następującym poleceniu.</span><span class="sxs-lookup"><span data-stu-id="07e3f-123">The next four commands assign values to variables to use in the following command.</span></span>
<span data-ttu-id="07e3f-124">Ponieważ można określić te ciągi bezpośrednio w **poleceniu Set-AzVMOperatingSystem,** ta metoda jest używana tylko w celu czytelności.</span><span class="sxs-lookup"><span data-stu-id="07e3f-124">Because you could specify these strings directly in the **Set-AzVMOperatingSystem** command, this approach is used only for readability.</span></span>
<span data-ttu-id="07e3f-125">Można jednak użyć takiego podejścia, jak to w skryptach.</span><span class="sxs-lookup"><span data-stu-id="07e3f-125">However, you might use an approach such as this in scripts.</span></span>
<span data-ttu-id="07e3f-126">Końcowe polecenie określa właściwości systemu operacyjnego maszyny wirtualnej przechowywanej w $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="07e3f-126">The final command sets operating system properties for the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="07e3f-127">To polecenie używa poświadczeń przechowywanych w $Credential.</span><span class="sxs-lookup"><span data-stu-id="07e3f-127">The command uses the credentials stored in $Credential.</span></span>
<span data-ttu-id="07e3f-128">W przypadku niektórych parametrów polecenie używa zmiennych przypisanych w poprzednich poleceniach.</span><span class="sxs-lookup"><span data-stu-id="07e3f-128">The command uses variables assigned in previous commands for some parameters.</span></span>

### <span data-ttu-id="07e3f-129">Przykład 2. Ustawianie właściwości systemu operacyjnego dla nowej maszyny wirtualnej z włączonym poprawianie poprawek</span><span class="sxs-lookup"><span data-stu-id="07e3f-129">Example 2: Set operating system properties for a new virtual machine with hot patching enabled</span></span>
```
$SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
$AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
$VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
$ComputerName = "ContosoVM122"
$WinRMCertUrl = "http://keyVaultName.vault.azure.net/secrets/secretName/secretVersion"
$TimeZone = "Pacific Standard Time"
$CustomData = "echo 'Hello World'"
$VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -WinRMHttp -WinRMHttps -WinRMCertificateUrl $WinRMCertUrl -ProvisionVMAgent -EnableAutoUpdate -TimeZone $TimeZone -PatchMode "AutomaticByPlatform" -EnableHotPatching
```

<span data-ttu-id="07e3f-130">Pierwsze polecenie konwertuje hasło na bezpieczny ciąg, a następnie zapisuje je w $SecurePassword danych.</span><span class="sxs-lookup"><span data-stu-id="07e3f-130">The first command converts a password to a secure string, and then stores it in the $SecurePassword variable.</span></span>
<span data-ttu-id="07e3f-131">Aby uzyskać więcej informacji, wpisz `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="07e3f-131">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>
<span data-ttu-id="07e3f-132">Drugie polecenie tworzy poświadczenia dla użytkownika FullerP i hasło przechowywane w programie $SecurePassword, a następnie przechowuje poświadczenia w $Credential danych.</span><span class="sxs-lookup"><span data-stu-id="07e3f-132">The second command creates a credential for the user FullerP and the password stored in $SecurePassword, and then stores the credential in the $Credential variable.</span></span>
<span data-ttu-id="07e3f-133">Aby uzyskać więcej informacji, wpisz `Get-Help New-Object` .</span><span class="sxs-lookup"><span data-stu-id="07e3f-133">For more information, type `Get-Help New-Object`.</span></span>
<span data-ttu-id="07e3f-134">Trzecie polecenie pobiera zestaw dostępności o nazwie AvailabilitySet03 w grupie zasobów o nazwie ResourceGroup11, a następnie przechowuje ten obiekt w $AvailabilitySet zasobów.</span><span class="sxs-lookup"><span data-stu-id="07e3f-134">The third command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="07e3f-135">Czwarte polecenie tworzy obiekt maszyny wirtualnej, a następnie przechowuje go w $VirtualMachine zmienną.</span><span class="sxs-lookup"><span data-stu-id="07e3f-135">The fourth command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="07e3f-136">To polecenie przypisuje nazwę i rozmiar do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="07e3f-136">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="07e3f-137">Maszynę wirtualną należy do zestawu dostępności przechowywanego w $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="07e3f-137">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="07e3f-138">Następne cztery polecenia przypiszą wartości do zmiennych, których można użyć w następującym poleceniu.</span><span class="sxs-lookup"><span data-stu-id="07e3f-138">The next four commands assign values to variables to use in the following command.</span></span>
<span data-ttu-id="07e3f-139">Ponieważ można określić te ciągi bezpośrednio w **poleceniu Set-AzVMOperatingSystem,** ta metoda jest używana tylko w celu czytelności.</span><span class="sxs-lookup"><span data-stu-id="07e3f-139">Because you could specify these strings directly in the **Set-AzVMOperatingSystem** command, this approach is used only for readability.</span></span>
<span data-ttu-id="07e3f-140">Można jednak użyć takiego podejścia, jak to w skryptach.</span><span class="sxs-lookup"><span data-stu-id="07e3f-140">However, you might use an approach such as this in scripts.</span></span>
<span data-ttu-id="07e3f-141">Końcowe polecenie określa właściwości systemu operacyjnego maszyny wirtualnej przechowywanej w $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="07e3f-141">The final command sets operating system properties for the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="07e3f-142">To polecenie używa poświadczeń przechowywanych w $Credential.</span><span class="sxs-lookup"><span data-stu-id="07e3f-142">The command uses the credentials stored in $Credential.</span></span>
<span data-ttu-id="07e3f-143">W przypadku niektórych parametrów polecenie używa zmiennych przypisanych w poprzednich poleceniach.</span><span class="sxs-lookup"><span data-stu-id="07e3f-143">The command uses variables assigned in previous commands for some parameters.</span></span>
<span data-ttu-id="07e3f-144">To polecenie włącza hotpatching na komputerze wirtualnym.</span><span class="sxs-lookup"><span data-stu-id="07e3f-144">The command enables Hotpatching on the virtual machine.</span></span>

### <span data-ttu-id="07e3f-145">Przykład 3. Ustawianie właściwości systemu operacyjnego dla nowej maszyny wirtualnej systemu Linux</span><span class="sxs-lookup"><span data-stu-id="07e3f-145">Example 3: Set operating system properties for a new Linux virtual machine</span></span>
```
$SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
$AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
$VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
$ComputerName = "ContosoVM122"
$CustomData = "echo 'Hello World'"
$VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -PatchMode "AutomaticByPlatform"
```

<span data-ttu-id="07e3f-146">Pierwsze polecenie konwertuje hasło na bezpieczny ciąg, a następnie zapisuje je w $SecurePassword danych.</span><span class="sxs-lookup"><span data-stu-id="07e3f-146">The first command converts a password to a secure string, and then stores it in the $SecurePassword variable.</span></span>
<span data-ttu-id="07e3f-147">Aby uzyskać więcej informacji, wpisz `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="07e3f-147">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>
<span data-ttu-id="07e3f-148">Drugie polecenie tworzy poświadczenia dla użytkownika FullerP i hasło przechowywane w programie $SecurePassword, a następnie przechowuje poświadczenia w $Credential danych.</span><span class="sxs-lookup"><span data-stu-id="07e3f-148">The second command creates a credential for the user FullerP and the password stored in $SecurePassword, and then stores the credential in the $Credential variable.</span></span>
<span data-ttu-id="07e3f-149">Aby uzyskać więcej informacji, wpisz `Get-Help New-Object` .</span><span class="sxs-lookup"><span data-stu-id="07e3f-149">For more information, type `Get-Help New-Object`.</span></span>
<span data-ttu-id="07e3f-150">Trzecie polecenie pobiera zestaw dostępności o nazwie AvailabilitySet03 w grupie zasobów o nazwie ResourceGroup11, a następnie przechowuje ten obiekt w $AvailabilitySet zasobów.</span><span class="sxs-lookup"><span data-stu-id="07e3f-150">The third command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="07e3f-151">Czwarte polecenie tworzy obiekt maszyny wirtualnej, a następnie przechowuje go w $VirtualMachine zmienną.</span><span class="sxs-lookup"><span data-stu-id="07e3f-151">The fourth command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="07e3f-152">To polecenie przypisuje nazwę i rozmiar do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="07e3f-152">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="07e3f-153">Maszynę wirtualną należy do zestawu dostępności przechowywanego w $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="07e3f-153">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="07e3f-154">Kolejne dwa polecenia przypiszą wartości do zmiennych, których można użyć w następującym poleceniu.</span><span class="sxs-lookup"><span data-stu-id="07e3f-154">The next two commands assign values to variables to use in the following command.</span></span>
<span data-ttu-id="07e3f-155">Końcowe polecenie określa właściwości systemu operacyjnego maszyny wirtualnej przechowywanej w $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="07e3f-155">The final command sets operating system properties for the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="07e3f-156">To polecenie używa poświadczeń przechowywanych w $Credential.</span><span class="sxs-lookup"><span data-stu-id="07e3f-156">The command uses the credentials stored in $Credential.</span></span>
<span data-ttu-id="07e3f-157">W przypadku niektórych parametrów polecenie używa zmiennych przypisanych w poprzednich poleceniach.</span><span class="sxs-lookup"><span data-stu-id="07e3f-157">The command uses variables assigned in previous commands for some parameters.</span></span>
<span data-ttu-id="07e3f-158">Polecenie ustawia wartość trybu poprawki na komputerze wirtualnym na wartość "AutomaticByPlatform".</span><span class="sxs-lookup"><span data-stu-id="07e3f-158">The command sets the patch mode value on the virtual machine to "AutomaticByPlatform".</span></span>

## <span data-ttu-id="07e3f-159">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="07e3f-159">PARAMETERS</span></span>

### <span data-ttu-id="07e3f-160">— Nazwa_komputera</span><span class="sxs-lookup"><span data-stu-id="07e3f-160">-ComputerName</span></span>
<span data-ttu-id="07e3f-161">Określa nazwę komputera.</span><span class="sxs-lookup"><span data-stu-id="07e3f-161">Specifies the name of the computer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07e3f-162">- Credential</span><span class="sxs-lookup"><span data-stu-id="07e3f-162">-Credential</span></span>
<span data-ttu-id="07e3f-163">Określa nazwę użytkownika i hasło dla maszyny wirtualnej jako **obiekt PSCredential.**</span><span class="sxs-lookup"><span data-stu-id="07e3f-163">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="07e3f-164">Aby uzyskać poświadczenia, użyj Get-Credential cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07e3f-164">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="07e3f-165">Aby uzyskać więcej informacji, wpisz `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="07e3f-165">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07e3f-166">- CustomData</span><span class="sxs-lookup"><span data-stu-id="07e3f-166">-CustomData</span></span>
<span data-ttu-id="07e3f-167">Określa ciąg, który ma być przekazywany do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="07e3f-167">Specifies a string to be passed to the virtual machine.</span></span> <span data-ttu-id="07e3f-168">Aby uzyskać więcej informacji, [zobacz Dane niestandardowe w maszyny wirtualne platformy Azure.](https://docs.microsoft.com/en-us/azure/virtual-machines/custom-data)</span><span class="sxs-lookup"><span data-stu-id="07e3f-168">For more information see [Custom Data on Azure VMs](https://docs.microsoft.com/en-us/azure/virtual-machines/custom-data).</span></span>
<span data-ttu-id="07e3f-169">**Uwaga: przechowywanie poufnych informacji w danych niestandardowych nie jest zalecane.**</span><span class="sxs-lookup"><span data-stu-id="07e3f-169">**Note: It is not recommended to store sensitive information in custom data.**</span></span>


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

### <span data-ttu-id="07e3f-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07e3f-170">-DefaultProfile</span></span>
<span data-ttu-id="07e3f-171">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="07e3f-171">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07e3f-172">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="07e3f-172">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="07e3f-173">Wskazuje, że to polecenie cmdlet wyłącza uwierzytelnianie hasłem.</span><span class="sxs-lookup"><span data-stu-id="07e3f-173">Indicates that this cmdlet disables password authentication.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07e3f-174">-DisableVMAgent</span><span class="sxs-lookup"><span data-stu-id="07e3f-174">-DisableVMAgent</span></span>
<span data-ttu-id="07e3f-175">Wyłącz agenta maszyny wirtualnej inicjowania obsługi administracyjnej.</span><span class="sxs-lookup"><span data-stu-id="07e3f-175">Disable Provision VM Agent.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07e3f-176">-EnableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="07e3f-176">-EnableAutoUpdate</span></span>
<span data-ttu-id="07e3f-177">Wskazuje, że to polecenie cmdlet umożliwia automatyczną aktualizację.</span><span class="sxs-lookup"><span data-stu-id="07e3f-177">Indicates that this cmdlet enables auto update.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07e3f-178">-EnableHotpatching</span><span class="sxs-lookup"><span data-stu-id="07e3f-178">-EnableHotpatching</span></span>
<span data-ttu-id="07e3f-179">Umożliwia klientom poprawianie maszyn wirtualnych platformy Azure bez konieczności ponownego rozruchu.</span><span class="sxs-lookup"><span data-stu-id="07e3f-179">Enables customers to patch their Azure VMs without requiring a reboot.</span></span> <span data-ttu-id="07e3f-180">Aby włączyćHotpatching, dla "provisionVMAgent" należy ustawić wartość true, a wartość "patchMode" musi być ustawiona na wartość "AutomaticByPlatform".</span><span class="sxs-lookup"><span data-stu-id="07e3f-180">For enableHotpatching, the 'provisionVMAgent' must be set to true and 'patchMode' must be set to 'AutomaticByPlatform'.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07e3f-181">— Linux</span><span class="sxs-lookup"><span data-stu-id="07e3f-181">-Linux</span></span>
<span data-ttu-id="07e3f-182">Wskazuje, że typem systemu operacyjnego jest Linux.</span><span class="sxs-lookup"><span data-stu-id="07e3f-182">Indicates that the type of operating system is Linux.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07e3f-183">-PatchMode</span><span class="sxs-lookup"><span data-stu-id="07e3f-183">-PatchMode</span></span>
<span data-ttu-id="07e3f-184">Określa tryb łatania poprawek przez gościa do maszyny wirtualnej IaaS.</span><span class="sxs-lookup"><span data-stu-id="07e3f-184">Specifies the mode of in-guest patching to IaaS virtual machine.</span></span><br><br>
<span data-ttu-id="07e3f-185">Możliwe wartości:</span><span class="sxs-lookup"><span data-stu-id="07e3f-185">Possible values are:</span></span><br>
<span data-ttu-id="07e3f-186">**Ręcznie** — kontrolujesz aplikację poprawek na maszynę wirtualną.</span><span class="sxs-lookup"><span data-stu-id="07e3f-186">**Manual** - You  control the application of patches to a virtual machine.</span></span> <span data-ttu-id="07e3f-187">W tym celu należy ręcznie zastosować poprawki wewnątrz maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="07e3f-187">You do this by applying patches manually inside the VM.</span></span> <span data-ttu-id="07e3f-188">W tym trybie aktualizacje automatyczne są wyłączone. właściwość WindowsConfiguration.enableAutomaticUpdates musi mieć wartość false</span><span class="sxs-lookup"><span data-stu-id="07e3f-188">In this mode, automatic updates are disabled; the property WindowsConfiguration.enableAutomaticUpdates must be false</span></span><br>
<span data-ttu-id="07e3f-189">**AutomaticByOS** — maszynę wirtualną zostanie automatycznie zaktualizowana przez system operacyjny.</span><span class="sxs-lookup"><span data-stu-id="07e3f-189">**AutomaticByOS** - The virtual machine will automatically be updated by the OS.</span></span> <span data-ttu-id="07e3f-190">Właściwość WindowsConfiguration.enableAutomaticUpdates musi być prawdziwa.</span><span class="sxs-lookup"><span data-stu-id="07e3f-190">The property WindowsConfiguration.enableAutomaticUpdates must be true.</span></span> <br >
<span data-ttu-id="07e3f-191">**AutomaticByPlatform** — maszynę wirtualną będzie automatycznie aktualizowana przez system operacyjny.</span><span class="sxs-lookup"><span data-stu-id="07e3f-191">**AutomaticByPlatform** - the virtual machine will automatically updated by the OS.</span></span> <span data-ttu-id="07e3f-192">Właściwości provisionVMAgent i WindowsConfiguration.enableAutomaticUpdates muszą być prawdziwe</span><span class="sxs-lookup"><span data-stu-id="07e3f-192">The properties provisionVMAgent and WindowsConfiguration.enableAutomaticUpdates must be true</span></span>

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

### <span data-ttu-id="07e3f-193">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="07e3f-193">-ProvisionVMAgent</span></span>
<span data-ttu-id="07e3f-194">Oznacza, że ustawienia wymagają, aby agent maszyny wirtualnej był zainstalowany na maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="07e3f-194">Indicates that the settings require that the virtual machine agent be installed on the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07e3f-195">- Strefa czasowa</span><span class="sxs-lookup"><span data-stu-id="07e3f-195">-TimeZone</span></span>
<span data-ttu-id="07e3f-196">Określa strefę czasową maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="07e3f-196">Specifies the time zone of the virtual machine.</span></span> <span data-ttu-id="07e3f-197">np. \" Pacyfik (czas \" standardowy).</span><span class="sxs-lookup"><span data-stu-id="07e3f-197">e.g. \"Pacific Standard Time\".</span></span> <br>
<span data-ttu-id="07e3f-198">Możliwe wartości mogą [być](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) TimeZoneInfo.Id z stref czasowych zwracanych przez [TimeZoneInfo.GetSystemTimeZones.](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.getsystemtimezones)</span><span class="sxs-lookup"><span data-stu-id="07e3f-198">Possible values can be [TimeZoneInfo.Id](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) value from time zones returned by [TimeZoneInfo.GetSystemTimeZones](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.getsystemtimezones).</span></span>

```yaml
Type: System.String
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07e3f-199">— MASZYNY WIRTUALNEJ</span><span class="sxs-lookup"><span data-stu-id="07e3f-199">-VM</span></span>
<span data-ttu-id="07e3f-200">Określa lokalny obiekt maszyny wirtualnej, na którym mają być ustawiane właściwości systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="07e3f-200">Specifies the local virtual machine object on which to set operating system properties.</span></span>
<span data-ttu-id="07e3f-201">Aby uzyskać obiekt maszyny wirtualnej, użyj Get-AzVM cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07e3f-201">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="07e3f-202">Utwórz obiekt maszyny wirtualnej za pomocą New-AzVMConfig cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07e3f-202">Create a virtual machine object by using the New-AzVMConfig cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="07e3f-203">— Windows</span><span class="sxs-lookup"><span data-stu-id="07e3f-203">-Windows</span></span>
<span data-ttu-id="07e3f-204">Wskazuje, że typem systemu operacyjnego jest system Windows.</span><span class="sxs-lookup"><span data-stu-id="07e3f-204">Indicates that the type of operating system is Windows.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07e3f-205">-WinRMCertificateUrl</span><span class="sxs-lookup"><span data-stu-id="07e3f-205">-WinRMCertificateUrl</span></span>
<span data-ttu-id="07e3f-206">Określa URI certyfikatu usługi WinRM.</span><span class="sxs-lookup"><span data-stu-id="07e3f-206">Specifies the URI of a WinRM certificate.</span></span>
<span data-ttu-id="07e3f-207">Musi to być przechowywane w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="07e3f-207">This needs to be stored in a Key Vault.</span></span>

```yaml
Type: System.Uri
Parameter Sets: WindowsWinRmHttps, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: True
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07e3f-208">—WinRMHttp</span><span class="sxs-lookup"><span data-stu-id="07e3f-208">-WinRMHttp</span></span>
<span data-ttu-id="07e3f-209">Wskazuje, że w tym systemie operacyjnym jest używany protokół HTTP WinRM.</span><span class="sxs-lookup"><span data-stu-id="07e3f-209">Indicates that this operating system uses HTTP WinRM.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07e3f-210">-WinRMHttps</span><span class="sxs-lookup"><span data-stu-id="07e3f-210">-WinRMHttps</span></span>
<span data-ttu-id="07e3f-211">Oznacza, że w tym systemie operacyjnym jest używany protokół HTTPS WinRM.</span><span class="sxs-lookup"><span data-stu-id="07e3f-211">Indicates that this operating system uses HTTPS WinRM.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsWinRmHttps, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: True
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07e3f-212">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07e3f-212">CommonParameters</span></span>
<span data-ttu-id="07e3f-213">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07e3f-213">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07e3f-214">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="07e3f-214">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07e3f-215">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="07e3f-215">INPUTS</span></span>

### <span data-ttu-id="07e3f-216">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="07e3f-216">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="07e3f-217">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="07e3f-217">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="07e3f-218">System.String</span><span class="sxs-lookup"><span data-stu-id="07e3f-218">System.String</span></span>

### <span data-ttu-id="07e3f-219">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="07e3f-219">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="07e3f-220">System.Uri</span><span class="sxs-lookup"><span data-stu-id="07e3f-220">System.Uri</span></span>

## <span data-ttu-id="07e3f-221">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="07e3f-221">OUTPUTS</span></span>

### <span data-ttu-id="07e3f-222">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="07e3f-222">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="07e3f-223">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="07e3f-223">NOTES</span></span>

## <span data-ttu-id="07e3f-224">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="07e3f-224">RELATED LINKS</span></span>

[<span data-ttu-id="07e3f-225">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="07e3f-225">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="07e3f-226">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="07e3f-226">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


