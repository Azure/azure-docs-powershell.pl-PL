---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 75A50C59-28D1-4D29-A420-D24BF479F79E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 29e5e7e0bc2fcc0ce93186cf966f18d6c9c3e372
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055123"
---
# <span data-ttu-id="8399f-101">Remove-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="8399f-101">Remove-AzureDisk</span></span>

## <span data-ttu-id="8399f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8399f-102">SYNOPSIS</span></span>
<span data-ttu-id="8399f-103">Usuwa dysk z repozytorium dysków Azure.</span><span class="sxs-lookup"><span data-stu-id="8399f-103">Removes a disk from the Azure disk repository.</span></span>

## <span data-ttu-id="8399f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8399f-104">SYNTAX</span></span>

```
Remove-AzureDisk [-DiskName] <String> [-DeleteVHD] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="8399f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8399f-105">DESCRIPTION</span></span>
<span data-ttu-id="8399f-106">Polecenie cmdlet **Remove-AzureDisk** usuwa dysk z repozytorium dysków Azure w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="8399f-106">The **Remove-AzureDisk** cmdlet removes a disk from the Azure disk repository in the current subscription.</span></span>
<span data-ttu-id="8399f-107">Domyślnie to polecenie cmdlet nie usuwa pliku wirtualnego dysku twardego (VHD) z magazynu obiektów BLOB.</span><span class="sxs-lookup"><span data-stu-id="8399f-107">By default, this cmdlet does not delete the virtual hard disk (VHD) file from blob storage.</span></span>
<span data-ttu-id="8399f-108">Aby usunąć dysk VHD, określ parametr *DeleteVHD* .</span><span class="sxs-lookup"><span data-stu-id="8399f-108">To delete the VHD, specify the *DeleteVHD* parameter.</span></span>

## <span data-ttu-id="8399f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8399f-109">EXAMPLES</span></span>

### <span data-ttu-id="8399f-110">Przykład 1: usuwanie dysku</span><span class="sxs-lookup"><span data-stu-id="8399f-110">Example 1: Remove a disk</span></span>
```
PS C:\> Remove-AzureDisk -DiskName "ContosoDataDisk"
```

<span data-ttu-id="8399f-111">To polecenie usuwa dysk o nazwie ContosoDataDisk z repozytorium dysków.</span><span class="sxs-lookup"><span data-stu-id="8399f-111">This command removes the disk named ContosoDataDisk disk from the disk repository.</span></span>
<span data-ttu-id="8399f-112">Polecenie nie usuwa wirtualnego dysku twardego.</span><span class="sxs-lookup"><span data-stu-id="8399f-112">The command does not delete the VHD.</span></span>

### <span data-ttu-id="8399f-113">Przykład 2: usuwanie i usuwanie dysku</span><span class="sxs-lookup"><span data-stu-id="8399f-113">Example 2: Remove and delete a disk</span></span>
```
PS C:\> Remove-AzureDisk -DiskName "ContosoDataDisk" -DeleteVHD
```

<span data-ttu-id="8399f-114">To polecenie usuwa dysk o nazwie ContosoDataDisk z repozytorium dysków.</span><span class="sxs-lookup"><span data-stu-id="8399f-114">This command removes the disk named ContosoDataDisk disk from the disk repository.</span></span>
<span data-ttu-id="8399f-115">To polecenie określa parametr DeleteVHD.</span><span class="sxs-lookup"><span data-stu-id="8399f-115">This command specifies the DeleteVHD parameter.</span></span>
<span data-ttu-id="8399f-116">Dlatego polecenie usuwa wirtualny dysk twardy z usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="8399f-116">Therefore, the command deletes the VHD from Azure Storage.</span></span>

## <span data-ttu-id="8399f-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8399f-117">PARAMETERS</span></span>

### <span data-ttu-id="8399f-118">-DeleteVHD</span><span class="sxs-lookup"><span data-stu-id="8399f-118">-DeleteVHD</span></span>
<span data-ttu-id="8399f-119">Wskazuje, że to polecenie cmdlet usuwa dysk VHD z magazynu obiektów BLOB.</span><span class="sxs-lookup"><span data-stu-id="8399f-119">Indicates that this cmdlet removes the VHD from blob storage.</span></span>

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

### <span data-ttu-id="8399f-120">-Diskname</span><span class="sxs-lookup"><span data-stu-id="8399f-120">-DiskName</span></span>
<span data-ttu-id="8399f-121">Określa nazwę dysku z danymi w repozytorium dysków, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8399f-121">Specifies the name of the data disk in the disk repository that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8399f-122">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="8399f-122">-InformationAction</span></span>
<span data-ttu-id="8399f-123">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="8399f-123">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="8399f-124">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="8399f-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8399f-125">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="8399f-125">Continue</span></span>
- <span data-ttu-id="8399f-126">Ignorować</span><span class="sxs-lookup"><span data-stu-id="8399f-126">Ignore</span></span>
- <span data-ttu-id="8399f-127">Inquire</span><span class="sxs-lookup"><span data-stu-id="8399f-127">Inquire</span></span>
- <span data-ttu-id="8399f-128">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="8399f-128">SilentlyContinue</span></span>
- <span data-ttu-id="8399f-129">Przestaw</span><span class="sxs-lookup"><span data-stu-id="8399f-129">Stop</span></span>
- <span data-ttu-id="8399f-130">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="8399f-130">Suspend</span></span>

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

### <span data-ttu-id="8399f-131">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="8399f-131">-InformationVariable</span></span>
<span data-ttu-id="8399f-132">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="8399f-132">Specifies an information variable.</span></span>

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

### <span data-ttu-id="8399f-133">-Profile</span><span class="sxs-lookup"><span data-stu-id="8399f-133">-Profile</span></span>
<span data-ttu-id="8399f-134">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8399f-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8399f-135">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="8399f-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8399f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8399f-136">CommonParameters</span></span>
<span data-ttu-id="8399f-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8399f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8399f-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8399f-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8399f-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8399f-139">INPUTS</span></span>

## <span data-ttu-id="8399f-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8399f-140">OUTPUTS</span></span>

## <span data-ttu-id="8399f-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8399f-141">NOTES</span></span>

## <span data-ttu-id="8399f-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8399f-142">RELATED LINKS</span></span>

[<span data-ttu-id="8399f-143">Dodaj-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="8399f-143">Add-AzureDisk</span></span>](./Add-AzureDisk.md)

[<span data-ttu-id="8399f-144">Get-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="8399f-144">Get-AzureDisk</span></span>](./Get-AzureDisk.md)

[<span data-ttu-id="8399f-145">Update-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="8399f-145">Update-AzureDisk</span></span>](./Update-AzureDisk.md)


