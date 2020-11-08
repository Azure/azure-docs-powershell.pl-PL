---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 64EF867E-5142-4317-9552-8BC94117208D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 899ecd0256bc3d6f88b8f942fa488db444a9bb41
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055032"
---
# <span data-ttu-id="9414a-101">Set-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="9414a-101">Set-AzureDataDisk</span></span>

## <span data-ttu-id="9414a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9414a-102">SYNOPSIS</span></span>
<span data-ttu-id="9414a-103">Modyfikuje buforowanie hosta istniejącego dysku danych na maszynie wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9414a-103">Modifies the host caching of an existing data disk on an Azure virtual machine.</span></span>

## <span data-ttu-id="9414a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9414a-104">SYNTAX</span></span>

### <span data-ttu-id="9414a-105">Noresize</span><span class="sxs-lookup"><span data-stu-id="9414a-105">NoResize</span></span>
```
Set-AzureDataDisk [-HostCaching] <String> [-LUN] <Int32> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="9414a-106">Resize</span><span class="sxs-lookup"><span data-stu-id="9414a-106">Resize</span></span>
```
Set-AzureDataDisk [-DiskName] <String> [-ResizedSizeInGB] <Int32> -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="9414a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="9414a-107">DESCRIPTION</span></span>
<span data-ttu-id="9414a-108">Polecenie cmdlet **Set-AzureDataDisk** modyfikuje atrybuty pamięci podręcznej istniejącego dysku danych na maszynie wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9414a-108">The **Set-AzureDataDisk** cmdlet modifies the cache attributes of an existing data disk on an Azure virtual machine.</span></span>
<span data-ttu-id="9414a-109">Określ, który dysk danych ma zostać zaktualizowany za pomocą numeru jednostki logicznej (LUN).</span><span class="sxs-lookup"><span data-stu-id="9414a-109">Specify which data disk to update by its logical unit number (LUN).</span></span>

## <span data-ttu-id="9414a-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9414a-110">EXAMPLES</span></span>

### <span data-ttu-id="9414a-111">Przykład 1. Modyfikowanie buforowania hosta dla dysku z danymi</span><span class="sxs-lookup"><span data-stu-id="9414a-111">Example 1: Modify the host caching for a data disk</span></span>
```
PS C:\> Get-AzureVM "ContosoService" | Set-AzureDataDisk -VM "VirtualMachine07" -LUN 2 -HostCaching ReadOnly | Update-AzureVM
```

<span data-ttu-id="9414a-112">To polecenie pobiera maszyny wirtualne uruchomione w usłudze o nazwie ContosoService przy użyciu polecenia cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="9414a-112">This command gets the virtual machines that run on the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="9414a-113">Polecenie przekazuje je do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="9414a-113">The command passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="9414a-114">Polecenie cmdlet ustawia dysk danych w jednostkach LUN 2 maszyny wirtualnej o nazwie VirtualMachine07, aby używać buforowania hosta ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="9414a-114">That cmdlet sets the data disk at LUN 2 of the virtual machine named VirtualMachine07 to use ReadOnly host caching.</span></span>
<span data-ttu-id="9414a-115">Polecenie powoduje zaktualizowanie maszyny wirtualnej w celu odzwierciedlenia wprowadzonych zmian przy użyciu polecenia cmdlet **Update-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="9414a-115">The command updates the virtual machine to reflect your changes by using the **Update-AzureVM** cmdlet.</span></span>

