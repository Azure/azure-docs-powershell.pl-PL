---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 45F35BDD-969E-4521-9E8D-3499A15434A6
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmextensionimagetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImageType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImageType.md
ms.openlocfilehash: 0e3c1a9113bf3872ca86227272e36abd67781b7b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706400"
---
# <span data-ttu-id="584e0-101">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="584e0-101">Get-AzVMExtensionImageType</span></span>

## <span data-ttu-id="584e0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="584e0-102">SYNOPSIS</span></span>
<span data-ttu-id="584e0-103">Pobiera typ rozszerzenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="584e0-103">Gets the type of an Azure extension.</span></span>

## <span data-ttu-id="584e0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="584e0-104">SYNTAX</span></span>

```
Get-AzVMExtensionImageType -Location <String> -PublisherName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="584e0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="584e0-105">DESCRIPTION</span></span>
<span data-ttu-id="584e0-106">Polecenie cmdlet **Get-AzVMExtensionImageType** Pobiera typ rozszerzenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="584e0-106">The **Get-AzVMExtensionImageType** cmdlet gets the type of an Azure extension.</span></span>

## <span data-ttu-id="584e0-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="584e0-107">EXAMPLES</span></span>

### <span data-ttu-id="584e0-108">Przykład 1: uzyskiwanie typu obrazu rozszerzenia</span><span class="sxs-lookup"><span data-stu-id="584e0-108">Example 1: Get an extension image type</span></span>
```
PS C:\> Get-AzVMExtensionImageType -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="584e0-109">To polecenie pobiera typ obrazu rozszerzenia dla określonego wydawcy i lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="584e0-109">This command gets the extension image type for the specified publisher and location.</span></span>

## <span data-ttu-id="584e0-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="584e0-110">PARAMETERS</span></span>

### <span data-ttu-id="584e0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="584e0-111">-DefaultProfile</span></span>
<span data-ttu-id="584e0-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="584e0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="584e0-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="584e0-113">-Location</span></span>
<span data-ttu-id="584e0-114">Określa lokalizację rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="584e0-114">Specifies the location of an extension.</span></span>
<span data-ttu-id="584e0-115">To polecenie cmdlet umożliwia pobieranie typu rozszerzenia w lokalizacji, w której ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="584e0-115">This cmdlet gets the type for an extension at the location that this parameter specifies.</span></span>

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

### <span data-ttu-id="584e0-116">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="584e0-116">-PublisherName</span></span>
<span data-ttu-id="584e0-117">Określa nazwę wydawcy rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="584e0-117">Specifies the name of a publisher of an extension.</span></span>
<span data-ttu-id="584e0-118">Aby uzyskać wydawcę rozszerzenia, użyj polecenia cmdlet Get-AzVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="584e0-118">To obtain an extension publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>
<span data-ttu-id="584e0-119">To polecenie cmdlet umożliwia pobieranie typu rozszerzenia od wydawcy, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="584e0-119">This cmdlet gets the type for an extension from the publisher that this parameter specifies.</span></span>

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

### <span data-ttu-id="584e0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="584e0-120">CommonParameters</span></span>
<span data-ttu-id="584e0-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="584e0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="584e0-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="584e0-122">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="584e0-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="584e0-123">INPUTS</span></span>

### <span data-ttu-id="584e0-124">System. String</span><span class="sxs-lookup"><span data-stu-id="584e0-124">System.String</span></span>

## <span data-ttu-id="584e0-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="584e0-125">OUTPUTS</span></span>

### <span data-ttu-id="584e0-126">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachineExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="584e0-126">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageType</span></span>

## <span data-ttu-id="584e0-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="584e0-127">NOTES</span></span>

## <span data-ttu-id="584e0-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="584e0-128">RELATED LINKS</span></span>

[<span data-ttu-id="584e0-129">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="584e0-129">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

[<span data-ttu-id="584e0-130">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="584e0-130">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

