---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: E0590AD4-F67B-48EF-8657-8890A2204CB6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 607cd288bcc9c86209a3ae0af569e964205f5cb4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055033"
---
# <span data-ttu-id="13282-101">Set-AzureAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="13282-101">Set-AzureAvailabilitySet</span></span>

## <span data-ttu-id="13282-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="13282-102">SYNOPSIS</span></span>
<span data-ttu-id="13282-103">Ustawia nazwę zestawu dostępności na maszynie wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="13282-103">Sets the name of the availability set on an Azure virtual machine.</span></span>

## <span data-ttu-id="13282-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="13282-104">SYNTAX</span></span>

```
Set-AzureAvailabilitySet [-AvailabilitySetName] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="13282-105">Opis</span><span class="sxs-lookup"><span data-stu-id="13282-105">DESCRIPTION</span></span>
<span data-ttu-id="13282-106">Polecenie cmdlet **Set-AzureAvailabilitySet** ustawia nazwę zestawu dostępności na maszynie wirtualnej platformy Azure po wdrożeniu.</span><span class="sxs-lookup"><span data-stu-id="13282-106">The **Set-AzureAvailabilitySet** cmdlet sets the name of the availability set on an Azure virtual machine after deployment.</span></span>

## <span data-ttu-id="13282-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="13282-107">EXAMPLES</span></span>

### <span data-ttu-id="13282-108">Przykład 1. Modyfikowanie nazwy zestawu dostępności</span><span class="sxs-lookup"><span data-stu-id="13282-108">Example 1: Modify the name of an availability set</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine24" | Set-AzureAvailabilitySet -AvailabilitySetName "AvailabilitySet14" | Update-AzureVM
```

<span data-ttu-id="13282-109">Pierwsze polecenie pobiera maszynę wirtualną o nazwie VirtualMachine07 w usłudze o nazwie ContosoService przy użyciu polecenia cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="13282-109">The first command gets the virtual machine named VirtualMachine07 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="13282-110">Polecenie przekazuje ten obiekt do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="13282-110">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="13282-111">To polecenie cmdlet modyfikuje nazwę zestawu dostępności dla tej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="13282-111">That cmdlet modifies the name of the availability set for that virtual machine.</span></span>
<span data-ttu-id="13282-112">Polecenie aktualizuje maszynę wirtualną.</span><span class="sxs-lookup"><span data-stu-id="13282-112">The command updates the virtual machine.</span></span>

## <span data-ttu-id="13282-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="13282-113">PARAMETERS</span></span>

### <span data-ttu-id="13282-114">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="13282-114">-AvailabilitySetName</span></span>
<span data-ttu-id="13282-115">Określa nazwę zestawu dostępności, do którego należy maszyna wirtualna.</span><span class="sxs-lookup"><span data-stu-id="13282-115">Specifies the name of the availability set to which the virtual machine belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13282-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="13282-116">-InformationAction</span></span>
<span data-ttu-id="13282-117">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="13282-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="13282-118">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="13282-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="13282-119">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="13282-119">Continue</span></span>
- <span data-ttu-id="13282-120">Ignorować</span><span class="sxs-lookup"><span data-stu-id="13282-120">Ignore</span></span>
- <span data-ttu-id="13282-121">Inquire</span><span class="sxs-lookup"><span data-stu-id="13282-121">Inquire</span></span>
- <span data-ttu-id="13282-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="13282-122">SilentlyContinue</span></span>
- <span data-ttu-id="13282-123">Przestaw</span><span class="sxs-lookup"><span data-stu-id="13282-123">Stop</span></span>
- <span data-ttu-id="13282-124">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="13282-124">Suspend</span></span>

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

### <span data-ttu-id="13282-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="13282-125">-InformationVariable</span></span>
<span data-ttu-id="13282-126">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="13282-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="13282-127">-Profile</span><span class="sxs-lookup"><span data-stu-id="13282-127">-Profile</span></span>
<span data-ttu-id="13282-128">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13282-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="13282-129">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="13282-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="13282-130">-VM</span><span class="sxs-lookup"><span data-stu-id="13282-130">-VM</span></span>
<span data-ttu-id="13282-131">Określa konfigurację maszyny wirtualnej, którą to polecenie cmdlet modyfikuje.</span><span class="sxs-lookup"><span data-stu-id="13282-131">Specifies the virtual machine configuration that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="13282-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13282-132">CommonParameters</span></span>
<span data-ttu-id="13282-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13282-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13282-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13282-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13282-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="13282-135">INPUTS</span></span>

## <span data-ttu-id="13282-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="13282-136">OUTPUTS</span></span>

## <span data-ttu-id="13282-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="13282-137">NOTES</span></span>

## <span data-ttu-id="13282-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="13282-138">RELATED LINKS</span></span>

[<span data-ttu-id="13282-139">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="13282-139">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="13282-140">Remove-AzureAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="13282-140">Remove-AzureAvailabilitySet</span></span>](./Remove-AzureAvailabilitySet.md)


