---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 39AADD19-2EDD-4C1F-BC9E-22186DD9A085
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmoperatingsystem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
ms.openlocfilehash: 874045a510c8ab87143e25994fd5f15d5be7e741
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893358"
---
# <span data-ttu-id="df47d-101">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="df47d-101">Set-AzVMOperatingSystem</span></span>

## <span data-ttu-id="df47d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="df47d-102">SYNOPSIS</span></span>
<span data-ttu-id="df47d-103">Ustawia właściwości systemu operacyjnego dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="df47d-103">Sets operating system properties for a virtual machine.</span></span>

## <span data-ttu-id="df47d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="df47d-104">SYNTAX</span></span>

### <span data-ttu-id="df47d-105">Windows (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="df47d-105">Windows (Default)</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df47d-106">WindowsWinRmHttps</span><span class="sxs-lookup"><span data-stu-id="df47d-106">WindowsWinRmHttps</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df47d-107">Linux</span><span class="sxs-lookup"><span data-stu-id="df47d-107">Linux</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Linux] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisablePasswordAuthentication]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df47d-108">Opis</span><span class="sxs-lookup"><span data-stu-id="df47d-108">DESCRIPTION</span></span>
<span data-ttu-id="df47d-109">Polecenie cmdlet **Set-AzVMOperatingSystem** ustawia właściwości systemu operacyjnego dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="df47d-109">The **Set-AzVMOperatingSystem** cmdlet sets operating system properties for a virtual machine.</span></span>
<span data-ttu-id="df47d-110">Możesz określić poświadczenia logowania, nazwę komputera i typ systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="df47d-110">You can specify logon credentials, computer name, and operating system type.</span></span>

## <span data-ttu-id="df47d-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="df47d-111">EXAMPLES</span></span>

### <span data-ttu-id="df47d-112">Przykład 1: Ustawianie właściwości systemu operacyjnego dla nowych maszyn wirtualnych</span><span class="sxs-lookup"><span data-stu-id="df47d-112">Example 1: Set operating system properties for a new virtual machines</span></span>
```
PS C:\> $SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
PS C:\> $ComputerName = "ContosoVM122"
PS C:\> $WinRMCertUrl = "http://keyVaultName.vault.azure.net/secrets/secretName/secretVersion"
PS C:\> $TimeZone = "Pacific Standard Time"
PS C:\> $CustomData = "echo 'Hello World'"
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $$VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -WinRMHttp -WinRMHttps -WinRMCertificateUrl $WinRMCertUrl -ProvisionVMAgent -EnableAutoUpdate -TimeZone $TimeZone
```

