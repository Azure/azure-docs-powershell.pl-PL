---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 5E85F58B-7C70-4F4A-B218-08F9AF512B76
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8aba9c72e3911f59db88e9be4262ee90ea460a5c
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/08/2020
ms.locfileid: "94061865"
---
# <span data-ttu-id="dc12f-101">Resume-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="dc12f-101">Resume-WAPackVM</span></span>

## <span data-ttu-id="dc12f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dc12f-102">SYNOPSIS</span></span>
<span data-ttu-id="dc12f-103">Wznawia wstrzymane maszyny wirtualne.</span><span class="sxs-lookup"><span data-stu-id="dc12f-103">Resumes paused virtual machines.</span></span>

## <span data-ttu-id="dc12f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dc12f-104">SYNTAX</span></span>

```
Resume-WAPackVM -VM <VirtualMachine> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="dc12f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="dc12f-105">DESCRIPTION</span></span>
<span data-ttu-id="dc12f-106">Te tematy są przestarzałe i zostaną usunięte w przyszłości.</span><span class="sxs-lookup"><span data-stu-id="dc12f-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="dc12f-107">W tym temacie opisano polecenie cmdlet w wersji 0.8.1 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="dc12f-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="dc12f-108">Aby sprawdzić używaną wersję modułu, należy wpisać ją w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="dc12f-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="dc12f-109">Polecenie cmdlet **Resume-WAPackVM** wznawia wstrzymane maszyny wirtualne.</span><span class="sxs-lookup"><span data-stu-id="dc12f-109">The **Resume-WAPackVM** cmdlet resumes paused virtual machines.</span></span>

## <span data-ttu-id="dc12f-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dc12f-110">EXAMPLES</span></span>

### <span data-ttu-id="dc12f-111">Przykład 1: Wznów działanie maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="dc12f-111">Example 1: Resume a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-WAPackVM -Name "ContosoV126"
PS C:\> Resume-WAPackVM -VM $VirtualMachine
```

<span data-ttu-id="dc12f-112">Pierwsze polecenie pobiera maszynę wirtualną o nazwie ContosoV126 przy użyciu polecenia cmdlet **Get-WAPackVM** , a następnie zapisuje ten obiekt w zmiennej $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="dc12f-112">The first command gets the virtual machine named ContosoV126 by using the **Get-WAPackVM** cmdlet, and then stores that object in the $VirtualMachine variable.</span></span>

<span data-ttu-id="dc12f-113">Drugie polecenie wznowi działanie maszyny wirtualnej przechowywanej w $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="dc12f-113">The second command resumes the virtual machine stored in $VirtualMachine.</span></span>

## <span data-ttu-id="dc12f-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dc12f-114">PARAMETERS</span></span>

### <span data-ttu-id="dc12f-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dc12f-115">-PassThru</span></span>
<span data-ttu-id="dc12f-116">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="dc12f-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="dc12f-117">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="dc12f-117">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc12f-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="dc12f-118">-Profile</span></span>
<span data-ttu-id="dc12f-119">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc12f-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="dc12f-120">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="dc12f-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="dc12f-121">-VM</span><span class="sxs-lookup"><span data-stu-id="dc12f-121">-VM</span></span>
<span data-ttu-id="dc12f-122">Umożliwia określenie maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="dc12f-122">Specifies a virtual machine.</span></span>
<span data-ttu-id="dc12f-123">Aby uzyskać maszynę wirtualną, użyj polecenia cmdlet **Get-WAPackVM** .</span><span class="sxs-lookup"><span data-stu-id="dc12f-123">To obtain a virtual machine, use the **Get-WAPackVM** cmdlet.</span></span>

```yaml
Type: VirtualMachine
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dc12f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc12f-124">CommonParameters</span></span>
<span data-ttu-id="dc12f-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc12f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc12f-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc12f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc12f-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dc12f-127">INPUTS</span></span>

## <span data-ttu-id="dc12f-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dc12f-128">OUTPUTS</span></span>

## <span data-ttu-id="dc12f-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dc12f-129">NOTES</span></span>

## <span data-ttu-id="dc12f-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dc12f-130">RELATED LINKS</span></span>

[<span data-ttu-id="dc12f-131">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="dc12f-131">Get-WAPackVM</span></span>](./Get-WAPackVM.md)

[<span data-ttu-id="dc12f-132">Nowe — WAPackVM</span><span class="sxs-lookup"><span data-stu-id="dc12f-132">New-WAPackVM</span></span>](./New-WAPackVM.md)

[<span data-ttu-id="dc12f-133">Remove-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="dc12f-133">Remove-WAPackVM</span></span>](./Remove-WAPackVM.md)

[<span data-ttu-id="dc12f-134">Restart-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="dc12f-134">Restart-WAPackVM</span></span>](./Restart-WAPackVM.md)

[<span data-ttu-id="dc12f-135">Set-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="dc12f-135">Set-WAPackVM</span></span>](./Set-WAPackVM.md)

[<span data-ttu-id="dc12f-136">Start — WAPackVM</span><span class="sxs-lookup"><span data-stu-id="dc12f-136">Start-WAPackVM</span></span>](./Start-WAPackVM.md)

[<span data-ttu-id="dc12f-137">Zatrzymaj — WAPackVM</span><span class="sxs-lookup"><span data-stu-id="dc12f-137">Stop-WAPackVM</span></span>](./Stop-WAPackVM.md)

[<span data-ttu-id="dc12f-138">Suspend — WAPackVM</span><span class="sxs-lookup"><span data-stu-id="dc12f-138">Suspend-WAPackVM</span></span>](./Suspend-WAPackVM.md)


