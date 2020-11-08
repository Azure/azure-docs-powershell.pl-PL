---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: ACBE32E5-AA8C-43CA-9FF4-4B59906C6B85
online version: ''
schema: 2.0.0
ms.openlocfilehash: 45d18179fba41d39456a11575fc2041ad4be8557
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055496"
---
# <span data-ttu-id="c8d1e-101">Get-AzureVMImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="c8d1e-101">Get-AzureVMImageDiskConfigSet</span></span>

## <span data-ttu-id="c8d1e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c8d1e-102">SYNOPSIS</span></span>
<span data-ttu-id="c8d1e-103">Pobiera obiekt zestawu konfiguracji dysku z kontekstu obrazu wejściowego.</span><span class="sxs-lookup"><span data-stu-id="c8d1e-103">Gets a disk configuration set object from the input image context.</span></span>

## <span data-ttu-id="c8d1e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c8d1e-104">SYNTAX</span></span>

```
Get-AzureVMImageDiskConfigSet [[-ImageContext] <OSImageContext>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="c8d1e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c8d1e-105">DESCRIPTION</span></span>
<span data-ttu-id="c8d1e-106">Polecenie cmdlet **Get-AzureVMImageDiskConfigSet** pobiera obiekt Set konfiguracji dysku z kontekstu obrazu wejściowego.</span><span class="sxs-lookup"><span data-stu-id="c8d1e-106">The **Get-AzureVMImageDiskConfigSet** cmdlet gets a disk configuration set object from the input image context.</span></span>

## <span data-ttu-id="c8d1e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c8d1e-107">EXAMPLES</span></span>

### <span data-ttu-id="c8d1e-108">Przykład 1: uzyskiwanie obiektu zestawu konfiguracji dysku z maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="c8d1e-108">Example 1: Get a disk configuration set object from a virtual machine</span></span>
```
PS C:\> Get-AzureVMImage -ImageName $Img | Get-AzureVMImageDiskConfigSet
```

<span data-ttu-id="c8d1e-109">To polecenie pobiera obiekt zestawu konfiguracji dysku z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c8d1e-109">This command gets a disk configuration set object from a virtual machine.</span></span>

## <span data-ttu-id="c8d1e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c8d1e-110">PARAMETERS</span></span>

### <span data-ttu-id="c8d1e-111">-ImageContext</span><span class="sxs-lookup"><span data-stu-id="c8d1e-111">-ImageContext</span></span>
<span data-ttu-id="c8d1e-112">Określa kontekst obrazu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c8d1e-112">Specifies the virtual machine image context.</span></span>

```yaml
Type: OSImageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c8d1e-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="c8d1e-113">-InformationAction</span></span>
<span data-ttu-id="c8d1e-114">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="c8d1e-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c8d1e-115">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="c8d1e-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c8d1e-116">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="c8d1e-116">Continue</span></span>
- <span data-ttu-id="c8d1e-117">Ignorować</span><span class="sxs-lookup"><span data-stu-id="c8d1e-117">Ignore</span></span>
- <span data-ttu-id="c8d1e-118">Inquire</span><span class="sxs-lookup"><span data-stu-id="c8d1e-118">Inquire</span></span>
- <span data-ttu-id="c8d1e-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c8d1e-119">SilentlyContinue</span></span>
- <span data-ttu-id="c8d1e-120">Przestaw</span><span class="sxs-lookup"><span data-stu-id="c8d1e-120">Stop</span></span>
- <span data-ttu-id="c8d1e-121">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="c8d1e-121">Suspend</span></span>

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

### <span data-ttu-id="c8d1e-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c8d1e-122">-InformationVariable</span></span>
<span data-ttu-id="c8d1e-123">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="c8d1e-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="c8d1e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8d1e-124">CommonParameters</span></span>
<span data-ttu-id="c8d1e-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8d1e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8d1e-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8d1e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8d1e-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c8d1e-127">INPUTS</span></span>

## <span data-ttu-id="c8d1e-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c8d1e-128">OUTPUTS</span></span>

### <span data-ttu-id="c8d1e-129">Microsoft. platformy windowsazure. Commands. servicemanagement. model. VirtualMachineImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="c8d1e-129">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.VirtualMachineImageDiskConfigSet</span></span>

## <span data-ttu-id="c8d1e-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c8d1e-130">NOTES</span></span>

## <span data-ttu-id="c8d1e-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c8d1e-131">RELATED LINKS</span></span>

[<span data-ttu-id="c8d1e-132">Nowe — AzureVMImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="c8d1e-132">New-AzureVMImageDiskConfigSet</span></span>](./New-AzureVMImageDiskConfigSet.md)

[<span data-ttu-id="c8d1e-133">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="c8d1e-133">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)


