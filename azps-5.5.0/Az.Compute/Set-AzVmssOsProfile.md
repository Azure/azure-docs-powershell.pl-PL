---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3E7B9EFA-8BC2-46EB-9AD7-43EAB7FF3891
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssosprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOsProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOsProfile.md
ms.openlocfilehash: 71bd8ca26755118a4bb9c075ae89bad765922f3d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238600"
---
# <span data-ttu-id="e6191-101">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="e6191-101">Set-AzVmssOsProfile</span></span>

## <span data-ttu-id="e6191-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6191-102">SYNOPSIS</span></span>
<span data-ttu-id="e6191-103">Ustawia właściwości profilu systemu operacyjnego MASZYNY WIRTUALNE.</span><span class="sxs-lookup"><span data-stu-id="e6191-103">Sets the VMSS operating system profile properties.</span></span>

## <span data-ttu-id="e6191-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e6191-104">SYNTAX</span></span>

```
Set-AzVmssOsProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-ComputerNamePrefix] <String>]
 [[-AdminUsername] <String>] [[-AdminPassword] <String>] [[-CustomData] <String>]
 [[-WindowsConfigurationProvisionVMAgent] <Boolean>] [[-WindowsConfigurationEnableAutomaticUpdate] <Boolean>]
 [[-TimeZone] <String>] [[-AdditionalUnattendContent] <AdditionalUnattendContent[]>]
 [[-Listener] <WinRMListener[]>] [[-LinuxConfigurationDisablePasswordAuthentication] <Boolean>]
 [[-PublicKey] <SshPublicKey[]>] [[-Secret] <VaultSecretGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6191-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="e6191-105">DESCRIPTION</span></span>
<span data-ttu-id="e6191-106">Polecenie **cmdlet Set-AzVmssOsProfile** ustawia właściwości profilu systemu operacyjnego skalowania maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e6191-106">The **Set-AzVmssOsProfile** cmdlet sets the Virtual Machine Scale Set operating system profile properties.</span></span>

## <span data-ttu-id="e6191-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e6191-107">EXAMPLES</span></span>

### <span data-ttu-id="e6191-108">Przykład 1. Ustawianie właściwości profilu systemu operacyjnego dla usługi maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="e6191-108">Example 1: Set the operating system profile properties for a VMSS</span></span>
```
PS C:\> Set-AzVmssOSProfile -VirtualMachineScaleSet "ContosoVMSS" -ComputerNamePrefix "Test" -AdminUsername $AdminUsername -AdminPassword $AdminPassword
```

<span data-ttu-id="e6191-109">To polecenie ustawia właściwości profilu systemu operacyjnego dla maszyn wirtualnych należących do maszyn wirtualnych o nazwie ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="e6191-109">This command sets operating system profile properties for the virtual machines that belong to the VMSS named ContosoVMSS.</span></span>
<span data-ttu-id="e6191-110">Polecenie ustawia prefiks nazwy komputera dla wszystkich wystąpień maszyn wirtualnych w usługach VIRTUALSS w celu przetestowania oraz dostarcza nazwę użytkownika i hasło administratora.</span><span class="sxs-lookup"><span data-stu-id="e6191-110">The command sets the computer name prefix for all the virtual machine instances in the VMSS to Test and supplies the administrator username and password.</span></span>

## <span data-ttu-id="e6191-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e6191-111">PARAMETERS</span></span>

### <span data-ttu-id="e6191-112">-AdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="e6191-112">-AdditionalUnattendContent</span></span>
<span data-ttu-id="e6191-113">Określa nienadzorowany obiekt zawartości.</span><span class="sxs-lookup"><span data-stu-id="e6191-113">Specifies an unattended content object.</span></span>
<span data-ttu-id="e6191-114">Obiekt można Add-AzVMAdditionalUnattendContent za pomocą tego obiektu.</span><span class="sxs-lookup"><span data-stu-id="e6191-114">You can use the Add-AzVMAdditionalUnattendContent to create the object.</span></span>

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

### <span data-ttu-id="e6191-115">-AdminPassword</span><span class="sxs-lookup"><span data-stu-id="e6191-115">-AdminPassword</span></span>
<span data-ttu-id="e6191-116">Określa hasło administratora, które ma być dla wszystkich wystąpień maszyn wirtualnych w usługach VIRTUALSS.</span><span class="sxs-lookup"><span data-stu-id="e6191-116">Specifies the administrator password to use for all the virtual machine instances in the VMSS.</span></span>

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

### <span data-ttu-id="e6191-117">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="e6191-117">-AdminUsername</span></span>
<span data-ttu-id="e6191-118">Określa nazwę konta administratora do użycia dla wszystkich wystąpień maszyn wirtualnych w usługach WIRTUALNEJ maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e6191-118">Specifies the administrator account name to use for all the virtual machine instances in the VMSS.</span></span> <br>
<span data-ttu-id="e6191-119">**Ograniczenie dostępne tylko w systemie Windows:** Nie może kończyć się \" na.\"</span><span class="sxs-lookup"><span data-stu-id="e6191-119">**Windows-only restriction:** Cannot end in \".\"</span></span> <br>
<span data-ttu-id="e6191-120">**Niedozwolone wartości:** \" \"administrator, \" \" administrator, \" \" użytkownik, \" \" użytkownik1, \" \" test, \" \" user2, \" \" test1, \" \" user3, \" \" admin1, \" \" 1, \" 123, \" \" \" a, \" \" actuser, \" \" adm, \" \" admin2, \" \" aspnet, \" \" backup, \" \" console, \" \" \" \" david, guest, \" \" \" \" john, owner, \" \" root, \" \" server, \" sql, \" \" \" support, \" \" support_388945a0, \" \" sys, \" \" test2, \" \" test3, \" \" user4, \" \" user5.</span><span class="sxs-lookup"><span data-stu-id="e6191-120">**Disallowed values:** \"administrator\", \"admin\", \"user\", \"user1\", \"test\", \"user2\", \"test1\", \"user3\", \"admin1\", \"1\", \"123\", \"a\", \"actuser\", \"adm\", \"admin2\", \"aspnet\", \"backup\", \"console\", \"david\", \"guest\", \"john\", \"owner\", \"root\", \"server\", \"sql\", \"support\", \"support_388945a0\", \"sys\", \"test2\", \"test3\", \"user4\", \"user5\".</span></span> <br>
<span data-ttu-id="e6191-121">**Minimalna długość (Linux):** 1 znak</span><span class="sxs-lookup"><span data-stu-id="e6191-121">**Minimum-length (Linux):** 1  character</span></span> <br>
<span data-ttu-id="e6191-122">**Maksymalna długość (Linux):** 64 znaki</span><span class="sxs-lookup"><span data-stu-id="e6191-122">**Max-length (Linux):** 64 characters</span></span> <br>
<span data-ttu-id="e6191-123">**Maksymalna długość (w systemie Windows):** 20 znaków</span><span class="sxs-lookup"><span data-stu-id="e6191-123">**Max-length (Windows):** 20 characters</span></span>  <br>
<li> <span data-ttu-id="e6191-124">Aby uzyskać dostęp główny do maszyny wirtualnej systemu Linux, zobacz Korzystanie z uprawnień głównych na komputerach wirtualnych systemu [Linux na platformie Azure.](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-use-root-privileges?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)</span><span class="sxs-lookup"><span data-stu-id="e6191-124">For root access to the Linux VM, see [Using root privileges on Linux virtual machines in Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-use-root-privileges?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span></span><br>
<li> <span data-ttu-id="e6191-125">Aby uzyskać listę wbudowanych użytkowników systemu Linux, których nie należy używać w tym polu, zobacz Wybieranie nazw użytkowników systemu Linux na [platformie Azure.](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-usernames?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)</span><span class="sxs-lookup"><span data-stu-id="e6191-125">For a list of built-in system users on Linux that should not be used in this field, see [Selecting User Names for Linux on Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-usernames?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span></span>

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

### <span data-ttu-id="e6191-126">-ComputerNamePrefix</span><span class="sxs-lookup"><span data-stu-id="e6191-126">-ComputerNamePrefix</span></span>
<span data-ttu-id="e6191-127">Określa prefiks nazwy komputera dla wszystkich wystąpień maszyn wirtualnych w programie VIRTUALSS.</span><span class="sxs-lookup"><span data-stu-id="e6191-127">Specifies the computer name prefix for all the virtual machine instances in the VMSS.</span></span>
<span data-ttu-id="e6191-128">Nazwy komputerów muszą mieć od 1 do 15 znaków.</span><span class="sxs-lookup"><span data-stu-id="e6191-128">Computer names must be 1 to 15 characters long.</span></span>

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

### <span data-ttu-id="e6191-129">- CustomData</span><span class="sxs-lookup"><span data-stu-id="e6191-129">-CustomData</span></span>
<span data-ttu-id="e6191-130">Określa zakodowany ciąg danych niestandardowych o podstawie 64.</span><span class="sxs-lookup"><span data-stu-id="e6191-130">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="e6191-131">Jest on dekodowany do tablicy binarnej zapisanej jako plik na komputerze wirtualnym.</span><span class="sxs-lookup"><span data-stu-id="e6191-131">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="e6191-132">Maksymalna długość tablicy binarnej to 65 535 bajtów.</span><span class="sxs-lookup"><span data-stu-id="e6191-132">The maximum length of the binary array is 65535 bytes.</span></span> <br>
<span data-ttu-id="e6191-133">Aby uzyskać informacje na temat korzystania z init w chmurze dla maszyny wirtualnej, zobacz Dostosowywanie maszyny wirtualnej systemu Linux podczas tworzenia za pomocą [init w chmurze.](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)</span><span class="sxs-lookup"><span data-stu-id="e6191-133">For using cloud-init for your VM, see [Using cloud-init to customize a Linux VM during creation](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span></span>

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

### <span data-ttu-id="e6191-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6191-134">-DefaultProfile</span></span>
<span data-ttu-id="e6191-135">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e6191-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6191-136">-LinuxConfigurationDisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="e6191-136">-LinuxConfigurationDisablePasswordAuthentication</span></span>
<span data-ttu-id="e6191-137">Wskazuje, że to polecenie cmdlet wyłącza uwierzytelnianie hasłem.</span><span class="sxs-lookup"><span data-stu-id="e6191-137">Indicates that this cmdlet disables password authentication.</span></span>

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

### <span data-ttu-id="e6191-138">- Słuchacz</span><span class="sxs-lookup"><span data-stu-id="e6191-138">-Listener</span></span>
<span data-ttu-id="e6191-139">Określa słuchaczy usługi Zarządzanie zdalne systemu Windows (WinRM).</span><span class="sxs-lookup"><span data-stu-id="e6191-139">Specifies the Windows Remote Management (WinRM) listeners.</span></span>
<span data-ttu-id="e6191-140">Umożliwia to zdalne korzystanie z programu Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e6191-140">This enables remote Windows PowerShell.</span></span>
<span data-ttu-id="e6191-141">Aby utworzyć słuchacza, Add-AzVmssWinRMListener użyć polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6191-141">You can use the Add-AzVmssWinRMListener cmdlet to create the listener.</span></span>

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

### <span data-ttu-id="e6191-142">-PublicKey</span><span class="sxs-lookup"><span data-stu-id="e6191-142">-PublicKey</span></span>
<span data-ttu-id="e6191-143">Określa obiekt klucza publicznego bezpiecznej powłoki (SSH).</span><span class="sxs-lookup"><span data-stu-id="e6191-143">Specifies the Secure Shell (SSH) public key object.</span></span>
<span data-ttu-id="e6191-144">Aby utworzyć obiekt, Add-AzVMSshPublicKey użyć polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6191-144">You can use the Add-AzVMSshPublicKey cmdlet to create the object.</span></span>

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

### <span data-ttu-id="e6191-145">- Tajna</span><span class="sxs-lookup"><span data-stu-id="e6191-145">-Secret</span></span>
<span data-ttu-id="e6191-146">Określa obiekt tajemnic, który zawiera odwołania do certyfikatów, które mają być umieszczane na maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e6191-146">Specifies the secrets object which contains the certificate references to place on the virtual machine.</span></span>
<span data-ttu-id="e6191-147">Możesz użyć tego Add-AzVmssSecret cmdlet, aby utworzyć tajny obiekt.</span><span class="sxs-lookup"><span data-stu-id="e6191-147">You can use the Add-AzVmssSecret cmdlet to create the secrets object.</span></span>

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

### <span data-ttu-id="e6191-148">- Strefa czasowa</span><span class="sxs-lookup"><span data-stu-id="e6191-148">-TimeZone</span></span>
<span data-ttu-id="e6191-149">Określa strefę czasową maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e6191-149">Specifies the time zone of the virtual machine.</span></span> <span data-ttu-id="e6191-150">np. \" Pacyfik (czas \" standardowy).</span><span class="sxs-lookup"><span data-stu-id="e6191-150">e.g. \"Pacific Standard Time\".</span></span> <br>
<span data-ttu-id="e6191-151">Możliwe wartości mogą [być](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) TimeZoneInfo.Id z stref czasowych zwracanych przez [TimeZoneInfo.GetSystemTimeZones.](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones)</span><span class="sxs-lookup"><span data-stu-id="e6191-151">Possible values can be [TimeZoneInfo.Id](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) value from time zones returned by [TimeZoneInfo.GetSystemTimeZones](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones).</span></span>

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

### <span data-ttu-id="e6191-152">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="e6191-152">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="e6191-153">Określa obiekt MASZYNY.MASZYNY.WIRTUALNE.</span><span class="sxs-lookup"><span data-stu-id="e6191-153">Specifies the VMSS object.</span></span>
<span data-ttu-id="e6191-154">Aby utworzyć obiekt, New-AzVmssConfig użyć polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6191-154">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="e6191-155">-WindowsConfigurationEnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="e6191-155">-WindowsConfigurationEnableAutomaticUpdate</span></span>
<span data-ttu-id="e6191-156">Wskazuje, czy dla maszyn wirtualnych w usługach MASZYNY WIRTUALNE są włączone aktualizacje automatyczne.</span><span class="sxs-lookup"><span data-stu-id="e6191-156">Indicates whether the virtual machines in the VMSS are enabled for automatic updates.</span></span>

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

### <span data-ttu-id="e6191-157">-WindowsConfigurationProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="e6191-157">-WindowsConfigurationProvisionVMAgent</span></span>
<span data-ttu-id="e6191-158">Wskazuje, czy agent maszyny wirtualnej powinien być aprowowany na komputerach wirtualnych w maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e6191-158">Indicates whether virtual machine agent should be provisioned on the virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="e6191-159">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e6191-159">-Confirm</span></span>
<span data-ttu-id="e6191-160">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e6191-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6191-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6191-161">-WhatIf</span></span>
<span data-ttu-id="e6191-162">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6191-162">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e6191-163">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e6191-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6191-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6191-164">CommonParameters</span></span>
<span data-ttu-id="e6191-165">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6191-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6191-166">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e6191-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6191-167">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e6191-167">INPUTS</span></span>

### <span data-ttu-id="e6191-168">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="e6191-168">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="e6191-169">System.String</span><span class="sxs-lookup"><span data-stu-id="e6191-169">System.String</span></span>

### <span data-ttu-id="e6191-170">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e6191-170">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="e6191-171">Microsoft.Azure.Management.Compute.Models.AdditionalUnattendContent[]</span><span class="sxs-lookup"><span data-stu-id="e6191-171">Microsoft.Azure.Management.Compute.Models.AdditionalUnattendContent[]</span></span>

### <span data-ttu-id="e6191-172">Microsoft.Azure.Management.Compute.Models.WinRMListener[]</span><span class="sxs-lookup"><span data-stu-id="e6191-172">Microsoft.Azure.Management.Compute.Models.WinRMListener[]</span></span>

### <span data-ttu-id="e6191-173">Microsoft.Azure.Management.Compute.Models.SshPublicKey[]</span><span class="sxs-lookup"><span data-stu-id="e6191-173">Microsoft.Azure.Management.Compute.Models.SshPublicKey[]</span></span>

### <span data-ttu-id="e6191-174">Microsoft.Azure.Management.Compute.Models.VaultSecretGroup[]</span><span class="sxs-lookup"><span data-stu-id="e6191-174">Microsoft.Azure.Management.Compute.Models.VaultSecretGroup[]</span></span>

## <span data-ttu-id="e6191-175">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e6191-175">OUTPUTS</span></span>

### <span data-ttu-id="e6191-176">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="e6191-176">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="e6191-177">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e6191-177">NOTES</span></span>

## <span data-ttu-id="e6191-178">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e6191-178">RELATED LINKS</span></span>

[<span data-ttu-id="e6191-179">Add-AzVMAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="e6191-179">Add-AzVMAdditionalUnattendContent</span></span>](./Add-AzVMAdditionalUnattendContent.md)

[<span data-ttu-id="e6191-180">Add-AzVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="e6191-180">Add-AzVmssWinRMListener</span></span>](./Add-AzVmssWinRMListener.md)

[<span data-ttu-id="e6191-181">Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="e6191-181">Add-AzVMSshPublicKey</span></span>](./Add-AzVMSshPublicKey.md)

[<span data-ttu-id="e6191-182">Add-AzVmssSecret</span><span class="sxs-lookup"><span data-stu-id="e6191-182">Add-AzVmssSecret</span></span>](./Add-AzVmssSecret.md)

[<span data-ttu-id="e6191-183">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="e6191-183">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)


