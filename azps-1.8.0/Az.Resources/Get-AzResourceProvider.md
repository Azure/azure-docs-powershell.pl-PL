---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6AB09621-488B-4A16-92D9-9C47EB87DA95
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceProvider.md
ms.openlocfilehash: 76a0164a5cf4c4d67ecb7f64667b9b87d9bc252c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708379"
---
# <span data-ttu-id="08987-101">Get-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="08987-101">Get-AzResourceProvider</span></span>

## <span data-ttu-id="08987-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="08987-102">SYNOPSIS</span></span>
<span data-ttu-id="08987-103">Pobiera dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="08987-103">Gets a resource provider.</span></span>

## <span data-ttu-id="08987-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="08987-104">SYNTAX</span></span>

### <span data-ttu-id="08987-105">ListAvailable (domyślny)</span><span class="sxs-lookup"><span data-stu-id="08987-105">ListAvailable (Default)</span></span>
```
Get-AzResourceProvider [-Location <String>] [-ListAvailable] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="08987-106">IndividualProvider</span><span class="sxs-lookup"><span data-stu-id="08987-106">IndividualProvider</span></span>
```
Get-AzResourceProvider -ProviderNamespace <String[]> [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="08987-107">Opis</span><span class="sxs-lookup"><span data-stu-id="08987-107">DESCRIPTION</span></span>
<span data-ttu-id="08987-108">Polecenie cmdlet **Get-AzResourceProvider** pobiera dostawcę zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="08987-108">The **Get-AzResourceProvider** cmdlet gets an Azure resource provider.</span></span>

## <span data-ttu-id="08987-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="08987-109">EXAMPLES</span></span>

## <span data-ttu-id="08987-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="08987-110">PARAMETERS</span></span>

### <span data-ttu-id="08987-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="08987-111">-ApiVersion</span></span>
<span data-ttu-id="08987-112">Określa wersję API obsługiwaną przez dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="08987-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="08987-113">Możesz określić inną wersję niż wersja domyślna.</span><span class="sxs-lookup"><span data-stu-id="08987-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="08987-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08987-114">-DefaultProfile</span></span>
<span data-ttu-id="08987-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="08987-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="08987-116">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="08987-116">-ListAvailable</span></span>
<span data-ttu-id="08987-117">Wskazuje, że ta operacja Pobiera wszystkich dostępnych dostawców zasobów.</span><span class="sxs-lookup"><span data-stu-id="08987-117">Indicates that this operation gets all available resource providers.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListAvailable
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08987-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="08987-118">-Location</span></span>
<span data-ttu-id="08987-119">Określa lokalizację dostawcy zasobów.</span><span class="sxs-lookup"><span data-stu-id="08987-119">Specifies the location of the resource provider.</span></span>

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

### <span data-ttu-id="08987-120">-Pre</span><span class="sxs-lookup"><span data-stu-id="08987-120">-Pre</span></span>
<span data-ttu-id="08987-121">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="08987-121">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08987-122">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="08987-122">-ProviderNamespace</span></span>
<span data-ttu-id="08987-123">Określa obszar nazw dostawcy zasobów.</span><span class="sxs-lookup"><span data-stu-id="08987-123">Specifies the namespace of the resource provider.</span></span>

```yaml
Type: System.String[]
Parameter Sets: IndividualProvider
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08987-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08987-124">CommonParameters</span></span>
<span data-ttu-id="08987-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08987-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08987-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08987-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08987-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="08987-127">INPUTS</span></span>

### <span data-ttu-id="08987-128">System. String []</span><span class="sxs-lookup"><span data-stu-id="08987-128">System.String[]</span></span>

## <span data-ttu-id="08987-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="08987-129">OUTPUTS</span></span>

### <span data-ttu-id="08987-130">Microsoft. Azure. Commands. resourceName. polecenia. cmdlet. SdkModels. PSResourceProvider</span><span class="sxs-lookup"><span data-stu-id="08987-130">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="08987-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="08987-131">NOTES</span></span>

## <span data-ttu-id="08987-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="08987-132">RELATED LINKS</span></span>

[<span data-ttu-id="08987-133">Rejestr — AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="08987-133">Register-AzResourceProvider</span></span>](./Register-AzResourceProvider.md)

[<span data-ttu-id="08987-134">Wyrejestrowanie — AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="08987-134">Unregister-AzResourceProvider</span></span>](./Unregister-AzResourceProvider.md)


