---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: F420A47F-D036-4B31-AA59-97CFC9C79E75
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4a53d0821832b29f0f1f6a0b2ab5f1353e3331a3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055164"
---
# <span data-ttu-id="dbf27-101">New-AzureVMImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="dbf27-101">New-AzureVMImageDiskConfigSet</span></span>

## <span data-ttu-id="dbf27-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dbf27-102">SYNOPSIS</span></span>
<span data-ttu-id="dbf27-103">Tworzy obiekt zestawu konfiguracyjnego dysku.</span><span class="sxs-lookup"><span data-stu-id="dbf27-103">Creates a disk configuration set object.</span></span>

## <span data-ttu-id="dbf27-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dbf27-104">SYNTAX</span></span>

```
New-AzureVMImageDiskConfigSet [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="dbf27-105">Opis</span><span class="sxs-lookup"><span data-stu-id="dbf27-105">DESCRIPTION</span></span>
<span data-ttu-id="dbf27-106">Polecenie cmdlet **New-AzureVMImageDiskConfigSet** tworzy obiekt zestawu konfiguracyjnego dysku przekazany do polecenia cmdlet aktualizacji obrazu.</span><span class="sxs-lookup"><span data-stu-id="dbf27-106">The **New-AzureVMImageDiskConfigSet** cmdlet creates a disk configuration set object that is passed to the image update cmdlet.</span></span>
<span data-ttu-id="dbf27-107">Hermetyzuje to OSDiskConfig oraz obiekt DataDiskConfig.</span><span class="sxs-lookup"><span data-stu-id="dbf27-107">It encapsulates the OSDiskConfig and the DataDiskConfig object.</span></span>
<span data-ttu-id="dbf27-108">Użyj poleceń cmdlet **Set-AzureVMImageOSDiskConfig** i **Set-AzureVMImageDataDiskConfig** w celu ustawienia dysku systemu operacyjnego i właściwości dysku danych dla obrazu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="dbf27-108">Use the **Set-AzureVMImageOSDiskConfig** and **Set-AzureVMImageDataDiskConfig** cmdlets to set the OS Disk and Data Disk properties for the virtual machine image.</span></span>

## <span data-ttu-id="dbf27-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dbf27-109">EXAMPLES</span></span>

### <span data-ttu-id="dbf27-110">Przykład 1. Tworzenie obiektu zestawu konfiguracji dysku</span><span class="sxs-lookup"><span data-stu-id="dbf27-110">Example 1: Create a disk configuration set object</span></span>
```
PS C:\> $Disk = New-AzureDiskConfigSet
PS C:\> $Disk = Set-AzureOSDiskConfig -DiskConfig $Disk -HostCaching ReadWrite
PS C:\> $Disk = Set-AzureDataDiskConfig -DiskConfig $Disk -Name "Test" -HostCaching "ReadWrite" -LUN 0
PS C:\> Update-AzureVMImage -ImageName "Image2" -Label "Test1" -Description "Test1" -DiskConfigSet $Disk;
```

<span data-ttu-id="dbf27-111">To polecenie tworzy obiekt zestawu konfiguracyjnego dysku i zapisuje wyniki w zmiennej o nazwie $Disk.</span><span class="sxs-lookup"><span data-stu-id="dbf27-111">This command creates a disk configuration set object and stores the results in the variable named $Disk.</span></span>
<span data-ttu-id="dbf27-112">Po utworzeniu konfiguracji dysku jest ona używana do ustawiania OSDiskConfig i DataDiskConfig.</span><span class="sxs-lookup"><span data-stu-id="dbf27-112">After the disk configuration is created, it is used to set the OSDiskConfig and DataDiskConfig.</span></span>
<span data-ttu-id="dbf27-113">Następnie maszyna wirtualna jest aktualizowana przy użyciu konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="dbf27-113">Then the virtual machine is updated with the configuration.</span></span>

## <span data-ttu-id="dbf27-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dbf27-114">PARAMETERS</span></span>

### <span data-ttu-id="dbf27-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="dbf27-115">-InformationAction</span></span>
<span data-ttu-id="dbf27-116">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="dbf27-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="dbf27-117">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="dbf27-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="dbf27-118">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="dbf27-118">Continue</span></span>
- <span data-ttu-id="dbf27-119">Ignorować</span><span class="sxs-lookup"><span data-stu-id="dbf27-119">Ignore</span></span>
- <span data-ttu-id="dbf27-120">Inquire</span><span class="sxs-lookup"><span data-stu-id="dbf27-120">Inquire</span></span>
- <span data-ttu-id="dbf27-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="dbf27-121">SilentlyContinue</span></span>
- <span data-ttu-id="dbf27-122">Przestaw</span><span class="sxs-lookup"><span data-stu-id="dbf27-122">Stop</span></span>
- <span data-ttu-id="dbf27-123">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="dbf27-123">Suspend</span></span>

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

### <span data-ttu-id="dbf27-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="dbf27-124">-InformationVariable</span></span>
<span data-ttu-id="dbf27-125">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="dbf27-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="dbf27-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbf27-126">CommonParameters</span></span>
<span data-ttu-id="dbf27-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbf27-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbf27-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbf27-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbf27-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dbf27-129">INPUTS</span></span>

## <span data-ttu-id="dbf27-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dbf27-130">OUTPUTS</span></span>

### <span data-ttu-id="dbf27-131">Microsoft. platformy windowsazure. Commands. servicemanagement. model. VirtualMachineImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="dbf27-131">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.VirtualMachineImageDiskConfigSet</span></span>

## <span data-ttu-id="dbf27-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dbf27-132">NOTES</span></span>

## <span data-ttu-id="dbf27-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dbf27-133">RELATED LINKS</span></span>

[<span data-ttu-id="dbf27-134">Get-AzureVMImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="dbf27-134">Get-AzureVMImageDiskConfigSet</span></span>](./Get-AzureVMImageDiskConfigSet.md)

[<span data-ttu-id="dbf27-135">Set-AzureVMImageOSDiskConfig</span><span class="sxs-lookup"><span data-stu-id="dbf27-135">Set-AzureVMImageOSDiskConfig</span></span>](./Set-AzureVMImageOSDiskConfig.md)

[<span data-ttu-id="dbf27-136">Set-AzureVMImageDataDiskConfig</span><span class="sxs-lookup"><span data-stu-id="dbf27-136">Set-AzureVMImageDataDiskConfig</span></span>](./Set-AzureVMImageDataDiskConfig.md)


