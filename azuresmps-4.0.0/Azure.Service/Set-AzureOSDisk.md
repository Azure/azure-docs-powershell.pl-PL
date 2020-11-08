---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 02DB15F5-5CE0-4FF0-8863-AF1B2BA5E775
online version: ''
schema: 2.0.0
ms.openlocfilehash: 41f72ace02132ba4184af08e995404b47f76d0b0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054794"
---
# <span data-ttu-id="ed14d-101">Set-AzureOSDisk</span><span class="sxs-lookup"><span data-stu-id="ed14d-101">Set-AzureOSDisk</span></span>

## <span data-ttu-id="ed14d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ed14d-102">SYNOPSIS</span></span>
<span data-ttu-id="ed14d-103">Modyfikuje tryb pamięci podręcznej hosta maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ed14d-103">Modifies the host cache mode of an Azure virtual machine.</span></span>

## <span data-ttu-id="ed14d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ed14d-104">SYNTAX</span></span>

### <span data-ttu-id="ed14d-105">Noresize</span><span class="sxs-lookup"><span data-stu-id="ed14d-105">NoResize</span></span>
```
Set-AzureOSDisk [-HostCaching] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="ed14d-106">Resize</span><span class="sxs-lookup"><span data-stu-id="ed14d-106">Resize</span></span>
```
Set-AzureOSDisk [[-HostCaching] <String>] [-ResizedSizeInGB] <Int32> -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="ed14d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ed14d-107">DESCRIPTION</span></span>
<span data-ttu-id="ed14d-108">Polecenie cmdlet **Set-AzureOSDisk** modyfikuje tryb pamięci podręcznej hosta na dysku systemu operacyjnego maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ed14d-108">The **Set-AzureOSDisk** cmdlet modifies the host cache mode of the operating system disk of an Azure virtual machine.</span></span>
<span data-ttu-id="ed14d-109">Obsługiwane tryby pamięci podręcznej hosta są tylko do odczytu i ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="ed14d-109">The supported host cache modes are ReadOnly and ReadWrite.</span></span>
<span data-ttu-id="ed14d-110">Uruchomienie tego polecenia cmdlet na maszynie wirtualnej, która jest uruchomiona, powoduje ponowne uruchomienie maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ed14d-110">If you run this cmdlet on a virtual machine that is running, that virtual machine restarts.</span></span>

## <span data-ttu-id="ed14d-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ed14d-111">EXAMPLES</span></span>

### <span data-ttu-id="ed14d-112">Przykład 1: Ustawianie trybu pamięci podręcznej hosta na wartość ReadOnly za pomocą potoku</span><span class="sxs-lookup"><span data-stu-id="ed14d-112">Example 1: Set the host cache mode to ReadOnly by using the pipeline</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine02" | Set-AzureOSDisk -HostCaching "ReadOnly"
```

<span data-ttu-id="ed14d-113">To polecenie pobiera maszynę wirtualną o nazwie VirtualMachine02 w usłudze o nazwie ContosoService przy użyciu polecenia cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="ed14d-113">This command gets the virtual machine named VirtualMachine02 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="ed14d-114">Polecenie przekazanie maszyny wirtualnej do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="ed14d-114">The command passes the virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ed14d-115">Bieżące polecenie cmdlet ustawia tryb pamięci podręcznej hosta na dysku systemu operacyjnego tej maszyny wirtualnej jako tylko do odczytu.</span><span class="sxs-lookup"><span data-stu-id="ed14d-115">The current cmdlet sets the host cache mode of the operating system disk of that virtual machine to be ReadOnly.</span></span>

### <span data-ttu-id="ed14d-116">Przykład 2: Ustawianie trybu pamięci podręcznej hosta na ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ed14d-116">Example 2: Set the host cache mode to ReadWrite</span></span>
```
PS C:\> $VM = Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine02"
PS C:\> Set-AzureOSDisk "ReadWrite" -VM $myVM2
```

<span data-ttu-id="ed14d-117">Pierwsze polecenie uzyskuje maszynę wirtualną o nazwie VirtualMachine02 w usłudze o nazwie ContosoService, a następnie zapisuje ją w zmiennej.</span><span class="sxs-lookup"><span data-stu-id="ed14d-117">The first command gets the virtual machine named VirtualMachine02 in the service named ContosoService, and then stores it in the variable.</span></span>

<span data-ttu-id="ed14d-118">Drugie polecenie ustawia tryb pamięci podręcznej hosta na dysku z systemem operacyjnym tej maszyny wirtualnej na ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="ed14d-118">The second command sets the host cache mode of the operating system disk of that virtual machine to be ReadWrite.</span></span>

## <span data-ttu-id="ed14d-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ed14d-119">PARAMETERS</span></span>

### <span data-ttu-id="ed14d-120">-HostCaching</span><span class="sxs-lookup"><span data-stu-id="ed14d-120">-HostCaching</span></span>
<span data-ttu-id="ed14d-121">Określa atrybut pamięć podręczna hosta dla dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="ed14d-121">Specifies the host cache attribute for the operating system disk.</span></span>
<span data-ttu-id="ed14d-122">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="ed14d-122">Valid values are:</span></span> 

- <span data-ttu-id="ed14d-123">Odczytu</span><span class="sxs-lookup"><span data-stu-id="ed14d-123">ReadOnly</span></span> 
- <span data-ttu-id="ed14d-124">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ed14d-124">ReadWrite</span></span>

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

```yaml
Type: String
Parameter Sets: Resize
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed14d-125">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="ed14d-125">-InformationAction</span></span>
<span data-ttu-id="ed14d-126">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="ed14d-126">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ed14d-127">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="ed14d-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ed14d-128">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="ed14d-128">Continue</span></span>
- <span data-ttu-id="ed14d-129">Ignorować</span><span class="sxs-lookup"><span data-stu-id="ed14d-129">Ignore</span></span>
- <span data-ttu-id="ed14d-130">Inquire</span><span class="sxs-lookup"><span data-stu-id="ed14d-130">Inquire</span></span>
- <span data-ttu-id="ed14d-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ed14d-131">SilentlyContinue</span></span>
- <span data-ttu-id="ed14d-132">Przestaw</span><span class="sxs-lookup"><span data-stu-id="ed14d-132">Stop</span></span>
- <span data-ttu-id="ed14d-133">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="ed14d-133">Suspend</span></span>

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

