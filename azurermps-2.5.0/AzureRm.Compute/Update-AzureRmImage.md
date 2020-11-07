---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermimage
schema: 2.0.0
ms.openlocfilehash: f1309453384f028c51bea20703d6ec75cc8a3a36
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899349"
---
# <span data-ttu-id="b0827-101">Update-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="b0827-101">Update-AzureRmImage</span></span>

## <span data-ttu-id="b0827-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b0827-102">SYNOPSIS</span></span>
<span data-ttu-id="b0827-103">Umożliwia zaktualizowanie obrazu.</span><span class="sxs-lookup"><span data-stu-id="b0827-103">Updates an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0827-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b0827-104">SYNTAX</span></span>

```
Update-AzureRmImage [-ResourceGroupName] <String> [-ImageName] <String> [-Image] <PSImage> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0827-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b0827-105">DESCRIPTION</span></span>
<span data-ttu-id="b0827-106">Polecenie cmdlet **Update-AzureRmImage** umożliwia zaktualizowanie obrazu.</span><span class="sxs-lookup"><span data-stu-id="b0827-106">The **Update-AzureRmImage** cmdlet updates an image.</span></span>

## <span data-ttu-id="b0827-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b0827-107">EXAMPLES</span></span>

### <span data-ttu-id="b0827-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b0827-108">Example 1</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzureRmImageDataDisk -Lun 1 | Update-AzureRmImage;
```

<span data-ttu-id="b0827-109">To polecenie usuwa dysk danych jednostki logicznej o numerze 1 z istniejącego obrazu "Image01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="b0827-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="b0827-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b0827-110">PARAMETERS</span></span>

### <span data-ttu-id="b0827-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b0827-111">-AsJob</span></span>
<span data-ttu-id="b0827-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="b0827-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b0827-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0827-113">-DefaultProfile</span></span>
<span data-ttu-id="b0827-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b0827-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0827-115">-Image</span><span class="sxs-lookup"><span data-stu-id="b0827-115">-Image</span></span>
<span data-ttu-id="b0827-116">Określa lokalny obiekt obrazu.</span><span class="sxs-lookup"><span data-stu-id="b0827-116">Specifies a local image object.</span></span>

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

### <span data-ttu-id="b0827-117">-ImageName</span><span class="sxs-lookup"><span data-stu-id="b0827-117">-ImageName</span></span>
<span data-ttu-id="b0827-118">Określa nazwę obrazu.</span><span class="sxs-lookup"><span data-stu-id="b0827-118">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="b0827-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0827-119">-ResourceGroupName</span></span>
<span data-ttu-id="b0827-120">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b0827-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="b0827-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b0827-121">-Confirm</span></span>
<span data-ttu-id="b0827-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0827-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0827-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0827-123">-WhatIf</span></span>
<span data-ttu-id="b0827-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0827-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0827-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b0827-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0827-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0827-126">CommonParameters</span></span>
<span data-ttu-id="b0827-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0827-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0827-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0827-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0827-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b0827-129">INPUTS</span></span>

### <span data-ttu-id="b0827-130">System. String</span><span class="sxs-lookup"><span data-stu-id="b0827-130">System.String</span></span>
<span data-ttu-id="b0827-131">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSImage</span><span class="sxs-lookup"><span data-stu-id="b0827-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="b0827-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b0827-132">OUTPUTS</span></span>

### <span data-ttu-id="b0827-133">System. Object</span><span class="sxs-lookup"><span data-stu-id="b0827-133">System.Object</span></span>

## <span data-ttu-id="b0827-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b0827-134">NOTES</span></span>

## <span data-ttu-id="b0827-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b0827-135">RELATED LINKS</span></span>

