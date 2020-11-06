---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6AB09621-488B-4A16-92D9-9C47EB87DA95
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceProvider.md
ms.openlocfilehash: a7c30ee436f35bee72e786c1d219e114236248da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549903"
---
# <span data-ttu-id="5ba9b-101">Get-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="5ba9b-101">Get-AzureRmResourceProvider</span></span>

## <span data-ttu-id="5ba9b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5ba9b-102">SYNOPSIS</span></span>
<span data-ttu-id="5ba9b-103">Pobiera dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="5ba9b-103">Gets a resource provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ba9b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5ba9b-104">SYNTAX</span></span>

### <span data-ttu-id="5ba9b-105">ListAvailable (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5ba9b-105">ListAvailable (Default)</span></span>
```
Get-AzureRmResourceProvider [-Location <String>] [-ListAvailable] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ba9b-106">IndividualProvider</span><span class="sxs-lookup"><span data-stu-id="5ba9b-106">IndividualProvider</span></span>
```
Get-AzureRmResourceProvider -ProviderNamespace <String> [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ba9b-107">Opis</span><span class="sxs-lookup"><span data-stu-id="5ba9b-107">DESCRIPTION</span></span>
<span data-ttu-id="5ba9b-108">Polecenie cmdlet **Get-AzureRmResourceProvider** pobiera dostawcę zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5ba9b-108">The **Get-AzureRmResourceProvider** cmdlet gets an Azure resource provider.</span></span>

## <span data-ttu-id="5ba9b-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5ba9b-109">EXAMPLES</span></span>

## <span data-ttu-id="5ba9b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5ba9b-110">PARAMETERS</span></span>

### <span data-ttu-id="5ba9b-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="5ba9b-111">-ApiVersion</span></span>
<span data-ttu-id="5ba9b-112">Określa wersję API obsługiwaną przez dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="5ba9b-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="5ba9b-113">Możesz określić inną wersję niż wersja domyślna.</span><span class="sxs-lookup"><span data-stu-id="5ba9b-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="5ba9b-114">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="5ba9b-114">-ListAvailable</span></span>
<span data-ttu-id="5ba9b-115">Wskazuje, że ta operacja Pobiera wszystkich dostępnych dostawców zasobów.</span><span class="sxs-lookup"><span data-stu-id="5ba9b-115">Indicates that this operation gets all available resource providers.</span></span>

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

### <span data-ttu-id="5ba9b-116">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="5ba9b-116">-Location</span></span>
<span data-ttu-id="5ba9b-117">Określa lokalizację dostawcy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5ba9b-117">Specifies the location of the resource provider.</span></span>

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

### <span data-ttu-id="5ba9b-118">-Pre</span><span class="sxs-lookup"><span data-stu-id="5ba9b-118">-Pre</span></span>
<span data-ttu-id="5ba9b-119">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="5ba9b-119">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="5ba9b-120">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="5ba9b-120">-ProviderNamespace</span></span>
<span data-ttu-id="5ba9b-121">Określa obszar nazw dostawcy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5ba9b-121">Specifies the namespace of the resource provider.</span></span>

```yaml
Type: System.String
Parameter Sets: IndividualProvider
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ba9b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ba9b-122">-DefaultProfile</span></span>
<span data-ttu-id="5ba9b-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5ba9b-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ba9b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ba9b-124">CommonParameters</span></span>
<span data-ttu-id="5ba9b-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ba9b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ba9b-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ba9b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ba9b-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5ba9b-127">INPUTS</span></span>

## <span data-ttu-id="5ba9b-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5ba9b-128">OUTPUTS</span></span>

### <span data-ttu-id="5ba9b-129">Microsoft. Azure. Commands. resourceName. polecenia. cmdlet. SdkModels. PSResourceProvider</span><span class="sxs-lookup"><span data-stu-id="5ba9b-129">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="5ba9b-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5ba9b-130">NOTES</span></span>

## <span data-ttu-id="5ba9b-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5ba9b-131">RELATED LINKS</span></span>

[<span data-ttu-id="5ba9b-132">Rejestr — AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="5ba9b-132">Register-AzureRmResourceProvider</span></span>](./Register-AzureRmResourceProvider.md)

[<span data-ttu-id="5ba9b-133">Wyrejestrowanie — AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="5ba9b-133">Unregister-AzureRmResourceProvider</span></span>](./Unregister-AzureRmResourceProvider.md)