### <span data-ttu-id="ed14d-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ed14d-134">-InformationVariable</span></span>
<span data-ttu-id="ed14d-135">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="ed14d-135">Specifies an information variable.</span></span>

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

### <span data-ttu-id="ed14d-136">-Profile</span><span class="sxs-lookup"><span data-stu-id="ed14d-136">-Profile</span></span>
<span data-ttu-id="ed14d-137">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed14d-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ed14d-138">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="ed14d-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ed14d-139">-ResizedSizeInGB</span><span class="sxs-lookup"><span data-stu-id="ed14d-139">-ResizedSizeInGB</span></span>
<span data-ttu-id="ed14d-140">Określa nowy rozmiar dysku systemu operacyjnego (w gigabajtach).</span><span class="sxs-lookup"><span data-stu-id="ed14d-140">Specifies a new size, in gigabytes, for the operating system disk.</span></span>
<span data-ttu-id="ed14d-141">Rozmiar musi być większy niż bieżący rozmiar.</span><span class="sxs-lookup"><span data-stu-id="ed14d-141">The size must be larger than the current size.</span></span>

```yaml
Type: Int32
Parameter Sets: Resize
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed14d-142">-VM</span><span class="sxs-lookup"><span data-stu-id="ed14d-142">-VM</span></span>
<span data-ttu-id="ed14d-143">Określa maszynę wirtualną, dla której to polecenie cmdlet modyfikuje dysk systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="ed14d-143">Specifies the virtual machine for which this cmdlet modifies the operating system disk.</span></span>
<span data-ttu-id="ed14d-144">Aby uzyskać obiekt maszyny wirtualnej, użyj polecenia cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="ed14d-144">To obtain a virtual machine object, use the **Get-AzureVM** cmdlet.</span></span>

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

### <span data-ttu-id="ed14d-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed14d-145">CommonParameters</span></span>
<span data-ttu-id="ed14d-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed14d-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed14d-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed14d-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed14d-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ed14d-148">INPUTS</span></span>

## <span data-ttu-id="ed14d-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ed14d-149">OUTPUTS</span></span>

## <span data-ttu-id="ed14d-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ed14d-150">NOTES</span></span>

## <span data-ttu-id="ed14d-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ed14d-151">RELATED LINKS</span></span>

[<span data-ttu-id="ed14d-152">Dodaj-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="ed14d-152">Add-AzureVMImage</span></span>](./Add-AzureVMImage.md)

[<span data-ttu-id="ed14d-153">Get-AzureOSDisk</span><span class="sxs-lookup"><span data-stu-id="ed14d-153">Get-AzureOSDisk</span></span>](./Get-AzureOSDisk.md)

[<span data-ttu-id="ed14d-154">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="ed14d-154">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="ed14d-155">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="ed14d-155">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="ed14d-156">Set-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="ed14d-156">Set-AzureDataDisk</span></span>](./Set-AzureDataDisk.md)

[<span data-ttu-id="ed14d-157">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="ed14d-157">Update-AzureVM</span></span>](./Update-AzureVM.md)


