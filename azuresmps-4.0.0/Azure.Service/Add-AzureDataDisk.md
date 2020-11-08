---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: FDEDBF4F-7507-43FF-A983-7E431C0C1950
online version: ''
schema: 2.0.0
ms.openlocfilehash: 967fbaf83efa12bd305fc9fe075a9abffdd62dc3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054701"
---
# <span data-ttu-id="88e31-101">Add-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="88e31-101">Add-AzureDataDisk</span></span>

## <span data-ttu-id="88e31-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="88e31-102">SYNOPSIS</span></span>
<span data-ttu-id="88e31-103">Dodaje dysk danych do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="88e31-103">Adds a data disk to a virtual machine.</span></span>

## <span data-ttu-id="88e31-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="88e31-104">SYNTAX</span></span>

### <span data-ttu-id="88e31-105">CreateNew (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="88e31-105">CreateNew (Default)</span></span>
```
Add-AzureDataDisk [-CreateNew] [-DiskSizeInGB] <Int32> [-DiskLabel] <String> [-LUN] <Int32>
 [-MediaLocation <String>] [-HostCaching <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="88e31-106">Przywoz</span><span class="sxs-lookup"><span data-stu-id="88e31-106">Import</span></span>
```
Add-AzureDataDisk [-Import] [-DiskName] <String> [-LUN] <Int32> [-HostCaching <String>] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="88e31-107">ImportFrom</span><span class="sxs-lookup"><span data-stu-id="88e31-107">ImportFrom</span></span>
```
Add-AzureDataDisk [-ImportFrom] [-DiskLabel] <String> [-LUN] <Int32> -MediaLocation <String>
 [-HostCaching <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="88e31-108">Opis</span><span class="sxs-lookup"><span data-stu-id="88e31-108">DESCRIPTION</span></span>
<span data-ttu-id="88e31-109">Polecenie cmdlet **Add-AzureDataDisk** umożliwia dodanie nowego lub istniejącego dysku danych do obiektu maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="88e31-109">The **Add-AzureDataDisk** cmdlet adds a new or existing data disk to an Azure virtual machine object.</span></span>
<span data-ttu-id="88e31-110">Użyj parametru *CreateNew* , aby utworzyć nowy dysk danych o określonym rozmiarze i etykiecie.</span><span class="sxs-lookup"><span data-stu-id="88e31-110">Use the *CreateNew* parameter to create a new data disk that has a specified size and label.</span></span>
<span data-ttu-id="88e31-111">Użyj parametru *Import* , aby dołączyć istniejący dysk z repozytorium obrazów.</span><span class="sxs-lookup"><span data-stu-id="88e31-111">Use the *Import* parameter to attach an existing disk from the image repository.</span></span>
<span data-ttu-id="88e31-112">Użyj parametru *ImportFrom* , aby dołączyć istniejący dysk z obiektu BLOB na koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="88e31-112">Use the *ImportFrom* parameter to attach an existing disk from a blob in a storage account.</span></span>
<span data-ttu-id="88e31-113">Możesz określić tryb pamięci podręcznej hosta dołączonego dysku danych.</span><span class="sxs-lookup"><span data-stu-id="88e31-113">You can specify the host-cache mode of the attached data disk.</span></span>

## <span data-ttu-id="88e31-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="88e31-114">EXAMPLES</span></span>

### <span data-ttu-id="88e31-115">Przykład 1: Importowanie dysku danych z repozytorium</span><span class="sxs-lookup"><span data-stu-id="88e31-115">Example 1: Import a data disk from the repository</span></span>
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine07" | Add-AzureDataDisk -Import -DiskName "Disk68" -LUN 0 | Update-AzureVM
```

