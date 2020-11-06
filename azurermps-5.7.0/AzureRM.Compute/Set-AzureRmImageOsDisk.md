---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmImageOsDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmImageOsDisk.md
ms.openlocfilehash: 8deb191a6a26e4fb0001a1cbb78540460256dd97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525301"
---
# <span data-ttu-id="b419e-101">Set-AzureRmImageOsDisk</span><span class="sxs-lookup"><span data-stu-id="b419e-101">Set-AzureRmImageOsDisk</span></span>

## <span data-ttu-id="b419e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b419e-102">SYNOPSIS</span></span>
<span data-ttu-id="b419e-103">Ustawia właściwości dysku systemu operacyjnego obiektu obrazu.</span><span class="sxs-lookup"><span data-stu-id="b419e-103">Sets the operating system disk properties on an image object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b419e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b419e-104">SYNTAX</span></span>

```
Set-AzureRmImageOsDisk [-Image] <Image> [[-OsType] <OperatingSystemTypes>]
 [[-OsState] <OperatingSystemStateTypes>] [[-BlobUri] <String>] [-Caching <CachingTypes>] [-DiskSizeGB <Int32>]
 [-StorageAccountType <StorageAccountTypes>] [-SnapshotId <String>] [-ManagedDiskId <String>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b419e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b419e-105">DESCRIPTION</span></span>
<span data-ttu-id="b419e-106">Polecenie cmdlet **Set-AzureRmImageOsDisk** ustawia właściwości dysku systemu operacyjnego w obiekcie obrazu.</span><span class="sxs-lookup"><span data-stu-id="b419e-106">The **Set-AzureRmImageOsDisk** cmdlet sets the operating system disk properties on an image object.</span></span>

## <span data-ttu-id="b419e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b419e-107">EXAMPLES</span></span>

### <span data-ttu-id="b419e-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b419e-108">Example 1</span></span>
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

<span data-ttu-id="b419e-109">Pierwsze polecenie tworzy obiekt obrazu, a następnie zapisuje go w zmiennej $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="b419e-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>

<span data-ttu-id="b419e-110">Kolejne trzy polecenia umożliwiają przypisanie ścieżek do dysków systemu operacyjnego i dwóch dysków z danymi do $osDiskVhdUri, $dataDiskVhdUri 1 i $dataDiskVhdUri 2 zmiennych.</span><span class="sxs-lookup"><span data-stu-id="b419e-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="b419e-111">Taka metoda dotyczy tylko czytelności następujących poleceń.</span><span class="sxs-lookup"><span data-stu-id="b419e-111">This approach is only for readability of the following commands.</span></span>

<span data-ttu-id="b419e-112">Kolejne trzy polecenia umożliwiają dodanie dysku systemu operacyjnego i dwóch dysków z danymi do obrazu przechowywanego w $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="b419e-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="b419e-113">Identyfikator URI każdego dysku jest przechowywany w $osDiskVhdUri, $dataDiskVhdUri 1 i $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="b419e-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>

<span data-ttu-id="b419e-114">Polecenie ostatnie powoduje utworzenie obrazu o nazwie "ImageName01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="b419e-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="b419e-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b419e-115">PARAMETERS</span></span>

### <span data-ttu-id="b419e-116">-BlobUri</span><span class="sxs-lookup"><span data-stu-id="b419e-116">-BlobUri</span></span>
<span data-ttu-id="b419e-117">Określa identyfikator URI obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="b419e-117">Specifies the Uri of the blob.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b419e-118">-Buforowanie</span><span class="sxs-lookup"><span data-stu-id="b419e-118">-Caching</span></span>
<span data-ttu-id="b419e-119">Określa tryb buforowania dysku.</span><span class="sxs-lookup"><span data-stu-id="b419e-119">Specifies the caching mode of the disk.</span></span>

```yaml
Type: CachingTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b419e-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="b419e-120">-DiskSizeGB</span></span>
<span data-ttu-id="b419e-121">Określa rozmiar dysku w GB.</span><span class="sxs-lookup"><span data-stu-id="b419e-121">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="b419e-122">-Image</span><span class="sxs-lookup"><span data-stu-id="b419e-122">-Image</span></span>
<span data-ttu-id="b419e-123">Określa lokalny obiekt obrazu.</span><span class="sxs-lookup"><span data-stu-id="b419e-123">Specifies a local image object.</span></span>

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

### <span data-ttu-id="b419e-124">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="b419e-124">-ManagedDiskId</span></span>
<span data-ttu-id="b419e-125">Określa identyfikator dysku zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="b419e-125">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="b419e-126">-OsState</span><span class="sxs-lookup"><span data-stu-id="b419e-126">-OsState</span></span>
<span data-ttu-id="b419e-127">Określa stan systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="b419e-127">Specifies the OS state.</span></span>

```yaml
Type: OperatingSystemStateTypes
Parameter Sets: (All)
Aliases: 
Accepted values: Generalized, Specialized

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b419e-128">-OsType</span><span class="sxs-lookup"><span data-stu-id="b419e-128">-OsType</span></span>
<span data-ttu-id="b419e-129">Określa typ OS.</span><span class="sxs-lookup"><span data-stu-id="b419e-129">Specifies the OS type.</span></span>

```yaml
Type: OperatingSystemTypes
Parameter Sets: (All)
Aliases: 
Accepted values: Windows, Linux

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b419e-130">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="b419e-130">-SnapshotId</span></span>
<span data-ttu-id="b419e-131">Określa identyfikator migawki.</span><span class="sxs-lookup"><span data-stu-id="b419e-131">Specifies the ID of a snapshot.</span></span>

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

### <span data-ttu-id="b419e-132">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="b419e-132">-StorageAccountType</span></span>
<span data-ttu-id="b419e-133">Typ konta magazynu obrazu systemu operacyjnego</span><span class="sxs-lookup"><span data-stu-id="b419e-133">The Storage Account type of Os Image Disk</span></span>

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

### <span data-ttu-id="b419e-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b419e-134">-Confirm</span></span>
<span data-ttu-id="b419e-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b419e-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b419e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b419e-136">-WhatIf</span></span>
<span data-ttu-id="b419e-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b419e-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b419e-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b419e-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b419e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b419e-139">CommonParameters</span></span>
<span data-ttu-id="b419e-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b419e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b419e-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b419e-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b419e-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b419e-142">INPUTS</span></span>

### <span data-ttu-id="b419e-143">Microsoft. Azure. Management. COMPUTE. models. Image</span><span class="sxs-lookup"><span data-stu-id="b419e-143">Microsoft.Azure.Management.Compute.Models.Image</span></span>
<span data-ttu-id="b419e-144">System. Nullable `1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[Microsoft. Azure. Management. COMPUTE. MODELES. OperatingSystemStateTypes; Microsoft. Azure. Management. COMPUTE, Version = 14.0.0.0, Culture = neutral; PublicKeyToken = 31bf3856ad364e35]] system. String system. Nullable. null ( `1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` [System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="b419e-144">System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]] System.String System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="b419e-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b419e-145">OUTPUTS</span></span>

### <span data-ttu-id="b419e-146">Microsoft. Azure. Management. COMPUTE. models. Image</span><span class="sxs-lookup"><span data-stu-id="b419e-146">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="b419e-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b419e-147">NOTES</span></span>

## <span data-ttu-id="b419e-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b419e-148">RELATED LINKS</span></span>

