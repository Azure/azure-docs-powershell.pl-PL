---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 42042533-9F84-4189-8C9F-01FD62F89DC3
online version: ''
schema: 2.0.0
ms.openlocfilehash: db14b17e42d23e481468f563768b606d8baa2802
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/08/2020
ms.locfileid: "94061876"
---
# <span data-ttu-id="1081e-101">Remove-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="1081e-101">Remove-WAPackVNet</span></span>

## <span data-ttu-id="1081e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1081e-102">SYNOPSIS</span></span>
<span data-ttu-id="1081e-103">Usuwa obiekty sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="1081e-103">Removes virtual network objects.</span></span>

## <span data-ttu-id="1081e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1081e-104">SYNTAX</span></span>

```
Remove-WAPackVNet -VNet <VMNetwork> [-PassThru] [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1081e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1081e-105">DESCRIPTION</span></span>
<span data-ttu-id="1081e-106">Te tematy są przestarzałe i zostaną usunięte w przyszłości.</span><span class="sxs-lookup"><span data-stu-id="1081e-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="1081e-107">W tym temacie opisano polecenie cmdlet w wersji 0.8.1 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="1081e-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="1081e-108">Aby sprawdzić używaną wersję modułu, należy wpisać ją w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="1081e-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="1081e-109">Polecenie cmdlet **Remove-WAPackVNet** usuwa obiekty sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="1081e-109">The **Remove-WAPackVNet** cmdlet removes virtual network objects.</span></span>

## <span data-ttu-id="1081e-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1081e-110">EXAMPLES</span></span>

### <span data-ttu-id="1081e-111">Przykład 1: usuwanie wirtualnej sieci</span><span class="sxs-lookup"><span data-stu-id="1081e-111">Example 1: Remove a virtualized network</span></span>
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet01"
PS C:\> Remove-WAPackVM -VNet $VNet
```

<span data-ttu-id="1081e-112">Pierwsze polecenie uzyskuje wirtualną sieć o nazwie ContosoVNet01 przy użyciu polecenia cmdlet **Get-WAPackVNet** , a następnie zapisuje ten obiekt w zmiennej $VNET.</span><span class="sxs-lookup"><span data-stu-id="1081e-112">The first command gets the virtualized network named ContosoVNet01 by using the **Get-WAPackVNet** cmdlet, and then stores that object in the $VNet variable.</span></span>
<span data-ttu-id="1081e-113">Drugie polecenie usuwa wirtualną sieć przechowywaną w $VNet.</span><span class="sxs-lookup"><span data-stu-id="1081e-113">The second command removes the virtualized network stored in $VNet.</span></span>
<span data-ttu-id="1081e-114">Polecenie wyświetli monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1081e-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="1081e-115">Przykład 2: usuwanie sieci wirtualnej bez potwierdzenia</span><span class="sxs-lookup"><span data-stu-id="1081e-115">Example 2: Remove a virtualized network without confirmation</span></span>
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet02"
PS C:\> Remove-WAPackVNet -VNet $VNet -Force
```

<span data-ttu-id="1081e-116">Pierwsze polecenie uzyskuje usługę w chmurze o nazwie ContosoVNet02 przy użyciu polecenia cmdlet **Get-WAPackVNet** , a następnie zapisuje ten obiekt w zmiennej $VNET.</span><span class="sxs-lookup"><span data-stu-id="1081e-116">The first command gets the cloud service named ContosoVNet02 by using the **Get-WAPackVNet** cmdlet, and then stores that object in the $VNet variable.</span></span>
<span data-ttu-id="1081e-117">Drugie polecenie usuwa wirtualną sieć przechowywaną w $VNet.</span><span class="sxs-lookup"><span data-stu-id="1081e-117">The second command removes the virtualized network stored in $VNet.</span></span>
<span data-ttu-id="1081e-118">To polecenie zawiera parametr *Force* .</span><span class="sxs-lookup"><span data-stu-id="1081e-118">This command includes the *Force* parameter.</span></span>
<span data-ttu-id="1081e-119">Polecenie nie wyświetla monitu o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1081e-119">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="1081e-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1081e-120">PARAMETERS</span></span>

### <span data-ttu-id="1081e-121">-Force</span><span class="sxs-lookup"><span data-stu-id="1081e-121">-Force</span></span>
<span data-ttu-id="1081e-122">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="1081e-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1081e-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1081e-123">-PassThru</span></span>
<span data-ttu-id="1081e-124">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="1081e-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="1081e-125">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="1081e-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1081e-126">-Profile</span><span class="sxs-lookup"><span data-stu-id="1081e-126">-Profile</span></span>
<span data-ttu-id="1081e-127">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1081e-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1081e-128">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="1081e-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1081e-129">-VNet</span><span class="sxs-lookup"><span data-stu-id="1081e-129">-VNet</span></span>
<span data-ttu-id="1081e-130">Określa wirtualną sieć.</span><span class="sxs-lookup"><span data-stu-id="1081e-130">Specifies a virtualized network.</span></span>
<span data-ttu-id="1081e-131">Aby uzyskać wirtualną sieć, użyj polecenia cmdlet **Get-WAPackVNet** .</span><span class="sxs-lookup"><span data-stu-id="1081e-131">To obtain a virtualized network, use the **Get-WAPackVNet** cmdlet.</span></span>

```yaml
Type: VMNetwork
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1081e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1081e-132">CommonParameters</span></span>
<span data-ttu-id="1081e-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1081e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1081e-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1081e-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1081e-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1081e-135">INPUTS</span></span>

## <span data-ttu-id="1081e-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1081e-136">OUTPUTS</span></span>

## <span data-ttu-id="1081e-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1081e-137">NOTES</span></span>

## <span data-ttu-id="1081e-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1081e-138">RELATED LINKS</span></span>

[<span data-ttu-id="1081e-139">Get-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="1081e-139">Get-WAPackVNet</span></span>](./Get-WAPackVNet.md)

[<span data-ttu-id="1081e-140">Nowe — WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="1081e-140">New-WAPackVNet</span></span>](./New-WAPackVNet.md)


