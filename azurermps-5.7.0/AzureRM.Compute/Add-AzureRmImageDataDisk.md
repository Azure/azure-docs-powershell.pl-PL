---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmImageDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmImageDataDisk.md
ms.openlocfilehash: 13f98e0e0b34e4e192f108e20bcb6f52047b7611
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548200"
---
# <span data-ttu-id="0c3c8-101">Add-AzureRmImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="0c3c8-101">Add-AzureRmImageDataDisk</span></span>

## <span data-ttu-id="0c3c8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0c3c8-102">SYNOPSIS</span></span>
<span data-ttu-id="0c3c8-103">Dodaje dysk danych do obiektu obrazu.</span><span class="sxs-lookup"><span data-stu-id="0c3c8-103">Adds a data disk to an image object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c3c8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0c3c8-104">SYNTAX</span></span>

```
Add-AzureRmImageDataDisk [-Image] <Image> [[-Lun] <Int32>] [[-BlobUri] <String>] [[-Caching] <CachingTypes>]
 [-DiskSizeGB <Int32>] [-StorageAccountType <StorageAccountTypes>] [-SnapshotId <String>]
 [-ManagedDiskId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c3c8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0c3c8-105">DESCRIPTION</span></span>
<span data-ttu-id="0c3c8-106">Polecenie cmdlet **Add-AzureRmImageDataDisk** dodaje dysk danych do obiektu obrazu.</span><span class="sxs-lookup"><span data-stu-id="0c3c8-106">The **Add-AzureRmImageDataDisk** cmdlet adds a data disk to an image object.</span></span>

## <span data-ttu-id="0c3c8-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0c3c8-107">EXAMPLES</span></span>

### <span data-ttu-id="0c3c8-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0c3c8-108">Example 1</span></span>
```
PS C:\> $imageConfig = New-AzureRmImageConfig -Location 'West US';
PS C:\> $osDiskVhdUri = "https://contoso.blob.core.windows.net/test/os.vhd"
PS C:\> $dataDiskVhdUri1 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $dataDiskVhdUri2 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> Set-AzureRmImageOsDisk -Image $imageConfig -OsType 'Windows' -OsState 'Generalized' -BlobUri $osDiskVhdUri;
PS C:\> Add-AzureRmImageDataDisk -Image $imageConfig -Lun 1 -BlobUri $dataDiskVhdUri1;
PS C:\> Add-AzureRmImageDataDisk -Image $imageConfig -Lun 2 -BlobUri $dataDiskVhdUri2;
PS C:\> New-AzureRmImage -Image $imageConfig -ImageName 'ImageName01' -ResourceGroupName 'ResourceGroup01';
```

<span data-ttu-id="0c3c8-109">Pierwsze polecenie tworzy obiekt obrazu, a następnie zapisuje go w zmiennej $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="0c3c8-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>

<span data-ttu-id="0c3c8-110">Kolejne trzy polecenia umożliwiają przypisanie ścieżek dysku systemu operacyjnego i dwóch dysków danych do $osDiskVhdUri, $dataDiskVhdUri 1 i $dataDiskVhdUri 2 zmiennych.</span><span class="sxs-lookup"><span data-stu-id="0c3c8-110">The next three commands assign paths of operating system disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="0c3c8-111">Taka metoda dotyczy tylko czytelności następujących poleceń.</span><span class="sxs-lookup"><span data-stu-id="0c3c8-111">This approach is only for readability of the following commands.</span></span>

<span data-ttu-id="0c3c8-112">Kolejne trzy polecenia umożliwiają dodanie dysku systemu operacyjnego i dwóch dysków z danymi do obrazu przechowywanego w $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="0c3c8-112">The next three commands each adds an operating system disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="0c3c8-113">Identyfikator URI każdego dysku jest przechowywany w $osDiskVhdUri, $dataDiskVhdUri 1 i $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="0c3c8-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>

<span data-ttu-id="0c3c8-114">Polecenie ostatnie powoduje utworzenie obrazu o nazwie ImageName01 w grupie zasób ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="0c3c8-114">The final command creates an image named ImageName01 in resource group ResourceGroup01.</span></span>

## <span data-ttu-id="0c3c8-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0c3c8-115">PARAMETERS</span></span>

### <span data-ttu-id="0c3c8-116">-BlobUri</span><span class="sxs-lookup"><span data-stu-id="0c3c8-116">-BlobUri</span></span>
<span data-ttu-id="0c3c8-117">Określa łącze jako identyfikator URI dla obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="0c3c8-117">Specifies the link, as a URI, of the blob.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c3c8-118">-Buforowanie</span><span class="sxs-lookup"><span data-stu-id="0c3c8-118">-Caching</span></span>
<span data-ttu-id="0c3c8-119">Określa tryb buforowania dysku.</span><span class="sxs-lookup"><span data-stu-id="0c3c8-119">Specifies the caching mode of the disk.</span></span>

```yaml
Type: CachingTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c3c8-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="0c3c8-120">-DiskSizeGB</span></span>
<span data-ttu-id="0c3c8-121">Określa rozmiar dysku w gigabajtach (GB).</span><span class="sxs-lookup"><span data-stu-id="0c3c8-121">Specifies the size of the disk in Gigabytes (GB).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c3c8-122">-Image</span><span class="sxs-lookup"><span data-stu-id="0c3c8-122">-Image</span></span>
<span data-ttu-id="0c3c8-123">Określa lokalny obiekt obrazu.</span><span class="sxs-lookup"><span data-stu-id="0c3c8-123">Specifies a local image object.</span></span>

