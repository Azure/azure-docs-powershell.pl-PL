---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 93A8B8EC-4ED0-4C87-AF92-9A246ECEF4F0
online version: ''
schema: 2.0.0
ms.openlocfilehash: a1b516722b0555c84400c0c8f5acd7f1b5c43d9c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054476"
---
# <span data-ttu-id="c2caa-101">Remove-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="c2caa-101">Remove-AzureVMAccessExtension</span></span>

## <span data-ttu-id="c2caa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c2caa-102">SYNOPSIS</span></span>
<span data-ttu-id="c2caa-103">Usuwa rozszerzenie VMAccess zastosowane na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c2caa-103">Removes the VMAccess extension applied on a virtual machine.</span></span>

## <span data-ttu-id="c2caa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c2caa-104">SYNTAX</span></span>

```
Remove-AzureVMAccessExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="c2caa-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c2caa-105">DESCRIPTION</span></span>
<span data-ttu-id="c2caa-106">Polecenie cmdlet **Remove-AzureVMAccessExtension** usuwa rozszerzenie VMAccess zastosowane na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c2caa-106">The **Remove-AzureVMAccessExtension** cmdlet removes the VMAccess extension applied on a virtual machine.</span></span>

## <span data-ttu-id="c2caa-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c2caa-107">EXAMPLES</span></span>

### <span data-ttu-id="c2caa-108">Przykład 1: Usuwanie rozszerzenia VMAccess z maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="c2caa-108">Example 1: Remove a VMAccess extension from a virtual machine</span></span>
```
PS C:\> Remove-AzureVMAccessExtension -VM $VM;
```

<span data-ttu-id="c2caa-109">To polecenie usuwa rozszerzenie VMAccess z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c2caa-109">This command removes a VMAccess extension from a virtual machine.</span></span>

## <span data-ttu-id="c2caa-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c2caa-110">PARAMETERS</span></span>

### <span data-ttu-id="c2caa-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="c2caa-111">-InformationAction</span></span>
<span data-ttu-id="c2caa-112">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="c2caa-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c2caa-113">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="c2caa-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c2caa-114">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="c2caa-114">Continue</span></span>
- <span data-ttu-id="c2caa-115">Ignorować</span><span class="sxs-lookup"><span data-stu-id="c2caa-115">Ignore</span></span>
- <span data-ttu-id="c2caa-116">Inquire</span><span class="sxs-lookup"><span data-stu-id="c2caa-116">Inquire</span></span>
- <span data-ttu-id="c2caa-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c2caa-117">SilentlyContinue</span></span>
- <span data-ttu-id="c2caa-118">Przestaw</span><span class="sxs-lookup"><span data-stu-id="c2caa-118">Stop</span></span>
- <span data-ttu-id="c2caa-119">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="c2caa-119">Suspend</span></span>

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

### <span data-ttu-id="c2caa-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c2caa-120">-InformationVariable</span></span>
<span data-ttu-id="c2caa-121">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="c2caa-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="c2caa-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="c2caa-122">-Profile</span></span>
<span data-ttu-id="c2caa-123">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2caa-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c2caa-124">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="c2caa-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c2caa-125">-VM</span><span class="sxs-lookup"><span data-stu-id="c2caa-125">-VM</span></span>
<span data-ttu-id="c2caa-126">Określa obiekt trwałej maszyny wirtualnej, którego to polecenie cmdlet usunie rozszerzenie VMAccess.</span><span class="sxs-lookup"><span data-stu-id="c2caa-126">Specifies the persistent virtual machine object that this cmdlet removes the VMAccess extension from.</span></span>

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

### <span data-ttu-id="c2caa-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2caa-127">CommonParameters</span></span>
<span data-ttu-id="c2caa-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2caa-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2caa-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2caa-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2caa-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c2caa-130">INPUTS</span></span>

## <span data-ttu-id="c2caa-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c2caa-131">OUTPUTS</span></span>

## <span data-ttu-id="c2caa-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c2caa-132">NOTES</span></span>

## <span data-ttu-id="c2caa-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c2caa-133">RELATED LINKS</span></span>

[<span data-ttu-id="c2caa-134">Get-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="c2caa-134">Get-AzureVMAccessExtension</span></span>](./Get-AzureVMAccessExtension.md)

[<span data-ttu-id="c2caa-135">Set-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="c2caa-135">Set-AzureVMAccessExtension</span></span>](./Set-AzureVMAccessExtension.md)


