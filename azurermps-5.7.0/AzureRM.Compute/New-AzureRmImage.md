---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmImage.md
ms.openlocfilehash: 5f723ea475ed909ee5445f3788386a2163af697d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717018"
---
# <span data-ttu-id="a8fa8-101">New-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="a8fa8-101">New-AzureRmImage</span></span>

## <span data-ttu-id="a8fa8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a8fa8-102">SYNOPSIS</span></span>
<span data-ttu-id="a8fa8-103">Tworzy obraz.</span><span class="sxs-lookup"><span data-stu-id="a8fa8-103">Creates an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8fa8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a8fa8-104">SYNTAX</span></span>

```
New-AzureRmImage [-ResourceGroupName] <String> [-ImageName] <String> [-Image] <Image> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a8fa8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a8fa8-105">DESCRIPTION</span></span>
<span data-ttu-id="a8fa8-106">Polecenie cmdlet **New-AzureRmImage** umożliwia utworzenie obrazu.</span><span class="sxs-lookup"><span data-stu-id="a8fa8-106">The **New-AzureRmImage** cmdlet creates an image.</span></span>

## <span data-ttu-id="a8fa8-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a8fa8-107">EXAMPLES</span></span>

### <span data-ttu-id="a8fa8-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a8fa8-108">Example 1</span></span>
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

<span data-ttu-id="a8fa8-109">Pierwsze polecenie tworzy obiekt obrazu, a następnie zapisuje go w zmiennej $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="a8fa8-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>

<span data-ttu-id="a8fa8-110">Kolejne trzy polecenia umożliwiają przypisanie ścieżek do dysków systemu operacyjnego i dwóch dysków z danymi do $osDiskVhdUri, $dataDiskVhdUri 1 i $dataDiskVhdUri 2 zmiennych.</span><span class="sxs-lookup"><span data-stu-id="a8fa8-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="a8fa8-111">Taka metoda dotyczy tylko czytelności następujących poleceń.</span><span class="sxs-lookup"><span data-stu-id="a8fa8-111">This approach is only for readability of the following commands.</span></span>

<span data-ttu-id="a8fa8-112">Kolejne trzy polecenia umożliwiają dodanie dysku systemu operacyjnego i dwóch dysków z danymi do obrazu przechowywanego w $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="a8fa8-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="a8fa8-113">Identyfikator URI każdego dysku jest przechowywany w $osDiskVhdUri, $dataDiskVhdUri 1 i $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="a8fa8-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>

<span data-ttu-id="a8fa8-114">Polecenie ostatnie powoduje utworzenie obrazu o nazwie "ImageName01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="a8fa8-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="a8fa8-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a8fa8-115">PARAMETERS</span></span>

### <span data-ttu-id="a8fa8-116">-Image</span><span class="sxs-lookup"><span data-stu-id="a8fa8-116">-Image</span></span>
<span data-ttu-id="a8fa8-117">Określa lokalny obiekt obrazu.</span><span class="sxs-lookup"><span data-stu-id="a8fa8-117">Specifies a local image object.</span></span>

```yaml
Type: Image
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a8fa8-118">-ImageName</span><span class="sxs-lookup"><span data-stu-id="a8fa8-118">-ImageName</span></span>
<span data-ttu-id="a8fa8-119">Określa nazwę obrazu.</span><span class="sxs-lookup"><span data-stu-id="a8fa8-119">Specifies the name of an image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8fa8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8fa8-120">-ResourceGroupName</span></span>
<span data-ttu-id="a8fa8-121">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a8fa8-121">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="a8fa8-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a8fa8-122">-Confirm</span></span>
<span data-ttu-id="a8fa8-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8fa8-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8fa8-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8fa8-124">-WhatIf</span></span>
<span data-ttu-id="a8fa8-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8fa8-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8fa8-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a8fa8-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8fa8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8fa8-127">CommonParameters</span></span>
<span data-ttu-id="a8fa8-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8fa8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8fa8-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8fa8-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8fa8-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a8fa8-130">INPUTS</span></span>

### <span data-ttu-id="a8fa8-131">System. String</span><span class="sxs-lookup"><span data-stu-id="a8fa8-131">System.String</span></span>
<span data-ttu-id="a8fa8-132">Microsoft. Azure. Management. COMPUTE. models. Image</span><span class="sxs-lookup"><span data-stu-id="a8fa8-132">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="a8fa8-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a8fa8-133">OUTPUTS</span></span>

### <span data-ttu-id="a8fa8-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="a8fa8-134">System.Object</span></span>

## <span data-ttu-id="a8fa8-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a8fa8-135">NOTES</span></span>

## <span data-ttu-id="a8fa8-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a8fa8-136">RELATED LINKS</span></span>

