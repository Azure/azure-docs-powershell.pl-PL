---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 2970E81E-A788-4829-B1FF-B522A91DE4B1
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzProviderFeature.md
ms.openlocfilehash: 1296e1e135acce9d4840e625d96931f6ecc11625
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892586"
---
# <span data-ttu-id="75f8e-101">Get-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="75f8e-101">Get-AzProviderFeature</span></span>

## <span data-ttu-id="75f8e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="75f8e-102">SYNOPSIS</span></span>
<span data-ttu-id="75f8e-103">Pobiera informacje o funkcjach dostawcy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="75f8e-103">Gets information about Azure provider features.</span></span>

## <span data-ttu-id="75f8e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="75f8e-104">SYNTAX</span></span>

### <span data-ttu-id="75f8e-105">ListAvailableParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="75f8e-105">ListAvailableParameterSet (Default)</span></span>
```
Get-AzProviderFeature [-ProviderNamespace <String>] [-ListAvailable]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75f8e-106">Funkcja getfeature</span><span class="sxs-lookup"><span data-stu-id="75f8e-106">GetFeature</span></span>
```
Get-AzProviderFeature -ProviderNamespace <String> -FeatureName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75f8e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="75f8e-107">DESCRIPTION</span></span>
<span data-ttu-id="75f8e-108">Polecenie cmdlet **Get-AzProviderFeature** Pobiera nazwę funkcji, nazwę dostawcy i stan rejestracji funkcji dostawcy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="75f8e-108">The **Get-AzProviderFeature** cmdlet gets the feature name, provider name, and registration status for Azure provider features.</span></span>

## <span data-ttu-id="75f8e-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="75f8e-109">EXAMPLES</span></span>

### <span data-ttu-id="75f8e-110">Przykład 1: Uzyskaj wszystkie dostępne funkcje</span><span class="sxs-lookup"><span data-stu-id="75f8e-110">Example 1: Get all available features</span></span>
```
PS C:\>Get-AzProviderFeature -ListAvailable
```

<span data-ttu-id="75f8e-111">To polecenie pobiera wszystkie dostępne funkcje.</span><span class="sxs-lookup"><span data-stu-id="75f8e-111">This command gets all available features.</span></span>

### <span data-ttu-id="75f8e-112">Przykład 2: uzyskiwanie informacji o konkretnej funkcji</span><span class="sxs-lookup"><span data-stu-id="75f8e-112">Example 2: Get information about a specific feature</span></span>
```
PS C:\>Get-AzProviderFeature -FeatureName "AllowPreReleaseRegions" -ProviderNamespace "Microsoft.Compute"
```

<span data-ttu-id="75f8e-113">To polecenie pobiera informacje dotyczące funkcji o nazwie AllowPreReleaseRegions dla określonego dostawcy.</span><span class="sxs-lookup"><span data-stu-id="75f8e-113">This command gets information for the feature named AllowPreReleaseRegions for the specified provider.</span></span>

## <span data-ttu-id="75f8e-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="75f8e-114">PARAMETERS</span></span>

### <span data-ttu-id="75f8e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75f8e-115">-DefaultProfile</span></span>
<span data-ttu-id="75f8e-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="75f8e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75f8e-117">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="75f8e-117">-FeatureName</span></span>
<span data-ttu-id="75f8e-118">Określa nazwę funkcji, którą należy pobrać.</span><span class="sxs-lookup"><span data-stu-id="75f8e-118">Specifies the name of the feature to get.</span></span>

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

### <span data-ttu-id="75f8e-119">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="75f8e-119">-ListAvailable</span></span>
<span data-ttu-id="75f8e-120">Wskazuje, że to polecenie cmdlet pobiera wszystkie funkcje.</span><span class="sxs-lookup"><span data-stu-id="75f8e-120">Indicates that this cmdlet gets all features.</span></span>

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

### <span data-ttu-id="75f8e-121">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="75f8e-121">-ProviderNamespace</span></span>
<span data-ttu-id="75f8e-122">Określa obszar nazw, dla którego to polecenie cmdlet pobiera funkcje dostawcy.</span><span class="sxs-lookup"><span data-stu-id="75f8e-122">Specifies the namespace for which this cmdlet gets provider features.</span></span>

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

### <span data-ttu-id="75f8e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75f8e-123">CommonParameters</span></span>
<span data-ttu-id="75f8e-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75f8e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75f8e-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75f8e-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75f8e-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="75f8e-126">INPUTS</span></span>

## <span data-ttu-id="75f8e-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="75f8e-127">OUTPUTS</span></span>

## <span data-ttu-id="75f8e-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="75f8e-128">NOTES</span></span>

## <span data-ttu-id="75f8e-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="75f8e-129">RELATED LINKS</span></span>

[<span data-ttu-id="75f8e-130">Rejestr — AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="75f8e-130">Register-AzProviderFeature</span></span>](./Register-AzProviderFeature.md)


