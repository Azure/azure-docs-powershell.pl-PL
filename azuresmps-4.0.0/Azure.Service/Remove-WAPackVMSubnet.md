---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E7766E3D-D8C2-42F1-840A-8EA633E98500
online version: ''
schema: 2.0.0
ms.openlocfilehash: a8a85934deb617b4f0d8e85ee3162222f16dd294
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/08/2020
ms.locfileid: "94061877"
---
# <span data-ttu-id="32888-101">Remove-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="32888-101">Remove-WAPackVMSubnet</span></span>

## <span data-ttu-id="32888-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="32888-102">SYNOPSIS</span></span>
<span data-ttu-id="32888-103">Usuwa obiekty podsieci maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="32888-103">Removes virtual machine subnet objects.</span></span>

## <span data-ttu-id="32888-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="32888-104">SYNTAX</span></span>

```
Remove-WAPackVMSubnet -VMSubnet <VMSubnet> [-PassThru] [-Force] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="32888-105">Opis</span><span class="sxs-lookup"><span data-stu-id="32888-105">DESCRIPTION</span></span>
<span data-ttu-id="32888-106">Te tematy są przestarzałe i zostaną usunięte w przyszłości.</span><span class="sxs-lookup"><span data-stu-id="32888-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="32888-107">W tym temacie opisano polecenie cmdlet w wersji 0.8.1 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="32888-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="32888-108">Aby sprawdzić używaną wersję modułu, należy wpisać ją w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="32888-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="32888-109">Polecenie cmdlet **Remove-WAPackVMSubnet** usuwa obiekty podsieci maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="32888-109">The **Remove-WAPackVMSubnet** cmdlet removes virtual machine subnet objects.</span></span>

## <span data-ttu-id="32888-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="32888-110">EXAMPLES</span></span>

### <span data-ttu-id="32888-111">Przykład 1: usuwanie podsieci maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="32888-111">Example 1: Remove a virtual machine subnet</span></span>
```
PS C:\> $VMSubnet = Get-WAPackVMSubnet -Name "ContosoVMSubnet01"
PS C:\> Remove-WAPackVMSubnet -VMSubnet $VMSubnet
```

<span data-ttu-id="32888-112">Pierwsze polecenie pobiera podsieć maszyny wirtualnej o nazwie ContosoVMSubnet01 przy użyciu polecenia cmdlet **Get-WAPackVMSubnet** , a następnie zapisuje ten obiekt w zmiennej $VMSubnet.</span><span class="sxs-lookup"><span data-stu-id="32888-112">The first command gets the virtual machine subnet named ContosoVMSubnet01 by using the **Get-WAPackVMSubnet** cmdlet, and then stores that object in the $VMSubnet variable.</span></span>

<span data-ttu-id="32888-113">Drugie polecenie usuwa podsieć maszyny wirtualnej przechowywaną w $VMSubnet.</span><span class="sxs-lookup"><span data-stu-id="32888-113">The second command removes the virtual machine subnet stored in $VMSubnet.</span></span>
<span data-ttu-id="32888-114">Polecenie wyświetli monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="32888-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="32888-115">Przykład 2: usunięcie maszyny wirtualnej bez potwierdzenia</span><span class="sxs-lookup"><span data-stu-id="32888-115">Example 2: Remove a virtual machine without confirmation</span></span>
```
PS C:\> $VMSubnet = Get-WAPackVMSubnet -Name "ContosoVMSubnet02"
PS C:\> Remove-WAPackVMSubnet -VMSubnet $VMSubnet -Force
```

<span data-ttu-id="32888-116">Pierwsze polecenie uzyskuje usługę w chmurze o nazwie ContosoVMSubnet02 przy użyciu polecenia cmdlet **Get-WAPackVMSubnet** , a następnie zapisuje ten obiekt w zmiennej $VMSubnet.</span><span class="sxs-lookup"><span data-stu-id="32888-116">The first command gets the cloud service named ContosoVMSubnet02 by using the **Get-WAPackVMSubnet** cmdlet, and then stores that object in the $VMSubnet variable.</span></span>

<span data-ttu-id="32888-117">Drugie polecenie usuwa podsieć maszyny wirtualnej przechowywaną w $VMSubnet.</span><span class="sxs-lookup"><span data-stu-id="32888-117">The second command removes the virtual machine subnet stored in $VMSubnet.</span></span>
<span data-ttu-id="32888-118">To polecenie zawiera parametr *Force* .</span><span class="sxs-lookup"><span data-stu-id="32888-118">This command includes the *Force* parameter.</span></span>
<span data-ttu-id="32888-119">Polecenie nie wyświetla monitu o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="32888-119">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="32888-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="32888-120">PARAMETERS</span></span>

### <span data-ttu-id="32888-121">-Force</span><span class="sxs-lookup"><span data-stu-id="32888-121">-Force</span></span>
<span data-ttu-id="32888-122">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="32888-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="32888-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="32888-123">-PassThru</span></span>
<span data-ttu-id="32888-124">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="32888-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="32888-125">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="32888-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="32888-126">-Profile</span><span class="sxs-lookup"><span data-stu-id="32888-126">-Profile</span></span>
<span data-ttu-id="32888-127">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32888-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="32888-128">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="32888-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="32888-129">-VMSubnet</span><span class="sxs-lookup"><span data-stu-id="32888-129">-VMSubnet</span></span>
<span data-ttu-id="32888-130">Określa podsieć maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="32888-130">Specifies a virtual machine subnet.</span></span>
<span data-ttu-id="32888-131">Aby uzyskać podsieć maszyny wirtualnej, użyj polecenia cmdlet **Get-WAPackVMSubnet** .</span><span class="sxs-lookup"><span data-stu-id="32888-131">To obtain a virtual machine subnet, use the **Get-WAPackVMSubnet** cmdlet.</span></span>

```yaml
Type: VMSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="32888-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32888-132">CommonParameters</span></span>
<span data-ttu-id="32888-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32888-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32888-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32888-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32888-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="32888-135">INPUTS</span></span>

## <span data-ttu-id="32888-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="32888-136">OUTPUTS</span></span>

## <span data-ttu-id="32888-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="32888-137">NOTES</span></span>

## <span data-ttu-id="32888-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="32888-138">RELATED LINKS</span></span>

[<span data-ttu-id="32888-139">Get-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="32888-139">Get-WAPackVMSubnet</span></span>](./Get-WAPackVMSubnet.md)

[<span data-ttu-id="32888-140">Nowe — WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="32888-140">New-WAPackVMSubnet</span></span>](./New-WAPackVMSubnet.md)


