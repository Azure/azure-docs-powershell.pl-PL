---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 39AADD19-2EDD-4C1F-BC9E-22186DD9A085
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmoperatingsystem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
ms.openlocfilehash: c22e1a09f20eca32cb21056ae45334f0d55ce14b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98334234"
---
# <span data-ttu-id="baea3-101">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="baea3-101">Set-AzVMOperatingSystem</span></span>

## <span data-ttu-id="baea3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="baea3-102">SYNOPSIS</span></span>
<span data-ttu-id="baea3-103">Ustawia właściwości systemu operacyjnego dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="baea3-103">Sets operating system properties for a virtual machine.</span></span>

## <span data-ttu-id="baea3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="baea3-104">SYNTAX</span></span>

### <span data-ttu-id="baea3-105">Windows (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="baea3-105">Windows (Default)</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-PatchMode <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="baea3-106">WindowsWinRmHttps</span><span class="sxs-lookup"><span data-stu-id="baea3-106">WindowsWinRmHttps</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri> [-PatchMode <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="baea3-107">WindowsDisableVMAgent</span><span class="sxs-lookup"><span data-stu-id="baea3-107">WindowsDisableVMAgent</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-PatchMode <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="baea3-108">WindowsDisableVMAgentWinRmHttps</span><span class="sxs-lookup"><span data-stu-id="baea3-108">WindowsDisableVMAgentWinRmHttps</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri> [-PatchMode <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="baea3-109">Linux</span><span class="sxs-lookup"><span data-stu-id="baea3-109">Linux</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Linux] [-ComputerName] <String> [-Credential] <PSCredential>
 [[-CustomData] <String>] [-DisablePasswordAuthentication] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="baea3-110">Opis</span><span class="sxs-lookup"><span data-stu-id="baea3-110">DESCRIPTION</span></span>
<span data-ttu-id="baea3-111">Polecenie cmdlet **Set-AzVMOperatingSystem** ustawia właściwości systemu operacyjnego dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="baea3-111">The **Set-AzVMOperatingSystem** cmdlet sets operating system properties for a virtual machine.</span></span>
<span data-ttu-id="baea3-112">Możesz określić poświadczenia logowania, nazwę komputera i typ systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="baea3-112">You can specify logon credentials, computer name, and operating system type.</span></span>

## <span data-ttu-id="baea3-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="baea3-113">EXAMPLES</span></span>

### <span data-ttu-id="baea3-114">Przykład 1: Ustawianie właściwości systemu operacyjnego dla nowych maszyn wirtualnych</span><span class="sxs-lookup"><span data-stu-id="baea3-114">Example 1: Set operating system properties for a new virtual machines</span></span>
```
$SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
$AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
$VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
$ComputerName = "ContosoVM122"
$WinRMCertUrl = "http://keyVaultName.vault.azure.net/secrets/secretName/secretVersion"
$TimeZone = "Pacific Standard Time"
$CustomData = "echo 'Hello World'"
$VirtualMachine = Set-AzVMOperatingSystem -VM $$VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -WinRMHttp -WinRMHttps -WinRMCertificateUrl $WinRMCertUrl -ProvisionVMAgent -EnableAutoUpdate -TimeZone $TimeZone -PatchMode "AutomaticByPlatform"
```

