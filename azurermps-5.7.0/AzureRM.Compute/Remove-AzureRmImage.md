---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmImage.md
ms.openlocfilehash: 054462398a0f7b3e8710928000f9c10fb42f04db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717016"
---
# <span data-ttu-id="ab3f5-101">Remove-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="ab3f5-101">Remove-AzureRmImage</span></span>

## <span data-ttu-id="ab3f5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ab3f5-102">SYNOPSIS</span></span>
<span data-ttu-id="ab3f5-103">Usuwa obraz.</span><span class="sxs-lookup"><span data-stu-id="ab3f5-103">Removes an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab3f5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ab3f5-104">SYNTAX</span></span>

```
Remove-AzureRmImage [-ResourceGroupName] <String> [-ImageName] <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ab3f5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ab3f5-105">DESCRIPTION</span></span>
<span data-ttu-id="ab3f5-106">Polecenie cmdlet **Remove-AzureRmImage** usuwa obraz..</span><span class="sxs-lookup"><span data-stu-id="ab3f5-106">The **Remove-AzureRmImage** cmdlet removes an image..</span></span>

## <span data-ttu-id="ab3f5-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ab3f5-107">EXAMPLES</span></span>

### <span data-ttu-id="ab3f5-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ab3f5-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' -Force;
```

<span data-ttu-id="ab3f5-109">To polecenie usuwa obraz o nazwie "Image01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="ab3f5-109">This command removes the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="ab3f5-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ab3f5-110">PARAMETERS</span></span>

### <span data-ttu-id="ab3f5-111">-Force</span><span class="sxs-lookup"><span data-stu-id="ab3f5-111">-Force</span></span>
<span data-ttu-id="ab3f5-112">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="ab3f5-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab3f5-113">-ImageName</span><span class="sxs-lookup"><span data-stu-id="ab3f5-113">-ImageName</span></span>
<span data-ttu-id="ab3f5-114">Określa nazwę obrazu.</span><span class="sxs-lookup"><span data-stu-id="ab3f5-114">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="ab3f5-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab3f5-115">-ResourceGroupName</span></span>
<span data-ttu-id="ab3f5-116">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ab3f5-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="ab3f5-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ab3f5-117">-Confirm</span></span>
<span data-ttu-id="ab3f5-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab3f5-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab3f5-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab3f5-119">-WhatIf</span></span>
<span data-ttu-id="ab3f5-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab3f5-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab3f5-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ab3f5-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab3f5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab3f5-122">CommonParameters</span></span>
<span data-ttu-id="ab3f5-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab3f5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab3f5-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab3f5-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab3f5-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ab3f5-125">INPUTS</span></span>

### <span data-ttu-id="ab3f5-126">System. String</span><span class="sxs-lookup"><span data-stu-id="ab3f5-126">System.String</span></span>

## <span data-ttu-id="ab3f5-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ab3f5-127">OUTPUTS</span></span>

### <span data-ttu-id="ab3f5-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="ab3f5-128">System.Object</span></span>

## <span data-ttu-id="ab3f5-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ab3f5-129">NOTES</span></span>

## <span data-ttu-id="ab3f5-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ab3f5-130">RELATED LINKS</span></span>

