---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 95DCD2EC-8327-4A46-B624-289D0A28F7EA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4614910b8c0ccd36bb8ef75ee98f662cf69a276a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055320"
---
# <span data-ttu-id="2d3ea-101">Get-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="2d3ea-101">Get-AzureDisk</span></span>

## <span data-ttu-id="2d3ea-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2d3ea-102">SYNOPSIS</span></span>
<span data-ttu-id="2d3ea-103">Pobiera informacje o dyskach w repozytorium dysków Azure.</span><span class="sxs-lookup"><span data-stu-id="2d3ea-103">Gets information about disks in the Azure disk repository.</span></span>

## <span data-ttu-id="2d3ea-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2d3ea-104">SYNTAX</span></span>

```
Get-AzureDisk [[-DiskName] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="2d3ea-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2d3ea-105">DESCRIPTION</span></span>
<span data-ttu-id="2d3ea-106">Polecenie cmdlet **Get-AzureDisk** pobiera informacje o dyskach przechowywanych w repozytorium dysków Azure na potrzeby bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="2d3ea-106">The **Get-AzureDisk** cmdlet gets information about the disks that are stored in the Azure disk repository for the current subscription.</span></span>
<span data-ttu-id="2d3ea-107">To polecenie cmdlet zwraca listę informacji dla wszystkich dysków w repozytorium.</span><span class="sxs-lookup"><span data-stu-id="2d3ea-107">This cmdlet returns a list of information for all disks in the repository.</span></span>
<span data-ttu-id="2d3ea-108">Aby wyświetlić informacje dotyczące określonego dysku, określ nazwę dysku.</span><span class="sxs-lookup"><span data-stu-id="2d3ea-108">To view information for a specific disk, specify the name of the disk.</span></span>

## <span data-ttu-id="2d3ea-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2d3ea-109">EXAMPLES</span></span>

### <span data-ttu-id="2d3ea-110">Przykład 1: uzyskiwanie informacji o dysku</span><span class="sxs-lookup"><span data-stu-id="2d3ea-110">Example 1: Get information about a disk</span></span>
```
PS C:\> Get-AzureDisk -DiskName "ContosoDataDisk"
```

<span data-ttu-id="2d3ea-111">To polecenie pobiera dane dotyczące dysku o nazwie ContosoDataDisk z repozytorium dysków.</span><span class="sxs-lookup"><span data-stu-id="2d3ea-111">This command gets information data about the disk named ContosoDataDisk from the disk repository.</span></span>

### <span data-ttu-id="2d3ea-112">Przykład 2: uzyskiwanie informacji o wszystkich dyskach</span><span class="sxs-lookup"><span data-stu-id="2d3ea-112">Example 2: Get information about all disks</span></span>
```
PS C:\> Get-AzureDisk
```

<span data-ttu-id="2d3ea-113">To polecenie pobiera informacje o wszystkich dyskach w repozytorium dysków.</span><span class="sxs-lookup"><span data-stu-id="2d3ea-113">This command gets information about all the disks in the disk repository.</span></span>

### <span data-ttu-id="2d3ea-114">Przykład 3: uzyskiwanie informacji o dysku</span><span class="sxs-lookup"><span data-stu-id="2d3ea-114">Example 3: Get information about a disk</span></span>
```
PS C:\> Get-AzureDisk | Where-Object {$_.AttachedTo -eq $Null } | Format-Table -AutoSize -Property "DiskName","DiskSizeInGB","MediaLink"
```

<span data-ttu-id="2d3ea-115">To polecenie pobiera dane dla wszystkich dysków w repozytorium dysków, które nie są obecnie dołączone do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2d3ea-115">This command gets data for all of the disks in the disk repository that are not currently attached to a virtual machine.</span></span>
<span data-ttu-id="2d3ea-116">Polecenie pobiera informacje o wszystkich dyskach i przekazuje poszczególne obiekty do polecenia cmdlet **WHERE-Object** .</span><span class="sxs-lookup"><span data-stu-id="2d3ea-116">The command gets information about all of the disks, and passes each object to the **Where-Object** cmdlet.</span></span>
<span data-ttu-id="2d3ea-117">Polecenie cmdlet powoduje porzucanie wszystkich dysków, które nie mają wartości $Null dla właściwości **AttachedTo** .</span><span class="sxs-lookup"><span data-stu-id="2d3ea-117">That cmdlet drops any disk that does not have a value of $Null for the **AttachedTo** property.</span></span>
<span data-ttu-id="2d3ea-118">Polecenie umożliwia sformatowanie listy jako tabeli przy użyciu polecenia cmdlet **formatowanie tabeli** .</span><span class="sxs-lookup"><span data-stu-id="2d3ea-118">The command formats the list as a table by using the **Format-Table** cmdlet.</span></span>

## <span data-ttu-id="2d3ea-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2d3ea-119">PARAMETERS</span></span>

### <span data-ttu-id="2d3ea-120">-Diskname</span><span class="sxs-lookup"><span data-stu-id="2d3ea-120">-DiskName</span></span>
<span data-ttu-id="2d3ea-121">Określa nazwę dysku w repozytorium dysków, w którym ten aplet polecenia pobiera informacje.</span><span class="sxs-lookup"><span data-stu-id="2d3ea-121">Specifies the name of the disk in the disk repository about which this cmdlet gets information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d3ea-122">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="2d3ea-122">-InformationAction</span></span>
<span data-ttu-id="2d3ea-123">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="2d3ea-123">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="2d3ea-124">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="2d3ea-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2d3ea-125">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="2d3ea-125">Continue</span></span>
- <span data-ttu-id="2d3ea-126">Ignorować</span><span class="sxs-lookup"><span data-stu-id="2d3ea-126">Ignore</span></span>
- <span data-ttu-id="2d3ea-127">Inquire</span><span class="sxs-lookup"><span data-stu-id="2d3ea-127">Inquire</span></span>
- <span data-ttu-id="2d3ea-128">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="2d3ea-128">SilentlyContinue</span></span>
- <span data-ttu-id="2d3ea-129">Przestaw</span><span class="sxs-lookup"><span data-stu-id="2d3ea-129">Stop</span></span>
- <span data-ttu-id="2d3ea-130">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="2d3ea-130">Suspend</span></span>

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

### <span data-ttu-id="2d3ea-131">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="2d3ea-131">-InformationVariable</span></span>
<span data-ttu-id="2d3ea-132">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="2d3ea-132">Specifies an information variable.</span></span>

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

### <span data-ttu-id="2d3ea-133">-Profile</span><span class="sxs-lookup"><span data-stu-id="2d3ea-133">-Profile</span></span>
<span data-ttu-id="2d3ea-134">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d3ea-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2d3ea-135">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="2d3ea-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2d3ea-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d3ea-136">CommonParameters</span></span>
<span data-ttu-id="2d3ea-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d3ea-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d3ea-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d3ea-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d3ea-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2d3ea-139">INPUTS</span></span>

## <span data-ttu-id="2d3ea-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2d3ea-140">OUTPUTS</span></span>

## <span data-ttu-id="2d3ea-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2d3ea-141">NOTES</span></span>

## <span data-ttu-id="2d3ea-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2d3ea-142">RELATED LINKS</span></span>

[<span data-ttu-id="2d3ea-143">Dodaj-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="2d3ea-143">Add-AzureDisk</span></span>](./Add-AzureDisk.md)

[<span data-ttu-id="2d3ea-144">Remove-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="2d3ea-144">Remove-AzureDisk</span></span>](./Remove-AzureDisk.md)

[<span data-ttu-id="2d3ea-145">Update-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="2d3ea-145">Update-AzureDisk</span></span>](./Update-AzureDisk.md)


