---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 39AADD19-2EDD-4C1F-BC9E-22186DD9A085
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMOperatingSystem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMOperatingSystem.md
ms.openlocfilehash: 01f9d007d54e7e96ac28e81b5081dc696d3af406
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546856"
---
# <span data-ttu-id="30597-101">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="30597-101">Set-AzureRmVMOperatingSystem</span></span>

## <span data-ttu-id="30597-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="30597-102">SYNOPSIS</span></span>
<span data-ttu-id="30597-103">Ustawia właściwości systemu operacyjnego dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="30597-103">Sets operating system properties for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30597-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="30597-104">SYNTAX</span></span>

### <span data-ttu-id="30597-105">Windows (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="30597-105">Windows (Default)</span></span>
```
Set-AzureRmVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [<CommonParameters>]
```

### <span data-ttu-id="30597-106">WindowsWinRmHttps</span><span class="sxs-lookup"><span data-stu-id="30597-106">WindowsWinRmHttps</span></span>
```
Set-AzureRmVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri> [<CommonParameters>]
```

### <span data-ttu-id="30597-107">Linux</span><span class="sxs-lookup"><span data-stu-id="30597-107">Linux</span></span>
```
Set-AzureRmVMOperatingSystem [-VM] <PSVirtualMachine> [-Linux] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisablePasswordAuthentication] [<CommonParameters>]
```

## <span data-ttu-id="30597-108">Opis</span><span class="sxs-lookup"><span data-stu-id="30597-108">DESCRIPTION</span></span>
<span data-ttu-id="30597-109">Polecenie cmdlet **Set-AzureRmVMOperatingSystem** ustawia właściwości systemu operacyjnego dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="30597-109">The **Set-AzureRmVMOperatingSystem** cmdlet sets operating system properties for a virtual machine.</span></span>
<span data-ttu-id="30597-110">Możesz określić poświadczenia logowania, nazwę komputera i typ systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="30597-110">You can specify logon credentials, computer name, and operating system type.</span></span>

## <span data-ttu-id="30597-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="30597-111">EXAMPLES</span></span>

### <span data-ttu-id="30597-112">Przykład 1: Ustawianie właściwości systemu operacyjnego dla nowych maszyn wirtualnych</span><span class="sxs-lookup"><span data-stu-id="30597-112">Example 1: Set operating system properties for a new virtual machines</span></span>
```
PS C:\> $SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
PS C:\> $ComputerName = "ContosoVM122"
PS C:\> $WinRMCertUrl = "http://keyVaultName.vault.azure.net/secrets/secretName/secretVersion"
PS C:\> $TimeZone = "Pacific Standard Time"
PS C:\> $CustomData = "echo 'Hello World'"
PS C:\> $VirtualMachine = Set-AzureRmVMOperatingSystem -VM $$VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -WinRMHttp -WinRMHttps -WinRMCertificateUrl $WinRMCertUrl -ProvisionVMAgent -EnableAutoUpdate -TimeZone $TimeZone
```

