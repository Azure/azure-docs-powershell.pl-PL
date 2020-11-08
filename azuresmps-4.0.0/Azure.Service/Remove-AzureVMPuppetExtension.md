---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9AAEDD44-D11E-47A3-BF0F-D8445A018759
online version: ''
schema: 2.0.0
ms.openlocfilehash: 46dbd7ec58cc112e6573fa3d9c6a52fe0ee14b33
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055409"
---
# <span data-ttu-id="c44af-101">Remove-AzureVMPuppetExtension</span><span class="sxs-lookup"><span data-stu-id="c44af-101">Remove-AzureVMPuppetExtension</span></span>

## <span data-ttu-id="c44af-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c44af-102">SYNOPSIS</span></span>
<span data-ttu-id="c44af-103">Usuwa rozszerzenie Puppet zastosowane na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c44af-103">Removes the Puppet extension applied on a virtual machine.</span></span>

## <span data-ttu-id="c44af-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c44af-104">SYNTAX</span></span>

```
Remove-AzureVMPuppetExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="c44af-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c44af-105">DESCRIPTION</span></span>
<span data-ttu-id="c44af-106">Polecenie cmdlet **Remove-AzureVMPuppetExtension** usuwa rozszerzenie Puppet zastosowane na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c44af-106">The **Remove-AzureVMPuppetExtension** cmdlet removes the Puppet extension applied on a virtual machine.</span></span>

## <span data-ttu-id="c44af-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c44af-107">EXAMPLES</span></span>

### <span data-ttu-id="c44af-108">Przykład 1: Usuwanie rozszerzenia Puppet zastosowanego na maszynie wirtualnej</span><span class="sxs-lookup"><span data-stu-id="c44af-108">Example 1: Remove the Puppet extension applied on a virtual machine</span></span>
```
PS C:\> Remove-AzureVMPuppetExtension -VM $VM;
```

<span data-ttu-id="c44af-109">To polecenie usuwa rozszerzenie Puppet zastosowane na określonej maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c44af-109">This command removes the Puppet extension applied on the specified virtual machine.</span></span>

## <span data-ttu-id="c44af-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c44af-110">PARAMETERS</span></span>

### <span data-ttu-id="c44af-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="c44af-111">-InformationAction</span></span>
<span data-ttu-id="c44af-112">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="c44af-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c44af-113">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="c44af-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c44af-114">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="c44af-114">Continue</span></span>
- <span data-ttu-id="c44af-115">Ignorować</span><span class="sxs-lookup"><span data-stu-id="c44af-115">Ignore</span></span>
- <span data-ttu-id="c44af-116">Inquire</span><span class="sxs-lookup"><span data-stu-id="c44af-116">Inquire</span></span>
- <span data-ttu-id="c44af-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c44af-117">SilentlyContinue</span></span>
- <span data-ttu-id="c44af-118">Przestaw</span><span class="sxs-lookup"><span data-stu-id="c44af-118">Stop</span></span>
- <span data-ttu-id="c44af-119">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="c44af-119">Suspend</span></span>

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

### <span data-ttu-id="c44af-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c44af-120">-InformationVariable</span></span>
<span data-ttu-id="c44af-121">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="c44af-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="c44af-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="c44af-122">-Profile</span></span>
<span data-ttu-id="c44af-123">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c44af-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c44af-124">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="c44af-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c44af-125">-VM</span><span class="sxs-lookup"><span data-stu-id="c44af-125">-VM</span></span>
<span data-ttu-id="c44af-126">Określa trwały obiekt maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c44af-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="c44af-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c44af-127">CommonParameters</span></span>
<span data-ttu-id="c44af-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c44af-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c44af-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c44af-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c44af-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c44af-130">INPUTS</span></span>

## <span data-ttu-id="c44af-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c44af-131">OUTPUTS</span></span>

## <span data-ttu-id="c44af-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c44af-132">NOTES</span></span>

## <span data-ttu-id="c44af-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c44af-133">RELATED LINKS</span></span>

[<span data-ttu-id="c44af-134">Get-AzureVMPuppetExtension</span><span class="sxs-lookup"><span data-stu-id="c44af-134">Get-AzureVMPuppetExtension</span></span>](./Get-AzureVMPuppetExtension.md)

[<span data-ttu-id="c44af-135">Set-AzureVMPuppetExtension</span><span class="sxs-lookup"><span data-stu-id="c44af-135">Set-AzureVMPuppetExtension</span></span>](./Set-AzureVMPuppetExtension.md)