<span data-ttu-id="baea3-115">Pierwsze polecenie konwertuje hasło na bezpieczny ciąg, a następnie zapisuje je w zmiennej $SecurePassword.</span><span class="sxs-lookup"><span data-stu-id="baea3-115">The first command converts a password to a secure string, and then stores it in the $SecurePassword variable.</span></span>
<span data-ttu-id="baea3-116">Aby uzyskać więcej informacji, wpisz tekst `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="baea3-116">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>
<span data-ttu-id="baea3-117">Drugie polecenie tworzy poświadczenie dla użytkownika FullerP i hasło przechowywane w $SecurePassword, a następnie zapisuje poświadczenia w zmiennej $Credential.</span><span class="sxs-lookup"><span data-stu-id="baea3-117">The second command creates a credential for the user FullerP and the password stored in $SecurePassword, and then stores the credential in the $Credential variable.</span></span>
<span data-ttu-id="baea3-118">Aby uzyskać więcej informacji, wpisz tekst `Get-Help New-Object` .</span><span class="sxs-lookup"><span data-stu-id="baea3-118">For more information, type `Get-Help New-Object`.</span></span>
<span data-ttu-id="baea3-119">Trzecia komenda Pobiera zestaw dostępności o nazwie AvailabilitySet03 w grupie zasobów o nazwie ResourceGroup11, a następnie zapisuje ten obiekt w zmiennej $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="baea3-119">The third command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="baea3-120">Czwarte polecenie tworzy obiekt maszyny wirtualnej, a następnie zapisuje go w zmiennej $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="baea3-120">The fourth command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="baea3-121">Polecenie przypisuje nazwę i rozmiar maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="baea3-121">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="baea3-122">Maszyna wirtualna należy do zestawu dostępności przechowywanego w $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="baea3-122">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="baea3-123">Następne cztery polecenia przypisują wartości do zmiennych, które mają być używane w poniższym poleceniu.</span><span class="sxs-lookup"><span data-stu-id="baea3-123">The next four commands assign values to variables to use in the following command.</span></span>
<span data-ttu-id="baea3-124">Ponieważ można określić te ciągi bezpośrednio w poleceniu **Set-AzVMOperatingSystem** , ta metoda jest używana tylko do czytelności.</span><span class="sxs-lookup"><span data-stu-id="baea3-124">Because you could specify these strings directly in the **Set-AzVMOperatingSystem** command, this approach is used only for readability.</span></span>
<span data-ttu-id="baea3-125">Możesz jednak skorzystać z takiej metody jak w przypadku skryptów.</span><span class="sxs-lookup"><span data-stu-id="baea3-125">However, you might use an approach such as this in scripts.</span></span>
<span data-ttu-id="baea3-126">Ostatnie polecenie ustawia właściwości systemu operacyjnego dla maszyny wirtualnej przechowywanej w $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="baea3-126">The final command sets operating system properties for the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="baea3-127">Polecenie korzysta z poświadczeń przechowywanych w $Credential.</span><span class="sxs-lookup"><span data-stu-id="baea3-127">The command uses the credentials stored in $Credential.</span></span>
<span data-ttu-id="baea3-128">W poleceniu użyto zmiennych przypisanych we wcześniejszych poleceniach dla określonych parametrów.</span><span class="sxs-lookup"><span data-stu-id="baea3-128">The command uses variables assigned in previous commands for some parameters.</span></span>

## <span data-ttu-id="baea3-129">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="baea3-129">PARAMETERS</span></span>

### <span data-ttu-id="baea3-130">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="baea3-130">-ComputerName</span></span>
<span data-ttu-id="baea3-131">Określa nazwę komputera.</span><span class="sxs-lookup"><span data-stu-id="baea3-131">Specifies the name of the computer.</span></span>

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

### <span data-ttu-id="baea3-132">— Poświadczenie</span><span class="sxs-lookup"><span data-stu-id="baea3-132">-Credential</span></span>
<span data-ttu-id="baea3-133">Określa nazwę użytkownika i hasło maszyny wirtualnej jako obiekt **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="baea3-133">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="baea3-134">Aby uzyskać poświadczenia, użyj polecenia cmdlet Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="baea3-134">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="baea3-135">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="baea3-135">For more information, type `Get-Help Get-Credential`.</span></span>

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

### <span data-ttu-id="baea3-136">-CustomData</span><span class="sxs-lookup"><span data-stu-id="baea3-136">-CustomData</span></span>
<span data-ttu-id="baea3-137">Określa zakodowany ciąg Base-64 z danymi niestandardowymi.</span><span class="sxs-lookup"><span data-stu-id="baea3-137">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="baea3-138">Ta tablica jest zdekodowana do tablicy binarnej zapisanej jako plik na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="baea3-138">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="baea3-139">Maksymalna długość tablicy binarnej to 65535 bajtów.</span><span class="sxs-lookup"><span data-stu-id="baea3-139">The maximum length of the binary array is 65535 bytes.</span></span><br>
<span data-ttu-id="baea3-140">**Uwaga: nie przekazuj żadnych kluczy tajnych ani haseł we właściwości customData**</span><span class="sxs-lookup"><span data-stu-id="baea3-140">**Note: Do not pass any secrets or passwords in customData property**</span></span><br>
<span data-ttu-id="baea3-141">Tej właściwości nie można zaktualizować po utworzeniu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="baea3-141">This property cannot be updated after the VM is created.</span></span> <br>
<span data-ttu-id="baea3-142">customData jest przekazywana do maszyny wirtualnej, która ma zostać zapisana jako plik, aby uzyskać więcej informacji, zobacz [dane niestandardowe na platformie Azure](https://azure.microsoft.com/en-us/blog/custom-data-and-cloud-init-on-windows-azure/) VM</span><span class="sxs-lookup"><span data-stu-id="baea3-142">customData is passed to the VM to be saved as a file, for more information see [Custom Data on Azure VMs](https://azure.microsoft.com/en-us/blog/custom-data-and-cloud-init-on-windows-azure/)</span></span> <br>
<span data-ttu-id="baea3-143">Aby uzyskać informacje na temat używania chmury-init dla maszyny wirtualnej Linux, zobacz [Używanie chmury-init w celu dostosowania maszyny wirtualnej Linux podczas jej tworzenia](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init) .</span><span class="sxs-lookup"><span data-stu-id="baea3-143">For using cloud-init for your Linux VM, see [Using cloud-init to customize a Linux VM during creation](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init)</span></span>

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

### <span data-ttu-id="baea3-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="baea3-144">-DefaultProfile</span></span>
<span data-ttu-id="baea3-145">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="baea3-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="baea3-146">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="baea3-146">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="baea3-147">Wskazuje, że to polecenie cmdlet wyłącza uwierzytelnianie hasła.</span><span class="sxs-lookup"><span data-stu-id="baea3-147">Indicates that this cmdlet disables password authentication.</span></span>

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

### <span data-ttu-id="baea3-148">-DisableVMAgent</span><span class="sxs-lookup"><span data-stu-id="baea3-148">-DisableVMAgent</span></span>
<span data-ttu-id="baea3-149">Wyłącz agenta obsługi maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="baea3-149">Disable Provision VM Agent.</span></span>

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

### <span data-ttu-id="baea3-150">-EnableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="baea3-150">-EnableAutoUpdate</span></span>
<span data-ttu-id="baea3-151">Wskazuje, że to polecenie cmdlet umożliwia automatyczne aktualizowanie.</span><span class="sxs-lookup"><span data-stu-id="baea3-151">Indicates that this cmdlet enables auto update.</span></span>

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

### <span data-ttu-id="baea3-152">-Linux</span><span class="sxs-lookup"><span data-stu-id="baea3-152">-Linux</span></span>
<span data-ttu-id="baea3-153">Wskazuje, że typ systemu operacyjnego to Linux.</span><span class="sxs-lookup"><span data-stu-id="baea3-153">Indicates that the type of operating system is Linux.</span></span>

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

### <span data-ttu-id="baea3-154">-Patchmode</span><span class="sxs-lookup"><span data-stu-id="baea3-154">-PatchMode</span></span>
<span data-ttu-id="baea3-155">Określa tryb IaaS maszyny wirtualnej w trybie gościnnym.</span><span class="sxs-lookup"><span data-stu-id="baea3-155">Specifies the mode of in-guest patching to IaaS virtual machine.</span></span><br><br>
<span data-ttu-id="baea3-156">Możliwe wartości:</span><span class="sxs-lookup"><span data-stu-id="baea3-156">Possible values are:</span></span><br>
<span data-ttu-id="baea3-157">**Ręczna** — możesz sterować stosowaniem poprawek na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="baea3-157">**Manual** - You  control the application of patches to a virtual machine.</span></span> <span data-ttu-id="baea3-158">W tym celu należy ręcznie zastosować poprawki w maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="baea3-158">You do this by applying patches manually inside the VM.</span></span> <span data-ttu-id="baea3-159">W tym trybie aktualizacje automatyczne są wyłączone. Właściwość WindowsConfiguration. enableAutomaticUpdates musi mieć wartość FAŁSZ</span><span class="sxs-lookup"><span data-stu-id="baea3-159">In this mode, automatic updates are disabled; the property WindowsConfiguration.enableAutomaticUpdates must be false</span></span><br>
<span data-ttu-id="baea3-160">**AutomaticByOS** — maszyna wirtualna zostanie automatycznie zaktualizowana przez system operacyjny.</span><span class="sxs-lookup"><span data-stu-id="baea3-160">**AutomaticByOS** - The virtual machine will automatically be updated by the OS.</span></span> <span data-ttu-id="baea3-161">Właściwość WindowsConfiguration. enableAutomaticUpdates musi mieć wartość true.</span><span class="sxs-lookup"><span data-stu-id="baea3-161">The property WindowsConfiguration.enableAutomaticUpdates must be true.</span></span> <br >
<span data-ttu-id="baea3-162">**AutomaticByPlatform** — maszyna wirtualna zostanie automatycznie zaktualizowana przez system operacyjny.</span><span class="sxs-lookup"><span data-stu-id="baea3-162">**AutomaticByPlatform** - the virtual machine will automatically updated by the OS.</span></span> <span data-ttu-id="baea3-163">Właściwości provisionVMAgent i WindowsConfiguration. enableAutomaticUpdates muszą być prawdziwe</span><span class="sxs-lookup"><span data-stu-id="baea3-163">The properties provisionVMAgent and WindowsConfiguration.enableAutomaticUpdates must be true</span></span>

```yaml
Type: System.String
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="baea3-164">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="baea3-164">-ProvisionVMAgent</span></span>
<span data-ttu-id="baea3-165">Wskazuje, że ustawienia wymagają zainstalowania agenta maszyny wirtualnej na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="baea3-165">Indicates that the settings require that the virtual machine agent be installed on the virtual machine.</span></span>

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