<span data-ttu-id="88e31-116">To polecenie pobiera obiekt maszyny wirtualnej dla maszyny wirtualnej o nazwie VirtualMachine07 w usłudze Cloud ContosoService przy użyciu polecenia cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="88e31-116">This command gets a virtual machine object for the virtual machine named VirtualMachine07 in the ContosoService cloud service by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="88e31-117">Polecenie przekazuje je do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="88e31-117">The command passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="88e31-118">To polecenie dołącza do maszyny wirtualnej istniejący dysk danych z repozytorium.</span><span class="sxs-lookup"><span data-stu-id="88e31-118">That command attaches an existing data disk from the repository to the virtual machine.</span></span>
<span data-ttu-id="88e31-119">Dysk danych ma jednostkę LUN równą 0.</span><span class="sxs-lookup"><span data-stu-id="88e31-119">The data disk has a LUN of 0.</span></span>
<span data-ttu-id="88e31-120">Polecenie powoduje zaktualizowanie maszyny wirtualnej w celu odzwierciedlenia wprowadzonych zmian przy użyciu polecenia cmdlet **Update-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="88e31-120">The command updates the virtual machine to reflect your changes by using the **Update-AzureVM** cmdlet.</span></span>

### <span data-ttu-id="88e31-121">Przykład 2: Dodawanie nowego dysku danych</span><span class="sxs-lookup"><span data-stu-id="88e31-121">Example 2: Add a new data disk</span></span>
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine08" | Add-AzureDataDisk -CreateNew -DiskSizeInGB 128 -DiskLabel "main" -LUN 0 | Update-AzureVM
```

<span data-ttu-id="88e31-122">To polecenie pobiera obiekt maszyny wirtualnej dla maszyny wirtualnej o nazwie VirtualMachine08.</span><span class="sxs-lookup"><span data-stu-id="88e31-122">This command gets a virtual machine object for the virtual machine named VirtualMachine08.</span></span>
<span data-ttu-id="88e31-123">Polecenie przekazuje je do bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88e31-123">The command passes it to the current cmdlet.</span></span>
<span data-ttu-id="88e31-124">To polecenie dołącza nowy dysk danych o nazwie MyNewDisk. VHD.</span><span class="sxs-lookup"><span data-stu-id="88e31-124">That command attaches a new data disk named MyNewDisk.vhd.</span></span>
<span data-ttu-id="88e31-125">Polecenie cmdlet powoduje utworzenie dysku w kontenerze VHD na domyślnym koncie magazynu bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="88e31-125">The cmdlet creates the disk in the vhds container in the default storage account of the current subscription.</span></span>
<span data-ttu-id="88e31-126">Polecenie aktualizuje maszynę wirtualną, aby odzwierciedlić wprowadzone zmiany.</span><span class="sxs-lookup"><span data-stu-id="88e31-126">The command updates the virtual machine to reflect your changes.</span></span>

### <span data-ttu-id="88e31-127">Przykład 3: Dodawanie dysku z danymi z określonej lokalizacji</span><span class="sxs-lookup"><span data-stu-id="88e31-127">Example 3: Add a data disk from a specified location</span></span>
```
PS C:\> Get-AzureVM "ContosoService" -Name "Database" | Add-AzureDataDisk -ImportFrom -MediaLocation "https://contosostorage.blob.core.windows.net/container07/Disk14.vhd" -DiskLabel "main" -LUN 0 | Update-AzureVM
```

<span data-ttu-id="88e31-128">To polecenie pobiera obiekt maszyny wirtualnej dla maszyny wirtualnej o nazwie Database.</span><span class="sxs-lookup"><span data-stu-id="88e31-128">This command gets a virtual machine object for the virtual machine named Database.</span></span>
<span data-ttu-id="88e31-129">Polecenie przekazuje je do bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88e31-129">The command passes it to the current cmdlet.</span></span>
<span data-ttu-id="88e31-130">To polecenie dołącza istniejący dysk danych o nazwie Disk14. VHD z określonej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="88e31-130">That command attaches an existing data disk named Disk14.vhd from the specified location.</span></span>
<span data-ttu-id="88e31-131">Polecenie aktualizuje maszynę wirtualną, aby odzwierciedlić wprowadzone zmiany.</span><span class="sxs-lookup"><span data-stu-id="88e31-131">The command updates the virtual machine to reflect your changes.</span></span>

## <span data-ttu-id="88e31-132">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="88e31-132">PARAMETERS</span></span>

### <span data-ttu-id="88e31-133">-CreateNew</span><span class="sxs-lookup"><span data-stu-id="88e31-133">-CreateNew</span></span>
<span data-ttu-id="88e31-134">Wskazuje, że to polecenie cmdlet tworzy dysk danych.</span><span class="sxs-lookup"><span data-stu-id="88e31-134">Indicates that this cmdlet creates a data disk.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: CreateNew
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88e31-135">-DiskLabel</span><span class="sxs-lookup"><span data-stu-id="88e31-135">-DiskLabel</span></span>
<span data-ttu-id="88e31-136">Określa etykietę dysku dla nowego dysku danych.</span><span class="sxs-lookup"><span data-stu-id="88e31-136">Specifies the disk label for a new data disk.</span></span>

```yaml
Type: String
Parameter Sets: CreateNew, ImportFrom
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88e31-137">-Diskname</span><span class="sxs-lookup"><span data-stu-id="88e31-137">-DiskName</span></span>
<span data-ttu-id="88e31-138">Określa nazwę dysku z danymi w repozytorium dysków.</span><span class="sxs-lookup"><span data-stu-id="88e31-138">Specifies the name of a data disk in the disk repository.</span></span>