### <span data-ttu-id="9414a-116">Przykład 2: modyfikowanie buforowania hosta dla wszystkich dysków z danymi na maszynie wirtualnej</span><span class="sxs-lookup"><span data-stu-id="9414a-116">Example 2: Modify the host caching for all data disks on a virtual machine</span></span>
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine07" | Get-AzureDataDisk | Set-AzureDataDisk -HostCaching ReadWrite | Update-AzureVM
```

<span data-ttu-id="9414a-117">To polecenie pobiera obiekt maszyny wirtualnej o nazwie VirtualMachine07 w chmurze usługi ContosoService.</span><span class="sxs-lookup"><span data-stu-id="9414a-117">This command gets an object for the virtual machine named VirtualMachine07 on the ContosoService cloud service.</span></span>
<span data-ttu-id="9414a-118">Polecenie przekazuje je do polecenia cmdlet **Get-AzureDataDisk** , które pobiera dyski danych dla tej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9414a-118">The command passes it to the **Get-AzureDataDisk** cmdlet, which gets the data disks for that virtual machine.</span></span>
<span data-ttu-id="9414a-119">Bieżące polecenie cmdlet ustawia tryb buforowania hosta każdego z dysków z danymi na ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="9414a-119">The current cmdlet then sets the host caching mode of each data disks to ReadWrite.</span></span>
<span data-ttu-id="9414a-120">Polecenie aktualizuje maszynę wirtualną, aby odzwierciedlić wprowadzone zmiany.</span><span class="sxs-lookup"><span data-stu-id="9414a-120">The command updates the virtual machine to reflect your changes.</span></span>

## <span data-ttu-id="9414a-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9414a-121">PARAMETERS</span></span>

### <span data-ttu-id="9414a-122">-Diskname</span><span class="sxs-lookup"><span data-stu-id="9414a-122">-DiskName</span></span>
<span data-ttu-id="9414a-123">Określa nazwę konfiguracji dysku danych, którą to polecenie cmdlet modyfikuje.</span><span class="sxs-lookup"><span data-stu-id="9414a-123">Specifies the name of the data disk configuration that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: Resize
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9414a-124">-HostCaching</span><span class="sxs-lookup"><span data-stu-id="9414a-124">-HostCaching</span></span>

> [!WARNING]
> <span data-ttu-id="9414a-125">Buforowanie dysków nie jest obsługiwane w przypadku dysków 4 TiB i większych.</span><span class="sxs-lookup"><span data-stu-id="9414a-125">Disk Caching is not supported for disks 4 TiB and larger.</span></span> <span data-ttu-id="9414a-126">Jeśli do maszyny wirtualnej jest podłączonych wiele dysków, każdy dysk o rozmiarze mniejszym niż 4 TiB będzie obsługiwać buforowanie.</span><span class="sxs-lookup"><span data-stu-id="9414a-126">If multiple disks are attached to your VM, each disk that is smaller than 4 TiB will support caching.</span></span>
>
> <span data-ttu-id="9414a-127">Zmiana ustawienia pamięci podręcznej dysku Azure powoduje odłączenie i ponowne załączenie dysku docelowego.</span><span class="sxs-lookup"><span data-stu-id="9414a-127">Changing the cache setting of an Azure disk detaches and re-attaches the target disk.</span></span> <span data-ttu-id="9414a-128">Jeśli jest to dysk systemu operacyjnego, maszyna wirtualna zostanie ponownie uruchomiona.</span><span class="sxs-lookup"><span data-stu-id="9414a-128">If it is the operating system disk, the VM is restarted.</span></span> <span data-ttu-id="9414a-129">Przed zmianą ustawienia pamięci podręcznej dysku Zatrzymaj wszystkie aplikacje/usługi, które mogą być dotknięte tym zakłóceniem.</span><span class="sxs-lookup"><span data-stu-id="9414a-129">Stop all applications/services that might be affected by this disruption before changing the disk cache setting.</span></span> <span data-ttu-id="9414a-130">Obserwowanie tych rekomendacji może spowodować uszkodzenie danych.</span><span class="sxs-lookup"><span data-stu-id="9414a-130">Not following those recommendations could lead to data corruption.</span></span>

<span data-ttu-id="9414a-131">Określa ustawienia buforowania na poziomie hosta dla dysku.</span><span class="sxs-lookup"><span data-stu-id="9414a-131">Specifies the host level caching settings of the disk.</span></span>
<span data-ttu-id="9414a-132">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="9414a-132">Valid values are:</span></span>

- <span data-ttu-id="9414a-133">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="9414a-133">None</span></span>
- <span data-ttu-id="9414a-134">Odczytu</span><span class="sxs-lookup"><span data-stu-id="9414a-134">ReadOnly</span></span>
- <span data-ttu-id="9414a-135">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="9414a-135">ReadWrite</span></span>

```yaml
Type: String
Parameter Sets: NoResize
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9414a-136">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="9414a-136">-InformationAction</span></span>
<span data-ttu-id="9414a-137">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="9414a-137">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="9414a-138">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="9414a-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9414a-139">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="9414a-139">Continue</span></span>
- <span data-ttu-id="9414a-140">Ignorować</span><span class="sxs-lookup"><span data-stu-id="9414a-140">Ignore</span></span>
- <span data-ttu-id="9414a-141">Inquire</span><span class="sxs-lookup"><span data-stu-id="9414a-141">Inquire</span></span>
- <span data-ttu-id="9414a-142">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="9414a-142">SilentlyContinue</span></span>
- <span data-ttu-id="9414a-143">Przestaw</span><span class="sxs-lookup"><span data-stu-id="9414a-143">Stop</span></span>
- <span data-ttu-id="9414a-144">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="9414a-144">Suspend</span></span>

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

