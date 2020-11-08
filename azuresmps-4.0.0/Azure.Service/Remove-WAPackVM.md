---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D04D79CE-F183-4A8D-B925-F640D89377BD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1d7c4e6bd9365ccf45b730024b5841e4356f556a
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/08/2020
ms.locfileid: "94061878"
---
# <span data-ttu-id="7d6f6-101">Remove-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="7d6f6-101">Remove-WAPackVM</span></span>

## <span data-ttu-id="7d6f6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7d6f6-102">SYNOPSIS</span></span>
<span data-ttu-id="7d6f6-103">Usuwa obiekty maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="7d6f6-103">Removes virtual machine objects.</span></span>

## <span data-ttu-id="7d6f6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7d6f6-104">SYNTAX</span></span>

```
Remove-WAPackVM -VM <VirtualMachine> [-PassThru] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7d6f6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7d6f6-105">DESCRIPTION</span></span>
<span data-ttu-id="7d6f6-106">Te tematy są przestarzałe i zostaną usunięte w przyszłości.</span><span class="sxs-lookup"><span data-stu-id="7d6f6-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="7d6f6-107">W tym temacie opisano polecenie cmdlet w wersji 0.8.1 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="7d6f6-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="7d6f6-108">Aby sprawdzić używaną wersję modułu, należy wpisać ją w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="7d6f6-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="7d6f6-109">Polecenie cmdlet **Remove-WAPackVM** usuwa obiekty maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="7d6f6-109">The **Remove-WAPackVM** cmdlet removes virtual machine objects.</span></span>

## <span data-ttu-id="7d6f6-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7d6f6-110">EXAMPLES</span></span>

### <span data-ttu-id="7d6f6-111">Przykład 1: usuwanie maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="7d6f6-111">Example 1: Remove a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-WAPackVM -Name "ContosoV126"
PS C:\> Remove-WAPackVM -VM $VirtualMachine
```

<span data-ttu-id="7d6f6-112">Pierwsze polecenie pobiera maszynę wirtualną o nazwie ContosoV126 przy użyciu polecenia cmdlet **Get-WAPackVM** , a następnie zapisuje ten obiekt w zmiennej $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="7d6f6-112">The first command gets the virtual machine named ContosoV126 by using the **Get-WAPackVM** cmdlet, and then stores that object in the $VirtualMachine variable.</span></span>

<span data-ttu-id="7d6f6-113">Drugie polecenie usuwa maszynę wirtualną przechowywaną w $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="7d6f6-113">The second command removes the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="7d6f6-114">Polecenie wyświetli monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7d6f6-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="7d6f6-115">Przykład 2: usunięcie maszyny wirtualnej bez potwierdzenia</span><span class="sxs-lookup"><span data-stu-id="7d6f6-115">Example 2: Remove a virtual machine without confirmation</span></span>
```
PS C:\> $VirtualMachine = Get-WAPackVM -Name "ContosoV126"
PS C:\> Remove-WAPackVM -VM $VirtualMachine -Force
```

<span data-ttu-id="7d6f6-116">Pierwsze polecenie pobiera maszynę wirtualną o nazwie ContosoV126 przy użyciu polecenia cmdlet **Get-WAPackVM** , a następnie zapisuje ten obiekt w zmiennej $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="7d6f6-116">The first command gets the virtual machine named ContosoV126 by using the **Get-WAPackVM** cmdlet, and then stores that object in the $VirtualMachine variable.</span></span>

<span data-ttu-id="7d6f6-117">Drugie polecenie usuwa maszynę wirtualną przechowywaną w $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="7d6f6-117">The second command removes the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="7d6f6-118">To polecenie zawiera parametr *Force* .</span><span class="sxs-lookup"><span data-stu-id="7d6f6-118">This command includes the *Force* parameter.</span></span>
<span data-ttu-id="7d6f6-119">Polecenie nie wyświetla monitu o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7d6f6-119">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="7d6f6-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7d6f6-120">PARAMETERS</span></span>

