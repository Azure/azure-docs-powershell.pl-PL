---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D563ACF6-6BCD-4463-8731-175BA047A74D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2ceb2af6b359d5b9660397ef654d6c56e045ce64
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055132"
---
# <span data-ttu-id="2ed47-101">Remove-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="2ed47-101">Remove-AzureDataDisk</span></span>

## <span data-ttu-id="2ed47-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2ed47-102">SYNOPSIS</span></span>
<span data-ttu-id="2ed47-103">Usuwa dysk danych z maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2ed47-103">Removes a data disk from an Azure virtual machine.</span></span>

## <span data-ttu-id="2ed47-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2ed47-104">SYNTAX</span></span>

```
Remove-AzureDataDisk [-LUN] <Int32> [-DeleteVHD] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="2ed47-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2ed47-105">DESCRIPTION</span></span>
<span data-ttu-id="2ed47-106">Polecenie cmdlet **Remove-AzureDataDisk** usuwa dysk danych z maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2ed47-106">The **Remove-AzureDataDisk** cmdlet removes a data disk from an Azure virtual machine.</span></span>
<span data-ttu-id="2ed47-107">Domyślnie to polecenie cmdlet nie usuwa obiektu BLOB dysku danych z konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="2ed47-107">By default, this cmdlet does not remove the data disk blob from the storage account.</span></span>

## <span data-ttu-id="2ed47-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2ed47-108">EXAMPLES</span></span>

### <span data-ttu-id="2ed47-109">Przykład 1: usuwanie dysku danych</span><span class="sxs-lookup"><span data-stu-id="2ed47-109">Example 1: Remove a data disk</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Remove-AzureDataDisk -LUN 0
```

<span data-ttu-id="2ed47-110">To polecenie pobiera maszynę wirtualną o nazwie VirtualMachine07 w usłudze o nazwie ContosoService przy użyciu polecenia cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="2ed47-110">This command gets the virtual machine named VirtualMachine07 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="2ed47-111">Polecenie przekazanie maszyny wirtualnej do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="2ed47-111">The command passes the virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="2ed47-112">Bieżące polecenie cmdlet usuwa dysk danych, który ma jednostkę LUN równą 0.</span><span class="sxs-lookup"><span data-stu-id="2ed47-112">The current cmdlet removes the data disk that has the LUN 0.</span></span>

