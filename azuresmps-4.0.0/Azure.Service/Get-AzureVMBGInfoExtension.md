---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: E4CB958B-AC85-4036-A6D6-002FAF40BB66
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5e74be3310b895ef4c941a59541a64f9c6d1b279
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054498"
---
# <span data-ttu-id="95a7d-101">Get-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="95a7d-101">Get-AzureVMBGInfoExtension</span></span>

## <span data-ttu-id="95a7d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="95a7d-102">SYNOPSIS</span></span>
<span data-ttu-id="95a7d-103">Pobiera rozszerzenie BGInfo zastosowane na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="95a7d-103">Gets the BGInfo extension applied on a virtual machine.</span></span>

## <span data-ttu-id="95a7d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="95a7d-104">SYNTAX</span></span>

```
Get-AzureVMBGInfoExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="95a7d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="95a7d-105">DESCRIPTION</span></span>
<span data-ttu-id="95a7d-106">Polecenie cmdlet **Get-AzureVMBGInfoExtension** pobiera rozszerzenie BgInfo zastosowane na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="95a7d-106">The **Get-AzureVMBGInfoExtension** cmdlet gets the BGInfo extension applied on a virtual machine.</span></span>

## <span data-ttu-id="95a7d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="95a7d-107">EXAMPLES</span></span>

### <span data-ttu-id="95a7d-108">Przykład 1: uzyskiwanie rozszerzenia BGInfo zastosowanego na określonej maszynie wirtualnej</span><span class="sxs-lookup"><span data-stu-id="95a7d-108">Example 1: Get the BGInfo extension applied on a specified virtual machine</span></span>
```
PS C:\> Get-AzureVMBGInfoExtension -VM $VM;
```

<span data-ttu-id="95a7d-109">To polecenie pobiera rozszerzenie BGInfo zastosowane na określonej maszynie wirtualnej</span><span class="sxs-lookup"><span data-stu-id="95a7d-109">This command gets the BGInfo extension applied on a specified virtual machine</span></span>

## <span data-ttu-id="95a7d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="95a7d-110">PARAMETERS</span></span>

### <span data-ttu-id="95a7d-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="95a7d-111">-InformationAction</span></span>
<span data-ttu-id="95a7d-112">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="95a7d-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="95a7d-113">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="95a7d-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="95a7d-114">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="95a7d-114">Continue</span></span>
- <span data-ttu-id="95a7d-115">Ignorować</span><span class="sxs-lookup"><span data-stu-id="95a7d-115">Ignore</span></span>
- <span data-ttu-id="95a7d-116">Inquire</span><span class="sxs-lookup"><span data-stu-id="95a7d-116">Inquire</span></span>
- <span data-ttu-id="95a7d-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="95a7d-117">SilentlyContinue</span></span>
- <span data-ttu-id="95a7d-118">Przestaw</span><span class="sxs-lookup"><span data-stu-id="95a7d-118">Stop</span></span>
- <span data-ttu-id="95a7d-119">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="95a7d-119">Suspend</span></span>

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

### <span data-ttu-id="95a7d-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="95a7d-120">-InformationVariable</span></span>
<span data-ttu-id="95a7d-121">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="95a7d-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="95a7d-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="95a7d-122">-Profile</span></span>
<span data-ttu-id="95a7d-123">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95a7d-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="95a7d-124">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="95a7d-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="95a7d-125">-VM</span><span class="sxs-lookup"><span data-stu-id="95a7d-125">-VM</span></span>
<span data-ttu-id="95a7d-126">Określa trwały obiekt maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="95a7d-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="95a7d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95a7d-127">CommonParameters</span></span>
<span data-ttu-id="95a7d-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95a7d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95a7d-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95a7d-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95a7d-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="95a7d-130">INPUTS</span></span>

## <span data-ttu-id="95a7d-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="95a7d-131">OUTPUTS</span></span>

## <span data-ttu-id="95a7d-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="95a7d-132">NOTES</span></span>

## <span data-ttu-id="95a7d-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="95a7d-133">RELATED LINKS</span></span>

[<span data-ttu-id="95a7d-134">Remove-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="95a7d-134">Remove-AzureVMBGInfoExtension</span></span>](./Remove-AzureVMBGInfoExtension.md)

[<span data-ttu-id="95a7d-135">Set-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="95a7d-135">Set-AzureVMBGInfoExtension</span></span>](./Set-AzureVMBGInfoExtension.md)