### <span data-ttu-id="baea3-166">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="baea3-166">-TimeZone</span></span>
<span data-ttu-id="baea3-167">Określa strefę czasową maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="baea3-167">Specifies the time zone of the virtual machine.</span></span> <span data-ttu-id="baea3-168">na przykład \" Pacyfik (czas standardowy) \" .</span><span class="sxs-lookup"><span data-stu-id="baea3-168">e.g. \"Pacific Standard Time\".</span></span> <br>
<span data-ttu-id="baea3-169">Możliwe wartości mogą być [TimeZoneInfo.ID](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) wartością ze stref czasowych zwróconych przez [TimeZoneInfo. GetSystemTimeZones](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones).</span><span class="sxs-lookup"><span data-stu-id="baea3-169">Possible values can be [TimeZoneInfo.Id](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) value from time zones returned by [TimeZoneInfo.GetSystemTimeZones](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones).</span></span>

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

### <span data-ttu-id="baea3-170">-VM</span><span class="sxs-lookup"><span data-stu-id="baea3-170">-VM</span></span>
<span data-ttu-id="baea3-171">Określa lokalny obiekt maszyny wirtualnej, na którym należy ustawić właściwości systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="baea3-171">Specifies the local virtual machine object on which to set operating system properties.</span></span>
<span data-ttu-id="baea3-172">Aby uzyskać obiekt maszyny wirtualnej, użyj polecenia cmdlet Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="baea3-172">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="baea3-173">Utwórz obiekt maszyny wirtualnej przy użyciu New-AzVMConfig polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="baea3-173">Create a virtual machine object by using the New-AzVMConfig cmdlet.</span></span>

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