### <span data-ttu-id="9414a-145">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="9414a-145">-InformationVariable</span></span>
<span data-ttu-id="9414a-146">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="9414a-146">Specifies an information variable.</span></span>

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

### <span data-ttu-id="9414a-147">-LUN</span><span class="sxs-lookup"><span data-stu-id="9414a-147">-LUN</span></span>
<span data-ttu-id="9414a-148">Określa jednostkę LUN dla dysku danych na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9414a-148">Specifies the LUN for the data drive in the virtual machine.</span></span>
<span data-ttu-id="9414a-149">Prawidłowe wartości to: od 0 do 15.</span><span class="sxs-lookup"><span data-stu-id="9414a-149">Valid values are: 0 through 15.</span></span>

```yaml
Type: Int32
Parameter Sets: NoResize
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9414a-150">-Profile</span><span class="sxs-lookup"><span data-stu-id="9414a-150">-Profile</span></span>
<span data-ttu-id="9414a-151">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9414a-151">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9414a-152">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="9414a-152">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9414a-153">-ResizedSizeInGB</span><span class="sxs-lookup"><span data-stu-id="9414a-153">-ResizedSizeInGB</span></span>
<span data-ttu-id="9414a-154">Określa nowy rozmiar (w gigabajtach) dysku danych.</span><span class="sxs-lookup"><span data-stu-id="9414a-154">Specifies the new size, in gigabytes, for the data disk.</span></span>
<span data-ttu-id="9414a-155">Nowy rozmiar musi być większy niż bieżący rozmiar.</span><span class="sxs-lookup"><span data-stu-id="9414a-155">The new size must be larger than the current size.</span></span>

```yaml
Type: Int32
Parameter Sets: Resize
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9414a-156">-VM</span><span class="sxs-lookup"><span data-stu-id="9414a-156">-VM</span></span>
<span data-ttu-id="9414a-157">Określa obiekt maszyny wirtualnej dołączony do dysku z danymi.</span><span class="sxs-lookup"><span data-stu-id="9414a-157">Specifies the virtual machine object that is attached to the data disk.</span></span>
<span data-ttu-id="9414a-158">Aby uzyskać obiekt maszyny wirtualnej, użyj polecenia cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="9414a-158">To obtain a virtual machine object, use the **Get-AzureVM** cmdlet.</span></span>

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

### <span data-ttu-id="9414a-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9414a-159">CommonParameters</span></span>
<span data-ttu-id="9414a-160">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9414a-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9414a-161">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9414a-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9414a-162">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9414a-162">INPUTS</span></span>

## <span data-ttu-id="9414a-163">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9414a-163">OUTPUTS</span></span>

## <span data-ttu-id="9414a-164">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9414a-164">NOTES</span></span>

## <span data-ttu-id="9414a-165">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9414a-165">RELATED LINKS</span></span>

[<span data-ttu-id="9414a-166">Dodaj-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="9414a-166">Add-AzureDataDisk</span></span>](./Add-AzureDataDisk.md)

[<span data-ttu-id="9414a-167">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="9414a-167">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="9414a-168">Get-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="9414a-168">Get-AzureDataDisk</span></span>](./Get-AzureDataDisk.md)

[<span data-ttu-id="9414a-169">Remove-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="9414a-169">Remove-AzureDataDisk</span></span>](./Remove-AzureDataDisk.md)

[<span data-ttu-id="9414a-170">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="9414a-170">Update-AzureVM</span></span>](./Update-AzureVM.md)


