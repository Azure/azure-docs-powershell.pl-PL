---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5CAF2D29-F4AE-4322-AA4F-61267723B955
online version: ''
schema: 2.0.0
ms.openlocfilehash: b2e19ad4b56e5141458f1fe9305a0c33691d024d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054463"
---
# <span data-ttu-id="afb07-101">Remove-AzureVMImageDataDiskConfig</span><span class="sxs-lookup"><span data-stu-id="afb07-101">Remove-AzureVMImageDataDiskConfig</span></span>

## <span data-ttu-id="afb07-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="afb07-102">SYNOPSIS</span></span>
<span data-ttu-id="afb07-103">Usuwa konfigurację dysku danych z obiektu DiskConfigSet.</span><span class="sxs-lookup"><span data-stu-id="afb07-103">Removes the data disk configuration from the DiskConfigSet object.</span></span>

## <span data-ttu-id="afb07-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="afb07-104">SYNTAX</span></span>

### <span data-ttu-id="afb07-105">RemoveByDiskName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="afb07-105">RemoveByDiskName (Default)</span></span>
```
Remove-AzureVMImageDataDiskConfig [-DiskConfig] <VirtualMachineImageDiskConfigSet> [-DataDiskName] <String>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="afb07-106">RemoveByDiskLun</span><span class="sxs-lookup"><span data-stu-id="afb07-106">RemoveByDiskLun</span></span>
```
Remove-AzureVMImageDataDiskConfig [-DiskConfig] <VirtualMachineImageDiskConfigSet> [-Lun] <Int32>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="afb07-107">Opis</span><span class="sxs-lookup"><span data-stu-id="afb07-107">DESCRIPTION</span></span>
<span data-ttu-id="afb07-108">Polecenie cmdlet **Remove-AzureVMImageDataDiskConfig** usuwa konfigurację dysku danych z obiektu **DiskConfigSet** .</span><span class="sxs-lookup"><span data-stu-id="afb07-108">The **Remove-AzureVMImageDataDiskConfig** cmdlet removes the data disk configuration from the **DiskConfigSet** object.</span></span>

## <span data-ttu-id="afb07-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="afb07-109">EXAMPLES</span></span>

### <span data-ttu-id="afb07-110">Przykład 1: Usuwanie konfiguracji dysku danych z obiektu DiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="afb07-110">Example 1: Remove the data disk configuration from the DiskConfigSet object</span></span>
```
PS C:\> $Disk = New-AzureDiskConfigSet
PS C:\> $Disk = Set-AzureDataDiskConfig -DiskConfig $Disk -HostCaching ReadWrite
PS C:\> Remove-AzureVMImageDataDiskConfig -DiskConfig $Disk
```

<span data-ttu-id="afb07-111">W tym przykładzie przedstawiono tworzenie **DiskConfigSet** , jego konfigurację, a następnie Usuwanie dysku danych.</span><span class="sxs-lookup"><span data-stu-id="afb07-111">This example creates a **DiskConfigSet** , configures it, then removes the data disk.</span></span>

## <span data-ttu-id="afb07-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="afb07-112">PARAMETERS</span></span>

### <span data-ttu-id="afb07-113">-Datadyskname</span><span class="sxs-lookup"><span data-stu-id="afb07-113">-DataDiskName</span></span>
<span data-ttu-id="afb07-114">Określa nazwę dysku danych, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="afb07-114">Specifies the name of the data disk that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByDiskName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afb07-115">-DiskConfig</span><span class="sxs-lookup"><span data-stu-id="afb07-115">-DiskConfig</span></span>
<span data-ttu-id="afb07-116">Określa obiekt Konfiguracja dysku, w którym są hermetyzowane obiekty dysk systemu operacyjnego i dysk danych.</span><span class="sxs-lookup"><span data-stu-id="afb07-116">Specifies the disk configuration object that encapsulates the operating system disk and data disk objects.</span></span>

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

### <span data-ttu-id="afb07-117">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="afb07-117">-InformationAction</span></span>
<span data-ttu-id="afb07-118">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="afb07-118">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="afb07-119">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="afb07-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="afb07-120">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="afb07-120">Continue</span></span>
- <span data-ttu-id="afb07-121">Ignorować</span><span class="sxs-lookup"><span data-stu-id="afb07-121">Ignore</span></span>
- <span data-ttu-id="afb07-122">Inquire</span><span class="sxs-lookup"><span data-stu-id="afb07-122">Inquire</span></span>
- <span data-ttu-id="afb07-123">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="afb07-123">SilentlyContinue</span></span>
- <span data-ttu-id="afb07-124">Przestaw</span><span class="sxs-lookup"><span data-stu-id="afb07-124">Stop</span></span>
- <span data-ttu-id="afb07-125">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="afb07-125">Suspend</span></span>

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

### <span data-ttu-id="afb07-126">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="afb07-126">-InformationVariable</span></span>
<span data-ttu-id="afb07-127">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="afb07-127">Specifies an information variable.</span></span>

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

### <span data-ttu-id="afb07-128">-LUN</span><span class="sxs-lookup"><span data-stu-id="afb07-128">-Lun</span></span>
<span data-ttu-id="afb07-129">Określa miejsce, w którym dysk danych jest zainstalowany na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="afb07-129">Specifies the slot where the data drive is mounted in the virtual machine.</span></span>

```yaml
Type: Int32
Parameter Sets: RemoveByDiskLun
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afb07-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afb07-130">CommonParameters</span></span>
<span data-ttu-id="afb07-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afb07-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afb07-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afb07-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afb07-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="afb07-133">INPUTS</span></span>

## <span data-ttu-id="afb07-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="afb07-134">OUTPUTS</span></span>

### <span data-ttu-id="afb07-135">Microsoft. platformy windowsazure. Commands. servicemanagement. model. VirtualMachineImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="afb07-135">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.VirtualMachineImageDiskConfigSet</span></span>

## <span data-ttu-id="afb07-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="afb07-136">NOTES</span></span>

## <span data-ttu-id="afb07-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="afb07-137">RELATED LINKS</span></span>

[<span data-ttu-id="afb07-138">Set-AzureVMImageDataDiskConfig</span><span class="sxs-lookup"><span data-stu-id="afb07-138">Set-AzureVMImageDataDiskConfig</span></span>](./Set-AzureVMImageDataDiskConfig.md)


