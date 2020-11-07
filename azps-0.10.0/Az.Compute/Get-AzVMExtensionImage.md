---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: F46041A3-355F-4449-B582-4D2F7314CA05
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmextensionimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMExtensionImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMExtensionImage.md
ms.openlocfilehash: 1864b4c2dcbd4b3d9934ffb15c54fae18082c920
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893746"
---
# <span data-ttu-id="3b1aa-101">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="3b1aa-101">Get-AzVMExtensionImage</span></span>

## <span data-ttu-id="3b1aa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3b1aa-102">SYNOPSIS</span></span>
<span data-ttu-id="3b1aa-103">Pobiera wszystkie wersje rozszerzenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3b1aa-103">Gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="3b1aa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3b1aa-104">SYNTAX</span></span>

```
Get-AzVMExtensionImage -Location <String> -PublisherName <String> -Type <String>
 [-FilterExpression <String>] [-Version <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3b1aa-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3b1aa-105">DESCRIPTION</span></span>
<span data-ttu-id="3b1aa-106">Polecenie cmdlet **Get-AzVMExtensionImage** pobiera wszystkie wersje rozszerzenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3b1aa-106">The **Get-AzVMExtensionImage** cmdlet gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="3b1aa-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3b1aa-107">EXAMPLES</span></span>

### <span data-ttu-id="3b1aa-108">Przykład 1: uzyskiwanie wersji obrazu rozszerzenia</span><span class="sxs-lookup"><span data-stu-id="3b1aa-108">Example 1: Get the versions of an extension image</span></span>
```
PS C:\> Get-AzVMExtensionImage -Location "Central US" -PublisherName "Fabrikam" -Type "FabrikamEndpointProtection"
```

<span data-ttu-id="3b1aa-109">To polecenie pobiera wszystkie wersje obrazu rozszerzenia dla określonej lokalizacji, wydawcy i typu.</span><span class="sxs-lookup"><span data-stu-id="3b1aa-109">This command gets all the versions of the extension image for the specified location, publisher, and type.</span></span>

## <span data-ttu-id="3b1aa-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3b1aa-110">PARAMETERS</span></span>

### <span data-ttu-id="3b1aa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b1aa-111">-DefaultProfile</span></span>
<span data-ttu-id="3b1aa-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3b1aa-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b1aa-113">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="3b1aa-113">-FilterExpression</span></span>
<span data-ttu-id="3b1aa-114">Określa wyrażenie filtru.</span><span class="sxs-lookup"><span data-stu-id="3b1aa-114">Specifies a filter expression.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b1aa-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="3b1aa-115">-Location</span></span>
<span data-ttu-id="3b1aa-116">Określa lokalizację rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="3b1aa-116">Specifies the location of an extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b1aa-117">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="3b1aa-117">-PublisherName</span></span>
<span data-ttu-id="3b1aa-118">Określa nazwę wydawcy rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="3b1aa-118">Specifies the name of an extension publisher.</span></span>
<span data-ttu-id="3b1aa-119">Aby uzyskać wydawcę rozszerzenia, użyj polecenia cmdlet Get-AzVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="3b1aa-119">To obtain an extension publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b1aa-120">-Type</span><span class="sxs-lookup"><span data-stu-id="3b1aa-120">-Type</span></span>
<span data-ttu-id="3b1aa-121">Określa typ rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="3b1aa-121">Specifies the type of the extension.</span></span>
<span data-ttu-id="3b1aa-122">Aby uzyskać typ rozszerzenia, użyj polecenia cmdlet Get-AzVMExtensionImageType.</span><span class="sxs-lookup"><span data-stu-id="3b1aa-122">To obtain an extension type, use the Get-AzVMExtensionImageType cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b1aa-123">-Version</span><span class="sxs-lookup"><span data-stu-id="3b1aa-123">-Version</span></span>
<span data-ttu-id="3b1aa-124">Określa wersję rozszerzenia, które jest pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b1aa-124">Specifies the version of the extension that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b1aa-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b1aa-125">CommonParameters</span></span>
<span data-ttu-id="3b1aa-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b1aa-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b1aa-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b1aa-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b1aa-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3b1aa-128">INPUTS</span></span>

### <span data-ttu-id="3b1aa-129">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="3b1aa-129">None</span></span>
<span data-ttu-id="3b1aa-130">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="3b1aa-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3b1aa-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3b1aa-131">OUTPUTS</span></span>

### <span data-ttu-id="3b1aa-132">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachineExtensionImage</span><span class="sxs-lookup"><span data-stu-id="3b1aa-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImage</span></span>

### <span data-ttu-id="3b1aa-133">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachineExtensionImageDetails</span><span class="sxs-lookup"><span data-stu-id="3b1aa-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageDetails</span></span>

## <span data-ttu-id="3b1aa-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3b1aa-134">NOTES</span></span>

## <span data-ttu-id="3b1aa-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3b1aa-135">RELATED LINKS</span></span>

[<span data-ttu-id="3b1aa-136">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="3b1aa-136">Get-AzVMExtensionImageType</span></span>](./Get-AzVMExtensionImageType.md)

[<span data-ttu-id="3b1aa-137">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="3b1aa-137">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="3b1aa-138">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="3b1aa-138">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)


