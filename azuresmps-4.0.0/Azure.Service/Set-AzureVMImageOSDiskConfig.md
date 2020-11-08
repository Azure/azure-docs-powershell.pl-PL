---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9CD39F1C-D858-4275-A6DE-10901DC962FE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4cb2557b411d46ce718f97ba7939efb4571ce025
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054410"
---
# <span data-ttu-id="b997f-101">Set-AzureVMImageOSDiskConfig</span><span class="sxs-lookup"><span data-stu-id="b997f-101">Set-AzureVMImageOSDiskConfig</span></span>

## <span data-ttu-id="b997f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b997f-102">SYNOPSIS</span></span>
<span data-ttu-id="b997f-103">Ustawia właściwości dysku systemu operacyjnego na obrazie maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b997f-103">Sets the operating system disk properties on a virtual machine image.</span></span>

## <span data-ttu-id="b997f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b997f-104">SYNTAX</span></span>

### <span data-ttu-id="b997f-105">UpdateAzureVMImageParamSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b997f-105">UpdateAzureVMImageParamSet (Default)</span></span>
```
Set-AzureVMImageOSDiskConfig [-DiskConfig] <VirtualMachineImageDiskConfigSet> [[-HostCaching] <String>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b997f-106">AddAzureVMImageParamSet</span><span class="sxs-lookup"><span data-stu-id="b997f-106">AddAzureVMImageParamSet</span></span>
```
Set-AzureVMImageOSDiskConfig [-DiskConfig] <VirtualMachineImageDiskConfigSet> [[-HostCaching] <String>]
 [-MediaLink] <Uri> [-OSState] <String> [-OS] <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="b997f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="b997f-107">DESCRIPTION</span></span>
<span data-ttu-id="b997f-108">Polecenie cmdlet **Set-AzureVMImageOSDiskConfig** ustawia właściwości dysku systemu operacyjnego obrazu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b997f-108">The **Set-AzureVMImageOSDiskConfig** cmdlet sets the operating system disk properties on a virtual machine image.</span></span>

## <span data-ttu-id="b997f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b997f-109">EXAMPLES</span></span>

### <span data-ttu-id="b997f-110">Przykład 1: Ustawianie właściwości dysku systemu operacyjnego w obrazie maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="b997f-110">Example 1: Set the operating system disk properties on a virtual machine image</span></span>
```
PS C:\> $Disk = New-AzureDiskConfigSet
PS C:\> $Disk = Set-AzureOSDiskConfig -DiskConfig $Disk -HostCaching ReadWrite
PS C:\> $Disk = Set-AzureDataDiskConfig -DiskConfig $Disk -Name "Test" -HostCaching "ReadWrite" -LUN 0
PS C:\> Update-AzureVMImage -ImageName "Image2" -Label "Test1" -Description "Test1" -DiskConfigSet $Disk;
```

<span data-ttu-id="b997f-111">W tym przykładzie są ustawiane właściwości dysku systemu operacyjnego obrazu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b997f-111">This example sets the operating system disk properties on a virtual machine image.</span></span>

## <span data-ttu-id="b997f-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b997f-112">PARAMETERS</span></span>

### <span data-ttu-id="b997f-113">-DiskConfig</span><span class="sxs-lookup"><span data-stu-id="b997f-113">-DiskConfig</span></span>
<span data-ttu-id="b997f-114">Określa obiekt Konfiguracja dysku, w którym są hermetyzowane obiekty dysk systemu operacyjnego i dysk danych.</span><span class="sxs-lookup"><span data-stu-id="b997f-114">Specifies the disk configuration object that encapsulates the operating system disk and Data Disk objects.</span></span>