```yaml
Type: Image
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0c3c8-124">-LUN</span><span class="sxs-lookup"><span data-stu-id="0c3c8-124">-Lun</span></span>
<span data-ttu-id="0c3c8-125">Określa numer jednostki logicznej (LUN).</span><span class="sxs-lookup"><span data-stu-id="0c3c8-125">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c3c8-126">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="0c3c8-126">-ManagedDiskId</span></span>
<span data-ttu-id="0c3c8-127">Określa identyfikator dysku zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="0c3c8-127">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="0c3c8-128">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="0c3c8-128">-SnapshotId</span></span>
<span data-ttu-id="0c3c8-129">Określa identyfikator migawki.</span><span class="sxs-lookup"><span data-stu-id="0c3c8-129">Specifies the ID of a snapshot.</span></span>

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

### <span data-ttu-id="0c3c8-130">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="0c3c8-130">-StorageAccountType</span></span>
<span data-ttu-id="0c3c8-131">Typ konta magazynu na dysku obrazu danych</span><span class="sxs-lookup"><span data-stu-id="0c3c8-131">The Storage Account type of the data image disk</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c3c8-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0c3c8-132">-Confirm</span></span>
<span data-ttu-id="0c3c8-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c3c8-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c3c8-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c3c8-134">-WhatIf</span></span>
<span data-ttu-id="0c3c8-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c3c8-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0c3c8-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0c3c8-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c3c8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c3c8-137">CommonParameters</span></span>
<span data-ttu-id="0c3c8-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c3c8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c3c8-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c3c8-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c3c8-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0c3c8-140">INPUTS</span></span>

### <span data-ttu-id="0c3c8-141">Microsoft. Azure. Management. COMPUTE. models. Image</span><span class="sxs-lookup"><span data-stu-id="0c3c8-141">Microsoft.Azure.Management.Compute.Models.Image</span></span>
<span data-ttu-id="0c3c8-142">System. Int32 system. String. String. Nullable `1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="0c3c8-142">System.Int32 System.String System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="0c3c8-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0c3c8-143">OUTPUTS</span></span>

### <span data-ttu-id="0c3c8-144">Microsoft. Azure. Management. COMPUTE. models. Image</span><span class="sxs-lookup"><span data-stu-id="0c3c8-144">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="0c3c8-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0c3c8-145">NOTES</span></span>

## <span data-ttu-id="0c3c8-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0c3c8-146">RELATED LINKS</span></span>
