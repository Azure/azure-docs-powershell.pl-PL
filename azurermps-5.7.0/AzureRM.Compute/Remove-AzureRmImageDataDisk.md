---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmImageDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmImageDataDisk.md
ms.openlocfilehash: 4115cabbeeb2a7c458ce52e80eb251cb972491f0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526930"
---
# <span data-ttu-id="f7de2-101">Remove-AzureRmImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="f7de2-101">Remove-AzureRmImageDataDisk</span></span>

## <span data-ttu-id="f7de2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f7de2-102">SYNOPSIS</span></span>
<span data-ttu-id="f7de2-103">Usuwa dysk danych z obiektu obrazu.</span><span class="sxs-lookup"><span data-stu-id="f7de2-103">Removes a data disk from an image object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7de2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f7de2-104">SYNTAX</span></span>

```
Remove-AzureRmImageDataDisk [-Image] <Image> [-Lun] <Int32> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7de2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f7de2-105">DESCRIPTION</span></span>
<span data-ttu-id="f7de2-106">Polecenie cmdlet **Remove-AzureRmImageDataDisk** usuwa dysk danych z obiektu obrazu.</span><span class="sxs-lookup"><span data-stu-id="f7de2-106">The **Remove-AzureRmImageDataDisk** cmdlet removes a data disk from an image object.</span></span>

## <span data-ttu-id="f7de2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f7de2-107">EXAMPLES</span></span>

### <span data-ttu-id="f7de2-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f7de2-108">Example 1</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzureRmImageDataDisk -Lun 1 | Update-AzureRmImage;
```

<span data-ttu-id="f7de2-109">To polecenie usuwa dysk danych jednostki logicznej o numerze 1 z istniejącego obrazu "Image01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="f7de2-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="f7de2-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f7de2-110">PARAMETERS</span></span>

### <span data-ttu-id="f7de2-111">-Image</span><span class="sxs-lookup"><span data-stu-id="f7de2-111">-Image</span></span>
<span data-ttu-id="f7de2-112">Określa lokalny obiekt obrazu.</span><span class="sxs-lookup"><span data-stu-id="f7de2-112">Specifies a local image object.</span></span>

```yaml
Type: Image
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f7de2-113">-LUN</span><span class="sxs-lookup"><span data-stu-id="f7de2-113">-Lun</span></span>
<span data-ttu-id="f7de2-114">Określa numer jednostki logicznej (LUN).</span><span class="sxs-lookup"><span data-stu-id="f7de2-114">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7de2-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f7de2-115">-Confirm</span></span>
<span data-ttu-id="f7de2-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7de2-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7de2-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7de2-117">-WhatIf</span></span>
<span data-ttu-id="f7de2-118">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7de2-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f7de2-119">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f7de2-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7de2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7de2-120">CommonParameters</span></span>
<span data-ttu-id="f7de2-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7de2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7de2-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7de2-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7de2-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f7de2-123">INPUTS</span></span>

### <span data-ttu-id="f7de2-124">Microsoft. Azure. Management. COMPUTE. models. Image</span><span class="sxs-lookup"><span data-stu-id="f7de2-124">Microsoft.Azure.Management.Compute.Models.Image</span></span>
<span data-ttu-id="f7de2-125">System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="f7de2-125">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="f7de2-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f7de2-126">OUTPUTS</span></span>

### <span data-ttu-id="f7de2-127">Microsoft. Azure. Management. COMPUTE. models. Image</span><span class="sxs-lookup"><span data-stu-id="f7de2-127">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="f7de2-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f7de2-128">NOTES</span></span>

## <span data-ttu-id="f7de2-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f7de2-129">RELATED LINKS</span></span>

