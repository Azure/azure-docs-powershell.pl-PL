---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 047C5FBD-CB0D-47BF-AE03-4DF32B4FAD87
online version: ''
schema: 2.0.0
ms.openlocfilehash: a546c9fdb066aaf1203055fd62d8eb01258569c8
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/08/2020
ms.locfileid: "94061826"
---
# <span data-ttu-id="70482-101">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="70482-101">Get-WAPackVM</span></span>

## <span data-ttu-id="70482-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="70482-102">SYNOPSIS</span></span>
<span data-ttu-id="70482-103">Pobiera obiekty maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="70482-103">Gets virtual machine objects.</span></span>

## <span data-ttu-id="70482-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="70482-104">SYNTAX</span></span>

### <span data-ttu-id="70482-105">Empty (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="70482-105">Empty (Default)</span></span>
```
Get-WAPackVM [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="70482-106">Odname</span><span class="sxs-lookup"><span data-stu-id="70482-106">FromName</span></span>
```
Get-WAPackVM [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="70482-107">FromId</span><span class="sxs-lookup"><span data-stu-id="70482-107">FromId</span></span>
```
Get-WAPackVM [-ID <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="70482-108">Opis</span><span class="sxs-lookup"><span data-stu-id="70482-108">DESCRIPTION</span></span>
<span data-ttu-id="70482-109">Te tematy są przestarzałe i zostaną usunięte w przyszłości.</span><span class="sxs-lookup"><span data-stu-id="70482-109">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="70482-110">W tym temacie opisano polecenie cmdlet w wersji 0.8.1 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="70482-110">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="70482-111">Aby sprawdzić używaną wersję modułu, należy wpisać ją w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="70482-111">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="70482-112">Polecenie cmdlet **Get-WAPackVM** Pobiera obiekty maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="70482-112">The **Get-WAPackVM** cmdlet gets virtual machine objects.</span></span>

## <span data-ttu-id="70482-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="70482-113">EXAMPLES</span></span>

### <span data-ttu-id="70482-114">Przykład 1: pobieranie maszyny wirtualnej za pomocą nazwy</span><span class="sxs-lookup"><span data-stu-id="70482-114">Example 1: Get a virtual machine by using a name</span></span>
```
PS C:\> Get-WAPackVM -Name "ContosoV126"
```

<span data-ttu-id="70482-115">To polecenie umożliwia pobieranie maszyny wirtualnej o nazwie ContosoV126.</span><span class="sxs-lookup"><span data-stu-id="70482-115">This command gets the virtual machine named ContosoV126.</span></span>

### <span data-ttu-id="70482-116">Przykład 2: uzyskiwanie maszyny wirtualnej przy użyciu identyfikatora</span><span class="sxs-lookup"><span data-stu-id="70482-116">Example 2: Get a virtual machine by using an ID</span></span>
```
PS C:\> Get-WAPackVM -Id 66242D17-189F-480D-87CF-8E1D749998C8
```

<span data-ttu-id="70482-117">To polecenie umożliwia wyświetlenie maszyny wirtualnej o określonym IDENTYFIKATORze.</span><span class="sxs-lookup"><span data-stu-id="70482-117">This command gets the virtual machine that has the specified ID.</span></span>

### <span data-ttu-id="70482-118">Przykład 3: pobieranie wszystkich maszyn wirtualnych</span><span class="sxs-lookup"><span data-stu-id="70482-118">Example 3: Get all virtual machines</span></span>
```
PS C:\> Get-WAPackVM
```

<span data-ttu-id="70482-119">To polecenie pobiera wszystkie maszyny wirtualne.</span><span class="sxs-lookup"><span data-stu-id="70482-119">This command gets all virtual machines.</span></span>

## <span data-ttu-id="70482-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="70482-120">PARAMETERS</span></span>

### <span data-ttu-id="70482-121">-ID</span><span class="sxs-lookup"><span data-stu-id="70482-121">-ID</span></span>
<span data-ttu-id="70482-122">Określa unikatowy identyfikator maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="70482-122">Specifies the unique ID of a virtual machine.</span></span>

```yaml
Type: Guid
Parameter Sets: FromId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70482-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="70482-123">-Name</span></span>
<span data-ttu-id="70482-124">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="70482-124">Specifies the name of a virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: FromName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70482-125">-Profile</span><span class="sxs-lookup"><span data-stu-id="70482-125">-Profile</span></span>
<span data-ttu-id="70482-126">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70482-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="70482-127">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="70482-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="70482-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70482-128">CommonParameters</span></span>
<span data-ttu-id="70482-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70482-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70482-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70482-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70482-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="70482-131">INPUTS</span></span>

## <span data-ttu-id="70482-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="70482-132">OUTPUTS</span></span>

## <span data-ttu-id="70482-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="70482-133">NOTES</span></span>

## <span data-ttu-id="70482-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="70482-134">RELATED LINKS</span></span>

[<span data-ttu-id="70482-135">Nowe — WAPackVM</span><span class="sxs-lookup"><span data-stu-id="70482-135">New-WAPackVM</span></span>](./New-WAPackVM.md)

[<span data-ttu-id="70482-136">Remove-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="70482-136">Remove-WAPackVM</span></span>](./Remove-WAPackVM.md)

[<span data-ttu-id="70482-137">Restart-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="70482-137">Restart-WAPackVM</span></span>](./Restart-WAPackVM.md)

[<span data-ttu-id="70482-138">Życiorys — WAPackVM</span><span class="sxs-lookup"><span data-stu-id="70482-138">Resume-WAPackVM</span></span>](./Resume-WAPackVM.md)

[<span data-ttu-id="70482-139">Set-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="70482-139">Set-WAPackVM</span></span>](./Set-WAPackVM.md)

[<span data-ttu-id="70482-140">Start — WAPackVM</span><span class="sxs-lookup"><span data-stu-id="70482-140">Start-WAPackVM</span></span>](./Start-WAPackVM.md)

[<span data-ttu-id="70482-141">Zatrzymaj — WAPackVM</span><span class="sxs-lookup"><span data-stu-id="70482-141">Stop-WAPackVM</span></span>](./Stop-WAPackVM.md)

[<span data-ttu-id="70482-142">Suspend — WAPackVM</span><span class="sxs-lookup"><span data-stu-id="70482-142">Suspend-WAPackVM</span></span>](./Suspend-WAPackVM.md)

[<span data-ttu-id="70482-143">Get-WAPackVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="70482-143">Get-WAPackVMOSDisk</span></span>](./Get-WAPackVMOSDisk.md)