<span data-ttu-id="30597-113">Pierwsze polecenie konwertuje hasło na bezpieczny ciąg, a następnie zapisuje je w zmiennej $SecurePassword.</span><span class="sxs-lookup"><span data-stu-id="30597-113">The first command converts a password to a secure string, and then stores it in the $SecurePassword variable.</span></span>
<span data-ttu-id="30597-114">Aby uzyskać więcej informacji, wpisz tekst `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="30597-114">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>

<span data-ttu-id="30597-115">Drugie polecenie tworzy poświadczenie dla użytkownika FullerP i hasło przechowywane w $SecurePassword, a następnie zapisuje poświadczenia w zmiennej $Credential.</span><span class="sxs-lookup"><span data-stu-id="30597-115">The second command creates a credential for the user FullerP and the password stored in $SecurePassword, and then stores the credential in the $Credential variable.</span></span>
<span data-ttu-id="30597-116">Aby uzyskać więcej informacji, wpisz tekst `Get-Help New-Object` .</span><span class="sxs-lookup"><span data-stu-id="30597-116">For more information, type `Get-Help New-Object`.</span></span>

<span data-ttu-id="30597-117">Trzecia komenda Pobiera zestaw dostępności o nazwie AvailablitySet03 w grupie zasobów o nazwie ResourceGroup11, a następnie zapisuje ten obiekt w zmiennej $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="30597-117">The third command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="30597-118">Czwarte polecenie tworzy obiekt maszyny wirtualnej, a następnie zapisuje go w zmiennej $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="30597-118">The fourth command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="30597-119">Polecenie przypisuje nazwę i rozmiar maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="30597-119">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="30597-120">Maszyna wirtualna należy do zestawu dostępności przechowywanego w $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="30597-120">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

<span data-ttu-id="30597-121">Następne cztery polecenia przypisują wartości do zmiennych, które mają być używane w poniższym poleceniu.</span><span class="sxs-lookup"><span data-stu-id="30597-121">The next four commands assign values to variables to use in the following command.</span></span>
<span data-ttu-id="30597-122">Ponieważ można określić te ciągi bezpośrednio w poleceniu **Set-AzureRmVMOperatingSystem** , ta metoda jest używana tylko do czytelności.</span><span class="sxs-lookup"><span data-stu-id="30597-122">Because you could specify these strings directly in the **Set-AzureRmVMOperatingSystem** command, this approach is used only for readability.</span></span>
<span data-ttu-id="30597-123">Możesz jednak skorzystać z takiej metody jak w przypadku skryptów.</span><span class="sxs-lookup"><span data-stu-id="30597-123">However, you might use an approach such as this in scripts.</span></span>

<span data-ttu-id="30597-124">Ostatnie polecenie ustawia właściwości systemu operacyjnego dla maszyny wirtualnej przechowywanej w $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="30597-124">The final command sets operating system properties for the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="30597-125">Polecenie korzysta z poświadczeń przechowywanych w $Credential.</span><span class="sxs-lookup"><span data-stu-id="30597-125">The command uses the credentials stored in $Credential.</span></span>
<span data-ttu-id="30597-126">W poleceniu użyto zmiennych przypisanych we wcześniejszych poleceniach dla określonych parametrów.</span><span class="sxs-lookup"><span data-stu-id="30597-126">The command uses variables assigned in previous commands for some parameters.</span></span>

## <span data-ttu-id="30597-127">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="30597-127">PARAMETERS</span></span>

### <span data-ttu-id="30597-128">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="30597-128">-ComputerName</span></span>
<span data-ttu-id="30597-129">Określa nazwę komputera.</span><span class="sxs-lookup"><span data-stu-id="30597-129">Specifies the name of the computer.</span></span>

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

### <span data-ttu-id="30597-130">— Poświadczenie</span><span class="sxs-lookup"><span data-stu-id="30597-130">-Credential</span></span>
<span data-ttu-id="30597-131">Określa nazwę użytkownika i hasło maszyny wirtualnej jako obiekt **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="30597-131">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="30597-132">Aby uzyskać poświadczenia, użyj polecenia cmdlet Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="30597-132">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="30597-133">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="30597-133">For more information, type `Get-Help Get-Credential`.</span></span>

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

### <span data-ttu-id="30597-134">-CustomData</span><span class="sxs-lookup"><span data-stu-id="30597-134">-CustomData</span></span>
<span data-ttu-id="30597-135">Określa zakodowany ciąg Base-64 z danymi niestandardowymi.</span><span class="sxs-lookup"><span data-stu-id="30597-135">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="30597-136">Ta tablica jest zdekodowana do tablicy binarnej zapisanej jako plik na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="30597-136">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="30597-137">Maksymalna długość tablicy binarnej to 65535 bajtów.</span><span class="sxs-lookup"><span data-stu-id="30597-137">The maximum length of the binary array is 65535 bytes.</span></span>

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

### <span data-ttu-id="30597-138">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="30597-138">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="30597-139">Wskazuje, że to polecenie cmdlet wyłącza uwierzytelnianie hasła.</span><span class="sxs-lookup"><span data-stu-id="30597-139">Indicates that this cmdlet disables password authentication.</span></span>

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

### <span data-ttu-id="30597-140">-EnableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="30597-140">-EnableAutoUpdate</span></span>
<span data-ttu-id="30597-141">Wskazuje, że to polecenie cmdlet umożliwia automatyczne aktualizowanie.</span><span class="sxs-lookup"><span data-stu-id="30597-141">Indicates that this cmdlet enables auto update.</span></span>

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

### <span data-ttu-id="30597-142">-Linux</span><span class="sxs-lookup"><span data-stu-id="30597-142">-Linux</span></span>
<span data-ttu-id="30597-143">Wskazuje, że typ systemu operacyjnego to Linux.</span><span class="sxs-lookup"><span data-stu-id="30597-143">Indicates that the type of operating system is Linux.</span></span>

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

### <span data-ttu-id="30597-144">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="30597-144">-ProvisionVMAgent</span></span>
<span data-ttu-id="30597-145">Wskazuje, że ustawienia wymagają zainstalowania agenta maszyny wirtualnej na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="30597-145">Indicates that the settings require that the virtual machine agent be installed on the virtual machine.</span></span>

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

### <span data-ttu-id="30597-146">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="30597-146">-TimeZone</span></span>
<span data-ttu-id="30597-147">Określa strefę czasową dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="30597-147">Specifies the time zone for the virtual machine.</span></span>

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

### <span data-ttu-id="30597-148">-VM</span><span class="sxs-lookup"><span data-stu-id="30597-148">-VM</span></span>
<span data-ttu-id="30597-149">Określa lokalny obiekt maszyny wirtualnej, na którym należy ustawić właściwości systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="30597-149">Specifies the local virtual machine object on which to set operating system properties.</span></span>
<span data-ttu-id="30597-150">Aby uzyskać obiekt maszyny wirtualnej, użyj polecenia cmdlet Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="30597-150">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>
<span data-ttu-id="30597-151">Utwórz obiekt maszyny wirtualnej przy użyciu New-AzureRmVMConfig polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30597-151">Create a virtual machine object by using the New-AzureRmVMConfig cmdlet.</span></span>

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

### <span data-ttu-id="30597-152">-Windows</span><span class="sxs-lookup"><span data-stu-id="30597-152">-Windows</span></span>
<span data-ttu-id="30597-153">Wskazuje, że typ systemu operacyjnego to Windows.</span><span class="sxs-lookup"><span data-stu-id="30597-153">Indicates that the type of operating system is Windows.</span></span>

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

### <span data-ttu-id="30597-154">-WinRMCertificateUrl</span><span class="sxs-lookup"><span data-stu-id="30597-154">-WinRMCertificateUrl</span></span>
<span data-ttu-id="30597-155">Określa identyfikator URI certyfikatu usługi WinRM.</span><span class="sxs-lookup"><span data-stu-id="30597-155">Specifies the URI of a WinRM certificate.</span></span>
<span data-ttu-id="30597-156">Należy je zapisać w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="30597-156">This needs to be stored in a Key Vault.</span></span>

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

### <span data-ttu-id="30597-157">-WinRMHttp</span><span class="sxs-lookup"><span data-stu-id="30597-157">-WinRMHttp</span></span>
<span data-ttu-id="30597-158">Wskazuje, że w tym systemie operacyjnym jest używany protokół HTTP WinRM.</span><span class="sxs-lookup"><span data-stu-id="30597-158">Indicates that this operating system uses HTTP WinRM.</span></span>

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

### <span data-ttu-id="30597-159">-WinRMHttps</span><span class="sxs-lookup"><span data-stu-id="30597-159">-WinRMHttps</span></span>
<span data-ttu-id="30597-160">Wskazuje, że w tym systemie operacyjnym jest używany protokół HTTPS.</span><span class="sxs-lookup"><span data-stu-id="30597-160">Indicates that this operating system uses HTTPS WinRM.</span></span>

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

### <span data-ttu-id="30597-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30597-161">CommonParameters</span></span>
<span data-ttu-id="30597-162">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30597-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30597-163">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30597-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30597-164">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="30597-164">INPUTS</span></span>

### <span data-ttu-id="30597-165">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="30597-165">None</span></span>
<span data-ttu-id="30597-166">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="30597-166">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="30597-167">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="30597-167">OUTPUTS</span></span>

## <span data-ttu-id="30597-168">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="30597-168">NOTES</span></span>

## <span data-ttu-id="30597-169">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="30597-169">RELATED LINKS</span></span>

[<span data-ttu-id="30597-170">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="30597-170">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="30597-171">Nowe — AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="30597-171">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)


