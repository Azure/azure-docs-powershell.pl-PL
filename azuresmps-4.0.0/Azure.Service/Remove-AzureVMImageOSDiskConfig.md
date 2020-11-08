---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1E1F98E9-FC45-4BEF-90F6-A21D7DB7C82F
online version: ''
schema: 2.0.0
ms.openlocfilehash: eac6db4400e5c51f295e0bbf549117ffdbc97644
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055411"
---
# <span data-ttu-id="829dc-101">Remove-AzureVMImageOSDiskConfig</span><span class="sxs-lookup"><span data-stu-id="829dc-101">Remove-AzureVMImageOSDiskConfig</span></span>

## <span data-ttu-id="829dc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="829dc-102">SYNOPSIS</span></span>
<span data-ttu-id="829dc-103">Usuwa konfigurację dysku systemu operacyjnego z obiektu DiskConfigSet.</span><span class="sxs-lookup"><span data-stu-id="829dc-103">Removes the operating system disk configuration from the DiskConfigSet object.</span></span>

## <span data-ttu-id="829dc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="829dc-104">SYNTAX</span></span>

```
Remove-AzureVMImageOSDiskConfig [-DiskConfig] <VirtualMachineImageDiskConfigSet>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="829dc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="829dc-105">DESCRIPTION</span></span>
<span data-ttu-id="829dc-106">Polecenie cmdlet **Remove-AzureVMImageOSDiskConfig** usuwa konfigurację dysku systemu operacyjnego z obiektu DiskConfigSet.</span><span class="sxs-lookup"><span data-stu-id="829dc-106">The **Remove-AzureVMImageOSDiskConfig** cmdlet removes the operating system disk configuration from the DiskConfigSet object.</span></span>

## <span data-ttu-id="829dc-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="829dc-107">EXAMPLES</span></span>

### <span data-ttu-id="829dc-108">Przykład 1: Usunięcie konfiguracji dysku systemu operacyjnego z DiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="829dc-108">Example 1: Remove the operating system disk configuration from a DiskConfigSet</span></span>
```
PS C:\> $Disk = New-AzureDiskConfigSet
PS C:\> $Disk = Set-AzureOSDiskConfig -DiskConfig $Disk -HostCaching ReadWrite
PS C:\> Remove-AzureVMImageOSDiskConfig -DiskConfig $Disk
```

<span data-ttu-id="829dc-109">To polecenie usuwa konfigurację dysku systemu operacyjnego z obiektu DiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="829dc-109">This command removes the operating system disk configuration from the DiskConfigSet object</span></span>

## <span data-ttu-id="829dc-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="829dc-110">PARAMETERS</span></span>

### <span data-ttu-id="829dc-111">-DiskConfig</span><span class="sxs-lookup"><span data-stu-id="829dc-111">-DiskConfig</span></span>
<span data-ttu-id="829dc-112">Określa obiekt Konfiguracja dysku, w którym są hermetyzowane obiekty dysk systemu operacyjnego i dysk danych.</span><span class="sxs-lookup"><span data-stu-id="829dc-112">Specifies the disk configuration object that encapsulates the operating system disk and Data Disk objects.</span></span>

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

### <span data-ttu-id="829dc-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="829dc-113">-InformationAction</span></span>
<span data-ttu-id="829dc-114">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="829dc-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="829dc-115">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="829dc-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="829dc-116">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="829dc-116">Continue</span></span>
- <span data-ttu-id="829dc-117">Ignorować</span><span class="sxs-lookup"><span data-stu-id="829dc-117">Ignore</span></span>
- <span data-ttu-id="829dc-118">Inquire</span><span class="sxs-lookup"><span data-stu-id="829dc-118">Inquire</span></span>
- <span data-ttu-id="829dc-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="829dc-119">SilentlyContinue</span></span>
- <span data-ttu-id="829dc-120">Przestaw</span><span class="sxs-lookup"><span data-stu-id="829dc-120">Stop</span></span>
- <span data-ttu-id="829dc-121">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="829dc-121">Suspend</span></span>

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

### <span data-ttu-id="829dc-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="829dc-122">-InformationVariable</span></span>
<span data-ttu-id="829dc-123">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="829dc-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="829dc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="829dc-124">CommonParameters</span></span>
<span data-ttu-id="829dc-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="829dc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="829dc-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="829dc-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="829dc-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="829dc-127">INPUTS</span></span>

## <span data-ttu-id="829dc-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="829dc-128">OUTPUTS</span></span>

### <span data-ttu-id="829dc-129">Microsoft. platformy windowsazure. Commands. servicemanagement. model. VirtualMachineImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="829dc-129">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.VirtualMachineImageDiskConfigSet</span></span>

## <span data-ttu-id="829dc-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="829dc-130">NOTES</span></span>

## <span data-ttu-id="829dc-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="829dc-131">RELATED LINKS</span></span>

[<span data-ttu-id="829dc-132">Set-AzureVMImageOSDiskConfig</span><span class="sxs-lookup"><span data-stu-id="829dc-132">Set-AzureVMImageOSDiskConfig</span></span>](./Set-AzureVMImageOSDiskConfig.md)


