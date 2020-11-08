---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 97E1A3FF-E479-44CD-8147-15408DF3F79A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3f8290b0e4f40305495b535b28b2a8f61d7911ed
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055509"
---
# <span data-ttu-id="099ef-101">Get-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="099ef-101">Get-AzureVMDiagnosticsExtension</span></span>

## <span data-ttu-id="099ef-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="099ef-102">SYNOPSIS</span></span>
<span data-ttu-id="099ef-103">Pobiera ustawienia rozszerzenia Diagnostyka platformy Azure na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="099ef-103">Gets the settings of the Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="099ef-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="099ef-104">SYNTAX</span></span>

```
Get-AzureVMDiagnosticsExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="099ef-105">Opis</span><span class="sxs-lookup"><span data-stu-id="099ef-105">DESCRIPTION</span></span>
<span data-ttu-id="099ef-106">Polecenie cmdlet **Get-AzureVMDiagnosticsExtension** pobiera ustawienia rozszerzenia Diagnostyka platformy Microsoft Azure na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="099ef-106">The **Get-AzureVMDiagnosticsExtension** cmdlet gets the settings of the Microsoft Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="099ef-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="099ef-107">EXAMPLES</span></span>

### <span data-ttu-id="099ef-108">Przykład 1: uzyskiwanie rozszerzenia diagnostycznego zastosowanego do maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="099ef-108">Example 1: Get the diagnostics extension applied to a virtual machine</span></span>
```
PS C:\> Get-AzureVMDiagnosticsExtension -VM $VM
```

<span data-ttu-id="099ef-109">To polecenie powoduje wyświetlenie rozszerzenia diagnostycznego zastosowanego do określonej maszyny wirtualnej jako zapisanej w zmiennej $VM.</span><span class="sxs-lookup"><span data-stu-id="099ef-109">This command gets the diagnostics extension applied to the specified virtual machine as stored in the variable $VM.</span></span>

## <span data-ttu-id="099ef-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="099ef-110">PARAMETERS</span></span>

### <span data-ttu-id="099ef-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="099ef-111">-InformationAction</span></span>
<span data-ttu-id="099ef-112">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="099ef-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="099ef-113">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="099ef-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="099ef-114">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="099ef-114">Continue</span></span>
- <span data-ttu-id="099ef-115">Ignorować</span><span class="sxs-lookup"><span data-stu-id="099ef-115">Ignore</span></span>
- <span data-ttu-id="099ef-116">Inquire</span><span class="sxs-lookup"><span data-stu-id="099ef-116">Inquire</span></span>
- <span data-ttu-id="099ef-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="099ef-117">SilentlyContinue</span></span>
- <span data-ttu-id="099ef-118">Przestaw</span><span class="sxs-lookup"><span data-stu-id="099ef-118">Stop</span></span>
- <span data-ttu-id="099ef-119">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="099ef-119">Suspend</span></span>

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

### <span data-ttu-id="099ef-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="099ef-120">-InformationVariable</span></span>
<span data-ttu-id="099ef-121">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="099ef-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="099ef-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="099ef-122">-Profile</span></span>
<span data-ttu-id="099ef-123">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="099ef-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="099ef-124">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="099ef-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="099ef-125">-VM</span><span class="sxs-lookup"><span data-stu-id="099ef-125">-VM</span></span>
<span data-ttu-id="099ef-126">Określa trwały obiekt maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="099ef-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="099ef-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="099ef-127">CommonParameters</span></span>
<span data-ttu-id="099ef-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="099ef-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="099ef-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="099ef-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="099ef-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="099ef-130">INPUTS</span></span>

## <span data-ttu-id="099ef-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="099ef-131">OUTPUTS</span></span>

## <span data-ttu-id="099ef-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="099ef-132">NOTES</span></span>

## <span data-ttu-id="099ef-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="099ef-133">RELATED LINKS</span></span>

[<span data-ttu-id="099ef-134">Remove-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="099ef-134">Remove-AzureVMDiagnosticsExtension</span></span>](./Remove-AzureVMDiagnosticsExtension.md)

[<span data-ttu-id="099ef-135">Set-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="099ef-135">Set-AzureVMDiagnosticsExtension</span></span>](./Set-AzureVMDiagnosticsExtension.md)


