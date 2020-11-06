---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: EFBBFB60-D972-47B8-997E-B737F0CA007E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResourceGroup.md
ms.openlocfilehash: 029404938ba7a253b5130f5c807e4b66c3847d43
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543008"
---
# <span data-ttu-id="66939-101">Find-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="66939-101">Find-AzureRmResourceGroup</span></span>

## <span data-ttu-id="66939-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="66939-102">SYNOPSIS</span></span>
<span data-ttu-id="66939-103">Umożliwia wyszukiwanie grup zasobów.</span><span class="sxs-lookup"><span data-stu-id="66939-103">Searches for resource groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66939-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="66939-104">SYNTAX</span></span>

```
Find-AzureRmResourceGroup [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66939-105">Opis</span><span class="sxs-lookup"><span data-stu-id="66939-105">DESCRIPTION</span></span>
<span data-ttu-id="66939-106">Polecenie cmdlet **Find-AzureRmResourceGroup** umożliwia wyszukiwanie grup zasobów przy użyciu określonych parametrów.</span><span class="sxs-lookup"><span data-stu-id="66939-106">The **Find-AzureRmResourceGroup** cmdlet searches for resource groups using the specified parameters.</span></span>

## <span data-ttu-id="66939-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="66939-107">EXAMPLES</span></span>

### <span data-ttu-id="66939-108">Przykład 1: Znajdowanie wszystkich grup zasobów</span><span class="sxs-lookup"><span data-stu-id="66939-108">Example 1: Find all resource groups</span></span>
```
PS C:\>Find-AzureRmResourceGroup
```

<span data-ttu-id="66939-109">To polecenie umożliwia znalezienie wszystkich grup zasobów.</span><span class="sxs-lookup"><span data-stu-id="66939-109">This command finds all resource groups.</span></span>

### <span data-ttu-id="66939-110">Przykład 2: Znajdowanie grup zasobów według nazwy tagu</span><span class="sxs-lookup"><span data-stu-id="66939-110">Example 2: Find resource groups by tag name</span></span>
```
PS C:\>Find-AzureRmResourceGroup -Tag @{ "testtag" = $null }
```

<span data-ttu-id="66939-111">To polecenie umożliwia znalezienie wszystkich grup zasobów mających znacznik o nazwie testtag.</span><span class="sxs-lookup"><span data-stu-id="66939-111">This command finds all resource groups that have a tag named testtag.</span></span>

### <span data-ttu-id="66939-112">Przykład 3: Znajdowanie grup zasobów według nazwy i wartości znacznika</span><span class="sxs-lookup"><span data-stu-id="66939-112">Example 3: Find resource groups by tag name and value</span></span>
```
PS C:\>Find-AzureRmResourceGroup -Tag @{"testtag" = "testval" }
```

<span data-ttu-id="66939-113">To polecenie umożliwia znalezienie wszystkich grup zasobów mających znacznik o nazwie testtag oraz wartość testval.</span><span class="sxs-lookup"><span data-stu-id="66939-113">This command finds all resource groups that have a tag named testtag and the value testval.</span></span>

## <span data-ttu-id="66939-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="66939-114">PARAMETERS</span></span>

### <span data-ttu-id="66939-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="66939-115">-ApiVersion</span></span>
<span data-ttu-id="66939-116">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="66939-116">Specifies the version of the resource provider API to use.</span></span> <span data-ttu-id="66939-117">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="66939-117">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="66939-118">-Pre</span><span class="sxs-lookup"><span data-stu-id="66939-118">-Pre</span></span>
<span data-ttu-id="66939-119">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="66939-119">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="66939-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="66939-120">-Tag</span></span>
<span data-ttu-id="66939-121">Określa informacje znacznika jako tabelę skrótów, aby filtrować wyniki.</span><span class="sxs-lookup"><span data-stu-id="66939-121">Specifies tag information, as a hash table, to filter your results.</span></span> <span data-ttu-id="66939-122">Użyj następujących formatów:</span><span class="sxs-lookup"><span data-stu-id="66939-122">Use the following formats:</span></span>

<span data-ttu-id="66939-123">@ {tagName = $null} lub @ {tagName = ' tagValue '}.</span><span class="sxs-lookup"><span data-stu-id="66939-123">@{tagName=$null} or @{tagName = 'tagValue'}.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66939-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66939-124">-DefaultProfile</span></span>
<span data-ttu-id="66939-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="66939-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66939-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66939-126">CommonParameters</span></span>
<span data-ttu-id="66939-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66939-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66939-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66939-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66939-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="66939-129">INPUTS</span></span>

## <span data-ttu-id="66939-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="66939-130">OUTPUTS</span></span>

### <span data-ttu-id="66939-131">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="66939-131">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="66939-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="66939-132">NOTES</span></span>

## <span data-ttu-id="66939-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="66939-133">RELATED LINKS</span></span>

