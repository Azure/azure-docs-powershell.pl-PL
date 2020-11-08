---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 734C98C1-0EF7-43E5-AB6F-A1C625FF9CE7
online version: ''
schema: 2.0.0
ms.openlocfilehash: f9713c8b39fa4e2842cdf1cfcbfe962ead86d729
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054501"
---
# <span data-ttu-id="f976a-101">Get-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="f976a-101">Get-AzureVMAccessExtension</span></span>

## <span data-ttu-id="f976a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f976a-102">SYNOPSIS</span></span>
<span data-ttu-id="f976a-103">Pobiera rozszerzenie VMAccess zastosowane na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f976a-103">Gets the VMAccess extension applied on a virtual machine.</span></span>

## <span data-ttu-id="f976a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f976a-104">SYNTAX</span></span>

```
Get-AzureVMAccessExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="f976a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f976a-105">DESCRIPTION</span></span>
<span data-ttu-id="f976a-106">Polecenie cmdlet **Get-AzureVMAccessExtension** pobiera rozszerzenie VMAccess zastosowane na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f976a-106">The **Get-AzureVMAccessExtension** cmdlet gets the VMAccess extension applied on a virtual machine.</span></span>

## <span data-ttu-id="f976a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f976a-107">EXAMPLES</span></span>

### <span data-ttu-id="f976a-108">Przykład 1: uzyskiwanie rozszerzenia VMAccess dla maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="f976a-108">Example 1: Get the VMAccess extension for a virtual machine</span></span>
```
PS C:\> Get-AzureVMAccessExtension -VM $VM;
```

<span data-ttu-id="f976a-109">To polecenie uzyskuje rozszerzenie VMAccess dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f976a-109">This command gets the VMAccess extension for a virtual machine.</span></span>

## <span data-ttu-id="f976a-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f976a-110">PARAMETERS</span></span>

### <span data-ttu-id="f976a-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="f976a-111">-InformationAction</span></span>
<span data-ttu-id="f976a-112">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="f976a-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="f976a-113">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="f976a-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f976a-114">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="f976a-114">Continue</span></span>
- <span data-ttu-id="f976a-115">Ignorować</span><span class="sxs-lookup"><span data-stu-id="f976a-115">Ignore</span></span>
- <span data-ttu-id="f976a-116">Inquire</span><span class="sxs-lookup"><span data-stu-id="f976a-116">Inquire</span></span>
- <span data-ttu-id="f976a-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="f976a-117">SilentlyContinue</span></span>
- <span data-ttu-id="f976a-118">Przestaw</span><span class="sxs-lookup"><span data-stu-id="f976a-118">Stop</span></span>
- <span data-ttu-id="f976a-119">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="f976a-119">Suspend</span></span>

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

### <span data-ttu-id="f976a-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="f976a-120">-InformationVariable</span></span>
<span data-ttu-id="f976a-121">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="f976a-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="f976a-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="f976a-122">-Profile</span></span>
<span data-ttu-id="f976a-123">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f976a-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f976a-124">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="f976a-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f976a-125">-VM</span><span class="sxs-lookup"><span data-stu-id="f976a-125">-VM</span></span>
<span data-ttu-id="f976a-126">Określa trwały obiekt maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f976a-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="f976a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f976a-127">CommonParameters</span></span>
<span data-ttu-id="f976a-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f976a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f976a-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f976a-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f976a-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f976a-130">INPUTS</span></span>

## <span data-ttu-id="f976a-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f976a-131">OUTPUTS</span></span>

## <span data-ttu-id="f976a-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f976a-132">NOTES</span></span>

## <span data-ttu-id="f976a-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f976a-133">RELATED LINKS</span></span>

[<span data-ttu-id="f976a-134">Remove-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="f976a-134">Remove-AzureVMAccessExtension</span></span>](./Remove-AzureVMAccessExtension.md)

[<span data-ttu-id="f976a-135">Set-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="f976a-135">Set-AzureVMAccessExtension</span></span>](./Set-AzureVMAccessExtension.md)


