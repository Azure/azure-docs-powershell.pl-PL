---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 69FBF1E7-E69A-42B5-AC17-C7CF8CAB3C9D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5da323d5284de94aaadfc92abdf819f861695335
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/08/2020
ms.locfileid: "94061853"
---
# <span data-ttu-id="3a877-101">Set-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="3a877-101">Set-WAPackVMRole</span></span>

## <span data-ttu-id="3a877-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3a877-102">SYNOPSIS</span></span>
<span data-ttu-id="3a877-103">Zmienia Właściwość Count wystąpień roli maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3a877-103">Changes the instance count property of a virtual machine role.</span></span>

## <span data-ttu-id="3a877-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3a877-104">SYNTAX</span></span>

```
Set-WAPackVMRole -VMRole <VMRole> -InstanceCount <Int32> [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="3a877-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3a877-105">DESCRIPTION</span></span>
<span data-ttu-id="3a877-106">Te tematy są przestarzałe i zostaną usunięte w przyszłości.</span><span class="sxs-lookup"><span data-stu-id="3a877-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="3a877-107">W tym temacie opisano polecenie cmdlet w wersji 0.8.1 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3a877-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="3a877-108">Aby sprawdzić używaną wersję modułu, należy wpisać ją w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="3a877-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="3a877-109">Polecenie cmdlet **Set-WAPackVMRole** zmienia Właściwość Count wystąpień roli maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3a877-109">The **Set-WAPackVMRole** cmdlet changes the instance count property of a virtual machine role.</span></span>

## <span data-ttu-id="3a877-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3a877-110">EXAMPLES</span></span>

### <span data-ttu-id="3a877-111">Przykład 1. Określanie liczby wystąpień dla roli maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="3a877-111">Example 1: Specify the instance count for a virtual machine role</span></span>
```
PS C:\> $VMRole = Get-WAPackVMRole -Name "ContosoVMRole01"
PS C:\> Set-WAPackVMRole -VMRole $VMRole -InstanceCount 3
```

<span data-ttu-id="3a877-112">Pierwsze polecenie uzyskuje rolę maszyny wirtualnej o nazwie ContosoVMRole01 przy użyciu polecenia cmdlet **Get-WAPackVMRole** , a następnie zapisuje ten obiekt w zmiennej $VMRole.</span><span class="sxs-lookup"><span data-stu-id="3a877-112">The first command gets the virtual machine role named ContosoVMRole01 by using the **Get-WAPackVMRole** cmdlet, and then stores that object in the $VMRole variable.</span></span>

<span data-ttu-id="3a877-113">Drugie i ostatnie polecenie ustawia nową liczbę wystąpień roli maszyny wirtualnej przechowywanej w $VMRole do 3.</span><span class="sxs-lookup"><span data-stu-id="3a877-113">The second and final command sets the new instance count of the virtual machine role stored in $VMRole to 3.</span></span>

## <span data-ttu-id="3a877-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3a877-114">PARAMETERS</span></span>

### <span data-ttu-id="3a877-115">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="3a877-115">-InstanceCount</span></span>
<span data-ttu-id="3a877-116">Określa liczbę wystąpień roli maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3a877-116">Specifies the instance count for a virtual machine role.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a877-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3a877-117">-PassThru</span></span>
<span data-ttu-id="3a877-118">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="3a877-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3a877-119">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="3a877-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3a877-120">-Profile</span><span class="sxs-lookup"><span data-stu-id="3a877-120">-Profile</span></span>
<span data-ttu-id="3a877-121">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a877-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3a877-122">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="3a877-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3a877-123">-VMRole</span><span class="sxs-lookup"><span data-stu-id="3a877-123">-VMRole</span></span>
<span data-ttu-id="3a877-124">Określa rolę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3a877-124">Specifies a virtual machine role.</span></span>
<span data-ttu-id="3a877-125">Aby uzyskać rolę maszyny wirtualnej, użyj polecenia cmdlet **Get-WAPackVMRole** .</span><span class="sxs-lookup"><span data-stu-id="3a877-125">To obtain a virtual machine role, use the **Get-WAPackVMRole** cmdlet.</span></span>

```yaml
Type: VMRole
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3a877-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a877-126">CommonParameters</span></span>
<span data-ttu-id="3a877-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a877-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a877-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a877-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a877-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3a877-129">INPUTS</span></span>

## <span data-ttu-id="3a877-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3a877-130">OUTPUTS</span></span>

## <span data-ttu-id="3a877-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3a877-131">NOTES</span></span>

## <span data-ttu-id="3a877-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3a877-132">RELATED LINKS</span></span>

[<span data-ttu-id="3a877-133">Get-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="3a877-133">Get-WAPackVMRole</span></span>](./Get-WAPackVMRole.md)

[<span data-ttu-id="3a877-134">Nowe — WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="3a877-134">New-WAPackVMRole</span></span>](./New-WAPackVMRole.md)

[<span data-ttu-id="3a877-135">Remove-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="3a877-135">Remove-WAPackVMRole</span></span>](./Remove-WAPackVMRole.md)


