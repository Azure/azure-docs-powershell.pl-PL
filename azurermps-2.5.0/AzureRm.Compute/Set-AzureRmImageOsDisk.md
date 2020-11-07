---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermimageosdisk
schema: 2.0.0
ms.openlocfilehash: 9d7d7436e6c653c257fb549854338a277d621ee0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898764"
---
# <span data-ttu-id="6d836-101">Set-AzureRmImageOsDisk</span><span class="sxs-lookup"><span data-stu-id="6d836-101">Set-AzureRmImageOsDisk</span></span>

## <span data-ttu-id="6d836-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6d836-102">SYNOPSIS</span></span>
<span data-ttu-id="6d836-103">Ustawia właściwości dysku systemu operacyjnego obiektu obrazu.</span><span class="sxs-lookup"><span data-stu-id="6d836-103">Sets the operating system disk properties on an image object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d836-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6d836-104">SYNTAX</span></span>

```
Set-AzureRmImageOsDisk [-Image] <PSImage> [[-OsType] <OperatingSystemTypes>]
 [[-OsState] <OperatingSystemStateTypes>] [[-BlobUri] <String>] [-Caching <CachingTypes>] [-DiskSizeGB <Int32>]
 [-StorageAccountType <StorageAccountTypes>] [-SnapshotId <String>] [-ManagedDiskId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d836-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6d836-105">DESCRIPTION</span></span>
<span data-ttu-id="6d836-106">Polecenie cmdlet **Set-AzureRmImageOsDisk** ustawia właściwości dysku systemu operacyjnego w obiekcie obrazu.</span><span class="sxs-lookup"><span data-stu-id="6d836-106">The **Set-AzureRmImageOsDisk** cmdlet sets the operating system disk properties on an image object.</span></span>

## <span data-ttu-id="6d836-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6d836-107">EXAMPLES</span></span>

### <span data-ttu-id="6d836-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6d836-108">Example 1</span></span>
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

<span data-ttu-id="6d836-109">Pierwsze polecenie tworzy obiekt obrazu, a następnie zapisuje go w zmiennej $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="6d836-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>

<span data-ttu-id="6d836-110">Kolejne trzy polecenia umożliwiają przypisanie ścieżek do dysków systemu operacyjnego i dwóch dysków z danymi do $osDiskVhdUri, $dataDiskVhdUri 1 i $dataDiskVhdUri 2 zmiennych.</span><span class="sxs-lookup"><span data-stu-id="6d836-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="6d836-111">Taka metoda dotyczy tylko czytelności następujących poleceń.</span><span class="sxs-lookup"><span data-stu-id="6d836-111">This approach is only for readability of the following commands.</span></span>

<span data-ttu-id="6d836-112">Kolejne trzy polecenia umożliwiają dodanie dysku systemu operacyjnego i dwóch dysków z danymi do obrazu przechowywanego w $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="6d836-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="6d836-113">Identyfikator URI każdego dysku jest przechowywany w $osDiskVhdUri, $dataDiskVhdUri 1 i $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="6d836-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>

<span data-ttu-id="6d836-114">Polecenie ostatnie powoduje utworzenie obrazu o nazwie "ImageName01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="6d836-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="6d836-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6d836-115">PARAMETERS</span></span>

### <span data-ttu-id="6d836-116">-BlobUri</span><span class="sxs-lookup"><span data-stu-id="6d836-116">-BlobUri</span></span>
<span data-ttu-id="6d836-117">Określa identyfikator URI obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="6d836-117">Specifies the Uri of the blob.</span></span>

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

### <span data-ttu-id="6d836-118">-Buforowanie</span><span class="sxs-lookup"><span data-stu-id="6d836-118">-Caching</span></span>
<span data-ttu-id="6d836-119">Określa tryb buforowania dysku.</span><span class="sxs-lookup"><span data-stu-id="6d836-119">Specifies the caching mode of the disk.</span></span>

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

### <span data-ttu-id="6d836-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d836-120">-DefaultProfile</span></span>
<span data-ttu-id="6d836-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6d836-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d836-122">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="6d836-122">-DiskSizeGB</span></span>
<span data-ttu-id="6d836-123">Określa rozmiar dysku w GB.</span><span class="sxs-lookup"><span data-stu-id="6d836-123">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="6d836-124">-Image</span><span class="sxs-lookup"><span data-stu-id="6d836-124">-Image</span></span>
<span data-ttu-id="6d836-125">Określa lokalny obiekt obrazu.</span><span class="sxs-lookup"><span data-stu-id="6d836-125">Specifies a local image object.</span></span>

```yaml
Type: PSImage
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d836-126">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="6d836-126">-ManagedDiskId</span></span>
<span data-ttu-id="6d836-127">Określa identyfikator dysku zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="6d836-127">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="6d836-128">-OsState</span><span class="sxs-lookup"><span data-stu-id="6d836-128">-OsState</span></span>
<span data-ttu-id="6d836-129">Określa stan systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="6d836-129">Specifies the OS state.</span></span>

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

### <span data-ttu-id="6d836-130">-OsType</span><span class="sxs-lookup"><span data-stu-id="6d836-130">-OsType</span></span>
<span data-ttu-id="6d836-131">Określa typ OS.</span><span class="sxs-lookup"><span data-stu-id="6d836-131">Specifies the OS type.</span></span>

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

### <span data-ttu-id="6d836-132">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="6d836-132">-SnapshotId</span></span>
<span data-ttu-id="6d836-133">Określa identyfikator migawki.</span><span class="sxs-lookup"><span data-stu-id="6d836-133">Specifies the ID of a snapshot.</span></span>

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

### <span data-ttu-id="6d836-134">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="6d836-134">-StorageAccountType</span></span>
<span data-ttu-id="6d836-135">Typ konta magazynu obrazu systemu operacyjnego</span><span class="sxs-lookup"><span data-stu-id="6d836-135">The Storage Account type of Os Image Disk</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d836-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6d836-136">-Confirm</span></span>
<span data-ttu-id="6d836-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d836-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d836-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d836-138">-WhatIf</span></span>
<span data-ttu-id="6d836-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d836-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6d836-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6d836-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d836-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d836-141">CommonParameters</span></span>
<span data-ttu-id="6d836-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d836-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d836-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d836-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d836-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6d836-144">INPUTS</span></span>

### <span data-ttu-id="6d836-145">Microsoft. Azure. Management. COMPUTE. models. Image</span><span class="sxs-lookup"><span data-stu-id="6d836-145">Microsoft.Azure.Management.Compute.Models.Image</span></span>
<span data-ttu-id="6d836-146">System. Nullable `1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[Microsoft. Azure. Management. COMPUTE. MODELES. OperatingSystemStateTypes; Microsoft. Azure. Management. COMPUTE, Version = 14.0.0.0, Culture = neutral; PublicKeyToken = 31bf3856ad364e35]] system. String system. Nullable. null ( `1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` [System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="6d836-146">System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]] System.String System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="6d836-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6d836-147">OUTPUTS</span></span>

### <span data-ttu-id="6d836-148">Microsoft. Azure. Management. COMPUTE. models. Image</span><span class="sxs-lookup"><span data-stu-id="6d836-148">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="6d836-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6d836-149">NOTES</span></span>

## <span data-ttu-id="6d836-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6d836-150">RELATED LINKS</span></span>