### <span data-ttu-id="7d6f6-121">-Force</span><span class="sxs-lookup"><span data-stu-id="7d6f6-121">-Force</span></span>
<span data-ttu-id="7d6f6-122">Wskazuje, że polecenie cmdlet powoduje usunięcie maszyny wirtualnej bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7d6f6-122">Indicates that the cmdlet removes a virtual machine without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="7d6f6-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7d6f6-123">-PassThru</span></span>
<span data-ttu-id="7d6f6-124">Wskazuje, że polecenie cmdlet zwraca wartość logiczną.</span><span class="sxs-lookup"><span data-stu-id="7d6f6-124">Indicates that the cmdlet returns a Boolean value.</span></span>
<span data-ttu-id="7d6f6-125">Jeśli operacja się powiedzie, polecenie cmdlet zwraca wartość $True.</span><span class="sxs-lookup"><span data-stu-id="7d6f6-125">If the operation succeeds, the cmdlet returns a value of $True.</span></span>
<span data-ttu-id="7d6f6-126">W przeciwnym razie zwraca wartość $False.</span><span class="sxs-lookup"><span data-stu-id="7d6f6-126">Otherwise, it returns a value of $False.</span></span>
<span data-ttu-id="7d6f6-127">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="7d6f6-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7d6f6-128">-Profile</span><span class="sxs-lookup"><span data-stu-id="7d6f6-128">-Profile</span></span>
<span data-ttu-id="7d6f6-129">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d6f6-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7d6f6-130">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="7d6f6-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7d6f6-131">-VM</span><span class="sxs-lookup"><span data-stu-id="7d6f6-131">-VM</span></span>
<span data-ttu-id="7d6f6-132">Umożliwia określenie maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="7d6f6-132">Specifies a virtual machine.</span></span>
<span data-ttu-id="7d6f6-133">Aby uzyskać maszynę wirtualną, użyj polecenia cmdlet **Get-WAPackVM** .</span><span class="sxs-lookup"><span data-stu-id="7d6f6-133">To obtain a virtual machine, use the **Get-WAPackVM** cmdlet.</span></span>

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

### <span data-ttu-id="7d6f6-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7d6f6-134">-Confirm</span></span>
<span data-ttu-id="7d6f6-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d6f6-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d6f6-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d6f6-136">-WhatIf</span></span>
<span data-ttu-id="7d6f6-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d6f6-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d6f6-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7d6f6-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d6f6-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d6f6-139">CommonParameters</span></span>
<span data-ttu-id="7d6f6-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d6f6-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d6f6-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d6f6-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d6f6-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7d6f6-142">INPUTS</span></span>

## <span data-ttu-id="7d6f6-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7d6f6-143">OUTPUTS</span></span>

## <span data-ttu-id="7d6f6-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7d6f6-144">NOTES</span></span>

## <span data-ttu-id="7d6f6-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7d6f6-145">RELATED LINKS</span></span>

[<span data-ttu-id="7d6f6-146">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="7d6f6-146">Get-WAPackVM</span></span>](./Get-WAPackVM.md)

[<span data-ttu-id="7d6f6-147">Nowe — WAPackVM</span><span class="sxs-lookup"><span data-stu-id="7d6f6-147">New-WAPackVM</span></span>](./New-WAPackVM.md)

[<span data-ttu-id="7d6f6-148">Restart-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="7d6f6-148">Restart-WAPackVM</span></span>](./Restart-WAPackVM.md)

[<span data-ttu-id="7d6f6-149">Życiorys — WAPackVM</span><span class="sxs-lookup"><span data-stu-id="7d6f6-149">Resume-WAPackVM</span></span>](./Resume-WAPackVM.md)

[<span data-ttu-id="7d6f6-150">Set-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="7d6f6-150">Set-WAPackVM</span></span>](./Set-WAPackVM.md)

[<span data-ttu-id="7d6f6-151">Start — WAPackVM</span><span class="sxs-lookup"><span data-stu-id="7d6f6-151">Start-WAPackVM</span></span>](./Start-WAPackVM.md)

[<span data-ttu-id="7d6f6-152">Zatrzymaj — WAPackVM</span><span class="sxs-lookup"><span data-stu-id="7d6f6-152">Stop-WAPackVM</span></span>](./Stop-WAPackVM.md)

[<span data-ttu-id="7d6f6-153">Suspend — WAPackVM</span><span class="sxs-lookup"><span data-stu-id="7d6f6-153">Suspend-WAPackVM</span></span>](./Suspend-WAPackVM.md)


