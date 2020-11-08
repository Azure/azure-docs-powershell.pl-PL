---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 08A7556E-C07F-4B3B-B9D6-B241C72860FA
online version: ''
schema: 2.0.0
ms.openlocfilehash: b01ac318982b62499164cd54c9d9a51356ad9830
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/08/2020
ms.locfileid: "94061855"
---
# <span data-ttu-id="820bc-101">Set-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="820bc-101">Set-WAPackVM</span></span>

## <span data-ttu-id="820bc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="820bc-102">SYNOPSIS</span></span>
<span data-ttu-id="820bc-103">Zmienia właściwości rozmiaru maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="820bc-103">Changes the size properties of a virtual machine.</span></span>

## <span data-ttu-id="820bc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="820bc-104">SYNTAX</span></span>

```
Set-WAPackVM -VM <VirtualMachine> -VMSizeProfile <HardwareProfile> [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="820bc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="820bc-105">DESCRIPTION</span></span>
<span data-ttu-id="820bc-106">Te tematy są przestarzałe i zostaną usunięte w przyszłości.</span><span class="sxs-lookup"><span data-stu-id="820bc-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="820bc-107">W tym temacie opisano polecenie cmdlet w wersji 0.8.1 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="820bc-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="820bc-108">Aby sprawdzić używaną wersję modułu, należy wpisać ją w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="820bc-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="820bc-109">Polecenie cmdlet **Set-WAPackVM** powoduje zmianę właściwości rozmiaru maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="820bc-109">The **Set-WAPackVM** cmdlet changes the size properties of a virtual machine.</span></span>

## <span data-ttu-id="820bc-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="820bc-110">EXAMPLES</span></span>

### <span data-ttu-id="820bc-111">Przykład 1. Określanie rozmiaru maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="820bc-111">Example 1: Specify the size for a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-WAPackVM -Name "ContosoV126"
PS C:\> $SizeProfile = Get-WAPackVMSizeProfile -Name "MediumSizeVM"
PS C:\> Set-WAPackVM -VM $VirtualMachine -VMSizeProfile $SizeProfile
```

<span data-ttu-id="820bc-112">Pierwsze polecenie pobiera maszynę wirtualną o nazwie ContosoV126 przy użyciu polecenia cmdlet **Get-WAPackVM** , a następnie zapisuje ten obiekt w zmiennej $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="820bc-112">The first command gets the virtual machine named ContosoV126 by using the **Get-WAPackVM** cmdlet, and then stores that object in the $VirtualMachine variable.</span></span>

<span data-ttu-id="820bc-113">Drugie polecenie pobiera profil rozmiaru o nazwie MediumSizeVM przy użyciu polecenia cmdlet **Get-WAPackVMSizeProfile** , a następnie zapisuje ten obiekt w zmiennej $SizeProfile.</span><span class="sxs-lookup"><span data-stu-id="820bc-113">The second command gets the size profile named MediumSizeVM by using the **Get-WAPackVMSizeProfile** cmdlet, and then stores that object in the $SizeProfile variable.</span></span>

<span data-ttu-id="820bc-114">Polecenie ostatnie powoduje przypisanie profilu rozmiaru przechowywanego w $SizeProfile do maszyny wirtualnej przechowywanej w $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="820bc-114">The final command assigns the size profile stored in $SizeProfile to the virtual machine stored in $VirtualMachine.</span></span>

## <span data-ttu-id="820bc-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="820bc-115">PARAMETERS</span></span>

### <span data-ttu-id="820bc-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="820bc-116">-PassThru</span></span>
<span data-ttu-id="820bc-117">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="820bc-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="820bc-118">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="820bc-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="820bc-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="820bc-119">-Profile</span></span>
<span data-ttu-id="820bc-120">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="820bc-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="820bc-121">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="820bc-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="820bc-122">-VM</span><span class="sxs-lookup"><span data-stu-id="820bc-122">-VM</span></span>
<span data-ttu-id="820bc-123">Umożliwia określenie maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="820bc-123">Specifies a virtual machine.</span></span>
<span data-ttu-id="820bc-124">Aby uzyskać maszynę wirtualną, użyj polecenia cmdlet **Get-WAPackVM** .</span><span class="sxs-lookup"><span data-stu-id="820bc-124">To obtain a virtual machine, use the **Get-WAPackVM** cmdlet.</span></span>

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

### <span data-ttu-id="820bc-125">-VMSizeProfile</span><span class="sxs-lookup"><span data-stu-id="820bc-125">-VMSizeProfile</span></span>
<span data-ttu-id="820bc-126">Określa profil rozmiaru maszyny wirtualnej jako obiekt **HardwareProfile** .</span><span class="sxs-lookup"><span data-stu-id="820bc-126">Specifies a size profile for a virtual machine as a **HardwareProfile** object.</span></span>
<span data-ttu-id="820bc-127">Aby uzyskać profil rozmiaru, użyj polecenia cmdlet **Get-WAPackVMSizeProfile** .</span><span class="sxs-lookup"><span data-stu-id="820bc-127">To obtain a size profile, use the **Get-WAPackVMSizeProfile** cmdlet.</span></span>

```yaml
Type: HardwareProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="820bc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="820bc-128">CommonParameters</span></span>
<span data-ttu-id="820bc-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="820bc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="820bc-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="820bc-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="820bc-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="820bc-131">INPUTS</span></span>

## <span data-ttu-id="820bc-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="820bc-132">OUTPUTS</span></span>

## <span data-ttu-id="820bc-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="820bc-133">NOTES</span></span>

## <span data-ttu-id="820bc-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="820bc-134">RELATED LINKS</span></span>

[<span data-ttu-id="820bc-135">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="820bc-135">Get-WAPackVM</span></span>](./Get-WAPackVM.md)

[<span data-ttu-id="820bc-136">Nowe — WAPackVM</span><span class="sxs-lookup"><span data-stu-id="820bc-136">New-WAPackVM</span></span>](./New-WAPackVM.md)

[<span data-ttu-id="820bc-137">Remove-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="820bc-137">Remove-WAPackVM</span></span>](./Remove-WAPackVM.md)

[<span data-ttu-id="820bc-138">Restart-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="820bc-138">Restart-WAPackVM</span></span>](./Restart-WAPackVM.md)

[<span data-ttu-id="820bc-139">Życiorys — WAPackVM</span><span class="sxs-lookup"><span data-stu-id="820bc-139">Resume-WAPackVM</span></span>](./Resume-WAPackVM.md)

[<span data-ttu-id="820bc-140">Start — WAPackVM</span><span class="sxs-lookup"><span data-stu-id="820bc-140">Start-WAPackVM</span></span>](./Start-WAPackVM.md)

[<span data-ttu-id="820bc-141">Zatrzymaj — WAPackVM</span><span class="sxs-lookup"><span data-stu-id="820bc-141">Stop-WAPackVM</span></span>](./Stop-WAPackVM.md)

[<span data-ttu-id="820bc-142">Suspend — WAPackVM</span><span class="sxs-lookup"><span data-stu-id="820bc-142">Suspend-WAPackVM</span></span>](./Suspend-WAPackVM.md)

[<span data-ttu-id="820bc-143">Get-WAPackVMSizeProfile</span><span class="sxs-lookup"><span data-stu-id="820bc-143">Get-WAPackVMSizeProfile</span></span>](./Get-WAPackVMSizeProfile.md)


