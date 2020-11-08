---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8A269A53-8FB2-4D4E-8FBB-A84BE658F75F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 002834bda663dda1c9ebe5f24bb0f1aa0007655c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055298"
---
# <span data-ttu-id="82f55-101">Get-AzureOSDisk</span><span class="sxs-lookup"><span data-stu-id="82f55-101">Get-AzureOSDisk</span></span>

## <span data-ttu-id="82f55-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="82f55-102">SYNOPSIS</span></span>
<span data-ttu-id="82f55-103">Pobiera dysk z systemem operacyjnym maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="82f55-103">Gets the operating system disk of an Azure virtual machine.</span></span>

## <span data-ttu-id="82f55-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="82f55-104">SYNTAX</span></span>

```
Get-AzureOSDisk -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="82f55-105">Opis</span><span class="sxs-lookup"><span data-stu-id="82f55-105">DESCRIPTION</span></span>
<span data-ttu-id="82f55-106">Polecenie cmdlet **Get-AzureOSDisk** pobiera dysk z systemem operacyjnym maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="82f55-106">The **Get-AzureOSDisk** cmdlet gets the operating system disk of an Azure virtual machine.</span></span>

## <span data-ttu-id="82f55-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="82f55-107">EXAMPLES</span></span>

### <span data-ttu-id="82f55-108">Przykład 1: uzyskiwanie dysku z systemem operacyjnym</span><span class="sxs-lookup"><span data-stu-id="82f55-108">Example 1: Get an operating system disk</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine02" | Get-AzureOSDisk
```

<span data-ttu-id="82f55-109">To polecenie pobiera maszynę wirtualną o nazwie VirtualMachine02 w usłudze o nazwie ContosoService przy użyciu polecenia cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="82f55-109">This command gets the virtual machine named VirtualMachine02 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="82f55-110">Polecenie przekazanie maszyny wirtualnej do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="82f55-110">The command passes the virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="82f55-111">Bieżące polecenie cmdlet umożliwia pobieranie dysku z systemem operacyjnym tej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="82f55-111">The current cmdlet gets the operating system disk of that virtual machine.</span></span>

## <span data-ttu-id="82f55-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="82f55-112">PARAMETERS</span></span>

### <span data-ttu-id="82f55-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="82f55-113">-InformationAction</span></span>
<span data-ttu-id="82f55-114">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="82f55-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="82f55-115">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="82f55-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="82f55-116">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="82f55-116">Continue</span></span>
- <span data-ttu-id="82f55-117">Ignorować</span><span class="sxs-lookup"><span data-stu-id="82f55-117">Ignore</span></span>
- <span data-ttu-id="82f55-118">Inquire</span><span class="sxs-lookup"><span data-stu-id="82f55-118">Inquire</span></span>
- <span data-ttu-id="82f55-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="82f55-119">SilentlyContinue</span></span>
- <span data-ttu-id="82f55-120">Przestaw</span><span class="sxs-lookup"><span data-stu-id="82f55-120">Stop</span></span>
- <span data-ttu-id="82f55-121">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="82f55-121">Suspend</span></span>

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

### <span data-ttu-id="82f55-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="82f55-122">-InformationVariable</span></span>
<span data-ttu-id="82f55-123">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="82f55-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="82f55-124">-Profile</span><span class="sxs-lookup"><span data-stu-id="82f55-124">-Profile</span></span>
<span data-ttu-id="82f55-125">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82f55-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="82f55-126">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="82f55-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="82f55-127">-VM</span><span class="sxs-lookup"><span data-stu-id="82f55-127">-VM</span></span>
<span data-ttu-id="82f55-128">Umożliwia określenie maszyny wirtualnej, dla której to polecenie cmdlet pobiera dysk z systemem operacyjnym.</span><span class="sxs-lookup"><span data-stu-id="82f55-128">Specifies the virtual machine for which this cmdlet gets the operating system disk.</span></span>
<span data-ttu-id="82f55-129">Aby uzyskać obiekt maszyny wirtualnej, użyj polecenia cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="82f55-129">To obtain a virtual machine object, use the **Get-AzureVM** cmdlet.</span></span>

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

### <span data-ttu-id="82f55-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82f55-130">CommonParameters</span></span>
<span data-ttu-id="82f55-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82f55-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82f55-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82f55-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82f55-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="82f55-133">INPUTS</span></span>

## <span data-ttu-id="82f55-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="82f55-134">OUTPUTS</span></span>

## <span data-ttu-id="82f55-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="82f55-135">NOTES</span></span>

## <span data-ttu-id="82f55-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="82f55-136">RELATED LINKS</span></span>

[<span data-ttu-id="82f55-137">Get-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="82f55-137">Get-AzureDataDisk</span></span>](./Get-AzureDataDisk.md)

[<span data-ttu-id="82f55-138">Set-AzureOSDisk</span><span class="sxs-lookup"><span data-stu-id="82f55-138">Set-AzureOSDisk</span></span>](./Set-AzureOSDisk.md)


