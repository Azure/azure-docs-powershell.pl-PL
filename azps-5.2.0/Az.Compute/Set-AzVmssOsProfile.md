---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3E7B9EFA-8BC2-46EB-9AD7-43EAB7FF3891
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssosprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOsProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOsProfile.md
ms.openlocfilehash: 71bd8ca26755118a4bb9c075ae89bad765922f3d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366989"
---
# <span data-ttu-id="35f9f-101">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="35f9f-101">Set-AzVmssOsProfile</span></span>

## <span data-ttu-id="35f9f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="35f9f-102">SYNOPSIS</span></span>
<span data-ttu-id="35f9f-103">Ustawia właściwości profilu systemu operacyjnego VMSS.</span><span class="sxs-lookup"><span data-stu-id="35f9f-103">Sets the VMSS operating system profile properties.</span></span>

## <span data-ttu-id="35f9f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="35f9f-104">SYNTAX</span></span>

```
Set-AzVmssOsProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-ComputerNamePrefix] <String>]
 [[-AdminUsername] <String>] [[-AdminPassword] <String>] [[-CustomData] <String>]
 [[-WindowsConfigurationProvisionVMAgent] <Boolean>] [[-WindowsConfigurationEnableAutomaticUpdate] <Boolean>]
 [[-TimeZone] <String>] [[-AdditionalUnattendContent] <AdditionalUnattendContent[]>]
 [[-Listener] <WinRMListener[]>] [[-LinuxConfigurationDisablePasswordAuthentication] <Boolean>]
 [[-PublicKey] <SshPublicKey[]>] [[-Secret] <VaultSecretGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35f9f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="35f9f-105">DESCRIPTION</span></span>
<span data-ttu-id="35f9f-106">Polecenie cmdlet **Set-AzVmssOsProfile** umożliwia ustawienie skali maszyny wirtualnej z ustawionymi właściwościami profilu systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="35f9f-106">The **Set-AzVmssOsProfile** cmdlet sets the Virtual Machine Scale Set operating system profile properties.</span></span>

## <span data-ttu-id="35f9f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="35f9f-107">EXAMPLES</span></span>

### <span data-ttu-id="35f9f-108">Przykład 1: Ustawianie właściwości profilu systemu operacyjnego dla VMSS</span><span class="sxs-lookup"><span data-stu-id="35f9f-108">Example 1: Set the operating system profile properties for a VMSS</span></span>
```
PS C:\> Set-AzVmssOSProfile -VirtualMachineScaleSet "ContosoVMSS" -ComputerNamePrefix "Test" -AdminUsername $AdminUsername -AdminPassword $AdminPassword
```

<span data-ttu-id="35f9f-109">To polecenie ustawia właściwości profilu systemu operacyjnego dla maszyn wirtualnych należących do VMSS o nazwie ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="35f9f-109">This command sets operating system profile properties for the virtual machines that belong to the VMSS named ContosoVMSS.</span></span>
<span data-ttu-id="35f9f-110">Polecenie ustawia prefiks nazwy komputera dla wszystkich wystąpień maszyny wirtualnej w VMSS, aby przetestować i poświadczyć nazwę użytkownika i hasło administratora.</span><span class="sxs-lookup"><span data-stu-id="35f9f-110">The command sets the computer name prefix for all the virtual machine instances in the VMSS to Test and supplies the administrator username and password.</span></span>

## <span data-ttu-id="35f9f-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="35f9f-111">PARAMETERS</span></span>

### <span data-ttu-id="35f9f-112">-AdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="35f9f-112">-AdditionalUnattendContent</span></span>
<span data-ttu-id="35f9f-113">Określa obiekt zawartości nienadzorowanej.</span><span class="sxs-lookup"><span data-stu-id="35f9f-113">Specifies an unattended content object.</span></span>
<span data-ttu-id="35f9f-114">Aby utworzyć obiekt, możesz użyć Add-AzVMAdditionalUnattendContent.</span><span class="sxs-lookup"><span data-stu-id="35f9f-114">You can use the Add-AzVMAdditionalUnattendContent to create the object.</span></span>

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

### <span data-ttu-id="35f9f-115">-AdminPassword</span><span class="sxs-lookup"><span data-stu-id="35f9f-115">-AdminPassword</span></span>
<span data-ttu-id="35f9f-116">Określa hasło administratora, które ma być używane dla wszystkich wystąpień maszyny wirtualnej w VMSS.</span><span class="sxs-lookup"><span data-stu-id="35f9f-116">Specifies the administrator password to use for all the virtual machine instances in the VMSS.</span></span>

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

### <span data-ttu-id="35f9f-117">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="35f9f-117">-AdminUsername</span></span>
<span data-ttu-id="35f9f-118">Określa nazwę konta administratora, która ma być używana dla wszystkich wystąpień maszyny wirtualnej w VMSS.</span><span class="sxs-lookup"><span data-stu-id="35f9f-118">Specifies the administrator account name to use for all the virtual machine instances in the VMSS.</span></span> <br>
<span data-ttu-id="35f9f-119">**Ograniczenie dotyczące systemu Windows:** Nie można zakończyć \" .\"</span><span class="sxs-lookup"><span data-stu-id="35f9f-119">**Windows-only restriction:** Cannot end in \".\"</span></span> <br>
<span data-ttu-id="35f9f-120">**Niedozwolone wartości:** \" Administrator \" , \" administrator \" , \" użytkownik \" , \" Użytkownik1 \" , \" test \" , Jan, \" \" \" Test1 \" , \" user3 \" , \" admin1 \" , \" 1 \" , \" 123 \" , \" a \" , \" actuser \" , \" adm \" , \" admin2 \" , \" ASPNET, \" Backup, Console, \" \" \" \" \" David \" , \" gość \" , \" Jan \" , \" właściciel \" , \" katalog_główny \" , \" serwer \" , \" SQL \" , \" Obsługa \" , \" Support_388945a0 \" , \" sys \" , \" Test2 \" , \" test3 \" , \" user4 \" , \" user5 \" .</span><span class="sxs-lookup"><span data-stu-id="35f9f-120">**Disallowed values:** \"administrator\", \"admin\", \"user\", \"user1\", \"test\", \"user2\", \"test1\", \"user3\", \"admin1\", \"1\", \"123\", \"a\", \"actuser\", \"adm\", \"admin2\", \"aspnet\", \"backup\", \"console\", \"david\", \"guest\", \"john\", \"owner\", \"root\", \"server\", \"sql\", \"support\", \"support_388945a0\", \"sys\", \"test2\", \"test3\", \"user4\", \"user5\".</span></span> <br>
<span data-ttu-id="35f9f-121">**Minimalna długość (Linux):** 1 znak</span><span class="sxs-lookup"><span data-stu-id="35f9f-121">**Minimum-length (Linux):** 1  character</span></span> <br>
<span data-ttu-id="35f9f-122">**Max-length (Linux):** 64 znaków</span><span class="sxs-lookup"><span data-stu-id="35f9f-122">**Max-length (Linux):** 64 characters</span></span> <br>
<span data-ttu-id="35f9f-123">**Maks.-length (Windows):** 20 znaków</span><span class="sxs-lookup"><span data-stu-id="35f9f-123">**Max-length (Windows):** 20 characters</span></span>  <br>
<li> <span data-ttu-id="35f9f-124">Aby uzyskać dostęp do maszyny wirtualnej Linux, zobacz [Używanie uprawnień głównych na maszynach wirtualnych systemu Linux na platformie Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-use-root-privileges?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="35f9f-124">For root access to the Linux VM, see [Using root privileges on Linux virtual machines in Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-use-root-privileges?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span></span><br>
<li> <span data-ttu-id="35f9f-125">Aby uzyskać listę wbudowanych użytkowników systemu Linux, których nie należy stosować w tym polu, zobacz [Wybieranie nazw użytkowników dla systemu Linux na platformie Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-usernames?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="35f9f-125">For a list of built-in system users on Linux that should not be used in this field, see [Selecting User Names for Linux on Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-usernames?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span></span>

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

### <span data-ttu-id="35f9f-126">-ComputerNamePrefix</span><span class="sxs-lookup"><span data-stu-id="35f9f-126">-ComputerNamePrefix</span></span>
<span data-ttu-id="35f9f-127">Określa prefiks nazwy komputera dla wszystkich wystąpień maszyny wirtualnej w VMSS.</span><span class="sxs-lookup"><span data-stu-id="35f9f-127">Specifies the computer name prefix for all the virtual machine instances in the VMSS.</span></span>
<span data-ttu-id="35f9f-128">Nazwy komputerów muszą zawierać od 1 do 15 znaków.</span><span class="sxs-lookup"><span data-stu-id="35f9f-128">Computer names must be 1 to 15 characters long.</span></span>

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

### <span data-ttu-id="35f9f-129">-CustomData</span><span class="sxs-lookup"><span data-stu-id="35f9f-129">-CustomData</span></span>
<span data-ttu-id="35f9f-130">Określa zakodowany ciąg Base-64 z danymi niestandardowymi.</span><span class="sxs-lookup"><span data-stu-id="35f9f-130">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="35f9f-131">Ta tablica jest zdekodowana do tablicy binarnej zapisanej jako plik na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="35f9f-131">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="35f9f-132">Maksymalna długość tablicy binarnej to 65535 bajtów.</span><span class="sxs-lookup"><span data-stu-id="35f9f-132">The maximum length of the binary array is 65535 bytes.</span></span> <br>
<span data-ttu-id="35f9f-133">Aby uzyskać informacje na temat używania chmury-init dla maszyny wirtualnej, zobacz [Używanie chmury-init w celu dostosowania maszyny wirtualnej Linux podczas jej tworzenia](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="35f9f-133">For using cloud-init for your VM, see [Using cloud-init to customize a Linux VM during creation](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span></span>

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

### <span data-ttu-id="35f9f-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35f9f-134">-DefaultProfile</span></span>
<span data-ttu-id="35f9f-135">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="35f9f-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35f9f-136">-LinuxConfigurationDisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="35f9f-136">-LinuxConfigurationDisablePasswordAuthentication</span></span>
<span data-ttu-id="35f9f-137">Wskazuje, że to polecenie cmdlet wyłącza uwierzytelnianie hasła.</span><span class="sxs-lookup"><span data-stu-id="35f9f-137">Indicates that this cmdlet disables password authentication.</span></span>

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

### <span data-ttu-id="35f9f-138">-Listener</span><span class="sxs-lookup"><span data-stu-id="35f9f-138">-Listener</span></span>
<span data-ttu-id="35f9f-139">Określa detektory zdalnego zarządzania systemem Windows (WinRM).</span><span class="sxs-lookup"><span data-stu-id="35f9f-139">Specifies the Windows Remote Management (WinRM) listeners.</span></span>
<span data-ttu-id="35f9f-140">Spowoduje to włączenie zdalnego środowiska Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="35f9f-140">This enables remote Windows PowerShell.</span></span>
<span data-ttu-id="35f9f-141">Do utworzenia odbiornika można użyć polecenia cmdlet Add-AzVmssWinRMListener.</span><span class="sxs-lookup"><span data-stu-id="35f9f-141">You can use the Add-AzVmssWinRMListener cmdlet to create the listener.</span></span>

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

### <span data-ttu-id="35f9f-142">-PublicKey</span><span class="sxs-lookup"><span data-stu-id="35f9f-142">-PublicKey</span></span>
<span data-ttu-id="35f9f-143">Określa obiekt klucza publicznego powłoki Secure Shell (SSH).</span><span class="sxs-lookup"><span data-stu-id="35f9f-143">Specifies the Secure Shell (SSH) public key object.</span></span>
<span data-ttu-id="35f9f-144">Aby utworzyć obiekt, możesz użyć polecenia cmdlet Add-AzVMSshPublicKey.</span><span class="sxs-lookup"><span data-stu-id="35f9f-144">You can use the Add-AzVMSshPublicKey cmdlet to create the object.</span></span>

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

### <span data-ttu-id="35f9f-145">-Secret</span><span class="sxs-lookup"><span data-stu-id="35f9f-145">-Secret</span></span>
<span data-ttu-id="35f9f-146">Określa obiekt tajny, który zawiera odwołania do certyfikatu do umieszczenia na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="35f9f-146">Specifies the secrets object which contains the certificate references to place on the virtual machine.</span></span>
<span data-ttu-id="35f9f-147">Aby utworzyć obiekt sekretny, możesz użyć polecenia cmdlet Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="35f9f-147">You can use the Add-AzVmssSecret cmdlet to create the secrets object.</span></span>

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

### <span data-ttu-id="35f9f-148">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="35f9f-148">-TimeZone</span></span>
<span data-ttu-id="35f9f-149">Określa strefę czasową maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="35f9f-149">Specifies the time zone of the virtual machine.</span></span> <span data-ttu-id="35f9f-150">na przykład \" Pacyfik (czas standardowy) \" .</span><span class="sxs-lookup"><span data-stu-id="35f9f-150">e.g. \"Pacific Standard Time\".</span></span> <br>
<span data-ttu-id="35f9f-151">Możliwe wartości mogą być [TimeZoneInfo.ID](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) wartością ze stref czasowych zwróconych przez [TimeZoneInfo. GetSystemTimeZones](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones).</span><span class="sxs-lookup"><span data-stu-id="35f9f-151">Possible values can be [TimeZoneInfo.Id](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) value from time zones returned by [TimeZoneInfo.GetSystemTimeZones](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones).</span></span>

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

### <span data-ttu-id="35f9f-152">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="35f9f-152">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="35f9f-153">Określa obiekt VMSS.</span><span class="sxs-lookup"><span data-stu-id="35f9f-153">Specifies the VMSS object.</span></span>
<span data-ttu-id="35f9f-154">Aby utworzyć obiekt, możesz użyć polecenia cmdlet New-AzVmssConfig.</span><span class="sxs-lookup"><span data-stu-id="35f9f-154">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="35f9f-155">-WindowsConfigurationEnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="35f9f-155">-WindowsConfigurationEnableAutomaticUpdate</span></span>
<span data-ttu-id="35f9f-156">Wskazuje, czy na komputerach wirtualnych w VMSS są włączone aktualizacje automatyczne.</span><span class="sxs-lookup"><span data-stu-id="35f9f-156">Indicates whether the virtual machines in the VMSS are enabled for automatic updates.</span></span>

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

### <span data-ttu-id="35f9f-157">-WindowsConfigurationProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="35f9f-157">-WindowsConfigurationProvisionVMAgent</span></span>
<span data-ttu-id="35f9f-158">Wskazuje, czy należy zainicjować obsługę administracyjną agenta maszyny wirtualnej na maszynach wirtualnych w VMSS.</span><span class="sxs-lookup"><span data-stu-id="35f9f-158">Indicates whether virtual machine agent should be provisioned on the virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="35f9f-159">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="35f9f-159">-Confirm</span></span>
<span data-ttu-id="35f9f-160">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35f9f-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35f9f-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35f9f-161">-WhatIf</span></span>
<span data-ttu-id="35f9f-162">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35f9f-162">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="35f9f-163">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="35f9f-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35f9f-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35f9f-164">CommonParameters</span></span>
<span data-ttu-id="35f9f-165">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35f9f-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35f9f-166">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="35f9f-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35f9f-167">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="35f9f-167">INPUTS</span></span>

### <span data-ttu-id="35f9f-168">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="35f9f-168">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="35f9f-169">System. String</span><span class="sxs-lookup"><span data-stu-id="35f9f-169">System.String</span></span>

### <span data-ttu-id="35f9f-170">System. Nullable "1 [[System. Boolean, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="35f9f-170">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="35f9f-171">Microsoft. Azure. Management. COMPUTE. MODELES. AdditionalUnattendContent []</span><span class="sxs-lookup"><span data-stu-id="35f9f-171">Microsoft.Azure.Management.Compute.Models.AdditionalUnattendContent[]</span></span>

### <span data-ttu-id="35f9f-172">Microsoft. Azure. Management. COMPUTE. MODELES. WinRMListener []</span><span class="sxs-lookup"><span data-stu-id="35f9f-172">Microsoft.Azure.Management.Compute.Models.WinRMListener[]</span></span>

### <span data-ttu-id="35f9f-173">Microsoft. Azure. Management. COMPUTE. MODELES. SshPublicKey []</span><span class="sxs-lookup"><span data-stu-id="35f9f-173">Microsoft.Azure.Management.Compute.Models.SshPublicKey[]</span></span>

### <span data-ttu-id="35f9f-174">Microsoft. Azure. Management. COMPUTE. MODELES. VaultSecretGroup []</span><span class="sxs-lookup"><span data-stu-id="35f9f-174">Microsoft.Azure.Management.Compute.Models.VaultSecretGroup[]</span></span>

## <span data-ttu-id="35f9f-175">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="35f9f-175">OUTPUTS</span></span>

### <span data-ttu-id="35f9f-176">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="35f9f-176">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="35f9f-177">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="35f9f-177">NOTES</span></span>

## <span data-ttu-id="35f9f-178">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="35f9f-178">RELATED LINKS</span></span>

[<span data-ttu-id="35f9f-179">Dodaj-AzVMAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="35f9f-179">Add-AzVMAdditionalUnattendContent</span></span>](./Add-AzVMAdditionalUnattendContent.md)

[<span data-ttu-id="35f9f-180">Dodaj-AzVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="35f9f-180">Add-AzVmssWinRMListener</span></span>](./Add-AzVmssWinRMListener.md)

[<span data-ttu-id="35f9f-181">Dodaj-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="35f9f-181">Add-AzVMSshPublicKey</span></span>](./Add-AzVMSshPublicKey.md)

[<span data-ttu-id="35f9f-182">Dodaj-AzVmssSecret</span><span class="sxs-lookup"><span data-stu-id="35f9f-182">Add-AzVmssSecret</span></span>](./Add-AzVmssSecret.md)

[<span data-ttu-id="35f9f-183">Nowe — AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="35f9f-183">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)