```yaml
Type: String
Parameter Sets: Import
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88e31-139">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="88e31-139">-DiskSizeInGB</span></span>
<span data-ttu-id="88e31-140">Określa rozmiar dysku logicznego (w gigabajtach) dla nowego dysku danych.</span><span class="sxs-lookup"><span data-stu-id="88e31-140">Specifies the logical disk size, in gigabytes, for a new data disk.</span></span>

```yaml
Type: Int32
Parameter Sets: CreateNew
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88e31-141">-HostCaching</span><span class="sxs-lookup"><span data-stu-id="88e31-141">-HostCaching</span></span>
<span data-ttu-id="88e31-142">Określa ustawienia buforowania na poziomie hosta dla dysku.</span><span class="sxs-lookup"><span data-stu-id="88e31-142">Specifies the host level caching settings of the disk.</span></span>
<span data-ttu-id="88e31-143">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="88e31-143">Valid values are:</span></span> 

- <span data-ttu-id="88e31-144">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="88e31-144">None</span></span> 
- <span data-ttu-id="88e31-145">Odczytu</span><span class="sxs-lookup"><span data-stu-id="88e31-145">ReadOnly</span></span> 
- <span data-ttu-id="88e31-146">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="88e31-146">ReadWrite</span></span>

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

### <span data-ttu-id="88e31-147">— Importowanie</span><span class="sxs-lookup"><span data-stu-id="88e31-147">-Import</span></span>
<span data-ttu-id="88e31-148">Wskazuje, że to polecenie cmdlet importuje istniejący dysk danych z repozytorium obrazów.</span><span class="sxs-lookup"><span data-stu-id="88e31-148">Indicates that this cmdlet imports an existing data disk from the image repository.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Import
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88e31-149">-ImportFrom</span><span class="sxs-lookup"><span data-stu-id="88e31-149">-ImportFrom</span></span>
<span data-ttu-id="88e31-150">Wskazuje, że to polecenie cmdlet importuje istniejący dysk danych z obiektu BLOB na koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="88e31-150">Indicates that this cmdlet imports an existing data disk from a blob in a storage account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ImportFrom
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88e31-151">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="88e31-151">-InformationAction</span></span>
<span data-ttu-id="88e31-152">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="88e31-152">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="88e31-153">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="88e31-153">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="88e31-154">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="88e31-154">Continue</span></span>
- <span data-ttu-id="88e31-155">Ignorować</span><span class="sxs-lookup"><span data-stu-id="88e31-155">Ignore</span></span>
- <span data-ttu-id="88e31-156">Inquire</span><span class="sxs-lookup"><span data-stu-id="88e31-156">Inquire</span></span>
- <span data-ttu-id="88e31-157">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="88e31-157">SilentlyContinue</span></span>
- <span data-ttu-id="88e31-158">Przestaw</span><span class="sxs-lookup"><span data-stu-id="88e31-158">Stop</span></span>
- <span data-ttu-id="88e31-159">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="88e31-159">Suspend</span></span>

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

