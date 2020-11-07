---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6AB09621-488B-4A16-92D9-9C47EB87DA95
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceProvider.md
ms.openlocfilehash: 8b7b4109441b10da0bf5c7f572c90f25a17293a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719383"
---
# <span data-ttu-id="fa6b7-101">Get-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="fa6b7-101">Get-AzureRmResourceProvider</span></span>

## <span data-ttu-id="fa6b7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fa6b7-102">SYNOPSIS</span></span>
<span data-ttu-id="fa6b7-103">Pobiera dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="fa6b7-103">Gets a resource provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fa6b7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fa6b7-104">SYNTAX</span></span>

### <span data-ttu-id="fa6b7-105">ListAvailable (domyślny)</span><span class="sxs-lookup"><span data-stu-id="fa6b7-105">ListAvailable (Default)</span></span>
```
Get-AzureRmResourceProvider [-Location <String>] [-ListAvailable] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fa6b7-106">IndividualProvider</span><span class="sxs-lookup"><span data-stu-id="fa6b7-106">IndividualProvider</span></span>
```
Get-AzureRmResourceProvider -ProviderNamespace <String[]> [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fa6b7-107">Opis</span><span class="sxs-lookup"><span data-stu-id="fa6b7-107">DESCRIPTION</span></span>
<span data-ttu-id="fa6b7-108">Polecenie cmdlet **Get-AzureRmResourceProvider** pobiera dostawcę zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="fa6b7-108">The **Get-AzureRmResourceProvider** cmdlet gets an Azure resource provider.</span></span>

## <span data-ttu-id="fa6b7-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fa6b7-109">EXAMPLES</span></span>

## <span data-ttu-id="fa6b7-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fa6b7-110">PARAMETERS</span></span>

### <span data-ttu-id="fa6b7-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="fa6b7-111">-ApiVersion</span></span>
<span data-ttu-id="fa6b7-112">Określa wersję API obsługiwaną przez dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="fa6b7-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="fa6b7-113">Możesz określić inną wersję niż wersja domyślna.</span><span class="sxs-lookup"><span data-stu-id="fa6b7-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="fa6b7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa6b7-114">-DefaultProfile</span></span>
<span data-ttu-id="fa6b7-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="fa6b7-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fa6b7-116">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="fa6b7-116">-ListAvailable</span></span>
<span data-ttu-id="fa6b7-117">Wskazuje, że ta operacja Pobiera wszystkich dostępnych dostawców zasobów.</span><span class="sxs-lookup"><span data-stu-id="fa6b7-117">Indicates that this operation gets all available resource providers.</span></span>

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

### <span data-ttu-id="fa6b7-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="fa6b7-118">-Location</span></span>
<span data-ttu-id="fa6b7-119">Określa lokalizację dostawcy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fa6b7-119">Specifies the location of the resource provider.</span></span>

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

### <span data-ttu-id="fa6b7-120">-Pre</span><span class="sxs-lookup"><span data-stu-id="fa6b7-120">-Pre</span></span>
<span data-ttu-id="fa6b7-121">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="fa6b7-121">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="fa6b7-122">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="fa6b7-122">-ProviderNamespace</span></span>
<span data-ttu-id="fa6b7-123">Określa obszar nazw dostawcy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fa6b7-123">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="fa6b7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa6b7-124">CommonParameters</span></span>
<span data-ttu-id="fa6b7-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa6b7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa6b7-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa6b7-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa6b7-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fa6b7-127">INPUTS</span></span>

## <span data-ttu-id="fa6b7-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fa6b7-128">OUTPUTS</span></span>

## <span data-ttu-id="fa6b7-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fa6b7-129">NOTES</span></span>

## <span data-ttu-id="fa6b7-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fa6b7-130">RELATED LINKS</span></span>

[<span data-ttu-id="fa6b7-131">Rejestr — AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="fa6b7-131">Register-AzureRmResourceProvider</span></span>](./Register-AzureRmResourceProvider.md)

[<span data-ttu-id="fa6b7-132">Wyrejestrowanie — AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="fa6b7-132">Unregister-AzureRmResourceProvider</span></span>](./Unregister-AzureRmResourceProvider.md)