### <span data-ttu-id="2ed47-113">Przykład 2: usuwanie dysku danych i pliku wirtualnego dysku twardego</span><span class="sxs-lookup"><span data-stu-id="2ed47-113">Example 2: Remove a data disk and the virtual hard disk file</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Remove-AzureDataDisk -LUN 0 -DeleteVHD | Update-AzureVM
```

<span data-ttu-id="2ed47-114">To polecenie umożliwia pobieranie maszyny wirtualnej o nazwie VirtualMachine07 w usłudze o nazwie ContosoService.</span><span class="sxs-lookup"><span data-stu-id="2ed47-114">This command gets the virtual machine named VirtualMachine07 in the service named ContosoService.</span></span>
<span data-ttu-id="2ed47-115">Polecenie przekazanie maszyny wirtualnej do bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ed47-115">The command passes the virtual machine to the current cmdlet.</span></span>
<span data-ttu-id="2ed47-116">Bieżące polecenie cmdlet usuwa dysk danych, który ma jednostkę LUN równą 0.</span><span class="sxs-lookup"><span data-stu-id="2ed47-116">The current cmdlet removes the data disk that has the LUN 0.</span></span>
<span data-ttu-id="2ed47-117">Polecenie zawiera parametr *DeleteVHD* .</span><span class="sxs-lookup"><span data-stu-id="2ed47-117">The command includes the *DeleteVHD* parameter.</span></span>
<span data-ttu-id="2ed47-118">Oznacza również usunięcie źródłowego wirtualnego dysku twardego.</span><span class="sxs-lookup"><span data-stu-id="2ed47-118">Therefore, it also deletes the underlying virtual hard disk.</span></span>
<span data-ttu-id="2ed47-119">Polecenie powoduje zaktualizowanie maszyny wirtualnej w celu odzwierciedlenia wprowadzonych zmian przy użyciu polecenia cmdlet **Update-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="2ed47-119">The command updates the virtual machine to reflect your changes by using the **Update-AzureVM** cmdlet.</span></span>

## <span data-ttu-id="2ed47-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2ed47-120">PARAMETERS</span></span>

### <span data-ttu-id="2ed47-121">-DeleteVHD</span><span class="sxs-lookup"><span data-stu-id="2ed47-121">-DeleteVHD</span></span>
<span data-ttu-id="2ed47-122">Wskazuje, że to polecenie cmdlet usuwa dysk danych i wirtualny dysk twardy (VHD) z magazynu obiektów BLOB.</span><span class="sxs-lookup"><span data-stu-id="2ed47-122">Indicates that this cmdlet removes the data disk and the virtual hard disk (VHD) from blob storage.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ed47-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="2ed47-123">-InformationAction</span></span>
<span data-ttu-id="2ed47-124">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="2ed47-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="2ed47-125">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="2ed47-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2ed47-126">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="2ed47-126">Continue</span></span>
- <span data-ttu-id="2ed47-127">Ignorować</span><span class="sxs-lookup"><span data-stu-id="2ed47-127">Ignore</span></span>
- <span data-ttu-id="2ed47-128">Inquire</span><span class="sxs-lookup"><span data-stu-id="2ed47-128">Inquire</span></span>
- <span data-ttu-id="2ed47-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="2ed47-129">SilentlyContinue</span></span>
- <span data-ttu-id="2ed47-130">Przestaw</span><span class="sxs-lookup"><span data-stu-id="2ed47-130">Stop</span></span>
- <span data-ttu-id="2ed47-131">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="2ed47-131">Suspend</span></span>

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

### <span data-ttu-id="2ed47-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="2ed47-132">-InformationVariable</span></span>
<span data-ttu-id="2ed47-133">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="2ed47-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="2ed47-134">-LUN</span><span class="sxs-lookup"><span data-stu-id="2ed47-134">-LUN</span></span>
<span data-ttu-id="2ed47-135">Określa logiczny numer jednostki (LUN) dla dysku z danymi na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2ed47-135">Specifies the logical unit number (LUN) for the data drive in the virtual machine.</span></span>
<span data-ttu-id="2ed47-136">Prawidłowe wartości to: od 0 do 15.</span><span class="sxs-lookup"><span data-stu-id="2ed47-136">Valid values are: 0 through 15.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ed47-137">-Profile</span><span class="sxs-lookup"><span data-stu-id="2ed47-137">-Profile</span></span>
<span data-ttu-id="2ed47-138">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ed47-138">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2ed47-139">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="2ed47-139">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2ed47-140">-VM</span><span class="sxs-lookup"><span data-stu-id="2ed47-140">-VM</span></span>
<span data-ttu-id="2ed47-141">Określa obiekt maszyny wirtualnej dołączony do dysku z danymi.</span><span class="sxs-lookup"><span data-stu-id="2ed47-141">Specifies the virtual machine object that is attached to the data disk.</span></span>
<span data-ttu-id="2ed47-142">Aby uzyskać obiekt maszyny wirtualnej, użyj polecenia cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="2ed47-142">To obtain a virtual machine object, use the **Get-AzureVM** cmdlet.</span></span>

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

### <span data-ttu-id="2ed47-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ed47-143">CommonParameters</span></span>
<span data-ttu-id="2ed47-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ed47-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ed47-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ed47-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ed47-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2ed47-146">INPUTS</span></span>

## <span data-ttu-id="2ed47-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2ed47-147">OUTPUTS</span></span>

## <span data-ttu-id="2ed47-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2ed47-148">NOTES</span></span>

## <span data-ttu-id="2ed47-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2ed47-149">RELATED LINKS</span></span>

[<span data-ttu-id="2ed47-150">Dodaj-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="2ed47-150">Add-AzureDataDisk</span></span>](./Add-AzureDataDisk.md)

[<span data-ttu-id="2ed47-151">Get-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="2ed47-151">Get-AzureDataDisk</span></span>](./Get-AzureDataDisk.md)

[<span data-ttu-id="2ed47-152">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="2ed47-152">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="2ed47-153">Set-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="2ed47-153">Set-AzureDataDisk</span></span>](./Set-AzureDataDisk.md)

[<span data-ttu-id="2ed47-154">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="2ed47-154">Update-AzureVM</span></span>](./Update-AzureVM.md)


