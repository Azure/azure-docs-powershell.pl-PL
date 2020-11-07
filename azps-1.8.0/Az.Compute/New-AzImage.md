---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzImage.md
ms.openlocfilehash: 892a3f6f47bd24046777aabd648fb2702d09961b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869023"
---
# <span data-ttu-id="b9771-101">New-AzImage</span><span class="sxs-lookup"><span data-stu-id="b9771-101">New-AzImage</span></span>

## <span data-ttu-id="b9771-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b9771-102">SYNOPSIS</span></span>
<span data-ttu-id="b9771-103">Tworzy obraz.</span><span class="sxs-lookup"><span data-stu-id="b9771-103">Creates an image.</span></span>

## <span data-ttu-id="b9771-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b9771-104">SYNTAX</span></span>

```
New-AzImage [-ResourceGroupName] <String> [-ImageName] <String> [-Image] <PSImage> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9771-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b9771-105">DESCRIPTION</span></span>
<span data-ttu-id="b9771-106">Polecenie cmdlet **New-AzImage** umożliwia utworzenie obrazu.</span><span class="sxs-lookup"><span data-stu-id="b9771-106">The **New-AzImage** cmdlet creates an image.</span></span>

## <span data-ttu-id="b9771-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b9771-107">EXAMPLES</span></span>

### <span data-ttu-id="b9771-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b9771-108">Example 1</span></span>
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

<span data-ttu-id="b9771-109">Pierwsze polecenie tworzy obiekt obrazu, a następnie zapisuje go w zmiennej $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="b9771-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="b9771-110">Kolejne trzy polecenia umożliwiają przypisanie ścieżek do dysków systemu operacyjnego i dwóch dysków z danymi do $osDiskVhdUri, $dataDiskVhdUri 1 i $dataDiskVhdUri 2 zmiennych.</span><span class="sxs-lookup"><span data-stu-id="b9771-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="b9771-111">Taka metoda dotyczy tylko czytelności następujących poleceń.</span><span class="sxs-lookup"><span data-stu-id="b9771-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="b9771-112">Kolejne trzy polecenia umożliwiają dodanie dysku systemu operacyjnego i dwóch dysków z danymi do obrazu przechowywanego w $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="b9771-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="b9771-113">Identyfikator URI każdego dysku jest przechowywany w $osDiskVhdUri, $dataDiskVhdUri 1 i $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="b9771-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="b9771-114">Polecenie ostatnie powoduje utworzenie obrazu o nazwie "ImageName01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="b9771-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="b9771-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b9771-115">PARAMETERS</span></span>

### <span data-ttu-id="b9771-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b9771-116">-AsJob</span></span>
<span data-ttu-id="b9771-117">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="b9771-117">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9771-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9771-118">-DefaultProfile</span></span>
<span data-ttu-id="b9771-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b9771-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9771-120">-Image</span><span class="sxs-lookup"><span data-stu-id="b9771-120">-Image</span></span>
<span data-ttu-id="b9771-121">Określa lokalny obiekt obrazu.</span><span class="sxs-lookup"><span data-stu-id="b9771-121">Specifies a local image object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSImage
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b9771-122">-ImageName</span><span class="sxs-lookup"><span data-stu-id="b9771-122">-ImageName</span></span>
<span data-ttu-id="b9771-123">Określa nazwę obrazu.</span><span class="sxs-lookup"><span data-stu-id="b9771-123">Specifies the name of an image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9771-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9771-124">-ResourceGroupName</span></span>
<span data-ttu-id="b9771-125">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b9771-125">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9771-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b9771-126">-Confirm</span></span>
<span data-ttu-id="b9771-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9771-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9771-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9771-128">-WhatIf</span></span>
<span data-ttu-id="b9771-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9771-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9771-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b9771-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9771-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9771-131">CommonParameters</span></span>
<span data-ttu-id="b9771-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9771-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9771-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9771-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9771-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b9771-134">INPUTS</span></span>

### <span data-ttu-id="b9771-135">System. String</span><span class="sxs-lookup"><span data-stu-id="b9771-135">System.String</span></span>

### <span data-ttu-id="b9771-136">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSImage</span><span class="sxs-lookup"><span data-stu-id="b9771-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="b9771-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b9771-137">OUTPUTS</span></span>

### <span data-ttu-id="b9771-138">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSImage</span><span class="sxs-lookup"><span data-stu-id="b9771-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="b9771-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b9771-139">NOTES</span></span>

## <span data-ttu-id="b9771-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b9771-140">RELATED LINKS</span></span>
