---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: C6DFD49F-26A5-4199-A844-CA0FC405BEDC
online version: ''
schema: 2.0.0
ms.openlocfilehash: f9fc407e2cf7375708fe82253f3d2fb40eb78f60
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055163"
---
# <span data-ttu-id="83ced-101">New-AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="83ced-101">New-AzureVMConfig</span></span>

## <span data-ttu-id="83ced-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="83ced-102">SYNOPSIS</span></span>
<span data-ttu-id="83ced-103">Umożliwia utworzenie obiektu konfiguracji maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="83ced-103">Creates an Azure virtual machine configuration object.</span></span>

## <span data-ttu-id="83ced-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="83ced-104">SYNTAX</span></span>

### <span data-ttu-id="83ced-105">ImageName (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="83ced-105">ImageName (Default)</span></span>
```
New-AzureVMConfig [-Name] <String> [-InstanceSize] <String> [[-HostCaching] <String>]
 [[-AvailabilitySetName] <String>] [[-Label] <String>] [-ImageName] <String> [[-MediaLocation] <String>]
 [[-DiskLabel] <String>] [-DisableBootDiagnostics] [-LicenseType <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="83ced-106">Dysk</span><span class="sxs-lookup"><span data-stu-id="83ced-106">DiskName</span></span>
```
New-AzureVMConfig [-Name] <String> [-InstanceSize] <String> [[-HostCaching] <String>]
 [[-AvailabilitySetName] <String>] [[-Label] <String>] [-DiskName] <String> [-DisableBootDiagnostics]
 [-LicenseType <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="83ced-107">Opis</span><span class="sxs-lookup"><span data-stu-id="83ced-107">DESCRIPTION</span></span>
<span data-ttu-id="83ced-108">Polecenie cmdlet **New-AzureVMConfig** umożliwia utworzenie obiektu konfiguracji maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="83ced-108">The **New-AzureVMConfig** cmdlet creates an Azure  virtual machine configuration object.</span></span>
<span data-ttu-id="83ced-109">Za pomocą tego obiektu można wykonać nowe wdrożenie i dodać nową maszynę wirtualną do istniejącego wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="83ced-109">You can use this object to perform a new deployment and add a new virtual machine to an existing deployment.</span></span>

## <span data-ttu-id="83ced-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="83ced-110">EXAMPLES</span></span>

### <span data-ttu-id="83ced-111">Przykład 1. Tworzenie konfiguracji maszyny wirtualnej systemu Windows</span><span class="sxs-lookup"><span data-stu-id="83ced-111">Example 1: Create a Windows virtual machine configuration</span></span>
```
PS C:\> $Image = (Get-AzureVMImage)[4].ImageName 
C:\PS> New-AzureVMConfig -Name "MyVM1" -InstanceSize ExtraSmall -ImageName $Image | Add-AzureProvisioningConfig -Windows -Password $AdminPassword | Add-AzureDataDisk -CreateNew -DiskSizeInGB 50 -DiskLabel "Datadisk1" -LUN 0 | New-AzureVM -ServiceName "MySvc1"
```

<span data-ttu-id="83ced-112">To polecenie umożliwia utworzenie konfiguracji maszyny wirtualnej systemu Windows z dyskiem systemu operacyjnego, dyskiem danych i konfiguracją dostarczania.</span><span class="sxs-lookup"><span data-stu-id="83ced-112">This command creates a Windows virtual machine configuration with operating system disk, data disk and provisioning configuration.</span></span>
<span data-ttu-id="83ced-113">Ta konfiguracja jest następnie używana do tworzenia nowej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="83ced-113">This configuration is then used to create a new virtual machine.</span></span>

### <span data-ttu-id="83ced-114">Przykład 2: Tworzenie konfiguracji maszyny wirtualnej Linux</span><span class="sxs-lookup"><span data-stu-id="83ced-114">Example 2: Create a Linux virtual machine configuration</span></span>
```
PS C:\> $Image = (Get-AzureVMImage)[7].ImageName
C:\PS> New-AzureVMConfig -Name "MyVM1" -InstanceSize ExtraSmall -ImageName $Image | Add-AzureProvisioningConfig -Linux -LinuxUser $LinuxUser -Password $AdminPassword | Add-AzureDataDisk -CreateNew -DiskSizeInGB 50 -DiskLabel "Datadisk1" -LUN 0 | New-AzureVM -ServiceName "MySvc1"
```

<span data-ttu-id="83ced-115">To polecenie tworzy nową konfigurację maszyny wirtualnej Linux z dyskiem systemu operacyjnego, dyskiem danych i konfiguracją dostarczania.</span><span class="sxs-lookup"><span data-stu-id="83ced-115">This command creates a new Linux virtual machine configuration with operating system disk, data disk and provisioning configuration.</span></span>
<span data-ttu-id="83ced-116">Ta konfiguracja jest następnie używana do tworzenia nowej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="83ced-116">This configuration is then used to create a new virtual machine.</span></span>

## <span data-ttu-id="83ced-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="83ced-117">PARAMETERS</span></span>

### <span data-ttu-id="83ced-118">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="83ced-118">-AvailabilitySetName</span></span>
<span data-ttu-id="83ced-119">Określa nazwę zestawu dostępności.</span><span class="sxs-lookup"><span data-stu-id="83ced-119">Specifies the name of the availability set.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83ced-120">-DisableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="83ced-120">-DisableBootDiagnostics</span></span>
<span data-ttu-id="83ced-121">Wskazuje, że konfiguracja wyłącza diagnostykę rozruchu.</span><span class="sxs-lookup"><span data-stu-id="83ced-121">Indicates that the configuration disables boot diagnostics.</span></span>
<span data-ttu-id="83ced-122">Domyślnie na maszynie wirtualnej jest włączona Diagnostyka rozruchu.</span><span class="sxs-lookup"><span data-stu-id="83ced-122">By default, boot diagnostics are enabled on the virtual machine.</span></span>

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

### <span data-ttu-id="83ced-123">-DiskLabel</span><span class="sxs-lookup"><span data-stu-id="83ced-123">-DiskLabel</span></span>
<span data-ttu-id="83ced-124">Określa etykietę dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="83ced-124">Specifies a label for the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: ImageName
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83ced-125">-Diskname</span><span class="sxs-lookup"><span data-stu-id="83ced-125">-DiskName</span></span>
<span data-ttu-id="83ced-126">Określa nazwę dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="83ced-126">Specifies a name for the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: DiskName
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83ced-127">-HostCaching</span><span class="sxs-lookup"><span data-stu-id="83ced-127">-HostCaching</span></span>
<span data-ttu-id="83ced-128">Określa tryb buforowania hosta dla dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="83ced-128">Specifies the host caching mode for the operating system disk.</span></span>

<span data-ttu-id="83ced-129">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="83ced-129">Valid values are:</span></span>

- <span data-ttu-id="83ced-130">Odczytu</span><span class="sxs-lookup"><span data-stu-id="83ced-130">ReadOnly</span></span>
- <span data-ttu-id="83ced-131">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="83ced-131">ReadWrite</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83ced-132">-ImageName</span><span class="sxs-lookup"><span data-stu-id="83ced-132">-ImageName</span></span>
<span data-ttu-id="83ced-133">Określa nazwę obrazu maszyny wirtualnej, który ma być używany dla dysku z systemem operacyjnym.</span><span class="sxs-lookup"><span data-stu-id="83ced-133">Specifies the name of the virtual machine image to use for the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: ImageName
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83ced-134">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="83ced-134">-InformationAction</span></span>
<span data-ttu-id="83ced-135">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="83ced-135">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="83ced-136">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="83ced-136">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="83ced-137">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="83ced-137">Continue</span></span>
- <span data-ttu-id="83ced-138">Ignorować</span><span class="sxs-lookup"><span data-stu-id="83ced-138">Ignore</span></span>
- <span data-ttu-id="83ced-139">Inquire</span><span class="sxs-lookup"><span data-stu-id="83ced-139">Inquire</span></span>
- <span data-ttu-id="83ced-140">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="83ced-140">SilentlyContinue</span></span>
- <span data-ttu-id="83ced-141">Przestaw</span><span class="sxs-lookup"><span data-stu-id="83ced-141">Stop</span></span>
- <span data-ttu-id="83ced-142">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="83ced-142">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83ced-143">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="83ced-143">-InformationVariable</span></span>
<span data-ttu-id="83ced-144">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="83ced-144">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83ced-145">-InstanceSize</span><span class="sxs-lookup"><span data-stu-id="83ced-145">-InstanceSize</span></span>
<span data-ttu-id="83ced-146">Określa rozmiar wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="83ced-146">Specifies the size of the instance.</span></span>

<span data-ttu-id="83ced-147">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="83ced-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="83ced-148">ExtraSmall</span><span class="sxs-lookup"><span data-stu-id="83ced-148">ExtraSmall</span></span>
- <span data-ttu-id="83ced-149">Mała</span><span class="sxs-lookup"><span data-stu-id="83ced-149">Small</span></span>
- <span data-ttu-id="83ced-150">Pożywkę</span><span class="sxs-lookup"><span data-stu-id="83ced-150">Medium</span></span>
- <span data-ttu-id="83ced-151">Większej</span><span class="sxs-lookup"><span data-stu-id="83ced-151">Large</span></span>
- <span data-ttu-id="83ced-152">ExtraLarge</span><span class="sxs-lookup"><span data-stu-id="83ced-152">ExtraLarge</span></span>
- <span data-ttu-id="83ced-153">A5</span><span class="sxs-lookup"><span data-stu-id="83ced-153">A5</span></span>
- <span data-ttu-id="83ced-154">A6</span><span class="sxs-lookup"><span data-stu-id="83ced-154">A6</span></span>
- <span data-ttu-id="83ced-155">A7</span><span class="sxs-lookup"><span data-stu-id="83ced-155">A7</span></span>
- <span data-ttu-id="83ced-156">A8</span><span class="sxs-lookup"><span data-stu-id="83ced-156">A8</span></span>
- <span data-ttu-id="83ced-157">A9</span><span class="sxs-lookup"><span data-stu-id="83ced-157">A9</span></span>
- <span data-ttu-id="83ced-158">Basic_A0</span><span class="sxs-lookup"><span data-stu-id="83ced-158">Basic_A0</span></span>
- <span data-ttu-id="83ced-159">Basic_A1</span><span class="sxs-lookup"><span data-stu-id="83ced-159">Basic_A1</span></span>
- <span data-ttu-id="83ced-160">Basic_A2</span><span class="sxs-lookup"><span data-stu-id="83ced-160">Basic_A2</span></span>
- <span data-ttu-id="83ced-161">Basic_A3</span><span class="sxs-lookup"><span data-stu-id="83ced-161">Basic_A3</span></span>
- <span data-ttu-id="83ced-162">Basic_A4</span><span class="sxs-lookup"><span data-stu-id="83ced-162">Basic_A4</span></span>
- <span data-ttu-id="83ced-163">Standard_D1</span><span class="sxs-lookup"><span data-stu-id="83ced-163">Standard_D1</span></span>
- <span data-ttu-id="83ced-164">Standard_D2</span><span class="sxs-lookup"><span data-stu-id="83ced-164">Standard_D2</span></span>
- <span data-ttu-id="83ced-165">Standard_D3</span><span class="sxs-lookup"><span data-stu-id="83ced-165">Standard_D3</span></span>
- <span data-ttu-id="83ced-166">Standard_D4</span><span class="sxs-lookup"><span data-stu-id="83ced-166">Standard_D4</span></span>
- <span data-ttu-id="83ced-167">Standard_D11</span><span class="sxs-lookup"><span data-stu-id="83ced-167">Standard_D11</span></span>
- <span data-ttu-id="83ced-168">Standard_D12</span><span class="sxs-lookup"><span data-stu-id="83ced-168">Standard_D12</span></span>
- <span data-ttu-id="83ced-169">Standard_D13</span><span class="sxs-lookup"><span data-stu-id="83ced-169">Standard_D13</span></span>
- <span data-ttu-id="83ced-170">Standard_D14</span><span class="sxs-lookup"><span data-stu-id="83ced-170">Standard_D14</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83ced-171">-Label</span><span class="sxs-lookup"><span data-stu-id="83ced-171">-Label</span></span>
<span data-ttu-id="83ced-172">Określa etykietę, którą należy przypisać do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="83ced-172">Specifies a label to assign to the virtual machine.</span></span>

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

### <span data-ttu-id="83ced-173">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="83ced-173">-LicenseType</span></span>
<span data-ttu-id="83ced-174">Określa typ licencji dla obrazu lub dysku licencjonowanego lokalnie.</span><span class="sxs-lookup"><span data-stu-id="83ced-174">Specifies the type of license for an image or disk that is licensed on-premises.</span></span>
<span data-ttu-id="83ced-175">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="83ced-175">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="83ced-176">Windows_Client</span><span class="sxs-lookup"><span data-stu-id="83ced-176">Windows_Client</span></span>
- <span data-ttu-id="83ced-177">Windows_Server</span><span class="sxs-lookup"><span data-stu-id="83ced-177">Windows_Server</span></span> 

<span data-ttu-id="83ced-178">Ten parametr można określić tylko w przypadku obrazów zawierających system operacyjny Windows Server.</span><span class="sxs-lookup"><span data-stu-id="83ced-178">Specify this parameter only for images that contain the Windows Server operating system.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83ced-179">-MediaLocation</span><span class="sxs-lookup"><span data-stu-id="83ced-179">-MediaLocation</span></span>
<span data-ttu-id="83ced-180">Określa lokalizację magazynu platformy Azure dla nowego dysku maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="83ced-180">Specifies the Azure storage location for the new virtual machine disk.</span></span>

```yaml
Type: String
Parameter Sets: ImageName
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83ced-181">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="83ced-181">-Name</span></span>
<span data-ttu-id="83ced-182">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="83ced-182">Specifies the name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83ced-183">-Profile</span><span class="sxs-lookup"><span data-stu-id="83ced-183">-Profile</span></span>
<span data-ttu-id="83ced-184">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83ced-184">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="83ced-185">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="83ced-185">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83ced-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83ced-186">CommonParameters</span></span>
<span data-ttu-id="83ced-187">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83ced-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83ced-188">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83ced-188">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83ced-189">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="83ced-189">INPUTS</span></span>

## <span data-ttu-id="83ced-190">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="83ced-190">OUTPUTS</span></span>

## <span data-ttu-id="83ced-191">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="83ced-191">NOTES</span></span>

## <span data-ttu-id="83ced-192">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="83ced-192">RELATED LINKS</span></span>

