---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 8A6B4C8C-B990-443B-9157-B5C35824269A
online version: ''
schema: 2.0.0
ms.openlocfilehash: b2d87c92f18c3aeb25aad210922dea0c93287fa6
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/08/2020
ms.locfileid: "94061894"
---
# <span data-ttu-id="ba030-101">Start-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="ba030-101">Start-WAPackVM</span></span>

## <span data-ttu-id="ba030-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ba030-102">SYNOPSIS</span></span>
<span data-ttu-id="ba030-103">Rozpoczynanie maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ba030-103">Starts a virtual machine.</span></span>

## <span data-ttu-id="ba030-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ba030-104">SYNTAX</span></span>

```
Start-WAPackVM -VM <VirtualMachine> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ba030-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ba030-105">DESCRIPTION</span></span>
<span data-ttu-id="ba030-106">Te tematy są przestarzałe i zostaną usunięte w przyszłości.</span><span class="sxs-lookup"><span data-stu-id="ba030-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="ba030-107">W tym temacie opisano polecenie cmdlet w wersji 0.8.1 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ba030-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="ba030-108">Aby sprawdzić używaną wersję modułu, należy wpisać ją w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="ba030-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="ba030-109">Polecenie cmdlet **Start-WAPackVM** rozpoczyna działanie maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ba030-109">The **Start-WAPackVM** cmdlet starts a virtual machine.</span></span>

## <span data-ttu-id="ba030-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ba030-110">EXAMPLES</span></span>

### <span data-ttu-id="ba030-111">Przykład 1. uruchomienie maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="ba030-111">Example 1: Start a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-WAPackVM -Name "ContosoV126"
PS C:\> Start-WAPackVM -VM $VirtualMachine
```

<span data-ttu-id="ba030-112">Pierwsze polecenie pobiera maszynę wirtualną o nazwie ContosoV126 przy użyciu polecenia cmdlet **Get-WAPackVM** , a następnie zapisuje ten obiekt w zmiennej $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="ba030-112">The first command gets the virtual machine named ContosoV126 by using the **Get-WAPackVM** cmdlet, and then stores that object in the $VirtualMachine variable.</span></span>

<span data-ttu-id="ba030-113">Drugie polecenie uruchamia maszynę wirtualną przechowywaną w $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="ba030-113">The second command starts the virtual machine stored in $VirtualMachine.</span></span>

## <span data-ttu-id="ba030-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ba030-114">PARAMETERS</span></span>

### <span data-ttu-id="ba030-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ba030-115">-PassThru</span></span>
<span data-ttu-id="ba030-116">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="ba030-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ba030-117">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="ba030-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ba030-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="ba030-118">-Profile</span></span>
<span data-ttu-id="ba030-119">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba030-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ba030-120">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="ba030-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ba030-121">-VM</span><span class="sxs-lookup"><span data-stu-id="ba030-121">-VM</span></span>
<span data-ttu-id="ba030-122">Umożliwia określenie maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ba030-122">Specifies a virtual machine.</span></span>
<span data-ttu-id="ba030-123">Aby uzyskać maszynę wirtualną, użyj polecenia cmdlet **Get-WAPackVM** .</span><span class="sxs-lookup"><span data-stu-id="ba030-123">To obtain a virtual machine, use the **Get-WAPackVM** cmdlet.</span></span>

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

### <span data-ttu-id="ba030-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba030-124">CommonParameters</span></span>
<span data-ttu-id="ba030-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba030-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba030-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba030-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba030-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ba030-127">INPUTS</span></span>

## <span data-ttu-id="ba030-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ba030-128">OUTPUTS</span></span>

## <span data-ttu-id="ba030-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ba030-129">NOTES</span></span>

## <span data-ttu-id="ba030-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ba030-130">RELATED LINKS</span></span>

[<span data-ttu-id="ba030-131">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="ba030-131">Get-WAPackVM</span></span>](./Get-WAPackVM.md)

[<span data-ttu-id="ba030-132">Nowe — WAPackVM</span><span class="sxs-lookup"><span data-stu-id="ba030-132">New-WAPackVM</span></span>](./New-WAPackVM.md)

[<span data-ttu-id="ba030-133">Remove-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="ba030-133">Remove-WAPackVM</span></span>](./Remove-WAPackVM.md)

[<span data-ttu-id="ba030-134">Restart-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="ba030-134">Restart-WAPackVM</span></span>](./Restart-WAPackVM.md)

[<span data-ttu-id="ba030-135">Życiorys — WAPackVM</span><span class="sxs-lookup"><span data-stu-id="ba030-135">Resume-WAPackVM</span></span>](./Resume-WAPackVM.md)

[<span data-ttu-id="ba030-136">Set-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="ba030-136">Set-WAPackVM</span></span>](./Set-WAPackVM.md)

[<span data-ttu-id="ba030-137">Zatrzymaj — WAPackVM</span><span class="sxs-lookup"><span data-stu-id="ba030-137">Stop-WAPackVM</span></span>](./Stop-WAPackVM.md)

[<span data-ttu-id="ba030-138">Suspend — WAPackVM</span><span class="sxs-lookup"><span data-stu-id="ba030-138">Suspend-WAPackVM</span></span>](./Suspend-WAPackVM.md)


