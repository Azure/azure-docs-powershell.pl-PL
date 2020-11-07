---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermimage
schema: 2.0.0
ms.openlocfilehash: 0a03126be62c528d0879eaff093d6a3969802ce5
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897678"
---
# <span data-ttu-id="ae2a0-101">New-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="ae2a0-101">New-AzureRmImage</span></span>

## <span data-ttu-id="ae2a0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ae2a0-102">SYNOPSIS</span></span>
<span data-ttu-id="ae2a0-103">Tworzy obraz.</span><span class="sxs-lookup"><span data-stu-id="ae2a0-103">Creates an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae2a0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ae2a0-104">SYNTAX</span></span>

```
New-AzureRmImage [-ResourceGroupName] <String> [-ImageName] <String> [-Image] <PSImage> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae2a0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ae2a0-105">DESCRIPTION</span></span>
<span data-ttu-id="ae2a0-106">Polecenie cmdlet **New-AzureRmImage** umożliwia utworzenie obrazu.</span><span class="sxs-lookup"><span data-stu-id="ae2a0-106">The **New-AzureRmImage** cmdlet creates an image.</span></span>

## <span data-ttu-id="ae2a0-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ae2a0-107">EXAMPLES</span></span>

### <span data-ttu-id="ae2a0-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ae2a0-108">Example 1</span></span>
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

<span data-ttu-id="ae2a0-109">Pierwsze polecenie tworzy obiekt obrazu, a następnie zapisuje go w zmiennej $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="ae2a0-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>

<span data-ttu-id="ae2a0-110">Kolejne trzy polecenia umożliwiają przypisanie ścieżek do dysków systemu operacyjnego i dwóch dysków z danymi do $osDiskVhdUri, $dataDiskVhdUri 1 i $dataDiskVhdUri 2 zmiennych.</span><span class="sxs-lookup"><span data-stu-id="ae2a0-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="ae2a0-111">Taka metoda dotyczy tylko czytelności następujących poleceń.</span><span class="sxs-lookup"><span data-stu-id="ae2a0-111">This approach is only for readability of the following commands.</span></span>

<span data-ttu-id="ae2a0-112">Kolejne trzy polecenia umożliwiają dodanie dysku systemu operacyjnego i dwóch dysków z danymi do obrazu przechowywanego w $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="ae2a0-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="ae2a0-113">Identyfikator URI każdego dysku jest przechowywany w $osDiskVhdUri, $dataDiskVhdUri 1 i $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="ae2a0-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>

<span data-ttu-id="ae2a0-114">Polecenie ostatnie powoduje utworzenie obrazu o nazwie "ImageName01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="ae2a0-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="ae2a0-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ae2a0-115">PARAMETERS</span></span>

### <span data-ttu-id="ae2a0-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ae2a0-116">-AsJob</span></span>
<span data-ttu-id="ae2a0-117">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="ae2a0-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ae2a0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae2a0-118">-DefaultProfile</span></span>
<span data-ttu-id="ae2a0-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ae2a0-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae2a0-120">-Image</span><span class="sxs-lookup"><span data-stu-id="ae2a0-120">-Image</span></span>
<span data-ttu-id="ae2a0-121">Określa lokalny obiekt obrazu.</span><span class="sxs-lookup"><span data-stu-id="ae2a0-121">Specifies a local image object.</span></span>

```yaml
Type: PSImage
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ae2a0-122">-ImageName</span><span class="sxs-lookup"><span data-stu-id="ae2a0-122">-ImageName</span></span>
<span data-ttu-id="ae2a0-123">Określa nazwę obrazu.</span><span class="sxs-lookup"><span data-stu-id="ae2a0-123">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="ae2a0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae2a0-124">-ResourceGroupName</span></span>
<span data-ttu-id="ae2a0-125">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ae2a0-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="ae2a0-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ae2a0-126">-Confirm</span></span>
<span data-ttu-id="ae2a0-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae2a0-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae2a0-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae2a0-128">-WhatIf</span></span>
<span data-ttu-id="ae2a0-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae2a0-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae2a0-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ae2a0-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae2a0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae2a0-131">CommonParameters</span></span>
<span data-ttu-id="ae2a0-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae2a0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae2a0-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae2a0-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae2a0-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ae2a0-134">INPUTS</span></span>

### <span data-ttu-id="ae2a0-135">System. String</span><span class="sxs-lookup"><span data-stu-id="ae2a0-135">System.String</span></span>
<span data-ttu-id="ae2a0-136">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSImage</span><span class="sxs-lookup"><span data-stu-id="ae2a0-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="ae2a0-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ae2a0-137">OUTPUTS</span></span>

### <span data-ttu-id="ae2a0-138">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSImage</span><span class="sxs-lookup"><span data-stu-id="ae2a0-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

### <span data-ttu-id="ae2a0-139">System. Object</span><span class="sxs-lookup"><span data-stu-id="ae2a0-139">System.Object</span></span>

## <span data-ttu-id="ae2a0-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ae2a0-140">NOTES</span></span>

## <span data-ttu-id="ae2a0-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ae2a0-141">RELATED LINKS</span></span>

