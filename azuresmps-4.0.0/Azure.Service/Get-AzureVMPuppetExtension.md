---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9AC28E79-0E3F-4AED-8BFE-8D1C4DCB7715
online version: ''
schema: 2.0.0
ms.openlocfilehash: fd7ece4f8f414df7be6e2d38920f516119f4b82a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055492"
---
# <span data-ttu-id="ef0ed-101">Get-AzureVMPuppetExtension</span><span class="sxs-lookup"><span data-stu-id="ef0ed-101">Get-AzureVMPuppetExtension</span></span>

## <span data-ttu-id="ef0ed-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ef0ed-102">SYNOPSIS</span></span>
<span data-ttu-id="ef0ed-103">Pobiera rozszerzenie Puppet zastosowane na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ef0ed-103">Gets the Puppet extension applied on a virtual machine.</span></span>

## <span data-ttu-id="ef0ed-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ef0ed-104">SYNTAX</span></span>

```
Get-AzureVMPuppetExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="ef0ed-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ef0ed-105">DESCRIPTION</span></span>
<span data-ttu-id="ef0ed-106">Polecenie cmdlet **Get-AzureVMPuppetExtension** pobiera rozszerzenie Puppet zastosowane na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ef0ed-106">The **Get-AzureVMPuppetExtension** cmdlet gets the Puppet extension applied on a virtual machine.</span></span>

## <span data-ttu-id="ef0ed-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ef0ed-107">EXAMPLES</span></span>

### <span data-ttu-id="ef0ed-108">Przykład 1: uzyskiwanie rozszerzenia Puppet zastosowanego na maszynie wirtualnej</span><span class="sxs-lookup"><span data-stu-id="ef0ed-108">Example 1: Get the Puppet extension applied on a virtual machine</span></span>
```
PS C:\> Get-AzureVMPuppetExtension -VM $VM
```

<span data-ttu-id="ef0ed-109">To polecenie pobiera rozszerzenie Puppet zastosowane na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ef0ed-109">This command gets the Puppet extension applied on a virtual machine.</span></span>

## <span data-ttu-id="ef0ed-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ef0ed-110">PARAMETERS</span></span>

### <span data-ttu-id="ef0ed-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="ef0ed-111">-InformationAction</span></span>
<span data-ttu-id="ef0ed-112">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="ef0ed-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ef0ed-113">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="ef0ed-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ef0ed-114">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="ef0ed-114">Continue</span></span>
- <span data-ttu-id="ef0ed-115">Ignorować</span><span class="sxs-lookup"><span data-stu-id="ef0ed-115">Ignore</span></span>
- <span data-ttu-id="ef0ed-116">Inquire</span><span class="sxs-lookup"><span data-stu-id="ef0ed-116">Inquire</span></span>
- <span data-ttu-id="ef0ed-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ef0ed-117">SilentlyContinue</span></span>
- <span data-ttu-id="ef0ed-118">Przestaw</span><span class="sxs-lookup"><span data-stu-id="ef0ed-118">Stop</span></span>
- <span data-ttu-id="ef0ed-119">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="ef0ed-119">Suspend</span></span>

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

### <span data-ttu-id="ef0ed-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ef0ed-120">-InformationVariable</span></span>
<span data-ttu-id="ef0ed-121">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="ef0ed-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="ef0ed-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="ef0ed-122">-Profile</span></span>
<span data-ttu-id="ef0ed-123">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef0ed-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ef0ed-124">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="ef0ed-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ef0ed-125">-VM</span><span class="sxs-lookup"><span data-stu-id="ef0ed-125">-VM</span></span>
<span data-ttu-id="ef0ed-126">Określa trwały obiekt maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ef0ed-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="ef0ed-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef0ed-127">CommonParameters</span></span>
<span data-ttu-id="ef0ed-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef0ed-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef0ed-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef0ed-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef0ed-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ef0ed-130">INPUTS</span></span>

## <span data-ttu-id="ef0ed-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ef0ed-131">OUTPUTS</span></span>

## <span data-ttu-id="ef0ed-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ef0ed-132">NOTES</span></span>

## <span data-ttu-id="ef0ed-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ef0ed-133">RELATED LINKS</span></span>

[<span data-ttu-id="ef0ed-134">Remove-AzureVMPuppetExtension</span><span class="sxs-lookup"><span data-stu-id="ef0ed-134">Remove-AzureVMPuppetExtension</span></span>](./Remove-AzureVMPuppetExtension.md)

[<span data-ttu-id="ef0ed-135">Set-AzureVMPuppetExtension</span><span class="sxs-lookup"><span data-stu-id="ef0ed-135">Set-AzureVMPuppetExtension</span></span>](./Set-AzureVMPuppetExtension.md)


