---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 16A34F31-1C61-4911-8C1F-9F82683524A1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 775d2deff8a83e758d48fb9328bf4156b142d20c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055359"
---
# <span data-ttu-id="56f4a-101">Add-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="56f4a-101">Add-AzureDisk</span></span>

## <span data-ttu-id="56f4a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="56f4a-102">SYNOPSIS</span></span>
<span data-ttu-id="56f4a-103">Dodaje dysk do repozytorium dysków Azure.</span><span class="sxs-lookup"><span data-stu-id="56f4a-103">Adds a disk to the Azure disk repository.</span></span>

## <span data-ttu-id="56f4a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="56f4a-104">SYNTAX</span></span>

```
Add-AzureDisk [-DiskName] <String> [-MediaLocation] <String> [-Label <String>] [-OS <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="56f4a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="56f4a-105">DESCRIPTION</span></span>
<span data-ttu-id="56f4a-106">Polecenie cmdlet **Add-AzureDisk** umożliwia dodanie dysku do repozytorium dysków Azure w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="56f4a-106">The **Add-AzureDisk** cmdlet adds a disk to the Azure disk repository in the current subscription.</span></span>
<span data-ttu-id="56f4a-107">To polecenie cmdlet umożliwia dodanie dysku systemowego lub dysku danych.</span><span class="sxs-lookup"><span data-stu-id="56f4a-107">This cmdlet can add a system disk or a data disk.</span></span>
<span data-ttu-id="56f4a-108">Aby dodać dysk systemowy, określ typ systemu operacyjnego za pomocą parametru *OS* .</span><span class="sxs-lookup"><span data-stu-id="56f4a-108">To add a system disk, specify an operating system type by using the *OS* parameter.</span></span>

## <span data-ttu-id="56f4a-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="56f4a-109">EXAMPLES</span></span>

### <span data-ttu-id="56f4a-110">Przykład 1: Dodawanie dysku startowego korzystającego z systemu operacyjnego Windows</span><span class="sxs-lookup"><span data-stu-id="56f4a-110">Example 1: Add a startup disk that uses the Windows operating system</span></span>
```
PS C:\> Add-AzureDisk -DiskName "MyWinDisk" -MediaLocation "http://contosostorage.blob.core.azure.com/vhds/winserver-system.vhd" -Label "StartupDisk" -OS "Windows"
```

<span data-ttu-id="56f4a-111">To polecenie umożliwia dodanie dysku systemowego do repozytorium dysków.</span><span class="sxs-lookup"><span data-stu-id="56f4a-111">This command adds a system disk to your disk repository.</span></span>
<span data-ttu-id="56f4a-112">Dysk systemowy korzysta z systemu operacyjnego Windows.</span><span class="sxs-lookup"><span data-stu-id="56f4a-112">The system disk uses the Windows operating system.</span></span>

### <span data-ttu-id="56f4a-113">Przykład 2: Dodawanie dysku z danymi</span><span class="sxs-lookup"><span data-stu-id="56f4a-113">Example 2: Add a data disk</span></span>
```
PS C:\> Add-AzureDisk -DiskName "MyDataDisk" -MediaLocation "http://yourstorageaccount.blob.core.azure.com/vhds/winserver-data.vhd" -Label "DataDisk"
```

<span data-ttu-id="56f4a-114">To polecenie dodaje dysk danych.</span><span class="sxs-lookup"><span data-stu-id="56f4a-114">This command adds a data disk.</span></span>

### <span data-ttu-id="56f4a-115">Przykład 3: Dodawanie dysku systemowego Linux</span><span class="sxs-lookup"><span data-stu-id="56f4a-115">Example 3: Add a Linux system disk</span></span>
```
PS C:\> Add-AzureDisk -DiskName "MyLinuxDisk" -MediaLocation "http://yourstorageaccount.blob.core.azure.com/vhds/linuxsys.vhd" -OS "Linux"
```

<span data-ttu-id="56f4a-116">To polecenie dodaje dysk systemowy Linux.</span><span class="sxs-lookup"><span data-stu-id="56f4a-116">This command adds a Linux system disk.</span></span>

## <span data-ttu-id="56f4a-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="56f4a-117">PARAMETERS</span></span>

### <span data-ttu-id="56f4a-118">-Diskname</span><span class="sxs-lookup"><span data-stu-id="56f4a-118">-DiskName</span></span>
<span data-ttu-id="56f4a-119">Określa nazwę dysku, który jest dodawany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56f4a-119">Specifies the name of the disk that this cmdlet adds.</span></span>

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

### <span data-ttu-id="56f4a-120">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="56f4a-120">-InformationAction</span></span>
<span data-ttu-id="56f4a-121">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="56f4a-121">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="56f4a-122">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="56f4a-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="56f4a-123">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="56f4a-123">Continue</span></span>
- <span data-ttu-id="56f4a-124">Ignorować</span><span class="sxs-lookup"><span data-stu-id="56f4a-124">Ignore</span></span>
- <span data-ttu-id="56f4a-125">Inquire</span><span class="sxs-lookup"><span data-stu-id="56f4a-125">Inquire</span></span>
- <span data-ttu-id="56f4a-126">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="56f4a-126">SilentlyContinue</span></span>
- <span data-ttu-id="56f4a-127">Przestaw</span><span class="sxs-lookup"><span data-stu-id="56f4a-127">Stop</span></span>
- <span data-ttu-id="56f4a-128">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="56f4a-128">Suspend</span></span>

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

### <span data-ttu-id="56f4a-129">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="56f4a-129">-InformationVariable</span></span>
<span data-ttu-id="56f4a-130">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="56f4a-130">Specifies an information variable.</span></span>

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

### <span data-ttu-id="56f4a-131">-Label</span><span class="sxs-lookup"><span data-stu-id="56f4a-131">-Label</span></span>
<span data-ttu-id="56f4a-132">Określa etykietę dysku, który jest dodawany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56f4a-132">Specifies a disk label for the disk that this cmdlet adds.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56f4a-133">-MediaLocation</span><span class="sxs-lookup"><span data-stu-id="56f4a-133">-MediaLocation</span></span>
<span data-ttu-id="56f4a-134">Określa fizyczną lokalizację dysku w usłudze Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="56f4a-134">Specifies the physical location of the disk in Azure Storage.</span></span>
<span data-ttu-id="56f4a-135">Ta wartość odwołuje się do strony obiektu BLOB na bieżącym koncie abonamentu i magazynu.</span><span class="sxs-lookup"><span data-stu-id="56f4a-135">This value refers to a blob page in the current subscription and storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56f4a-136">-OS</span><span class="sxs-lookup"><span data-stu-id="56f4a-136">-OS</span></span>
<span data-ttu-id="56f4a-137">Określa typ systemu operacyjnego dla dysku systemowego.</span><span class="sxs-lookup"><span data-stu-id="56f4a-137">Specifies the operating system type for a system disk.</span></span>
<span data-ttu-id="56f4a-138">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="56f4a-138">Valid values are:</span></span> 

- <span data-ttu-id="56f4a-139">Microsoft</span><span class="sxs-lookup"><span data-stu-id="56f4a-139">Windows</span></span> 
- <span data-ttu-id="56f4a-140">Linux</span><span class="sxs-lookup"><span data-stu-id="56f4a-140">Linux</span></span> 

<span data-ttu-id="56f4a-141">Jeśli nie podano tego parametru, polecenie cmdlet doda dysk jako dysk danych.</span><span class="sxs-lookup"><span data-stu-id="56f4a-141">If you do not specify this parameter, the cmdlet adds the disk as a data disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56f4a-142">-Profile</span><span class="sxs-lookup"><span data-stu-id="56f4a-142">-Profile</span></span>
<span data-ttu-id="56f4a-143">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56f4a-143">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="56f4a-144">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="56f4a-144">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="56f4a-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56f4a-145">CommonParameters</span></span>
<span data-ttu-id="56f4a-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56f4a-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56f4a-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56f4a-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56f4a-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="56f4a-148">INPUTS</span></span>

## <span data-ttu-id="56f4a-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="56f4a-149">OUTPUTS</span></span>

### <span data-ttu-id="56f4a-150">DiskContext</span><span class="sxs-lookup"><span data-stu-id="56f4a-150">DiskContext</span></span>

## <span data-ttu-id="56f4a-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="56f4a-151">NOTES</span></span>

## <span data-ttu-id="56f4a-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="56f4a-152">RELATED LINKS</span></span>

[<span data-ttu-id="56f4a-153">Get-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="56f4a-153">Get-AzureDisk</span></span>](./Get-AzureDisk.md)

[<span data-ttu-id="56f4a-154">Remove-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="56f4a-154">Remove-AzureDisk</span></span>](./Remove-AzureDisk.md)

[<span data-ttu-id="56f4a-155">Update-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="56f4a-155">Update-AzureDisk</span></span>](./Update-AzureDisk.md)


