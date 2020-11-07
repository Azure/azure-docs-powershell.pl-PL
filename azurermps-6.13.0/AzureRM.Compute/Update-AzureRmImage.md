---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmImage.md
ms.openlocfilehash: 34c4eefe2792de239b2f3ae2a9348704497a4bd5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717457"
---
# <span data-ttu-id="3cf16-101">Update-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="3cf16-101">Update-AzureRmImage</span></span>

## <span data-ttu-id="3cf16-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3cf16-102">SYNOPSIS</span></span>
<span data-ttu-id="3cf16-103">Umożliwia zaktualizowanie obrazu.</span><span class="sxs-lookup"><span data-stu-id="3cf16-103">Updates an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3cf16-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3cf16-104">SYNTAX</span></span>

```
Update-AzureRmImage [-ResourceGroupName] <String> [-ImageName] <String> [-Image] <PSImage> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3cf16-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3cf16-105">DESCRIPTION</span></span>
<span data-ttu-id="3cf16-106">Polecenie cmdlet **Update-AzureRmImage** umożliwia zaktualizowanie obrazu.</span><span class="sxs-lookup"><span data-stu-id="3cf16-106">The **Update-AzureRmImage** cmdlet updates an image.</span></span>

## <span data-ttu-id="3cf16-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3cf16-107">EXAMPLES</span></span>

### <span data-ttu-id="3cf16-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3cf16-108">Example 1</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzureRmImageDataDisk -Lun 1 | Update-AzureRmImage;
```

<span data-ttu-id="3cf16-109">To polecenie usuwa dysk danych jednostki logicznej o numerze 1 z istniejącego obrazu "Image01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="3cf16-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="3cf16-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3cf16-110">PARAMETERS</span></span>

### <span data-ttu-id="3cf16-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3cf16-111">-AsJob</span></span>
<span data-ttu-id="3cf16-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="3cf16-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3cf16-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cf16-113">-DefaultProfile</span></span>
<span data-ttu-id="3cf16-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3cf16-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3cf16-115">-Image</span><span class="sxs-lookup"><span data-stu-id="3cf16-115">-Image</span></span>
<span data-ttu-id="3cf16-116">Określa lokalny obiekt obrazu.</span><span class="sxs-lookup"><span data-stu-id="3cf16-116">Specifies a local image object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSImage
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3cf16-117">-ImageName</span><span class="sxs-lookup"><span data-stu-id="3cf16-117">-ImageName</span></span>
<span data-ttu-id="3cf16-118">Określa nazwę obrazu.</span><span class="sxs-lookup"><span data-stu-id="3cf16-118">Specifies the name of an image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cf16-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cf16-119">-ResourceGroupName</span></span>
<span data-ttu-id="3cf16-120">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3cf16-120">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cf16-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3cf16-121">-Confirm</span></span>
<span data-ttu-id="3cf16-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3cf16-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3cf16-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cf16-123">-WhatIf</span></span>
<span data-ttu-id="3cf16-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3cf16-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3cf16-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3cf16-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3cf16-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cf16-126">CommonParameters</span></span>
<span data-ttu-id="3cf16-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cf16-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cf16-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3cf16-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cf16-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3cf16-129">INPUTS</span></span>

### <span data-ttu-id="3cf16-130">System. String</span><span class="sxs-lookup"><span data-stu-id="3cf16-130">System.String</span></span>

### <span data-ttu-id="3cf16-131">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSImage</span><span class="sxs-lookup"><span data-stu-id="3cf16-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>
<span data-ttu-id="3cf16-132">Parametry: obraz (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3cf16-132">Parameters: Image (ByValue)</span></span>

## <span data-ttu-id="3cf16-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3cf16-133">OUTPUTS</span></span>

### <span data-ttu-id="3cf16-134">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSImage</span><span class="sxs-lookup"><span data-stu-id="3cf16-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="3cf16-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3cf16-135">NOTES</span></span>

## <span data-ttu-id="3cf16-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3cf16-136">RELATED LINKS</span></span>
