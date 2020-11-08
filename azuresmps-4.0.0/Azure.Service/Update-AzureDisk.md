---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 849714BC-8B19-453E-B790-A9C38F9D48CB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8ef8bd3b1fef6a3af01193a104f6917c4131064f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054391"
---
# <span data-ttu-id="5f64f-101">Update-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="5f64f-101">Update-AzureDisk</span></span>

## <span data-ttu-id="5f64f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5f64f-102">SYNOPSIS</span></span>
<span data-ttu-id="5f64f-103">Zmienia etykietę dysku w repozytorium dysków Azure.</span><span class="sxs-lookup"><span data-stu-id="5f64f-103">Changes the label of a disk in the Azure disk repository.</span></span>

## <span data-ttu-id="5f64f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5f64f-104">SYNTAX</span></span>

### <span data-ttu-id="5f64f-105">Resize</span><span class="sxs-lookup"><span data-stu-id="5f64f-105">Resize</span></span>
```
Update-AzureDisk [-DiskName] <String> [[-Label] <String>] [-ResizedSizeInGB] <Int32>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="5f64f-106">Noresize</span><span class="sxs-lookup"><span data-stu-id="5f64f-106">NoResize</span></span>
```
Update-AzureDisk [-DiskName] <String> [-Label] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="5f64f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="5f64f-107">DESCRIPTION</span></span>
<span data-ttu-id="5f64f-108">Polecenie cmdlet **Update-AzureDisk** powoduje zmianę etykiety skojarzonej z dyskiem w repozytorium dysku bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5f64f-108">The **Update-AzureDisk** cmdlet changes the label that is associated with a disk in the disk repository of the current Azure subscription.</span></span>

## <span data-ttu-id="5f64f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5f64f-109">EXAMPLES</span></span>

### <span data-ttu-id="5f64f-110">Przykład 1. Zmienianie etykiety dysku</span><span class="sxs-lookup"><span data-stu-id="5f64f-110">Example 1: Change the label of a disk</span></span>
```
PS C:\> Update-AzureDisk ?DiskName "ContosoOSDisk" -Label "DoNotUse"
```

<span data-ttu-id="5f64f-111">To polecenie powoduje zmianę etykiety dysku o nazwie ContosoOSDisk na DoNotUse.</span><span class="sxs-lookup"><span data-stu-id="5f64f-111">This command changes the label of the disk named ContosoOSDisk to DoNotUse.</span></span>

## <span data-ttu-id="5f64f-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5f64f-112">PARAMETERS</span></span>

### <span data-ttu-id="5f64f-113">-Diskname</span><span class="sxs-lookup"><span data-stu-id="5f64f-113">-DiskName</span></span>
<span data-ttu-id="5f64f-114">Określa nazwę dysku, który jest modyfikowany przez to polecenie.</span><span class="sxs-lookup"><span data-stu-id="5f64f-114">Specifies the name of the disk that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f64f-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="5f64f-115">-InformationAction</span></span>
<span data-ttu-id="5f64f-116">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="5f64f-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="5f64f-117">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="5f64f-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5f64f-118">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="5f64f-118">Continue</span></span>
- <span data-ttu-id="5f64f-119">Ignorować</span><span class="sxs-lookup"><span data-stu-id="5f64f-119">Ignore</span></span>
- <span data-ttu-id="5f64f-120">Inquire</span><span class="sxs-lookup"><span data-stu-id="5f64f-120">Inquire</span></span>
- <span data-ttu-id="5f64f-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="5f64f-121">SilentlyContinue</span></span>
- <span data-ttu-id="5f64f-122">Przestaw</span><span class="sxs-lookup"><span data-stu-id="5f64f-122">Stop</span></span>
- <span data-ttu-id="5f64f-123">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="5f64f-123">Suspend</span></span>

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

### <span data-ttu-id="5f64f-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="5f64f-124">-InformationVariable</span></span>
<span data-ttu-id="5f64f-125">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="5f64f-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="5f64f-126">-Label</span><span class="sxs-lookup"><span data-stu-id="5f64f-126">-Label</span></span>
<span data-ttu-id="5f64f-127">Określa nową etykietę dla dysku.</span><span class="sxs-lookup"><span data-stu-id="5f64f-127">Specifies the new label for the disk.</span></span>

```yaml
Type: String
Parameter Sets: Resize
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: NoResize
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f64f-128">-Profile</span><span class="sxs-lookup"><span data-stu-id="5f64f-128">-Profile</span></span>
<span data-ttu-id="5f64f-129">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5f64f-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5f64f-130">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="5f64f-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5f64f-131">-ResizedSizeInGB</span><span class="sxs-lookup"><span data-stu-id="5f64f-131">-ResizedSizeInGB</span></span>
<span data-ttu-id="5f64f-132">Określa nowy rozmiar dysku (w gigabajtach).</span><span class="sxs-lookup"><span data-stu-id="5f64f-132">Specifies the new size, in gigabytes, for the disk.</span></span>

```yaml
Type: Int32
Parameter Sets: Resize
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f64f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f64f-133">CommonParameters</span></span>
<span data-ttu-id="5f64f-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f64f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f64f-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f64f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f64f-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5f64f-136">INPUTS</span></span>

## <span data-ttu-id="5f64f-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5f64f-137">OUTPUTS</span></span>

### <span data-ttu-id="5f64f-138">DiskContext</span><span class="sxs-lookup"><span data-stu-id="5f64f-138">DiskContext</span></span>

## <span data-ttu-id="5f64f-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5f64f-139">NOTES</span></span>

## <span data-ttu-id="5f64f-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5f64f-140">RELATED LINKS</span></span>

[<span data-ttu-id="5f64f-141">Dodaj-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="5f64f-141">Add-AzureDisk</span></span>](./Add-AzureDisk.md)

[<span data-ttu-id="5f64f-142">Get-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="5f64f-142">Get-AzureDisk</span></span>](./Get-AzureDisk.md)

[<span data-ttu-id="5f64f-143">Remove-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="5f64f-143">Remove-AzureDisk</span></span>](./Remove-AzureDisk.md)


