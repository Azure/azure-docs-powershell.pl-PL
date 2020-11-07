---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzImage.md
ms.openlocfilehash: 13829081952be7ab79c6d7badde4dc687aa845ed
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893798"
---
# <span data-ttu-id="23d8e-101">Get-AzImage</span><span class="sxs-lookup"><span data-stu-id="23d8e-101">Get-AzImage</span></span>

## <span data-ttu-id="23d8e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="23d8e-102">SYNOPSIS</span></span>
<span data-ttu-id="23d8e-103">Pobiera właściwości obrazu.</span><span class="sxs-lookup"><span data-stu-id="23d8e-103">Gets the properties of an image.</span></span>

## <span data-ttu-id="23d8e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="23d8e-104">SYNTAX</span></span>

```
Get-AzImage [[-ResourceGroupName] <String>] [[-ImageName] <String>] [[-Expand] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23d8e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="23d8e-105">DESCRIPTION</span></span>
<span data-ttu-id="23d8e-106">Polecenie cmdlet **Get-AzImage** pobiera właściwości obrazu.</span><span class="sxs-lookup"><span data-stu-id="23d8e-106">The **Get-AzImage** cmdlet gets the properties of an image.</span></span>

## <span data-ttu-id="23d8e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="23d8e-107">EXAMPLES</span></span>

### <span data-ttu-id="23d8e-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="23d8e-108">Example 1</span></span>
```
PS C:\> Get-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01'
```

<span data-ttu-id="23d8e-109">To polecenie pobiera właściwości obrazu o nazwie "Image01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="23d8e-109">This command gets the properties of the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="23d8e-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="23d8e-110">Example 2</span></span>
```
PS C:\> Get-AzImage -ResourceGroupName 'ResourceGroup01'
```

<span data-ttu-id="23d8e-111">To polecenie pobiera właściwości wszystkich obrazów w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="23d8e-111">This command gets the properties of all images in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="23d8e-112">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="23d8e-112">Example 3</span></span>
```
PS C:\> Get-AzImage
```

<span data-ttu-id="23d8e-113">To polecenie pobiera właściwości wszystkich obrazów w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="23d8e-113">This command gets the properties of all images under the subscription.</span></span>

## <span data-ttu-id="23d8e-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="23d8e-114">PARAMETERS</span></span>

### <span data-ttu-id="23d8e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23d8e-115">-DefaultProfile</span></span>
<span data-ttu-id="23d8e-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="23d8e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23d8e-117">-Expand</span><span class="sxs-lookup"><span data-stu-id="23d8e-117">-Expand</span></span>
<span data-ttu-id="23d8e-118">Określa zapytanie rozwijające wyrażenie.</span><span class="sxs-lookup"><span data-stu-id="23d8e-118">Specifies the expand expression query.</span></span>

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

### <span data-ttu-id="23d8e-119">-ImageName</span><span class="sxs-lookup"><span data-stu-id="23d8e-119">-ImageName</span></span>
<span data-ttu-id="23d8e-120">Określa nazwę obrazu.</span><span class="sxs-lookup"><span data-stu-id="23d8e-120">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="23d8e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23d8e-121">-ResourceGroupName</span></span>
<span data-ttu-id="23d8e-122">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="23d8e-122">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="23d8e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23d8e-123">CommonParameters</span></span>
<span data-ttu-id="23d8e-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23d8e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23d8e-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23d8e-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23d8e-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="23d8e-126">INPUTS</span></span>

### <span data-ttu-id="23d8e-127">System. String</span><span class="sxs-lookup"><span data-stu-id="23d8e-127">System.String</span></span>

## <span data-ttu-id="23d8e-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="23d8e-128">OUTPUTS</span></span>

### <span data-ttu-id="23d8e-129">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSImage</span><span class="sxs-lookup"><span data-stu-id="23d8e-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="23d8e-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="23d8e-130">NOTES</span></span>

## <span data-ttu-id="23d8e-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="23d8e-131">RELATED LINKS</span></span>

