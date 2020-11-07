---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6AB09621-488B-4A16-92D9-9C47EB87DA95
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzResourceProvider.md
ms.openlocfilehash: cc890bf13922069ac9f4d20d6a9e8d0c3aa04c94
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892557"
---
# <span data-ttu-id="d4aeb-101">Get-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="d4aeb-101">Get-AzResourceProvider</span></span>

## <span data-ttu-id="d4aeb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d4aeb-102">SYNOPSIS</span></span>
<span data-ttu-id="d4aeb-103">Pobiera dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="d4aeb-103">Gets a resource provider.</span></span>

## <span data-ttu-id="d4aeb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d4aeb-104">SYNTAX</span></span>

### <span data-ttu-id="d4aeb-105">ListAvailable (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d4aeb-105">ListAvailable (Default)</span></span>
```
Get-AzResourceProvider [-Location <String>] [-ListAvailable] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d4aeb-106">IndividualProvider</span><span class="sxs-lookup"><span data-stu-id="d4aeb-106">IndividualProvider</span></span>
```
Get-AzResourceProvider -ProviderNamespace <String[]> [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d4aeb-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d4aeb-107">DESCRIPTION</span></span>
<span data-ttu-id="d4aeb-108">Polecenie cmdlet **Get-AzResourceProvider** pobiera dostawcę zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d4aeb-108">The **Get-AzResourceProvider** cmdlet gets an Azure resource provider.</span></span>

## <span data-ttu-id="d4aeb-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d4aeb-109">EXAMPLES</span></span>

## <span data-ttu-id="d4aeb-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d4aeb-110">PARAMETERS</span></span>

### <span data-ttu-id="d4aeb-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d4aeb-111">-ApiVersion</span></span>
<span data-ttu-id="d4aeb-112">Określa wersję API obsługiwaną przez dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="d4aeb-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="d4aeb-113">Możesz określić inną wersję niż wersja domyślna.</span><span class="sxs-lookup"><span data-stu-id="d4aeb-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="d4aeb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4aeb-114">-DefaultProfile</span></span>
<span data-ttu-id="d4aeb-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="d4aeb-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d4aeb-116">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="d4aeb-116">-ListAvailable</span></span>
<span data-ttu-id="d4aeb-117">Wskazuje, że ta operacja Pobiera wszystkich dostępnych dostawców zasobów.</span><span class="sxs-lookup"><span data-stu-id="d4aeb-117">Indicates that this operation gets all available resource providers.</span></span>

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

### <span data-ttu-id="d4aeb-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="d4aeb-118">-Location</span></span>
<span data-ttu-id="d4aeb-119">Określa lokalizację dostawcy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d4aeb-119">Specifies the location of the resource provider.</span></span>

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

### <span data-ttu-id="d4aeb-120">-Pre</span><span class="sxs-lookup"><span data-stu-id="d4aeb-120">-Pre</span></span>
<span data-ttu-id="d4aeb-121">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="d4aeb-121">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="d4aeb-122">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="d4aeb-122">-ProviderNamespace</span></span>
<span data-ttu-id="d4aeb-123">Określa obszar nazw dostawcy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d4aeb-123">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="d4aeb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4aeb-124">CommonParameters</span></span>
<span data-ttu-id="d4aeb-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4aeb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4aeb-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4aeb-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4aeb-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d4aeb-127">INPUTS</span></span>

## <span data-ttu-id="d4aeb-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d4aeb-128">OUTPUTS</span></span>

## <span data-ttu-id="d4aeb-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d4aeb-129">NOTES</span></span>

## <span data-ttu-id="d4aeb-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d4aeb-130">RELATED LINKS</span></span>

[<span data-ttu-id="d4aeb-131">Rejestr — AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="d4aeb-131">Register-AzResourceProvider</span></span>](./Register-AzResourceProvider.md)

[<span data-ttu-id="d4aeb-132">Wyrejestrowanie — AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="d4aeb-132">Unregister-AzResourceProvider</span></span>](./Unregister-AzResourceProvider.md)


