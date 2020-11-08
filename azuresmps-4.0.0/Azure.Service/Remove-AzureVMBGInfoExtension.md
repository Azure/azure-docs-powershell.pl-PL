---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8C735528-3844-452F-983B-41AC5CD4E414
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1ea39b2c06a5daf7540009f480e7c2ec211e7f47
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054474"
---
# <span data-ttu-id="6f0a7-101">Remove-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="6f0a7-101">Remove-AzureVMBGInfoExtension</span></span>

## <span data-ttu-id="6f0a7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6f0a7-102">SYNOPSIS</span></span>
<span data-ttu-id="6f0a7-103">Usuwa rozszerzenie BGInfo zastosowane na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6f0a7-103">Removes the BGInfo extension applied on a virtual machine.</span></span>

## <span data-ttu-id="6f0a7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6f0a7-104">SYNTAX</span></span>

```
Remove-AzureVMBGInfoExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="6f0a7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6f0a7-105">DESCRIPTION</span></span>
<span data-ttu-id="6f0a7-106">Polecenie cmdlet **Remove-AzureVMBGInfoExtension** usuwa rozszerzenie BgInfo zastosowane na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6f0a7-106">The **Remove-AzureVMBGInfoExtension** cmdlet removes the BGInfo extension applied on a virtual machine.</span></span>

## <span data-ttu-id="6f0a7-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6f0a7-107">EXAMPLES</span></span>

### <span data-ttu-id="6f0a7-108">Przykład 1: Usuwanie rozszerzenia BGInfo na maszynie wirtualnej</span><span class="sxs-lookup"><span data-stu-id="6f0a7-108">Example 1: Remove the BGInfo extension on a virtual machine</span></span>
```
PS C:\> Remove-AzureVMBGInfoExtension -VM $VM;
```

<span data-ttu-id="6f0a7-109">To polecenie usuwa rozszerzenie BGInfo zastosowane na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6f0a7-109">This command removes the BGInfo extension applied on a virtual machine.</span></span>

## <span data-ttu-id="6f0a7-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6f0a7-110">PARAMETERS</span></span>

### <span data-ttu-id="6f0a7-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="6f0a7-111">-InformationAction</span></span>
<span data-ttu-id="6f0a7-112">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="6f0a7-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="6f0a7-113">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="6f0a7-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6f0a7-114">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="6f0a7-114">Continue</span></span>
- <span data-ttu-id="6f0a7-115">Ignorować</span><span class="sxs-lookup"><span data-stu-id="6f0a7-115">Ignore</span></span>
- <span data-ttu-id="6f0a7-116">Inquire</span><span class="sxs-lookup"><span data-stu-id="6f0a7-116">Inquire</span></span>
- <span data-ttu-id="6f0a7-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="6f0a7-117">SilentlyContinue</span></span>
- <span data-ttu-id="6f0a7-118">Przestaw</span><span class="sxs-lookup"><span data-stu-id="6f0a7-118">Stop</span></span>
- <span data-ttu-id="6f0a7-119">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="6f0a7-119">Suspend</span></span>

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

### <span data-ttu-id="6f0a7-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="6f0a7-120">-InformationVariable</span></span>
<span data-ttu-id="6f0a7-121">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="6f0a7-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="6f0a7-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="6f0a7-122">-Profile</span></span>
<span data-ttu-id="6f0a7-123">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6f0a7-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6f0a7-124">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="6f0a7-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6f0a7-125">-VM</span><span class="sxs-lookup"><span data-stu-id="6f0a7-125">-VM</span></span>
<span data-ttu-id="6f0a7-126">Określa trwały obiekt maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6f0a7-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="6f0a7-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f0a7-127">CommonParameters</span></span>
<span data-ttu-id="6f0a7-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f0a7-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f0a7-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f0a7-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f0a7-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6f0a7-130">INPUTS</span></span>

## <span data-ttu-id="6f0a7-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6f0a7-131">OUTPUTS</span></span>

## <span data-ttu-id="6f0a7-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6f0a7-132">NOTES</span></span>

## <span data-ttu-id="6f0a7-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6f0a7-133">RELATED LINKS</span></span>

[<span data-ttu-id="6f0a7-134">Get-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="6f0a7-134">Get-AzureVMBGInfoExtension</span></span>](./Get-AzureVMBGInfoExtension.md)

[<span data-ttu-id="6f0a7-135">Set-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="6f0a7-135">Set-AzureVMBGInfoExtension</span></span>](./Set-AzureVMBGInfoExtension.md)