<span data-ttu-id="df47d-113">Pierwsze polecenie konwertuje hasło na bezpieczny ciąg, a następnie zapisuje je w zmiennej $SecurePassword.</span><span class="sxs-lookup"><span data-stu-id="df47d-113">The first command converts a password to a secure string, and then stores it in the $SecurePassword variable.</span></span>
<span data-ttu-id="df47d-114">Aby uzyskać więcej informacji, wpisz tekst `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="df47d-114">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>

<span data-ttu-id="df47d-115">Drugie polecenie tworzy poświadczenie dla użytkownika FullerP i hasło przechowywane w $SecurePassword, a następnie zapisuje poświadczenia w zmiennej $Credential.</span><span class="sxs-lookup"><span data-stu-id="df47d-115">The second command creates a credential for the user FullerP and the password stored in $SecurePassword, and then stores the credential in the $Credential variable.</span></span>
<span data-ttu-id="df47d-116">Aby uzyskać więcej informacji, wpisz tekst `Get-Help New-Object` .</span><span class="sxs-lookup"><span data-stu-id="df47d-116">For more information, type `Get-Help New-Object`.</span></span>

<span data-ttu-id="df47d-117">Trzecia komenda Pobiera zestaw dostępności o nazwie AvailablitySet03 w grupie zasobów o nazwie ResourceGroup11, a następnie zapisuje ten obiekt w zmiennej $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="df47d-117">The third command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="df47d-118">Czwarte polecenie tworzy obiekt maszyny wirtualnej, a następnie zapisuje go w zmiennej $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="df47d-118">The fourth command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="df47d-119">Polecenie przypisuje nazwę i rozmiar maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="df47d-119">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="df47d-120">Maszyna wirtualna należy do zestawu dostępności przechowywanego w $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="df47d-120">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

<span data-ttu-id="df47d-121">Następne cztery polecenia przypisują wartości do zmiennych, które mają być używane w poniższym poleceniu.</span><span class="sxs-lookup"><span data-stu-id="df47d-121">The next four commands assign values to variables to use in the following command.</span></span>
<span data-ttu-id="df47d-122">Ponieważ można określić te ciągi bezpośrednio w poleceniu **Set-AzVMOperatingSystem** , ta metoda jest używana tylko do czytelności.</span><span class="sxs-lookup"><span data-stu-id="df47d-122">Because you could specify these strings directly in the **Set-AzVMOperatingSystem** command, this approach is used only for readability.</span></span>
<span data-ttu-id="df47d-123">Możesz jednak skorzystać z takiej metody jak w przypadku skryptów.</span><span class="sxs-lookup"><span data-stu-id="df47d-123">However, you might use an approach such as this in scripts.</span></span>

<span data-ttu-id="df47d-124">Ostatnie polecenie ustawia właściwości systemu operacyjnego dla maszyny wirtualnej przechowywanej w $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="df47d-124">The final command sets operating system properties for the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="df47d-125">Polecenie korzysta z poświadczeń przechowywanych w $Credential.</span><span class="sxs-lookup"><span data-stu-id="df47d-125">The command uses the credentials stored in $Credential.</span></span>
<span data-ttu-id="df47d-126">W poleceniu użyto zmiennych przypisanych we wcześniejszych poleceniach dla określonych parametrów.</span><span class="sxs-lookup"><span data-stu-id="df47d-126">The command uses variables assigned in previous commands for some parameters.</span></span>

## <span data-ttu-id="df47d-127">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="df47d-127">PARAMETERS</span></span>

### <span data-ttu-id="df47d-128">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="df47d-128">-ComputerName</span></span>
<span data-ttu-id="df47d-129">Określa nazwę komputera.</span><span class="sxs-lookup"><span data-stu-id="df47d-129">Specifies the name of the computer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df47d-130">— Poświadczenie</span><span class="sxs-lookup"><span data-stu-id="df47d-130">-Credential</span></span>
<span data-ttu-id="df47d-131">Określa nazwę użytkownika i hasło maszyny wirtualnej jako obiekt **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="df47d-131">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="df47d-132">Aby uzyskać poświadczenia, użyj polecenia cmdlet Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="df47d-132">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="df47d-133">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="df47d-133">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df47d-134">-CustomData</span><span class="sxs-lookup"><span data-stu-id="df47d-134">-CustomData</span></span>
<span data-ttu-id="df47d-135">Określa zakodowany ciąg Base-64 z danymi niestandardowymi.</span><span class="sxs-lookup"><span data-stu-id="df47d-135">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="df47d-136">Ta tablica jest zdekodowana do tablicy binarnej zapisanej jako plik na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="df47d-136">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="df47d-137">Maksymalna długość tablicy binarnej to 65535 bajtów.</span><span class="sxs-lookup"><span data-stu-id="df47d-137">The maximum length of the binary array is 65535 bytes.</span></span>

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

### <span data-ttu-id="df47d-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df47d-138">-DefaultProfile</span></span>
<span data-ttu-id="df47d-139">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="df47d-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df47d-140">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="df47d-140">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="df47d-141">Wskazuje, że to polecenie cmdlet wyłącza uwierzytelnianie hasła.</span><span class="sxs-lookup"><span data-stu-id="df47d-141">Indicates that this cmdlet disables password authentication.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df47d-142">-EnableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="df47d-142">-EnableAutoUpdate</span></span>
<span data-ttu-id="df47d-143">Wskazuje, że to polecenie cmdlet umożliwia automatyczne aktualizowanie.</span><span class="sxs-lookup"><span data-stu-id="df47d-143">Indicates that this cmdlet enables auto update.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df47d-144">-Linux</span><span class="sxs-lookup"><span data-stu-id="df47d-144">-Linux</span></span>
<span data-ttu-id="df47d-145">Wskazuje, że typ systemu operacyjnego to Linux.</span><span class="sxs-lookup"><span data-stu-id="df47d-145">Indicates that the type of operating system is Linux.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df47d-146">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="df47d-146">-ProvisionVMAgent</span></span>
<span data-ttu-id="df47d-147">Wskazuje, że ustawienia wymagają zainstalowania agenta maszyny wirtualnej na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="df47d-147">Indicates that the settings require that the virtual machine agent be installed on the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df47d-148">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="df47d-148">-TimeZone</span></span>
<span data-ttu-id="df47d-149">Określa strefę czasową dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="df47d-149">Specifies the time zone for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: Windows, WindowsWinRmHttps
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df47d-150">-VM</span><span class="sxs-lookup"><span data-stu-id="df47d-150">-VM</span></span>
<span data-ttu-id="df47d-151">Określa lokalny obiekt maszyny wirtualnej, na którym należy ustawić właściwości systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="df47d-151">Specifies the local virtual machine object on which to set operating system properties.</span></span>
<span data-ttu-id="df47d-152">Aby uzyskać obiekt maszyny wirtualnej, użyj polecenia cmdlet Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="df47d-152">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="df47d-153">Utwórz obiekt maszyny wirtualnej przy użyciu New-AzVMConfig polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df47d-153">Create a virtual machine object by using the New-AzVMConfig cmdlet.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="df47d-154">-Windows</span><span class="sxs-lookup"><span data-stu-id="df47d-154">-Windows</span></span>
<span data-ttu-id="df47d-155">Wskazuje, że typ systemu operacyjnego to Windows.</span><span class="sxs-lookup"><span data-stu-id="df47d-155">Indicates that the type of operating system is Windows.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df47d-156">-WinRMCertificateUrl</span><span class="sxs-lookup"><span data-stu-id="df47d-156">-WinRMCertificateUrl</span></span>
<span data-ttu-id="df47d-157">Określa identyfikator URI certyfikatu usługi WinRM.</span><span class="sxs-lookup"><span data-stu-id="df47d-157">Specifies the URI of a WinRM certificate.</span></span>
<span data-ttu-id="df47d-158">Należy je zapisać w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="df47d-158">This needs to be stored in a Key Vault.</span></span>

```yaml
Type: Uri
Parameter Sets: WindowsWinRmHttps
Aliases: 

