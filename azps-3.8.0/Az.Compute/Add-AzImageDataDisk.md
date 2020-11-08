---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azimagedatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzImageDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzImageDataDisk.md
ms.openlocfilehash: 0a50aa781177adb6ff457c3cc7d0a59ad8b350d0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94049263"
---
# <span data-ttu-id="7ccec-101">Add-AzImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="7ccec-101">Add-AzImageDataDisk</span></span>

## <span data-ttu-id="7ccec-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7ccec-102">SYNOPSIS</span></span>
<span data-ttu-id="7ccec-103">Dodaje dysk danych do obiektu obrazu.</span><span class="sxs-lookup"><span data-stu-id="7ccec-103">Adds a data disk to an image object.</span></span>

## <span data-ttu-id="7ccec-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7ccec-104">SYNTAX</span></span>

```
Add-AzImageDataDisk [-Image] <PSImage> [[-Lun] <Int32>] [[-BlobUri] <String>] [[-Caching] <CachingTypes>]
 [-DiskSizeGB <Int32>] [-StorageAccountType <String>] [-SnapshotId <String>] [-ManagedDiskId <String>]
 [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7ccec-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7ccec-105">DESCRIPTION</span></span>
<span data-ttu-id="7ccec-106">Polecenie cmdlet **Add-AzImageDataDisk** dodaje dysk danych do obiektu obrazu.</span><span class="sxs-lookup"><span data-stu-id="7ccec-106">The **Add-AzImageDataDisk** cmdlet adds a data disk to an image object.</span></span>

## <span data-ttu-id="7ccec-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7ccec-107">EXAMPLES</span></span>

### <span data-ttu-id="7ccec-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7ccec-108">Example 1</span></span>
```
PS C:\> $imageConfig = New-AzImageConfig -Location 'West US';
PS C:\> $osDiskVhdUri = "https://contoso.blob.core.windows.net/test/os.vhd"
PS C:\> $dataDiskVhdUri1 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $dataDiskVhdUri2 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> Set-AzImageOsDisk -Image $imageConfig -OsType 'Windows' -OsState 'Generalized' -BlobUri $osDiskVhdUri;
PS C:\> Add-AzImageDataDisk -Image $imageConfig -Lun 1 -BlobUri $dataDiskVhdUri1;
PS C:\> Add-AzImageDataDisk -Image $imageConfig -Lun 2 -BlobUri $dataDiskVhdUri2;
PS C:\> New-AzImage -Image $imageConfig -ImageName 'ImageName01' -ResourceGroupName 'ResourceGroup01';
```

<span data-ttu-id="7ccec-109">Pierwsze polecenie tworzy obiekt obrazu, a następnie zapisuje go w zmiennej $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="7ccec-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="7ccec-110">Kolejne trzy polecenia umożliwiają przypisanie ścieżek dysku systemu operacyjnego i dwóch dysków danych do $osDiskVhdUri, $dataDiskVhdUri 1 i $dataDiskVhdUri 2 zmiennych.</span><span class="sxs-lookup"><span data-stu-id="7ccec-110">The next three commands assign paths of operating system disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="7ccec-111">Taka metoda dotyczy tylko czytelności następujących poleceń.</span><span class="sxs-lookup"><span data-stu-id="7ccec-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="7ccec-112">Kolejne trzy polecenia umożliwiają dodanie dysku systemu operacyjnego i dwóch dysków z danymi do obrazu przechowywanego w $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="7ccec-112">The next three commands each adds an operating system disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="7ccec-113">Identyfikator URI każdego dysku jest przechowywany w $osDiskVhdUri, $dataDiskVhdUri 1 i $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="7ccec-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="7ccec-114">Polecenie ostatnie powoduje utworzenie obrazu o nazwie ImageName01 w grupie zasób ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="7ccec-114">The final command creates an image named ImageName01 in resource group ResourceGroup01.</span></span>

## <span data-ttu-id="7ccec-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7ccec-115">PARAMETERS</span></span>

### <span data-ttu-id="7ccec-116">-BlobUri</span><span class="sxs-lookup"><span data-stu-id="7ccec-116">-BlobUri</span></span>
<span data-ttu-id="7ccec-117">Określa łącze jako identyfikator URI dla obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="7ccec-117">Specifies the link, as a URI, of the blob.</span></span>

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

### <span data-ttu-id="7ccec-118">-Buforowanie</span><span class="sxs-lookup"><span data-stu-id="7ccec-118">-Caching</span></span>
<span data-ttu-id="7ccec-119">Określa tryb buforowania dysku.</span><span class="sxs-lookup"><span data-stu-id="7ccec-119">Specifies the caching mode of the disk.</span></span>

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

### <span data-ttu-id="7ccec-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ccec-120">-DefaultProfile</span></span>
<span data-ttu-id="7ccec-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7ccec-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ccec-122">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="7ccec-122">-DiskEncryptionSetId</span></span>
<span data-ttu-id="7ccec-123">Określa identyfikator zasobu zestawu szyfrowania dysków zarządzanego przez klienta.</span><span class="sxs-lookup"><span data-stu-id="7ccec-123">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="7ccec-124">Ten parametr może być określony tylko dla dysków zarządzanych.</span><span class="sxs-lookup"><span data-stu-id="7ccec-124">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="7ccec-125">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="7ccec-125">-DiskSizeGB</span></span>
<span data-ttu-id="7ccec-126">Określa rozmiar dysku w gigabajtach (GB).</span><span class="sxs-lookup"><span data-stu-id="7ccec-126">Specifies the size of the disk in Gigabytes (GB).</span></span>

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

### <span data-ttu-id="7ccec-127">-Image</span><span class="sxs-lookup"><span data-stu-id="7ccec-127">-Image</span></span>
<span data-ttu-id="7ccec-128">Określa lokalny obiekt obrazu.</span><span class="sxs-lookup"><span data-stu-id="7ccec-128">Specifies a local image object.</span></span>

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

### <span data-ttu-id="7ccec-129">-LUN</span><span class="sxs-lookup"><span data-stu-id="7ccec-129">-Lun</span></span>
<span data-ttu-id="7ccec-130">Określa numer jednostki logicznej (LUN).</span><span class="sxs-lookup"><span data-stu-id="7ccec-130">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="7ccec-131">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="7ccec-131">-ManagedDiskId</span></span>
<span data-ttu-id="7ccec-132">Określa identyfikator dysku zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="7ccec-132">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="7ccec-133">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="7ccec-133">-SnapshotId</span></span>
<span data-ttu-id="7ccec-134">Określa identyfikator migawki.</span><span class="sxs-lookup"><span data-stu-id="7ccec-134">Specifies the ID of a snapshot.</span></span>

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

### <span data-ttu-id="7ccec-135">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="7ccec-135">-StorageAccountType</span></span>
<span data-ttu-id="7ccec-136">Typ konta magazynu na dysku obrazu danych</span><span class="sxs-lookup"><span data-stu-id="7ccec-136">The Storage Account type of the data image disk</span></span>

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

### <span data-ttu-id="7ccec-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7ccec-137">-Confirm</span></span>
<span data-ttu-id="7ccec-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ccec-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ccec-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ccec-139">-WhatIf</span></span>
<span data-ttu-id="7ccec-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ccec-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7ccec-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7ccec-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ccec-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ccec-142">CommonParameters</span></span>
<span data-ttu-id="7ccec-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ccec-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ccec-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7ccec-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ccec-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7ccec-145">INPUTS</span></span>

### <span data-ttu-id="7ccec-146">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSImage</span><span class="sxs-lookup"><span data-stu-id="7ccec-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

### <span data-ttu-id="7ccec-147">System. Int32</span><span class="sxs-lookup"><span data-stu-id="7ccec-147">System.Int32</span></span>

### <span data-ttu-id="7ccec-148">System. String</span><span class="sxs-lookup"><span data-stu-id="7ccec-148">System.String</span></span>

### <span data-ttu-id="7ccec-149">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. models. CachingTypes, Microsoft. Azure. Management. Framework</span><span class="sxs-lookup"><span data-stu-id="7ccec-149">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="7ccec-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7ccec-150">OUTPUTS</span></span>

### <span data-ttu-id="7ccec-151">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSImage</span><span class="sxs-lookup"><span data-stu-id="7ccec-151">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="7ccec-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7ccec-152">NOTES</span></span>

## <span data-ttu-id="7ccec-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7ccec-153">RELATED LINKS</span></span>
