---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermimagedatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmImageDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmImageDataDisk.md
ms.openlocfilehash: fddf20c748591f339ffa3cf66f3aba4a189ec3db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547504"
---
# <span data-ttu-id="87cba-101">Add-AzureRmImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="87cba-101">Add-AzureRmImageDataDisk</span></span>

## <span data-ttu-id="87cba-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="87cba-102">SYNOPSIS</span></span>
<span data-ttu-id="87cba-103">Dodaje dysk danych do obiektu obrazu.</span><span class="sxs-lookup"><span data-stu-id="87cba-103">Adds a data disk to an image object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87cba-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="87cba-104">SYNTAX</span></span>

```
Add-AzureRmImageDataDisk [-Image] <PSImage> [[-Lun] <Int32>] [[-BlobUri] <String>] [[-Caching] <CachingTypes>]
 [-DiskSizeGB <Int32>] [-StorageAccountType <String>] [-SnapshotId <String>] [-ManagedDiskId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87cba-105">Opis</span><span class="sxs-lookup"><span data-stu-id="87cba-105">DESCRIPTION</span></span>
<span data-ttu-id="87cba-106">Polecenie cmdlet **Add-AzureRmImageDataDisk** dodaje dysk danych do obiektu obrazu.</span><span class="sxs-lookup"><span data-stu-id="87cba-106">The **Add-AzureRmImageDataDisk** cmdlet adds a data disk to an image object.</span></span>

## <span data-ttu-id="87cba-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="87cba-107">EXAMPLES</span></span>

### <span data-ttu-id="87cba-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="87cba-108">Example 1</span></span>
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

<span data-ttu-id="87cba-109">Pierwsze polecenie tworzy obiekt obrazu, a następnie zapisuje go w zmiennej $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="87cba-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="87cba-110">Kolejne trzy polecenia umożliwiają przypisanie ścieżek dysku systemu operacyjnego i dwóch dysków danych do $osDiskVhdUri, $dataDiskVhdUri 1 i $dataDiskVhdUri 2 zmiennych.</span><span class="sxs-lookup"><span data-stu-id="87cba-110">The next three commands assign paths of operating system disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="87cba-111">Taka metoda dotyczy tylko czytelności następujących poleceń.</span><span class="sxs-lookup"><span data-stu-id="87cba-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="87cba-112">Kolejne trzy polecenia umożliwiają dodanie dysku systemu operacyjnego i dwóch dysków z danymi do obrazu przechowywanego w $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="87cba-112">The next three commands each adds an operating system disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="87cba-113">Identyfikator URI każdego dysku jest przechowywany w $osDiskVhdUri, $dataDiskVhdUri 1 i $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="87cba-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="87cba-114">Polecenie ostatnie powoduje utworzenie obrazu o nazwie ImageName01 w grupie zasób ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="87cba-114">The final command creates an image named ImageName01 in resource group ResourceGroup01.</span></span>

## <span data-ttu-id="87cba-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="87cba-115">PARAMETERS</span></span>

### <span data-ttu-id="87cba-116">-BlobUri</span><span class="sxs-lookup"><span data-stu-id="87cba-116">-BlobUri</span></span>
<span data-ttu-id="87cba-117">Określa łącze jako identyfikator URI dla obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="87cba-117">Specifies the link, as a URI, of the blob.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87cba-118">-Buforowanie</span><span class="sxs-lookup"><span data-stu-id="87cba-118">-Caching</span></span>
<span data-ttu-id="87cba-119">Określa tryb buforowania dysku.</span><span class="sxs-lookup"><span data-stu-id="87cba-119">Specifies the caching mode of the disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87cba-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87cba-120">-DefaultProfile</span></span>
<span data-ttu-id="87cba-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="87cba-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87cba-122">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="87cba-122">-DiskSizeGB</span></span>
<span data-ttu-id="87cba-123">Określa rozmiar dysku w gigabajtach (GB).</span><span class="sxs-lookup"><span data-stu-id="87cba-123">Specifies the size of the disk in Gigabytes (GB).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87cba-124">-Image</span><span class="sxs-lookup"><span data-stu-id="87cba-124">-Image</span></span>
<span data-ttu-id="87cba-125">Określa lokalny obiekt obrazu.</span><span class="sxs-lookup"><span data-stu-id="87cba-125">Specifies a local image object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSImage
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="87cba-126">-LUN</span><span class="sxs-lookup"><span data-stu-id="87cba-126">-Lun</span></span>
<span data-ttu-id="87cba-127">Określa numer jednostki logicznej (LUN).</span><span class="sxs-lookup"><span data-stu-id="87cba-127">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87cba-128">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="87cba-128">-ManagedDiskId</span></span>
<span data-ttu-id="87cba-129">Określa identyfikator dysku zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="87cba-129">Specifies the ID of a managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87cba-130">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="87cba-130">-SnapshotId</span></span>
<span data-ttu-id="87cba-131">Określa identyfikator migawki.</span><span class="sxs-lookup"><span data-stu-id="87cba-131">Specifies the ID of a snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87cba-132">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="87cba-132">-StorageAccountType</span></span>
<span data-ttu-id="87cba-133">Typ konta magazynu na dysku obrazu danych</span><span class="sxs-lookup"><span data-stu-id="87cba-133">The Storage Account type of the data image disk</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87cba-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="87cba-134">-Confirm</span></span>
<span data-ttu-id="87cba-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87cba-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87cba-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87cba-136">-WhatIf</span></span>
<span data-ttu-id="87cba-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87cba-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="87cba-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="87cba-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87cba-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87cba-139">CommonParameters</span></span>
<span data-ttu-id="87cba-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87cba-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87cba-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87cba-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87cba-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="87cba-142">INPUTS</span></span>

### <span data-ttu-id="87cba-143">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSImage</span><span class="sxs-lookup"><span data-stu-id="87cba-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

### <span data-ttu-id="87cba-144">System. Int32</span><span class="sxs-lookup"><span data-stu-id="87cba-144">System.Int32</span></span>

### <span data-ttu-id="87cba-145">System. String</span><span class="sxs-lookup"><span data-stu-id="87cba-145">System.String</span></span>

### <span data-ttu-id="87cba-146">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. models. CachingTypes, Microsoft. Azure. Management. Framework</span><span class="sxs-lookup"><span data-stu-id="87cba-146">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=21.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="87cba-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="87cba-147">OUTPUTS</span></span>

### <span data-ttu-id="87cba-148">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSImage</span><span class="sxs-lookup"><span data-stu-id="87cba-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="87cba-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="87cba-149">NOTES</span></span>

## <span data-ttu-id="87cba-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="87cba-150">RELATED LINKS</span></span>
