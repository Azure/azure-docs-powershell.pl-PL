---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 45F35BDD-969E-4521-9E8D-3499A15434A6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmextensionimagetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMExtensionImageType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMExtensionImageType.md
ms.openlocfilehash: c4af2c651438659508e231bf2710e88de19830cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546676"
---
# <span data-ttu-id="96a39-101">Get-AzureRmVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="96a39-101">Get-AzureRmVMExtensionImageType</span></span>

## <span data-ttu-id="96a39-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="96a39-102">SYNOPSIS</span></span>
<span data-ttu-id="96a39-103">Pobiera typ rozszerzenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="96a39-103">Gets the type of an Azure extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="96a39-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="96a39-104">SYNTAX</span></span>

```
Get-AzureRmVMExtensionImageType -Location <String> -PublisherName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96a39-105">Opis</span><span class="sxs-lookup"><span data-stu-id="96a39-105">DESCRIPTION</span></span>
<span data-ttu-id="96a39-106">Polecenie cmdlet **Get-AzureRmVMExtensionImageType** Pobiera typ rozszerzenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="96a39-106">The **Get-AzureRmVMExtensionImageType** cmdlet gets the type of an Azure extension.</span></span>

## <span data-ttu-id="96a39-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="96a39-107">EXAMPLES</span></span>

### <span data-ttu-id="96a39-108">Przykład 1: uzyskiwanie typu obrazu rozszerzenia</span><span class="sxs-lookup"><span data-stu-id="96a39-108">Example 1: Get an extension image type</span></span>
```
PS C:\> Get-AzureRmVMExtensionImageType -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="96a39-109">To polecenie pobiera typ obrazu rozszerzenia dla określonego wydawcy i lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="96a39-109">This command gets the extension image type for the specified publisher and location.</span></span>

## <span data-ttu-id="96a39-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="96a39-110">PARAMETERS</span></span>

### <span data-ttu-id="96a39-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96a39-111">-DefaultProfile</span></span>
<span data-ttu-id="96a39-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="96a39-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96a39-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="96a39-113">-Location</span></span>
<span data-ttu-id="96a39-114">Określa lokalizację rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="96a39-114">Specifies the location of an extension.</span></span>
<span data-ttu-id="96a39-115">To polecenie cmdlet umożliwia pobieranie typu rozszerzenia w lokalizacji, w której ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="96a39-115">This cmdlet gets the type for an extension at the location that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96a39-116">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="96a39-116">-PublisherName</span></span>
<span data-ttu-id="96a39-117">Określa nazwę wydawcy rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="96a39-117">Specifies the name of a publisher of an extension.</span></span>
<span data-ttu-id="96a39-118">Aby uzyskać wydawcę rozszerzenia, użyj polecenia cmdlet Get-AzureRmVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="96a39-118">To obtain an extension publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>
<span data-ttu-id="96a39-119">To polecenie cmdlet umożliwia pobieranie typu rozszerzenia od wydawcy, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="96a39-119">This cmdlet gets the type for an extension from the publisher that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96a39-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96a39-120">CommonParameters</span></span>
<span data-ttu-id="96a39-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96a39-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96a39-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96a39-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96a39-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="96a39-123">INPUTS</span></span>

### <span data-ttu-id="96a39-124">System. String</span><span class="sxs-lookup"><span data-stu-id="96a39-124">System.String</span></span>

## <span data-ttu-id="96a39-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="96a39-125">OUTPUTS</span></span>

### <span data-ttu-id="96a39-126">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachineExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="96a39-126">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageType</span></span>

## <span data-ttu-id="96a39-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="96a39-127">NOTES</span></span>

## <span data-ttu-id="96a39-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="96a39-128">RELATED LINKS</span></span>

[<span data-ttu-id="96a39-129">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="96a39-129">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)

[<span data-ttu-id="96a39-130">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="96a39-130">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)


