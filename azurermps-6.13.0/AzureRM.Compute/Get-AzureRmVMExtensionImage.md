---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: F46041A3-355F-4449-B582-4D2F7314CA05
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmextensionimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMExtensionImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMExtensionImage.md
ms.openlocfilehash: 4a348d4e3aa6089ae3e8f3c0bdf871156111ce93
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554279"
---
# <span data-ttu-id="a0268-101">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="a0268-101">Get-AzureRmVMExtensionImage</span></span>

## <span data-ttu-id="a0268-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a0268-102">SYNOPSIS</span></span>
<span data-ttu-id="a0268-103">Pobiera wszystkie wersje rozszerzenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a0268-103">Gets all versions for an Azure extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0268-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a0268-104">SYNTAX</span></span>

```
Get-AzureRmVMExtensionImage -Location <String> -PublisherName <String> -Type <String>
 [-FilterExpression <String>] [-Version <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a0268-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a0268-105">DESCRIPTION</span></span>
<span data-ttu-id="a0268-106">Polecenie cmdlet **Get-AzureRmVMExtensionImage** pobiera wszystkie wersje rozszerzenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a0268-106">The **Get-AzureRmVMExtensionImage** cmdlet gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="a0268-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a0268-107">EXAMPLES</span></span>

### <span data-ttu-id="a0268-108">Przykład 1: uzyskiwanie wersji obrazu rozszerzenia</span><span class="sxs-lookup"><span data-stu-id="a0268-108">Example 1: Get the versions of an extension image</span></span>
```
PS C:\> Get-AzureRmVMExtensionImage -Location "Central US" -PublisherName "Fabrikam" -Type "FabrikamEndpointProtection"
```

<span data-ttu-id="a0268-109">To polecenie pobiera wszystkie wersje obrazu rozszerzenia dla określonej lokalizacji, wydawcy i typu.</span><span class="sxs-lookup"><span data-stu-id="a0268-109">This command gets all the versions of the extension image for the specified location, publisher, and type.</span></span>

## <span data-ttu-id="a0268-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a0268-110">PARAMETERS</span></span>

### <span data-ttu-id="a0268-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0268-111">-DefaultProfile</span></span>
<span data-ttu-id="a0268-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a0268-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0268-113">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="a0268-113">-FilterExpression</span></span>
<span data-ttu-id="a0268-114">Określa wyrażenie filtru.</span><span class="sxs-lookup"><span data-stu-id="a0268-114">Specifies a filter expression.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0268-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="a0268-115">-Location</span></span>
<span data-ttu-id="a0268-116">Określa lokalizację rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="a0268-116">Specifies the location of an extension.</span></span>

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

### <span data-ttu-id="a0268-117">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="a0268-117">-PublisherName</span></span>
<span data-ttu-id="a0268-118">Określa nazwę wydawcy rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="a0268-118">Specifies the name of an extension publisher.</span></span>
<span data-ttu-id="a0268-119">Aby uzyskać wydawcę rozszerzenia, użyj polecenia cmdlet Get-AzureRmVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="a0268-119">To obtain an extension publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="a0268-120">-Type</span><span class="sxs-lookup"><span data-stu-id="a0268-120">-Type</span></span>
<span data-ttu-id="a0268-121">Określa typ rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="a0268-121">Specifies the type of the extension.</span></span>
<span data-ttu-id="a0268-122">Aby uzyskać typ rozszerzenia, użyj polecenia cmdlet Get-AzureRmVMExtensionImageType.</span><span class="sxs-lookup"><span data-stu-id="a0268-122">To obtain an extension type, use the Get-AzureRmVMExtensionImageType cmdlet.</span></span>

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

### <span data-ttu-id="a0268-123">-Version</span><span class="sxs-lookup"><span data-stu-id="a0268-123">-Version</span></span>
<span data-ttu-id="a0268-124">Określa wersję rozszerzenia, które jest pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0268-124">Specifies the version of the extension that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0268-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0268-125">CommonParameters</span></span>
<span data-ttu-id="a0268-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0268-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0268-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0268-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0268-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a0268-128">INPUTS</span></span>

### <span data-ttu-id="a0268-129">System. String</span><span class="sxs-lookup"><span data-stu-id="a0268-129">System.String</span></span>

## <span data-ttu-id="a0268-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a0268-130">OUTPUTS</span></span>

### <span data-ttu-id="a0268-131">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachineExtensionImage</span><span class="sxs-lookup"><span data-stu-id="a0268-131">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImage</span></span>

### <span data-ttu-id="a0268-132">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachineExtensionImageDetails</span><span class="sxs-lookup"><span data-stu-id="a0268-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageDetails</span></span>

## <span data-ttu-id="a0268-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a0268-133">NOTES</span></span>

## <span data-ttu-id="a0268-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a0268-134">RELATED LINKS</span></span>

[<span data-ttu-id="a0268-135">Get-AzureRmVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="a0268-135">Get-AzureRmVMExtensionImageType</span></span>](./Get-AzureRmVMExtensionImageType.md)

[<span data-ttu-id="a0268-136">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="a0268-136">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="a0268-137">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="a0268-137">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)