Required: True
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df47d-159">-WinRMHttp</span><span class="sxs-lookup"><span data-stu-id="df47d-159">-WinRMHttp</span></span>
<span data-ttu-id="df47d-160">Wskazuje, że w tym systemie operacyjnym jest używany protokół HTTP WinRM.</span><span class="sxs-lookup"><span data-stu-id="df47d-160">Indicates that this operating system uses HTTP WinRM.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df47d-161">-WinRMHttps</span><span class="sxs-lookup"><span data-stu-id="df47d-161">-WinRMHttps</span></span>
<span data-ttu-id="df47d-162">Wskazuje, że w tym systemie operacyjnym jest używany protokół HTTPS.</span><span class="sxs-lookup"><span data-stu-id="df47d-162">Indicates that this operating system uses HTTPS WinRM.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WindowsWinRmHttps
Aliases: 

Required: True
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df47d-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df47d-163">CommonParameters</span></span>
<span data-ttu-id="df47d-164">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df47d-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df47d-165">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df47d-165">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df47d-166">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="df47d-166">INPUTS</span></span>

### <span data-ttu-id="df47d-167">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="df47d-167">PSVirtualMachine</span></span>
<span data-ttu-id="df47d-168">Parametr "VM" akceptuje wartość typu "PSVirtualMachine" z procesu</span><span class="sxs-lookup"><span data-stu-id="df47d-168">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="df47d-169">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="df47d-169">OUTPUTS</span></span>

### <span data-ttu-id="df47d-170">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="df47d-170">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="df47d-171">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="df47d-171">NOTES</span></span>

## <span data-ttu-id="df47d-172">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="df47d-172">RELATED LINKS</span></span>

[<span data-ttu-id="df47d-173">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="df47d-173">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="df47d-174">Nowe — AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="df47d-174">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


