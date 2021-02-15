---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzImage.md
ms.openlocfilehash: ff291afae70636863dff8ce34b5610cd77ce1251
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238850"
---
# <span data-ttu-id="a20a4-101">New-AzImage</span><span class="sxs-lookup"><span data-stu-id="a20a4-101">New-AzImage</span></span>

## <span data-ttu-id="a20a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a20a4-102">SYNOPSIS</span></span>
<span data-ttu-id="a20a4-103">Tworzy obraz.</span><span class="sxs-lookup"><span data-stu-id="a20a4-103">Creates an image.</span></span>

## <span data-ttu-id="a20a4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a20a4-104">SYNTAX</span></span>

```
New-AzImage [-ResourceGroupName] <String> [-ImageName] <String> [-Image] <PSImage> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a20a4-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="a20a4-105">DESCRIPTION</span></span>
<span data-ttu-id="a20a4-106">Polecenie **cmdlet New-AzImage** tworzy obraz.</span><span class="sxs-lookup"><span data-stu-id="a20a4-106">The **New-AzImage** cmdlet creates an image.</span></span>

## <span data-ttu-id="a20a4-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a20a4-107">EXAMPLES</span></span>

### <span data-ttu-id="a20a4-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a20a4-108">Example 1</span></span>
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

<span data-ttu-id="a20a4-109">Pierwsze polecenie tworzy obiekt obrazu, a następnie zapisuje go w $imageConfig zmienną.</span><span class="sxs-lookup"><span data-stu-id="a20a4-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="a20a4-110">Następne trzy polecenia przypiszą ścieżki dysku systemu operacyjnego i dwie dyskietki danych do zmiennych $osDiskVhdUri, $dataDiskVhdUri 1 i $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="a20a4-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="a20a4-111">Ta metoda ma na celu tylko czytelność następujących poleceń.</span><span class="sxs-lookup"><span data-stu-id="a20a4-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="a20a4-112">Następne trzy polecenia dodają dysk systemu operacyjnego i dwa dyski dla danych do obrazu przechowywanego w $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="a20a4-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="a20a4-113">Dane URI każdego dysku są przechowywane w $osDiskVhdUri, $dataDiskVhdUri 1 i $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="a20a4-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="a20a4-114">Końcowe polecenie tworzy obraz o nazwie "ImageName01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="a20a4-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="a20a4-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a20a4-115">PARAMETERS</span></span>

### <span data-ttu-id="a20a4-116">— AsJob</span><span class="sxs-lookup"><span data-stu-id="a20a4-116">-AsJob</span></span>
<span data-ttu-id="a20a4-117">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="a20a4-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a20a4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a20a4-118">-DefaultProfile</span></span>
<span data-ttu-id="a20a4-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a20a4-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a20a4-120">— Obraz</span><span class="sxs-lookup"><span data-stu-id="a20a4-120">-Image</span></span>
<span data-ttu-id="a20a4-121">Określa obiekt obrazu lokalnego.</span><span class="sxs-lookup"><span data-stu-id="a20a4-121">Specifies a local image object.</span></span>

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

### <span data-ttu-id="a20a4-122">-ImageName</span><span class="sxs-lookup"><span data-stu-id="a20a4-122">-ImageName</span></span>
<span data-ttu-id="a20a4-123">Określa nazwę obrazu.</span><span class="sxs-lookup"><span data-stu-id="a20a4-123">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="a20a4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a20a4-124">-ResourceGroupName</span></span>
<span data-ttu-id="a20a4-125">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a20a4-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="a20a4-126">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a20a4-126">-Confirm</span></span>
<span data-ttu-id="a20a4-127">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a20a4-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a20a4-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a20a4-128">-WhatIf</span></span>
<span data-ttu-id="a20a4-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a20a4-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a20a4-130">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a20a4-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a20a4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a20a4-131">CommonParameters</span></span>
<span data-ttu-id="a20a4-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a20a4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a20a4-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a20a4-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a20a4-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a20a4-134">INPUTS</span></span>

### <span data-ttu-id="a20a4-135">System.String</span><span class="sxs-lookup"><span data-stu-id="a20a4-135">System.String</span></span>

### <span data-ttu-id="a20a4-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="a20a4-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="a20a4-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a20a4-137">OUTPUTS</span></span>

### <span data-ttu-id="a20a4-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="a20a4-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="a20a4-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a20a4-139">NOTES</span></span>

## <span data-ttu-id="a20a4-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a20a4-140">RELATED LINKS</span></span>
