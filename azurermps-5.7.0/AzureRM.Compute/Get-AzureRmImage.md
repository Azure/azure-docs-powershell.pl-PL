---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmImage.md
ms.openlocfilehash: 3976418d89076b290500343775ca42e2fb975659
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546887"
---
# <span data-ttu-id="f9572-101">Get-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="f9572-101">Get-AzureRmImage</span></span>

## <span data-ttu-id="f9572-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f9572-102">SYNOPSIS</span></span>
<span data-ttu-id="f9572-103">Pobiera właściwości obrazu.</span><span class="sxs-lookup"><span data-stu-id="f9572-103">Gets the properties of an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9572-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f9572-104">SYNTAX</span></span>

```
Get-AzureRmImage [[-ResourceGroupName] <String>] [[-ImageName] <String>] [[-Expand] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="f9572-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f9572-105">DESCRIPTION</span></span>
<span data-ttu-id="f9572-106">Polecenie cmdlet **Get-AzureRmImage** pobiera właściwości obrazu.</span><span class="sxs-lookup"><span data-stu-id="f9572-106">The **Get-AzureRmImage** cmdlet gets the properties of an image.</span></span>

## <span data-ttu-id="f9572-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f9572-107">EXAMPLES</span></span>

### <span data-ttu-id="f9572-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f9572-108">Example 1</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01'
```

<span data-ttu-id="f9572-109">To polecenie pobiera właściwości obrazu o nazwie "Image01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="f9572-109">This command gets the properties of the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="f9572-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="f9572-110">Example 2</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01'
```

<span data-ttu-id="f9572-111">To polecenie pobiera właściwości wszystkich obrazów w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="f9572-111">This command gets the properties of all images in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="f9572-112">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="f9572-112">Example 3</span></span>
```
PS C:\> Get-AzureRmImage
```

<span data-ttu-id="f9572-113">To polecenie pobiera właściwości wszystkich obrazów w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="f9572-113">This command gets the properties of all images under the subscription.</span></span>

## <span data-ttu-id="f9572-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f9572-114">PARAMETERS</span></span>

### <span data-ttu-id="f9572-115">-Expand</span><span class="sxs-lookup"><span data-stu-id="f9572-115">-Expand</span></span>
<span data-ttu-id="f9572-116">Określa zapytanie rozwijające wyrażenie.</span><span class="sxs-lookup"><span data-stu-id="f9572-116">Specifies the expand expression query.</span></span>

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

### <span data-ttu-id="f9572-117">-ImageName</span><span class="sxs-lookup"><span data-stu-id="f9572-117">-ImageName</span></span>
<span data-ttu-id="f9572-118">Określa nazwę obrazu.</span><span class="sxs-lookup"><span data-stu-id="f9572-118">Specifies the name of an image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9572-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9572-119">-ResourceGroupName</span></span>
<span data-ttu-id="f9572-120">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f9572-120">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9572-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9572-121">CommonParameters</span></span>
<span data-ttu-id="f9572-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9572-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9572-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9572-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9572-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f9572-124">INPUTS</span></span>

### <span data-ttu-id="f9572-125">System. String</span><span class="sxs-lookup"><span data-stu-id="f9572-125">System.String</span></span>

## <span data-ttu-id="f9572-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f9572-126">OUTPUTS</span></span>

### <span data-ttu-id="f9572-127">System. Object</span><span class="sxs-lookup"><span data-stu-id="f9572-127">System.Object</span></span>

## <span data-ttu-id="f9572-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f9572-128">NOTES</span></span>

## <span data-ttu-id="f9572-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f9572-129">RELATED LINKS</span></span>