```yaml
Type: VirtualMachineImageDiskConfigSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b997f-115">-HostCaching</span><span class="sxs-lookup"><span data-stu-id="b997f-115">-HostCaching</span></span>
<span data-ttu-id="b997f-116">Określa atrybut pamięć podręczna hosta dla dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="b997f-116">Specifies the host cache attribute for the operating system disk.</span></span>

<span data-ttu-id="b997f-117">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="b997f-117">Valid values are:</span></span>

<span data-ttu-id="b997f-118">--ReadOnly--ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b997f-118">--ReadOnly --ReadWrite</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b997f-119">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="b997f-119">-InformationAction</span></span>
<span data-ttu-id="b997f-120">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="b997f-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b997f-121">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="b997f-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b997f-122">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="b997f-122">Continue</span></span>
- <span data-ttu-id="b997f-123">Ignorować</span><span class="sxs-lookup"><span data-stu-id="b997f-123">Ignore</span></span>
- <span data-ttu-id="b997f-124">Inquire</span><span class="sxs-lookup"><span data-stu-id="b997f-124">Inquire</span></span>
- <span data-ttu-id="b997f-125">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b997f-125">SilentlyContinue</span></span>
- <span data-ttu-id="b997f-126">Przestaw</span><span class="sxs-lookup"><span data-stu-id="b997f-126">Stop</span></span>
- <span data-ttu-id="b997f-127">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="b997f-127">Suspend</span></span>

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

### <span data-ttu-id="b997f-128">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b997f-128">-InformationVariable</span></span>
<span data-ttu-id="b997f-129">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="b997f-129">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b997f-130">-MediaLink</span><span class="sxs-lookup"><span data-stu-id="b997f-130">-MediaLink</span></span>
<span data-ttu-id="b997f-131">Określa identyfikator URI lokalizacji, w której jest tworzony nowy wirtualny dysk twardy po dodaniu nowego dysku danych.</span><span class="sxs-lookup"><span data-stu-id="b997f-131">Specifies the URI of the location where the new virtual hard drive is created when the new data disk is added.</span></span>

```yaml
Type: Uri
Parameter Sets: AddAzureVMImageParamSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b997f-132">-OS</span><span class="sxs-lookup"><span data-stu-id="b997f-132">-OS</span></span>
<span data-ttu-id="b997f-133">Określa system operacyjny konfiguracji dysku.</span><span class="sxs-lookup"><span data-stu-id="b997f-133">Specifies the operating system of the disk configuration.</span></span>

<span data-ttu-id="b997f-134">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="b997f-134">Valid values are:</span></span>

- <span data-ttu-id="b997f-135">Microsoft</span><span class="sxs-lookup"><span data-stu-id="b997f-135">Windows</span></span>
- <span data-ttu-id="b997f-136">Linux</span><span class="sxs-lookup"><span data-stu-id="b997f-136">Linux</span></span>

```yaml
Type: String
Parameter Sets: AddAzureVMImageParamSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b997f-137">-OSState</span><span class="sxs-lookup"><span data-stu-id="b997f-137">-OSState</span></span>
<span data-ttu-id="b997f-138">Określa stan systemu operacyjnego dla obrazu maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="b997f-138">Specifies the operating system state for virtual machine image</span></span>

<span data-ttu-id="b997f-139">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="b997f-139">Valid values are:</span></span>

- <span data-ttu-id="b997f-140">Uogólniony</span><span class="sxs-lookup"><span data-stu-id="b997f-140">Generalized</span></span>
- <span data-ttu-id="b997f-141">Przeznaczona</span><span class="sxs-lookup"><span data-stu-id="b997f-141">Specialized</span></span>

<span data-ttu-id="b997f-142">Użycie tego parametru wskazuje, że zamierzasz przechwycić obraz maszyny wirtualnej na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="b997f-142">The use of this parameter indicates your intent to capture the virtual machine image to Azure.</span></span>

```yaml
Type: String
Parameter Sets: AddAzureVMImageParamSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b997f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b997f-143">CommonParameters</span></span>
<span data-ttu-id="b997f-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b997f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b997f-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b997f-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b997f-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b997f-146">INPUTS</span></span>

## <span data-ttu-id="b997f-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b997f-147">OUTPUTS</span></span>

### <span data-ttu-id="b997f-148">Microsoft. platformy windowsazure. Commands. servicemanagement. model. VirtualMachineImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="b997f-148">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.VirtualMachineImageDiskConfigSet</span></span>

## <span data-ttu-id="b997f-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b997f-149">NOTES</span></span>

## <span data-ttu-id="b997f-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b997f-150">RELATED LINKS</span></span>

[<span data-ttu-id="b997f-151">Remove-AzureVMImageOSDiskConfig</span><span class="sxs-lookup"><span data-stu-id="b997f-151">Remove-AzureVMImageOSDiskConfig</span></span>](./Remove-AzureVMImageOSDiskConfig.md)