### <span data-ttu-id="baea3-174">-Windows</span><span class="sxs-lookup"><span data-stu-id="baea3-174">-Windows</span></span>
<span data-ttu-id="baea3-175">Wskazuje, że typ systemu operacyjnego to Windows.</span><span class="sxs-lookup"><span data-stu-id="baea3-175">Indicates that the type of operating system is Windows.</span></span>

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

### <span data-ttu-id="baea3-176">-WinRMCertificateUrl</span><span class="sxs-lookup"><span data-stu-id="baea3-176">-WinRMCertificateUrl</span></span>
<span data-ttu-id="baea3-177">Określa identyfikator URI certyfikatu usługi WinRM.</span><span class="sxs-lookup"><span data-stu-id="baea3-177">Specifies the URI of a WinRM certificate.</span></span>
<span data-ttu-id="baea3-178">Należy je zapisać w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="baea3-178">This needs to be stored in a Key Vault.</span></span>

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

### <span data-ttu-id="baea3-179">-WinRMHttp</span><span class="sxs-lookup"><span data-stu-id="baea3-179">-WinRMHttp</span></span>
<span data-ttu-id="baea3-180">Wskazuje, że w tym systemie operacyjnym jest używany protokół HTTP WinRM.</span><span class="sxs-lookup"><span data-stu-id="baea3-180">Indicates that this operating system uses HTTP WinRM.</span></span>

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

### <span data-ttu-id="baea3-181">-WinRMHttps</span><span class="sxs-lookup"><span data-stu-id="baea3-181">-WinRMHttps</span></span>
<span data-ttu-id="baea3-182">Wskazuje, że w tym systemie operacyjnym jest używany protokół HTTPS.</span><span class="sxs-lookup"><span data-stu-id="baea3-182">Indicates that this operating system uses HTTPS WinRM.</span></span>

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

### <span data-ttu-id="baea3-183">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="baea3-183">CommonParameters</span></span>
<span data-ttu-id="baea3-184">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="baea3-184">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="baea3-185">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="baea3-185">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="baea3-186">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="baea3-186">INPUTS</span></span>

### <span data-ttu-id="baea3-187">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="baea3-187">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="baea3-188">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="baea3-188">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="baea3-189">System. String</span><span class="sxs-lookup"><span data-stu-id="baea3-189">System.String</span></span>

### <span data-ttu-id="baea3-190">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="baea3-190">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="baea3-191">System. URI</span><span class="sxs-lookup"><span data-stu-id="baea3-191">System.Uri</span></span>

## <span data-ttu-id="baea3-192">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="baea3-192">OUTPUTS</span></span>

### <span data-ttu-id="baea3-193">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="baea3-193">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="baea3-194">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="baea3-194">NOTES</span></span>

## <span data-ttu-id="baea3-195">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="baea3-195">RELATED LINKS</span></span>

[<span data-ttu-id="baea3-196">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="baea3-196">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="baea3-197">Nowe — AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="baea3-197">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


