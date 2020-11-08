---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 45F35BDD-969E-4521-9E8D-3499A15434A6
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmextensionimagetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImageType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImageType.md
ms.openlocfilehash: eb2c92b0efcbcd5333c600fe481e21752a96be9e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94064281"
---
# <span data-ttu-id="08666-101">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="08666-101">Get-AzVMExtensionImageType</span></span>

## <span data-ttu-id="08666-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="08666-102">SYNOPSIS</span></span>
<span data-ttu-id="08666-103">Pobiera typ rozszerzenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="08666-103">Gets the type of an Azure extension.</span></span>

## <span data-ttu-id="08666-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="08666-104">SYNTAX</span></span>

```
Get-AzVMExtensionImageType -Location <String> -PublisherName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="08666-105">Opis</span><span class="sxs-lookup"><span data-stu-id="08666-105">DESCRIPTION</span></span>
<span data-ttu-id="08666-106">Polecenie cmdlet **Get-AzVMExtensionImageType** Pobiera typ rozszerzenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="08666-106">The **Get-AzVMExtensionImageType** cmdlet gets the type of an Azure extension.</span></span>

## <span data-ttu-id="08666-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="08666-107">EXAMPLES</span></span>

### <span data-ttu-id="08666-108">Przykład 1: uzyskiwanie typu obrazu rozszerzenia</span><span class="sxs-lookup"><span data-stu-id="08666-108">Example 1: Get an extension image type</span></span>
```
PS C:\> Get-AzVMExtensionImageType -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="08666-109">To polecenie pobiera typ obrazu rozszerzenia dla określonego wydawcy i lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="08666-109">This command gets the extension image type for the specified publisher and location.</span></span>

## <span data-ttu-id="08666-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="08666-110">PARAMETERS</span></span>

### <span data-ttu-id="08666-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08666-111">-DefaultProfile</span></span>
<span data-ttu-id="08666-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="08666-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="08666-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="08666-113">-Location</span></span>
<span data-ttu-id="08666-114">Określa lokalizację rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="08666-114">Specifies the location of an extension.</span></span>
<span data-ttu-id="08666-115">To polecenie cmdlet umożliwia pobieranie typu rozszerzenia w lokalizacji, w której ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="08666-115">This cmdlet gets the type for an extension at the location that this parameter specifies.</span></span>

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

### <span data-ttu-id="08666-116">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="08666-116">-PublisherName</span></span>
<span data-ttu-id="08666-117">Określa nazwę wydawcy rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="08666-117">Specifies the name of a publisher of an extension.</span></span>
<span data-ttu-id="08666-118">Aby uzyskać wydawcę rozszerzenia, użyj polecenia cmdlet Get-AzVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="08666-118">To obtain an extension publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>
<span data-ttu-id="08666-119">To polecenie cmdlet umożliwia pobieranie typu rozszerzenia od wydawcy, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="08666-119">This cmdlet gets the type for an extension from the publisher that this parameter specifies.</span></span>

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

### <span data-ttu-id="08666-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08666-120">CommonParameters</span></span>
<span data-ttu-id="08666-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08666-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08666-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="08666-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08666-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="08666-123">INPUTS</span></span>

### <span data-ttu-id="08666-124">System. String</span><span class="sxs-lookup"><span data-stu-id="08666-124">System.String</span></span>

## <span data-ttu-id="08666-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="08666-125">OUTPUTS</span></span>

### <span data-ttu-id="08666-126">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachineExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="08666-126">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageType</span></span>

## <span data-ttu-id="08666-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="08666-127">NOTES</span></span>

## <span data-ttu-id="08666-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="08666-128">RELATED LINKS</span></span>

[<span data-ttu-id="08666-129">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="08666-129">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

[<span data-ttu-id="08666-130">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="08666-130">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)


