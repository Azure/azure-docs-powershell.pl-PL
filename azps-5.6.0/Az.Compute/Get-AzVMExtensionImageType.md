---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 45F35BDD-969E-4521-9E8D-3499A15434A6
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmextensionimagetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImageType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImageType.md
ms.openlocfilehash: 551774d61e7887dfe115f37f67ce66fe95147406
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958986"
---
# <span data-ttu-id="def0d-101">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="def0d-101">Get-AzVMExtensionImageType</span></span>

## <span data-ttu-id="def0d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="def0d-102">SYNOPSIS</span></span>
<span data-ttu-id="def0d-103">Pobiera typ rozszerzenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="def0d-103">Gets the type of an Azure extension.</span></span>

## <span data-ttu-id="def0d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="def0d-104">SYNTAX</span></span>

```
Get-AzVMExtensionImageType -Location <String> -PublisherName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="def0d-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="def0d-105">DESCRIPTION</span></span>
<span data-ttu-id="def0d-106">Polecenie **cmdlet Get-AzVMExtensionImageType** pobiera typ rozszerzenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="def0d-106">The **Get-AzVMExtensionImageType** cmdlet gets the type of an Azure extension.</span></span>

## <span data-ttu-id="def0d-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="def0d-107">EXAMPLES</span></span>

### <span data-ttu-id="def0d-108">Przykład 1. Uzyskiwanie typu obrazu rozszerzenia</span><span class="sxs-lookup"><span data-stu-id="def0d-108">Example 1: Get an extension image type</span></span>
```
PS C:\> Get-AzVMExtensionImageType -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="def0d-109">To polecenie pobiera typ obrazu rozszerzenia dla określonego wydawcy i jego lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="def0d-109">This command gets the extension image type for the specified publisher and location.</span></span>

## <span data-ttu-id="def0d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="def0d-110">PARAMETERS</span></span>

### <span data-ttu-id="def0d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="def0d-111">-DefaultProfile</span></span>
<span data-ttu-id="def0d-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="def0d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="def0d-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="def0d-113">-Location</span></span>
<span data-ttu-id="def0d-114">Określa lokalizację rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="def0d-114">Specifies the location of an extension.</span></span>
<span data-ttu-id="def0d-115">To polecenie cmdlet pobiera typ rozszerzenia w lokalizacji, która jest określana przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="def0d-115">This cmdlet gets the type for an extension at the location that this parameter specifies.</span></span>

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

### <span data-ttu-id="def0d-116">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="def0d-116">-PublisherName</span></span>
<span data-ttu-id="def0d-117">Określa nazwę wydawcy rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="def0d-117">Specifies the name of a publisher of an extension.</span></span>
<span data-ttu-id="def0d-118">Aby uzyskać wydawcę rozszerzenia, użyj Get-AzVMImagePublisher cmdlet.</span><span class="sxs-lookup"><span data-stu-id="def0d-118">To obtain an extension publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>
<span data-ttu-id="def0d-119">To polecenie cmdlet pobiera typ rozszerzenia od wydawcy, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="def0d-119">This cmdlet gets the type for an extension from the publisher that this parameter specifies.</span></span>

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

### <span data-ttu-id="def0d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="def0d-120">CommonParameters</span></span>
<span data-ttu-id="def0d-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="def0d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="def0d-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="def0d-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="def0d-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="def0d-123">INPUTS</span></span>

### <span data-ttu-id="def0d-124">System.String</span><span class="sxs-lookup"><span data-stu-id="def0d-124">System.String</span></span>

## <span data-ttu-id="def0d-125">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="def0d-125">OUTPUTS</span></span>

### <span data-ttu-id="def0d-126">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="def0d-126">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageType</span></span>

## <span data-ttu-id="def0d-127">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="def0d-127">NOTES</span></span>

## <span data-ttu-id="def0d-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="def0d-128">RELATED LINKS</span></span>

[<span data-ttu-id="def0d-129">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="def0d-129">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

[<span data-ttu-id="def0d-130">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="def0d-130">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)


