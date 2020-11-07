---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2970E81E-A788-4829-B1FF-B522A91DE4B1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmProviderFeature.md
ms.openlocfilehash: 5969a8c5d817f206d45dcbe67d438db3fba955ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543519"
---
# <span data-ttu-id="7c4e2-101">Get-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="7c4e2-101">Get-AzureRmProviderFeature</span></span>

## <span data-ttu-id="7c4e2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7c4e2-102">SYNOPSIS</span></span>
<span data-ttu-id="7c4e2-103">Pobiera informacje o funkcjach dostawcy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7c4e2-103">Gets information about Azure provider features.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c4e2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7c4e2-104">SYNTAX</span></span>

### <span data-ttu-id="7c4e2-105">ListAvailableParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7c4e2-105">ListAvailableParameterSet (Default)</span></span>
```
Get-AzureRmProviderFeature [-ProviderNamespace <String>] [-ListAvailable]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c4e2-106">Funkcja getfeature</span><span class="sxs-lookup"><span data-stu-id="7c4e2-106">GetFeature</span></span>
```
Get-AzureRmProviderFeature -ProviderNamespace <String> -FeatureName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c4e2-107">Opis</span><span class="sxs-lookup"><span data-stu-id="7c4e2-107">DESCRIPTION</span></span>
<span data-ttu-id="7c4e2-108">Polecenie cmdlet **Get-AzureRmProviderFeature** Pobiera nazwę funkcji, nazwę dostawcy i stan rejestracji funkcji dostawcy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7c4e2-108">The **Get-AzureRmProviderFeature** cmdlet gets the feature name, provider name, and registration status for Azure provider features.</span></span>

## <span data-ttu-id="7c4e2-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7c4e2-109">EXAMPLES</span></span>

### <span data-ttu-id="7c4e2-110">Przykład 1: Uzyskaj wszystkie dostępne funkcje</span><span class="sxs-lookup"><span data-stu-id="7c4e2-110">Example 1: Get all available features</span></span>
```
PS C:\>Get-AzureRmProviderFeature -ListAvailable
```

<span data-ttu-id="7c4e2-111">To polecenie pobiera wszystkie dostępne funkcje.</span><span class="sxs-lookup"><span data-stu-id="7c4e2-111">This command gets all available features.</span></span>

### <span data-ttu-id="7c4e2-112">Przykład 2: uzyskiwanie informacji o konkretnej funkcji</span><span class="sxs-lookup"><span data-stu-id="7c4e2-112">Example 2: Get information about a specific feature</span></span>
```
PS C:\>Get-AzureRmProviderFeature -FeatureName "AllowPreReleaseRegions" -ProviderNamespace "Microsoft.Compute"
```

<span data-ttu-id="7c4e2-113">To polecenie pobiera informacje dotyczące funkcji o nazwie AllowPreReleaseRegions dla określonego dostawcy.</span><span class="sxs-lookup"><span data-stu-id="7c4e2-113">This command gets information for the feature named AllowPreReleaseRegions for the specified provider.</span></span>

## <span data-ttu-id="7c4e2-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7c4e2-114">PARAMETERS</span></span>

### <span data-ttu-id="7c4e2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c4e2-115">-DefaultProfile</span></span>
<span data-ttu-id="7c4e2-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="7c4e2-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7c4e2-117">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="7c4e2-117">-FeatureName</span></span>
<span data-ttu-id="7c4e2-118">Określa nazwę funkcji, którą należy pobrać.</span><span class="sxs-lookup"><span data-stu-id="7c4e2-118">Specifies the name of the feature to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetFeature
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c4e2-119">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="7c4e2-119">-ListAvailable</span></span>
<span data-ttu-id="7c4e2-120">Wskazuje, że to polecenie cmdlet pobiera wszystkie funkcje.</span><span class="sxs-lookup"><span data-stu-id="7c4e2-120">Indicates that this cmdlet gets all features.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListAvailableParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c4e2-121">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="7c4e2-121">-ProviderNamespace</span></span>
<span data-ttu-id="7c4e2-122">Określa obszar nazw, dla którego to polecenie cmdlet pobiera funkcje dostawcy.</span><span class="sxs-lookup"><span data-stu-id="7c4e2-122">Specifies the namespace for which this cmdlet gets provider features.</span></span>

```yaml
Type: System.String
Parameter Sets: ListAvailableParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetFeature
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c4e2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c4e2-123">CommonParameters</span></span>
<span data-ttu-id="7c4e2-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c4e2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c4e2-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c4e2-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c4e2-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7c4e2-126">INPUTS</span></span>

## <span data-ttu-id="7c4e2-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7c4e2-127">OUTPUTS</span></span>

## <span data-ttu-id="7c4e2-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7c4e2-128">NOTES</span></span>

## <span data-ttu-id="7c4e2-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7c4e2-129">RELATED LINKS</span></span>

[<span data-ttu-id="7c4e2-130">Rejestr — AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="7c4e2-130">Register-AzureRmProviderFeature</span></span>](./Register-AzureRmProviderFeature.md)

