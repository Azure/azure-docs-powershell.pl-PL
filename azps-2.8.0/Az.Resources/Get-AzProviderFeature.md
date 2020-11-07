---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 2970E81E-A788-4829-B1FF-B522A91DE4B1
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderFeature.md
ms.openlocfilehash: 46a18d981bae7a8528a866d4f21cf5b07b64732f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871847"
---
# <span data-ttu-id="d3669-101">Get-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="d3669-101">Get-AzProviderFeature</span></span>

## <span data-ttu-id="d3669-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d3669-102">SYNOPSIS</span></span>
<span data-ttu-id="d3669-103">Pobiera informacje o funkcjach dostawcy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d3669-103">Gets information about Azure provider features.</span></span>

## <span data-ttu-id="d3669-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d3669-104">SYNTAX</span></span>

### <span data-ttu-id="d3669-105">ListAvailableParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d3669-105">ListAvailableParameterSet (Default)</span></span>
```
Get-AzProviderFeature [-ProviderNamespace <String>] [-ListAvailable] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d3669-106">Funkcja getfeature</span><span class="sxs-lookup"><span data-stu-id="d3669-106">GetFeature</span></span>
```
Get-AzProviderFeature -ProviderNamespace <String> -FeatureName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3669-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d3669-107">DESCRIPTION</span></span>
<span data-ttu-id="d3669-108">Polecenie cmdlet **Get-AzProviderFeature** Pobiera nazwę funkcji, nazwę dostawcy i stan rejestracji funkcji dostawcy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d3669-108">The **Get-AzProviderFeature** cmdlet gets the feature name, provider name, and registration status for Azure provider features.</span></span>

## <span data-ttu-id="d3669-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d3669-109">EXAMPLES</span></span>

### <span data-ttu-id="d3669-110">Przykład 1: Uzyskaj wszystkie dostępne funkcje</span><span class="sxs-lookup"><span data-stu-id="d3669-110">Example 1: Get all available features</span></span>
```
PS C:\>Get-AzProviderFeature -ListAvailable
```

<span data-ttu-id="d3669-111">To polecenie pobiera wszystkie dostępne funkcje.</span><span class="sxs-lookup"><span data-stu-id="d3669-111">This command gets all available features.</span></span>

### <span data-ttu-id="d3669-112">Przykład 2: uzyskiwanie informacji o konkretnej funkcji</span><span class="sxs-lookup"><span data-stu-id="d3669-112">Example 2: Get information about a specific feature</span></span>
```
PS C:\>Get-AzProviderFeature -FeatureName "AllowPreReleaseRegions" -ProviderNamespace "Microsoft.Compute"
```

<span data-ttu-id="d3669-113">To polecenie pobiera informacje dotyczące funkcji o nazwie AllowPreReleaseRegions dla określonego dostawcy.</span><span class="sxs-lookup"><span data-stu-id="d3669-113">This command gets information for the feature named AllowPreReleaseRegions for the specified provider.</span></span>

## <span data-ttu-id="d3669-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d3669-114">PARAMETERS</span></span>

### <span data-ttu-id="d3669-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3669-115">-DefaultProfile</span></span>
<span data-ttu-id="d3669-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="d3669-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d3669-117">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="d3669-117">-FeatureName</span></span>
<span data-ttu-id="d3669-118">Określa nazwę funkcji, którą należy pobrać.</span><span class="sxs-lookup"><span data-stu-id="d3669-118">Specifies the name of the feature to get.</span></span>

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

### <span data-ttu-id="d3669-119">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="d3669-119">-ListAvailable</span></span>
<span data-ttu-id="d3669-120">Wskazuje, że to polecenie cmdlet pobiera wszystkie funkcje.</span><span class="sxs-lookup"><span data-stu-id="d3669-120">Indicates that this cmdlet gets all features.</span></span>

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

### <span data-ttu-id="d3669-121">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="d3669-121">-ProviderNamespace</span></span>
<span data-ttu-id="d3669-122">Określa obszar nazw, dla którego to polecenie cmdlet pobiera funkcje dostawcy.</span><span class="sxs-lookup"><span data-stu-id="d3669-122">Specifies the namespace for which this cmdlet gets provider features.</span></span>

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

### <span data-ttu-id="d3669-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3669-123">CommonParameters</span></span>
<span data-ttu-id="d3669-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3669-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3669-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3669-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3669-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d3669-126">INPUTS</span></span>

### <span data-ttu-id="d3669-127">System. String</span><span class="sxs-lookup"><span data-stu-id="d3669-127">System.String</span></span>

## <span data-ttu-id="d3669-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d3669-128">OUTPUTS</span></span>

### <span data-ttu-id="d3669-129">Microsoft. Azure. Commands. resourceName. polecenia. cmdlet. SdkModels. PSProviderFeature</span><span class="sxs-lookup"><span data-stu-id="d3669-129">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span></span>

## <span data-ttu-id="d3669-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d3669-130">NOTES</span></span>

## <span data-ttu-id="d3669-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d3669-131">RELATED LINKS</span></span>

[<span data-ttu-id="d3669-132">Rejestr — AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="d3669-132">Register-AzProviderFeature</span></span>](./Register-AzProviderFeature.md)


