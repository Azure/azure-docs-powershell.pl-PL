---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: DC870E11-2129-4906-8357-D9BC1CF2E08E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermlocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmLocation.md
ms.openlocfilehash: a3169a78747a34a831ed6bd738e5647c3a4d9eb5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549584"
---
# <span data-ttu-id="d9a71-101">Get-AzureRmLocation</span><span class="sxs-lookup"><span data-stu-id="d9a71-101">Get-AzureRmLocation</span></span>

## <span data-ttu-id="d9a71-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d9a71-102">SYNOPSIS</span></span>
<span data-ttu-id="d9a71-103">Pobiera wszystkie lokalizacje i dostawców zasobów obsługiwanych dla każdej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="d9a71-103">Gets all locations and the supported resource providers for each location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9a71-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d9a71-104">SYNTAX</span></span>

```
Get-AzureRmLocation [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d9a71-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d9a71-105">DESCRIPTION</span></span>
<span data-ttu-id="d9a71-106">Polecenie cmdlet **Get-AzureRmLocation** pobiera wszystkie lokalizacje i dostawców zasobów obsługiwanych dla każdej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="d9a71-106">The **Get-AzureRmLocation** cmdlet gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="d9a71-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d9a71-107">EXAMPLES</span></span>

### <span data-ttu-id="d9a71-108">Przykład 1: pobieranie wszystkich lokalizacji i obsługiwanych dostawców zasobów</span><span class="sxs-lookup"><span data-stu-id="d9a71-108">Example 1: Get all locations and the supported resource providers</span></span>
```
PS C:\>Get-AzureRmLocation
```

<span data-ttu-id="d9a71-109">To polecenie pobiera wszystkie lokalizacje i dostawców zasobów obsługiwanych dla każdej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="d9a71-109">This command gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="d9a71-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d9a71-110">PARAMETERS</span></span>

### <span data-ttu-id="d9a71-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d9a71-111">-ApiVersion</span></span>
<span data-ttu-id="d9a71-112">Określa wersję API obsługiwaną przez dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="d9a71-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="d9a71-113">Możesz określić inną wersję niż wersja domyślna.</span><span class="sxs-lookup"><span data-stu-id="d9a71-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="d9a71-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9a71-114">-DefaultProfile</span></span>
<span data-ttu-id="d9a71-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="d9a71-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d9a71-116">-Pre</span><span class="sxs-lookup"><span data-stu-id="d9a71-116">-Pre</span></span>
<span data-ttu-id="d9a71-117">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="d9a71-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9a71-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9a71-118">CommonParameters</span></span>
<span data-ttu-id="d9a71-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9a71-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9a71-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9a71-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9a71-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d9a71-121">INPUTS</span></span>

### <span data-ttu-id="d9a71-122">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="d9a71-122">None</span></span>
<span data-ttu-id="d9a71-123">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="d9a71-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d9a71-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d9a71-124">OUTPUTS</span></span>

### <span data-ttu-id="d9a71-125">System. Collections. Generic. list "1 [Microsoft. Azure. Commands.</span><span class="sxs-lookup"><span data-stu-id="d9a71-125">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProviderLocation]</span></span>

## <span data-ttu-id="d9a71-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d9a71-126">NOTES</span></span>

## <span data-ttu-id="d9a71-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d9a71-127">RELATED LINKS</span></span>