### <span data-ttu-id="88e31-160">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="88e31-160">-InformationVariable</span></span>
<span data-ttu-id="88e31-161">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="88e31-161">Specifies an information variable.</span></span>

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

### <span data-ttu-id="88e31-162">-LUN</span><span class="sxs-lookup"><span data-stu-id="88e31-162">-LUN</span></span>
<span data-ttu-id="88e31-163">Określa logiczny numer jednostki (LUN) dla dysku z danymi na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="88e31-163">Specifies the logical unit number (LUN) for the data drive in the virtual machine.</span></span>
<span data-ttu-id="88e31-164">Prawidłowe wartości to: od 0 do 15.</span><span class="sxs-lookup"><span data-stu-id="88e31-164">Valid values are: 0 through 15.</span></span>
<span data-ttu-id="88e31-165">Każdy dysk z danymi musi mieć unikatową jednostkę LUN.</span><span class="sxs-lookup"><span data-stu-id="88e31-165">Each data disk must have a unique LUN.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88e31-166">-MediaLocation</span><span class="sxs-lookup"><span data-stu-id="88e31-166">-MediaLocation</span></span>
<span data-ttu-id="88e31-167">Określa lokalizację obiektu BLOB na koncie usługi Azure Storage, w którym to polecenie cmdlet przechowuje dysk danych.</span><span class="sxs-lookup"><span data-stu-id="88e31-167">Specifies the location of the blob in an Azure storage account where this cmdlet stores the data disk.</span></span>
<span data-ttu-id="88e31-168">Jeśli nie podano lokalizacji, polecenie cmdlet zapisuje dysk danych w kontenerze VHD na domyślnym koncie magazynu dla bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="88e31-168">If you do not specify a location, the cmdlet stores the data disk in the vhds container in the default storage account for the current subscription.</span></span>
<span data-ttu-id="88e31-169">Jeśli kontener wirtualnych dysków twardych nie istnieje, polecenie cmdlet tworzy kontener dysków VHD.</span><span class="sxs-lookup"><span data-stu-id="88e31-169">If a vhds container does not exist, the cmdlet creates a vhds container.</span></span>

```yaml
Type: String
Parameter Sets: CreateNew
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ImportFrom
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88e31-170">-Profile</span><span class="sxs-lookup"><span data-stu-id="88e31-170">-Profile</span></span>
<span data-ttu-id="88e31-171">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88e31-171">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="88e31-172">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="88e31-172">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="88e31-173">-VM</span><span class="sxs-lookup"><span data-stu-id="88e31-173">-VM</span></span>
<span data-ttu-id="88e31-174">Określa obiekt maszyny wirtualnej, do którego to polecenie cmdlet dołącza dysk danych.</span><span class="sxs-lookup"><span data-stu-id="88e31-174">Specifies the virtual machine object to which this cmdlet attaches a data disk.</span></span>
<span data-ttu-id="88e31-175">Aby uzyskać obiekt maszyny wirtualnej, użyj polecenia cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="88e31-175">To obtain a virtual machine object, use the **Get-AzureVM** cmdlet.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="88e31-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88e31-176">CommonParameters</span></span>
<span data-ttu-id="88e31-177">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88e31-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88e31-178">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88e31-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88e31-179">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="88e31-179">INPUTS</span></span>

## <span data-ttu-id="88e31-180">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="88e31-180">OUTPUTS</span></span>

## <span data-ttu-id="88e31-181">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="88e31-181">NOTES</span></span>

## <span data-ttu-id="88e31-182">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="88e31-182">RELATED LINKS</span></span>

[<span data-ttu-id="88e31-183">Get-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="88e31-183">Get-AzureDataDisk</span></span>](./Get-AzureDataDisk.md)

[<span data-ttu-id="88e31-184">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="88e31-184">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="88e31-185">Remove-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="88e31-185">Remove-AzureDataDisk</span></span>](./Remove-AzureDataDisk.md)

[<span data-ttu-id="88e31-186">Set-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="88e31-186">Set-AzureDataDisk</span></span>](./Set-AzureDataDisk.md)

[<span data-ttu-id="88e31-187">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="88e31-187">Update-AzureVM</span></span>](./Update-AzureVM.md)


