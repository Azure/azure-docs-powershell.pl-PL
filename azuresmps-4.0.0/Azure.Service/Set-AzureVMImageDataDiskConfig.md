---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 6C7CB0AE-C788-4E6F-AD48-E30B547A2269
online version: ''
schema: 2.0.0
ms.openlocfilehash: a7512ef446227742c2a3564c5f3e5f38f1e2ccce
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054402"
---
# <span data-ttu-id="d7202-101">Set-AzureVMImageDataDiskConfig</span><span class="sxs-lookup"><span data-stu-id="d7202-101">Set-AzureVMImageDataDiskConfig</span></span>

## <span data-ttu-id="d7202-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d7202-102">SYNOPSIS</span></span>
<span data-ttu-id="d7202-103">Ustawia właściwości dysku danych w obrazie maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d7202-103">Sets the Data Disk properties on the virtual machine image.</span></span>

## <span data-ttu-id="d7202-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d7202-104">SYNTAX</span></span>

### <span data-ttu-id="d7202-105">UpdateAzureVMImageParamSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d7202-105">UpdateAzureVMImageParamSet (Default)</span></span>
```
Set-AzureVMImageDataDiskConfig [-DiskConfig] <VirtualMachineImageDiskConfigSet> [-DataDiskName] <String>
 [-Lun] <Int32> [-HostCaching] <String> [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="d7202-106">AddAzureVMImageParamSet</span><span class="sxs-lookup"><span data-stu-id="d7202-106">AddAzureVMImageParamSet</span></span>
```
Set-AzureVMImageDataDiskConfig [-DiskConfig] <VirtualMachineImageDiskConfigSet> [-Lun] <Int32>
 [-HostCaching] <String> [-MediaLink] <Uri> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="d7202-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d7202-107">DESCRIPTION</span></span>
<span data-ttu-id="d7202-108">Polecenie cmdlet **Set-AzureVMImageDataDiskConfig** ustawia właściwości dysku danych w obrazie maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d7202-108">The **Set-AzureVMImageDataDiskConfig** cmdlet sets the Data Disk properties on the virtual machine image.</span></span>

## <span data-ttu-id="d7202-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d7202-109">EXAMPLES</span></span>

### <span data-ttu-id="d7202-110">Przykład 1: Ustawianie właściwości dysku danych w obrazie maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="d7202-110">Example 1: Set Data Disk properties on a virtual machine image</span></span>
```
PS C:\> $Disk = New-AzureDiskConfigSet
PS C:\> $Disk = Set-AzureOSDiskConfig -DiskConfig $Disk -HostCaching ReadWrite
PS C:\> $Disk = Set-AzureDataDiskConfig -DiskConfig $Disk -Name "Test" -HostCaching "ReadWrite" -LUN 0
PS C:\> Update-AzureVMImage -ImageName "Image2" -Label "Test1" -Description "Test1" -DiskConfigSet $Disk;
```

<span data-ttu-id="d7202-111">To polecenie ustawia właściwości dysku danych na maszynie wirtualnej, a następnie aktualizuje obraz maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d7202-111">This command sets data disk properties on a virtual machine then updates the virtual machine image.</span></span>

## <span data-ttu-id="d7202-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d7202-112">PARAMETERS</span></span>

### <span data-ttu-id="d7202-113">-Datadyskname</span><span class="sxs-lookup"><span data-stu-id="d7202-113">-DataDiskName</span></span>
<span data-ttu-id="d7202-114">Określa nazwę dysku danych, który jest konfigurowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7202-114">Specifies the name of the data disk that this cmdlet configures.</span></span>

```yaml
Type: String
Parameter Sets: UpdateAzureVMImageParamSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7202-115">-DiskConfig</span><span class="sxs-lookup"><span data-stu-id="d7202-115">-DiskConfig</span></span>
<span data-ttu-id="d7202-116">Określa obiekt Konfiguracja dysku, w którym są hermetyzowane obiekty dysk systemu operacyjnego i dysk danych.</span><span class="sxs-lookup"><span data-stu-id="d7202-116">Specifies the disk configuration object that encapsulates the operating system disk and Data Disk objects.</span></span>

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

### <span data-ttu-id="d7202-117">-HostCaching</span><span class="sxs-lookup"><span data-stu-id="d7202-117">-HostCaching</span></span>
<span data-ttu-id="d7202-118">Określa atrybut pamięć podręczna hosta dla dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="d7202-118">Specifies the host cache attribute for the operating system disk.</span></span>

<span data-ttu-id="d7202-119">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="d7202-119">Valid values are:</span></span>

<span data-ttu-id="d7202-120">--ReadOnly--ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d7202-120">--ReadOnly --ReadWrite</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7202-121">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="d7202-121">-InformationAction</span></span>
<span data-ttu-id="d7202-122">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="d7202-122">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="d7202-123">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="d7202-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d7202-124">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="d7202-124">Continue</span></span>
- <span data-ttu-id="d7202-125">Ignorować</span><span class="sxs-lookup"><span data-stu-id="d7202-125">Ignore</span></span>
- <span data-ttu-id="d7202-126">Inquire</span><span class="sxs-lookup"><span data-stu-id="d7202-126">Inquire</span></span>
- <span data-ttu-id="d7202-127">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="d7202-127">SilentlyContinue</span></span>
- <span data-ttu-id="d7202-128">Przestaw</span><span class="sxs-lookup"><span data-stu-id="d7202-128">Stop</span></span>
- <span data-ttu-id="d7202-129">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="d7202-129">Suspend</span></span>

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

### <span data-ttu-id="d7202-130">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="d7202-130">-InformationVariable</span></span>
<span data-ttu-id="d7202-131">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="d7202-131">Specifies an information variable.</span></span>

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

### <span data-ttu-id="d7202-132">-LUN</span><span class="sxs-lookup"><span data-stu-id="d7202-132">-Lun</span></span>
<span data-ttu-id="d7202-133">Określa miejsce, w którym dysk danych jest zainstalowany na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d7202-133">Specifies the slot where the data drive is mounted in the virtual machine.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7202-134">-MediaLink</span><span class="sxs-lookup"><span data-stu-id="d7202-134">-MediaLink</span></span>
<span data-ttu-id="d7202-135">Określa identyfikator URI lokalizacji, w której jest tworzony nowy wirtualny dysk twardy po dodaniu nowego dysku danych.</span><span class="sxs-lookup"><span data-stu-id="d7202-135">Specifies the URI of the location where the new virtual hard drive is created when the new data disk is added.</span></span>

```yaml
Type: Uri
Parameter Sets: AddAzureVMImageParamSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7202-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7202-136">CommonParameters</span></span>
<span data-ttu-id="d7202-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7202-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7202-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7202-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7202-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d7202-139">INPUTS</span></span>

## <span data-ttu-id="d7202-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d7202-140">OUTPUTS</span></span>

### <span data-ttu-id="d7202-141">Microsoft. platformy windowsazure. Commands. servicemanagement. model. VirtualMachineImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="d7202-141">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.VirtualMachineImageDiskConfigSet</span></span>

## <span data-ttu-id="d7202-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d7202-142">NOTES</span></span>

## <span data-ttu-id="d7202-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d7202-143">RELATED LINKS</span></span>

[<span data-ttu-id="d7202-144">Remove-AzureVMImageDataDiskConfig</span><span class="sxs-lookup"><span data-stu-id="d7202-144">Remove-AzureVMImageDataDiskConfig</span></span>](./Remove-AzureVMImageDataDiskConfig.md)


