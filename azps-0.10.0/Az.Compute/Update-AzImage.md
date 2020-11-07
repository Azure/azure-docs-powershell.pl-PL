---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzImage.md
ms.openlocfilehash: 1a04ca9df307b8d6251c6a8378df86827a76d001
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891598"
---
# <span data-ttu-id="eccfa-101">Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="eccfa-101">Update-AzImage</span></span>

## <span data-ttu-id="eccfa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="eccfa-102">SYNOPSIS</span></span>
<span data-ttu-id="eccfa-103">Umożliwia zaktualizowanie obrazu.</span><span class="sxs-lookup"><span data-stu-id="eccfa-103">Updates an image.</span></span>

## <span data-ttu-id="eccfa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="eccfa-104">SYNTAX</span></span>

```
Update-AzImage [-ResourceGroupName] <String> [-ImageName] <String> [-Image] <PSImage> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eccfa-105">Opis</span><span class="sxs-lookup"><span data-stu-id="eccfa-105">DESCRIPTION</span></span>
<span data-ttu-id="eccfa-106">Polecenie cmdlet **Update-AzImage** umożliwia zaktualizowanie obrazu.</span><span class="sxs-lookup"><span data-stu-id="eccfa-106">The **Update-AzImage** cmdlet updates an image.</span></span>

## <span data-ttu-id="eccfa-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="eccfa-107">EXAMPLES</span></span>

### <span data-ttu-id="eccfa-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="eccfa-108">Example 1</span></span>
```
PS C:\> Get-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzImageDataDisk -Lun 1 | Update-AzImage;
```

<span data-ttu-id="eccfa-109">To polecenie usuwa dysk danych jednostki logicznej o numerze 1 z istniejącego obrazu "Image01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="eccfa-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="eccfa-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="eccfa-110">PARAMETERS</span></span>

### <span data-ttu-id="eccfa-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eccfa-111">-AsJob</span></span>
<span data-ttu-id="eccfa-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="eccfa-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="eccfa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eccfa-113">-DefaultProfile</span></span>
<span data-ttu-id="eccfa-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="eccfa-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eccfa-115">-Image</span><span class="sxs-lookup"><span data-stu-id="eccfa-115">-Image</span></span>
<span data-ttu-id="eccfa-116">Określa lokalny obiekt obrazu.</span><span class="sxs-lookup"><span data-stu-id="eccfa-116">Specifies a local image object.</span></span>

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

### <span data-ttu-id="eccfa-117">-ImageName</span><span class="sxs-lookup"><span data-stu-id="eccfa-117">-ImageName</span></span>
<span data-ttu-id="eccfa-118">Określa nazwę obrazu.</span><span class="sxs-lookup"><span data-stu-id="eccfa-118">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="eccfa-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eccfa-119">-ResourceGroupName</span></span>
<span data-ttu-id="eccfa-120">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="eccfa-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="eccfa-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="eccfa-121">-Confirm</span></span>
<span data-ttu-id="eccfa-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eccfa-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eccfa-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eccfa-123">-WhatIf</span></span>
<span data-ttu-id="eccfa-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eccfa-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eccfa-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="eccfa-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eccfa-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eccfa-126">CommonParameters</span></span>
<span data-ttu-id="eccfa-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eccfa-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eccfa-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eccfa-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eccfa-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eccfa-129">INPUTS</span></span>

### <span data-ttu-id="eccfa-130">System. String</span><span class="sxs-lookup"><span data-stu-id="eccfa-130">System.String</span></span>
<span data-ttu-id="eccfa-131">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSImage</span><span class="sxs-lookup"><span data-stu-id="eccfa-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="eccfa-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="eccfa-132">OUTPUTS</span></span>

### <span data-ttu-id="eccfa-133">System. Object</span><span class="sxs-lookup"><span data-stu-id="eccfa-133">System.Object</span></span>

## <span data-ttu-id="eccfa-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="eccfa-134">NOTES</span></span>

## <span data-ttu-id="eccfa-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="eccfa-135">RELATED LINKS</span></span>

