---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 2970E81E-A788-4829-B1FF-B522A91DE4B1
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderFeature.md
ms.openlocfilehash: 67a0eee0dfe46b7b846958e1aa3f2be515a6b213
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102016049"
---
# <span data-ttu-id="650da-101">Get-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="650da-101">Get-AzProviderFeature</span></span>

## <span data-ttu-id="650da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="650da-102">SYNOPSIS</span></span>
<span data-ttu-id="650da-103">Pobiera informacje o funkcjach dostawców platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="650da-103">Gets information about Azure provider features.</span></span>

## <span data-ttu-id="650da-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="650da-104">SYNTAX</span></span>

### <span data-ttu-id="650da-105">ListAvailableParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="650da-105">ListAvailableParameterSet (Default)</span></span>
```
Get-AzProviderFeature [-ProviderNamespace <String>] [-ListAvailable] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="650da-106">GetFeature</span><span class="sxs-lookup"><span data-stu-id="650da-106">GetFeature</span></span>
```
Get-AzProviderFeature -ProviderNamespace <String> -FeatureName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="650da-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="650da-107">DESCRIPTION</span></span>
<span data-ttu-id="650da-108">Polecenie **cmdlet Get-AzProviderFeature** pobiera nazwę funkcji, nazwę dostawcy i stan rejestracji funkcji dostawcy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="650da-108">The **Get-AzProviderFeature** cmdlet gets the feature name, provider name, and registration status for Azure provider features.</span></span>

## <span data-ttu-id="650da-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="650da-109">EXAMPLES</span></span>

### <span data-ttu-id="650da-110">Przykład 1. Uzyskiwanie wszystkich dostępnych funkcji</span><span class="sxs-lookup"><span data-stu-id="650da-110">Example 1: Get all available features</span></span>
```
PS C:\>Get-AzProviderFeature -ListAvailable
```

<span data-ttu-id="650da-111">To polecenie otrzymuje dostęp do wszystkich dostępnych funkcji.</span><span class="sxs-lookup"><span data-stu-id="650da-111">This command gets all available features.</span></span>

### <span data-ttu-id="650da-112">Przykład 2. Uzyskiwanie informacji o określonej funkcji</span><span class="sxs-lookup"><span data-stu-id="650da-112">Example 2: Get information about a specific feature</span></span>
```
PS C:\>Get-AzProviderFeature -FeatureName "AllowPreReleaseRegions" -ProviderNamespace "Microsoft.Compute"
```

<span data-ttu-id="650da-113">To polecenie pobiera informacje dotyczące funkcji o nazwie AllowPreReleaseRegions dla określonego dostawcy.</span><span class="sxs-lookup"><span data-stu-id="650da-113">This command gets information for the feature named AllowPreReleaseRegions for the specified provider.</span></span>

## <span data-ttu-id="650da-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="650da-114">PARAMETERS</span></span>

### <span data-ttu-id="650da-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="650da-115">-DefaultProfile</span></span>
<span data-ttu-id="650da-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="650da-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="650da-117">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="650da-117">-FeatureName</span></span>
<span data-ttu-id="650da-118">Określa nazwę funkcji do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="650da-118">Specifies the name of the feature to get.</span></span>

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

### <span data-ttu-id="650da-119">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="650da-119">-ListAvailable</span></span>
<span data-ttu-id="650da-120">Wskazuje, że to polecenie cmdlet otrzymuje wszystkie funkcje.</span><span class="sxs-lookup"><span data-stu-id="650da-120">Indicates that this cmdlet gets all features.</span></span>

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

### <span data-ttu-id="650da-121">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="650da-121">-ProviderNamespace</span></span>
<span data-ttu-id="650da-122">Określa przestrzeń nazw, dla której to polecenie cmdlet otrzymuje funkcje dostawcy.</span><span class="sxs-lookup"><span data-stu-id="650da-122">Specifies the namespace for which this cmdlet gets provider features.</span></span>

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

### <span data-ttu-id="650da-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="650da-123">CommonParameters</span></span>
<span data-ttu-id="650da-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="650da-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="650da-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="650da-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="650da-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="650da-126">INPUTS</span></span>

### <span data-ttu-id="650da-127">System.String</span><span class="sxs-lookup"><span data-stu-id="650da-127">System.String</span></span>

## <span data-ttu-id="650da-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="650da-128">OUTPUTS</span></span>

### <span data-ttu-id="650da-129">Microsoft.Azure.Commands.ResourceManager.Cmdlet.SdkModels.PSProviderFeature</span><span class="sxs-lookup"><span data-stu-id="650da-129">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span></span>

## <span data-ttu-id="650da-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="650da-130">NOTES</span></span>

## <span data-ttu-id="650da-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="650da-131">RELATED LINKS</span></span>

[<span data-ttu-id="650da-132">Register-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="650da-132">Register-AzProviderFeature</span></span>](./Register-AzProviderFeature.md)


